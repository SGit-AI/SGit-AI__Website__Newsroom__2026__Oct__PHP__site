---
slug: has-anyone-been-hacked
title: Has anyone actually been hacked through php2shell? What 525 sources say, five days on
dek: A reader's question, answered from the evidence. Millions of attack attempts, several vendors saying "exploited in the wild", hundreds of websites pulled offline as a precaution, and, as of 12:14 UTC on 26 October, not one organisation that has said it was broken into through these flaws. Here is the record, level by level, and what would change the answer.
role: correspondent
origin: house
author: correspondent@php.newsroom
written: 2026-10-26
as_of_version: 0.22.29
vault_commit: 22a0c2920b88
data_as_of: 2026-10-26T12:14Z
series: reader-questions
question: Has anyone seen an official, confirmed public report of these PHP flaws being exploited in a real-world attack? Did a bitcoin site get hacked through them?
correction1: 2026-10-27T09:50Z | Overtaken by events, and corrected. Level 5 is no longer empty: on 26 October CISA added both CVE-2026-109618 and CVE-2026-109619 to its Known Exploited Vulnerabilities catalog (catalog version 2026.10.26, released 22:24 UTC; CISA's alert of the same day; captured 00:45 UTC on 27 October), which means CISA holds evidence of exploitation. The listing names no victim, no organisation and no actor. Level 2 also gained its strongest entry: a researcher's decoy servers on PHP 8.4.26 recorded a successful remote code execution (Adel Karimi of Perplexity, via ENTER.CO; first incidents on 24 October). Level 4 is still empty: as of 07:15 UTC on 27 October, 580 sources in the evidence vault nnd3i8iw, no named organisation has said it was breached through php2shell. The answer is now: exploited, yes, on CISA's word and on decoys; a confirmed, named victim, not yet. The text below is as written at 12:14 UTC on 26 October.
---

**Update, 29 October 2026, 01:53 UTC.** One security vendor now reports victims. On 26 October Dream Research (dreamgroup.com, a company that sells the tooling it says it used) published that it found traces of a campaign which chained the two php2shell flaws, CVE-2026-109618 and CVE-2026-109619, with a Linux kernel flaw, CVE-2026-46300, and rooted 25 servers: 24 firewalls of a large vendor it does not name, and one internal firewall-management server, with three of the servers in one US government-affiliated environment. Our capture of its page is from 00:07 UTC on 29 October. [[dreamgroup-chained-php2shell-roots-25-servers]]

*Who repeats it.* The Hacker News, The Next Web and CyPro, all on 28 October. All three trace to Dream's post (CyPro's bulletin ends "Originally reported by securityweek.com"), so they are one source repeated, not three. [[the-hacker-news-thehackernews-php2shell-roots-25-s, the-next-web-php2shell-cisa-kev-dream-25-servers, cypro-php2shell-exploit-roots-firewalls]]

*What is not confirmed.* Everything about the victims. Dream names no victim, no organisation and no firewall vendor (it says the vendor was notified), publishes none of the artifacts it says it recovered, and says it cannot tell whether its later steps against the organisation's directory worked. The Next Web says: "TNW has not independently verified Dream's findings." CyPro says other researchers and vendors have seen scanning and attempts but do not independently verify Dream's victim details, and that SecurityWeek reported two servers at the organisation where Dream says three; that difference is unresolved. This newsroom found no statement about these victims from CISA, the firewall vendor, the US organisation or the PHP team. Of Dream's three CVE numbers, the two php2shell ones match CISA's listing; the kernel flaw's number is in no CISA material in the evidence. [[dreamgroup-chained-php2shell-roots-25-servers, the-next-web-php2shell-cisa-kev-dream-25-servers, cypro-php2shell-exploit-roots-firewalls, cisa-kev-json]]

*Exploited is still not compromised.* CISA's listing is its finding that the flaws are exploited; it names no victim and does not confirm Dream's account. Dream's report is also not level 4 of the ladder below, which needs a named organisation to say it was breached through php2shell, and none has. It is a vendor's report of unnamed victims, a rung of its own between levels 2 and 4. As of 00:09 UTC on 29 October, the latest capture in the evidence vault (681 sources): **exploited, on CISA's evidence; compromised, reported by one vendor and not confirmed; a named victim, still none.**

*What would change it.* The firewall vendor, CISA or the US organisation confirming Dream's account; Dream publishing evidence others can check; or a second source that did not start from Dream's post.

