---
slug: steal-my-bitcoin
title: Someone stole the bitcoin. What that does, and does not, tell us about php2shell
dek: A researcher won a public "steal my bitcoin" bounty by breaking into a deliberately vulnerable server with the php2shell flaw, and published how. It is the clearest proof yet that the bug gives full control of a machine. It is also a game, not a victim. Here is the difference, in plain terms and then in detail.
role: correspondent
origin: house
author: correspondent@php.newsroom
written: 2026-10-26
as_of_version: 0.22.29
vault_commit: 22a0c2920b88
data_as_of: 2026-10-26T12:14Z
series: reader-questions
question: Did the stealmybitcoin site get popped with a PHP vuln, and is that a real-world exploitation of these CVEs?
correction1: 2026-10-27T09:50Z | An update. Since this was written, CISA added both CVEs to its Known Exploited Vulnerabilities catalog (26 October), and a researcher's honeypots on PHP 8.4.26 recorded a successful remote code execution against Apache with mod_php (Adel Karimi of Perplexity, via ENTER.CO). Both strengthen what this piece says the challenge proves: the flaw works in practice, on more than one server mode. Neither names a victim: as of 07:15 UTC on 27 October no organisation has said it was breached through php2shell, so the funnel's bottom step is still unmet. The text below is as written at 12:14 UTC on 26 October.
---

**26 October 2026.** The same group chat that asked whether anyone had actually been hacked through php2shell ([our answer here](/articles/has-anyone-been-hacked/index.html)) came back with a link: a site called *Steal My Bitcoin* now reads **"Challenge won"**, and a researcher has published a step-by-step account of how they did it. The obvious question: was this a real php2shell break-in at last? This piece answers it, starting plain and ending technical, so you can stop wherever you have what you need. We do not reproduce the exploit; we explain what it is.

> **In one minute.** Someone built a server *on purpose* to be vulnerable to php2shell, put about $2,000 of bitcoin on it, and invited the internet to steal it. On 25 October a skilled researcher did, in roughly 19 hours, and wrote up how. That is **real proof the flaw gives an attacker full control of a machine**: the strongest public demonstration so far. But it is **a game with a consenting target, not a victim**: nobody was harmed, nothing was breached that its owner did not offer up. So it does **not** change this site's standing answer: still **no named organisation compromised** through php2shell in the real world. And the working exploit is **bespoke to that one server**: it is not a weapon that drops onto arbitrary websites.

## The three things people are mixing up

![Three columns: the flaw itself (real and confirmed), the challenge (a game, won), a real-world breach (still none named)](/assets/articles/steal-my-bitcoin/three-things.png "A won bounty proves the bug works; it is not proof that a real organisation was a victim.")

When a bounty like this is won, three separate facts get collapsed into one scary headline. Keep them apart:

1. **The flaw is real.** php2shell (CVE-2026-109618 and CVE-2026-109619) is a genuine, critical remote-code-execution bug, fixed on 21 October. That it can, in principle, give full control of an unpatched server has never been in doubt. [[php-net-advisory, github-ghsa-w8hw-w9fx-j79w, openwall-oss-security-2026-10-21-6]]
2. **The challenge is a game.** *Steal My Bitcoin* is a server its owner deliberately left vulnerable, advertised, and baited with bitcoin. A researcher won the pot. That is a *consenting* target.
3. **A real-world breach is still unproven.** No organisation has said it was broken into through php2shell. As of 12:14 UTC on 26 October, across 525 captured sources, that holds. This challenge does not touch it. [[cisa-kev-json, huntress-php2shell-rapid-response]]

## Was it the same bug as php2shell?

Yes. The published write-up targets **PHP 8.4.26**, one version below the 8.4.27 that carries the fix, and abuses the same mechanism the PHP advisory names: PHP's **session upload-progress** feature, the memory disclosure that leaks server memory, and the memory-corruption flaws behind the two CVEs. [[php-net-advisory, github-ghsa-w8hw-w9fx-j79w]] So this is not a new vulnerability. It is the known php2shell family, demonstrated end to end on an unpatched build.

## How the chain works, without the recipe

Our own [flaws page](/flaws/index.html) already explains the mechanism; here it is as four plain moves. This is to *understand* what happened, not to repeat it: there are no addresses, offsets or payloads here or on the site.

![Four boxes: a crafted upload, memory is leaked, memory is corrupted, a command runs](/assets/articles/steal-my-bitcoin/chain.png "The php2shell chain in four moves, at the level the PHP advisory itself describes.")