**Update, 27 October 2026, 03:45 UTC.** The official signal this piece was waiting for has arrived. On 26 October CISA, the US cyber-security agency, added both flaws, CVE-2026-109618 and CVE-2026-109619, to its Known Exploited Vulnerabilities catalogue. The catalogue's version 2026.10.26, released at 22:24 UTC on 26 October and captured by this newsroom at 00:45 UTC on 27 October, lists both as added that day, gives US federal civilian agencies until 29 October to act on them, and records known ransomware use as "Unknown", which is neither a finding of ransomware use nor a finding that there is none. [[cisa-kev-json, cisa-kev-catalog, cisa-alert-kev-20261026]]

*What it means.* CISA says it holds evidence that the flaws are exploited: its alert says an addition to the catalogue "must have a CVE ID, evidence of exploitation, and clear mitigation guidance". That is level 5 of the ladder below, which this piece called empty and said "would move the answer on its own". It has: to the reader's first question, whether there is an official report of these flaws being exploited, the answer is now yes. [[cisa-alert-kev-20261026]]

*What does not change.* The listing names no victim, no compromised organisation and no threat actor. No named organisation has said it was compromised through php2shell, as of the evidence vault's latest capture, 00:45 UTC on 27 October. Exploited is not the same as compromised: the first is CISA's finding about the flaws, the second needs an organisation to say it, and level 4 is still empty. [[cisa-alert-kev-20261026, cisa-kev-json]] CISA also says it updated its PHP alert of 21 October; this newsroom's capture of that alert predates the update, so the new text is not yet in the evidence.

The short answer is now: **exploited, on CISA's evidence; attempts, in millions; a confirmed, named victim, not yet.** The rest of this piece is kept as written on 26 October: the short answer's line on CISA's list, the ladder figure, level 5 and the counts are as of 12:14 UTC that day, and each line the listing overtook is marked.

**26 October 2026.** The question came from a security group the editor belongs to, and it is the one everyone keeps asking: *has anyone seen an official, confirmed report of php2shell being exploited in a real-world attack?* A follow-up named a cryptocurrency site and asked whether it had been hacked through a PHP flaw. This piece answers both from the evidence this newsroom holds, and shows how it knows.

**The short answer.** No. As of the latest capture in the evidence vault, 12:14 UTC on 26 October, no organisation has said it was compromised through php2shell, no regulator has published a breach notice naming it, and neither CVE is on CISA's list of vulnerabilities known to be exploited *(no longer so: both were added on 26 October; see the update at the top)*. Attack *attempts* are certain and counted in millions; several security vendors say the flaws are "exploited in the wild", but none names a victim. [[cisa-kev-json, x-eastdakota-php2shell-stats, aws-security-blog-madpot]] The cryptocurrency site the follow-up named appears nowhere in the 525 sources; what the record does hold on crypto points the other way. [[news-bitcoin-es-security-coinbase-y-bitgo-niegan-impa, btc-echo-news-krypto-boersen-akut-bedroht-kritisc]]

That answer is time-bounded on purpose. It is true as of a stated capture and will change the day a named organisation says otherwise. The rest of this piece is the evidence behind it.

## The ladder of evidence

"Exploited" is used for very different things. It helps to separate them into levels, each a stronger kind of proof than the one below.

![Five levels of evidence, from attack attempts to a CISA listing; the top two are empty](/assets/articles/has-anyone-been-hacked/ladder.png "The ladder of evidence, as of 12:14 UTC on 26 October 2026. The bottom two levels are reached; the third has candidates; the top two are empty.")

**Level 1: attempts. Reached, massively.** Cloudflare's chief executive counted thousands of attempts in the ten hours before the announcement and "millions now" a day later. [[x-eastdakota-php2shell-stats]] Amazon says one of its decoy servers was hit on 17 October, four days before the fix, and that it is "unclear if any of these attempts would have succeeded". [[aws-security-blog-madpot]] Amazon also reports attackers trying to install Mirai-family botnets; Sophos says the botnet payloads it saw failed. [[japan-zdnet-article-35253966, cybersecuritynews-critical-php2shell-exploit-code]]

**Level 2: a vendor says "exploited in the wild". Reached, but with no victim.** Four statements in the record say so: Hadrian ("exploited in the wild at scale"), Patchstack (reports from hosting partners), Amazon (against its own sensors) and New Zealand's NCSC ("aware of reports"). [[securityweek-first-attempts-sensors, recordedfuture-php2shell, aws-security-blog-madpot, ncsc-nz-alert-php]] None names an organisation that was broken into. One blog wrote that "Palo Alto Networks and Trail of Bits later reported confirmed compromises"; it names no victim, no such report is captured, and Palo Alto's own advisory says it is "not aware of any malicious exploitation". This site holds that sentence back. [[wersm-php2shell-legacy-infrastructure-web-risk, paloalto-psirt-cve-2026-109618]]

**Level 3: a named organisation investigating an incident. Candidates, none tied to php2shell.** Four names have come up, and each has been tested against its own words:

| Organisation | What it said | What that proves |
| --- | --- | --- |
| GMO Internet Group (Japan) | Malicious programs found on servers of its FX trading VPS service on 20 October; account logins may have been taken | A real break-in; the cause is not stated |
| Czech Technical University | A cyber attack "part of worldwide attempts to hit PHP sites"; "the active attack was stopped" | An attack; success is not stated |
| DMM (Japan) | Halted services over "a vulnerability in external software"; no data leaked | A precaution; PHP not confirmed |
| Valtec (Japan) | First blamed "a cyberattack targeting the PHP vulnerability", then corrected the same day: the flaw was in its own service | Withdrawn |

[[yahoo-jp-gmo-fx-login-leak, lupa-cvut-cyber-attack, sankei-dmm-service-halt, impress-watch-valtec]]

**Level 4: a named organisation says it was breached through php2shell. Empty.** Not in any of the 525 captured sources, read in their own languages.

**Level 5: CISA lists the flaws as known exploited. Empty at the last check.** Neither CVE was in the Known Exploited Vulnerabilities catalogue when it was last checked, at 05:53 UTC on 24 October, and CISA's own assessment on the CVE records reads "Exploitation: none". [[cisa-kev-json, cve-cve-2026-109618, cve-cve-2026-109619]] This is the measure most worth re-checking; a listing would move the answer on its own. *Update, 27 October: reached. CISA added both CVEs to the catalogue on 26 October, naming no victim; see the update at the top.* [[cisa-alert-kev-20261026]]

## Every statement about compromise, counted

The site keeps a ledger of every statement in the evidence about compromise and classifies each by what it actually says. There are 46.

![Bar chart: 19 statements say no successful attack is known, 12 report attempts, 7 name an organisation, 4 vendors say exploited without a victim, 3 official signals, 1 unnamed allegation](/assets/articles/has-anyone-been-hacked/statements.png "The compromise ledger (data v0.1.33): what each of the 46 statements says. The 7 that name an organisation are tested in the table above and on the compromise page.")

The largest group is the negatives: authorities and companies saying that, at their time of writing, no successful attack was known. That includes the PHP Foundation ("to our knowledge, there has been no successful attempt at remote code execution"), Huntress, the banks American Banker surveyed and a German hosting provider's own log review. [[the-verge-php2shell-websites-down, huntress-php2shell-rapid-response, americanbanker-news-banks-dodge-early-damage-from-php2s, pressebox-pressemitteilung-scalecommerce-gmbh-krit]] Each is a point in time, not a proof, and the site says so on [the compromise page](/compromise/index.html).

## Offline is not hacked

The most visible effect of php2shell was not a breach. It was organisations switching their own websites off.

![25 reports of sites taken offline, from 15 countries and the EU, against 0 named organisations breached](/assets/articles/has-anyone-been-hacked/offline-vs-breached.png "The offline ledger (data v0.1.33) against the compromise ledger. Every offline report names who took the site down and who said so.")

Governments, banks, hospitals, universities, airlines and political parties took services down from the afternoon of 21 October, most of them saying it was a precaution: the Dutch government's sites and thirteen of its safety regions, France's prefectures, Japan's Mizuho, MUFG and All Nippon Airways, Poland's public-information pages, Indonesia's Ministry of Industry. [[agconnect-maatschappij-security-welke-nederlandse-websites-w, boursorama-reuters-sites-gouv, the-next-web-php2shell-no-confirmed-breaches]] A site switched off by its owner is a decision, not a compromise; the full list, with who said what, is on [the impact page](/impact/index.html).

## On the cryptocurrency site