A specially shaped **file upload** makes PHP's upload-progress tracker hold on to data it should have released. The flaw then **leaks scraps of the server's own memory** back to the attacker, the "Heartbleed-like" disclosure that tells them where everything sits, defeating the random-layout defence modern systems rely on. With that map, a **use-after-free and a type confusion** let them corrupt exactly the right bytes and seize control of the running program. Control becomes a **shell command**, running as the web server, before any of the site's own code is reached. The only complete fix is to update; turning the upload-progress feature off closes this particular path. [[php-net-advisory, openwall-oss-security-2026-10-21-7]]

## So is it a new attack vector?

Not a new *vulnerability*, but there is one genuinely interesting wrinkle for defenders. This site's [affected-systems analysis](/affected/index.html) tracks which PHP "server modes" (SAPIs) the flaw has been shown to hit: Apache mod_php (the clearest case), PHP-FPM (disputed), php-cgi, FrankenPHP, LiteSpeed. The challenge ran neither of the usual two. It ran **PHP's own built-in web server** (`php -S`) with several worker processes behind nginx, a mode the project's own documentation says is **not meant for production**. The win is a concrete demonstration that this built-in server, too, can be driven all the way to code execution. It is a data point the primary advisories did not cover, and we have flagged it to be captured and added to the affected-systems table.

## How replicable is it, really?

This is where the honest answer diverges from the scary one. The vulnerability *class* travels: any unpatched, reachable PHP server is at risk in principle. But the *working exploit* in the write-up is bespoke to that one challenge box.

![Four rows: pinned to one PHP build; an unusual server mode; a race, not a certainty; re-tuned per target](/assets/articles/steal-my-bitcoin/replicable.png "Why a working lab exploit is not a drop-in weapon against arbitrary websites.")

Memory-corruption exploits are tuned to the exact compiled build; the author notes a different stack (a Debian PHP-FPM setup) would not match. It targets the unusual built-in-server mode. It is a **race** that, by the author's own account, succeeds only about seven times in ten even against the box it was written for. And against any different production server, an attacker would have to **redevelop** it, not re-run it. That is exactly why, five days in, we see attempts in the *millions* but reliable, general exploitation remains hard, and why Sophos reported finding working exploitation difficult even with AI assistance. [[aws-security-blog-madpot, thehackernews-php2shell-4days, imperva-blog-php2shell]]

## Is it a real-world scenario?

No, and that distinction is the whole point of this site. A *real-world* compromise means an attacker reaches a system that someone was defending, without permission, and takes something that matters. *Steal My Bitcoin* is the opposite in every way: the target was built to fall, the owner invited the attack, the "loss" was a prize deliberately offered, and (the author notes) the key recovered did not even match the advertised wallet. It is a research exercise and a bounty, and a genuinely impressive one. It belongs on the level of our [ladder of evidence](/articles/has-anyone-been-hacked/index.html) that says *"a working exploit has been demonstrated"*, which was already lit by watchTowr's reproduction and the public proof-of-concept code. It does not reach the level that says *"a named organisation was breached,"* which remains empty.

![Funnel: runs PHP, exposed and unpatched, a working exploit exists, weaponised at scale, a named organisation breached](/assets/articles/steal-my-bitcoin/funnel.png "Where php2shell actually sits. The challenge proves the middle level; the bottom two are still not met.")

## What a defender should take from it

- **Patch.** 8.5.12, 8.4.27, 8.3.36 or 8.2.35, or your distribution's backport. 8.4.26 is vulnerable; the challenge shows what "vulnerable" means in practice. [[php-net-advisory, github-ghsa-w8hw-w9fx-j79w]]
- **As a stopgap, turn off upload-progress** (`session.upload_progress.enabled=0`). It closes this path but is not a substitute for the update. [[php-net-advisory, openwall-oss-security-2026-10-21-7]]
- **Do not run the built-in `php -S` server in production.** The challenge is a live reminder that it is fully exploitable and was never meant to face the internet.
- **Assume memory disclosure beats ASLR.** The leak-then-corrupt pattern means "randomised memory layout" is not a backstop against this flaw.
- **Keep the proportion.** One consenting honeypot fell to a specialist in 19 hours. That is a reason to patch, not evidence that the web is being quietly emptied. The real-world count of named victims is still zero.

*Sources on this page marked with a hashed link are in the evidence vault. The challenge site (stealmybitcoin.com) and the researcher's write-up are external and have been referred to the researcher for capture into the vault, so a later version of this article can cite them with their hashes like everything else. This is the second in a series answering questions readers ask, each from the evidence and dated.*