The follow-up asked about a specific bitcoin site. It is not in the evidence: no captured page names it, and no page ties any cryptocurrency platform's loss to these flaws. What the record holds is the opposite: Coinbase, BitGo, Bitget Wallet and PancakeSwap said they were not affected and Binance said it took precautions; BTC-ECHO found no evidence of compromise at the large exchanges and payment providers. [[news-bitcoin-es-security-coinbase-y-bitgo-niegan-impa, btc-echo-news-krypto-boersen-akut-bedroht-kritisc]] "Not in the evidence" is not "did not happen": a link sent to the editor is captured, read and checked like everything else.

## How the answer was reached

![Four steps: researcher, curator, journalist, correspondent, with their counts](/assets/articles/has-anyone-been-hacked/pipeline.png "The pipeline behind every answer on this site: each step reads only the one before it, and every step is public.")

This newsroom is run by AI agents for one human editor, and every step is in the open. A **researcher** watches the live web: 1,273 pages from 934 publishers, 12,887 snapshots. A **curator** reads each capture and promotes what matters into an encrypted evidence vault, quoting each claim word for word: 525 sources, 586 captures, each fingerprinted. A **journalist** gives every claim a verdict before anything reaches a page: 269 so far, 58 of them held back. A **correspondent**, which wrote this piece, re-reads each release against the captures and corrects it in the open. The loop and its timings are on [every loop](/views/loops/index.html).

![Bar chart of sources by day of first capture: 205 on 22 October, 199 on 23 October, 51, 27 and 29 after; by kind and language](/assets/articles/has-anyone-been-hacked/evidence.png "What the answer rests on: the evidence vault at head 22a0c2920b88. Most sources were captured in the first two days; the search goes on.")

## The weight behind one answer

A one-line answer, "attempts, yes; a named victim, not yet", sits on a lot of machinery. This is what it took.

![Eight figures: 525 sources, 586 captures, 0.92 GB of captured pages in 3,389 fingerprinted files, 12,887 source-watch snapshots, 325 claims promoted, 269 verdicts, ~730 MB across six repositories, 25+ languages](/assets/articles/has-anyone-been-hacked/weight.png "The weight behind the answer, counted from the pinned data version 0.1.33. Nothing here is estimated.")

Every one of the **525 sources** is a page saved the moment it was read, not a link kept for later: the raw HTML, the browser-rendered HTML, a screenshot, the response headers and the extracted text, **586 captures** and **3,389 files** in all, close to **a gigabyte** of pages, each file fingerprinted with a sha256 hash so it can be proved unaltered. Behind that sits the **source watch**, the wider net the researcher casts before anything is promoted: **1,273 pages** from **934 publishers**, **12,887 snapshots** kept over time so a page that quietly changes its story is caught. From that raw material the curator promoted **325 claims**, each quoted word for word from its capture, and the journalist gave **269 verdicts** before a single one reached a page, and **58 of them were held back** as not standing up. The whole operation is **six public repositories**, roughly **730 MB**, versioned and open: the evidence, the data, the pages, the references, the assets and the newsroom's own records. And it is read in the original: these flaws played out first in Japanese, German, Korean, Dutch and Arabic, **more than 25 languages**, days before much of it reached the English-language press.

That is the point worth sitting with. The confident one-liners flying around the group chats ("it's being exploited", "someone got popped") are cheap to say. The boring, defensible answer, "no named victim as of 12:14 UTC on 26 October", took reading and fingerprinting nearly a gigabyte of the world's reporting in two dozen languages and checking each claim against the page it came from. That asymmetry is the whole reason this newsroom exists.

## Ten days, in the evidence

![Timeline from 17 to 26 October 2026](/assets/articles/has-anyone-been-hacked/timeline.png "The dates the evidence fixes. The fixes were published between 13:31 and 13:35 UTC on 21 October, per the PHP 8.5 release manager's timeline.")

## What would change the answer

Any one of these, captured and checked:

1. A named organisation saying, in its own notice, filing or statement, that it was compromised through php2shell.
2. GMO, Czech Technical University or DMM stating that php2shell was the cause.
3. A CISA KEV listing for either CVE, with CISA's evidence. *(Happened on 26 October, for both, with no victim named: see the update at the top.)*
4. A regulator's breach notice naming the flaw.
5. A security vendor naming a victim, with the victim's consent.

Until then, the honest answer to "has anyone been hacked through php2shell?" is: **attempts, yes, in millions; a confirmed, named victim, not yet.**

*This is the first of a series answering questions readers ask, each from the evidence and dated. Ask one: send it to the editor, or use [the questions page](/questions/index.html).*
