# Briefing for a PHP or platform engineer: Which versions, which SAPIs, which settings, which commands?

> Research: collected from outside sources and what this site derives from them; every fact links to a saved copy of its source.

The php2shell story for a PHP or platform engineer: a thirty-second answer, what to decide, a reading path, the claims it rests on with their status and sources, and what is still open.

Briefing for Drew, php or platform engineer · ******Deeply technical · from the same 70 claims, selected and ordered for one reader

# Which versions, which SAPIs, which settings, which commands?

D
The answer in thirty seconds

Target 8.5.12, 8.4.27, 8.3.36 or 8.2.35; restart every worker and rebuild images. Until then: session.upload_progress.enabled=0 in php.ini or the pool, low post_max_size, fatal_error_backtraces=0 on 8.5, pm.max_requests=1 on FPM. Verify with php -v inside the running container. Keep session.upload_progress.enabled=0 after the update as well: CVE-2026-115560, published by PHP on 23 October (as Cloudflare and SOCRadar report), affects the fixed releases under a rare session setting and is fixed only in the next regular release.

[Read the site as Drew →](../../flaws/index.html)

Versions, SAPIs, settings and what each does. The claims are the primary records' own words where they exist.

## What to decide or do
- Target 8.5.12, 8.4.27, 8.3.36 or 8.2.35; restart every worker; rebuild images.
- memory_limit=-1 via php_admin_value; post_max_size 8M or 32M; cgroup limits not RLIMIT; session.upload_progress.enabled=0 in php.ini or the pool, never ini_set; fatal_error_backtraces=0 on 8.5; pm.max_requests=1.
- The CVE record calls 7.4 to 8.1 unaffected by omission; the backport branches say otherwise. Do not trust a scanner on this.
- The 8.5.12 fix may have a follow-up; watch php.net and oss-security.
- Verify the running version with phpinfo or php -v inside the container, after the restart.

## Your reading path
- [Your briefing](../../briefings/engineer/index.html) 4 min
- [The two flaws](../../flaws/index.html) 4 min
- [If you run PHP](../../playbook/index.html) 3 min
- [Affected systems](../../affected/index.html) 1 min
- [The code](https://refs.php.oct.2026.newsroom.sgit.ai/code/) 7 min

About 19 minutes in all. Choose *read as Drew* and the bar under the menu keeps your place on every page.

### What this briefing covers
- fixed versions
- which SAPI is how exposed
- the exact settings and where they must be set
- how to verify the running version

### What you can skip
- the board line
- the money

## Words you will meet

[PHP](../../glossary/index.html#php)[PHP-FPM](../../glossary/index.html#fpm)[SAPI](../../glossary/index.html#sapi)[CVE](../../glossary/index.html#cve)[Backport](../../glossary/index.html#backport)[Primary source](../../glossary/index.html#primary)[CVSS](../../glossary/index.html#cvss)[Vulnerability](../../glossary/index.html#vulnerability)[GitHub advisory (GHSA)](../../glossary/index.html#ghsa)[Remote code execution (RCE)](../../glossary/index.html#rce)[mod_php](../../glossary/index.html#mod-php)[Out of memory (OOM)](../../glossary/index.html#oom)[longjmp](../../glossary/index.html#longjmp)[Exploit, exploitation](../../glossary/index.html#exploit)

Each is underlined where it first appears; hover or tap for a one-line definition, or open [the glossary](../../glossary/index.html).

## The facts this rests on
- confirmed two or more primary sources agree, or the fact was counted from a captured file
- reported one party says so, and it has not been contradicted
- disputed the sources disagree, and both readings are shown
- contradicted a primary source says otherwise
- unverified even the reporting outlet could not check it
- p/n primary sources among the n cited; a blocked capture is counted and marked

| Claim | Who says it | Status | [Fact-check](../../factcheck/index.html) | Primary | Sources |
|---|---|---|---|---|---|
| Two critical vulnerabilities, CVE-2026-109618 and CVE-2026-109619, each CVSS v4.0 9.2, fixed in PHP 8.5.12, 8.4.27, 8.3.36 and 8.2.35 [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/two-cves-9.2/) | PHP Group (CNA), GitHub advisories, php.net | confirmed | **A6** Established●●●●●● | 5/5 | [CVE record](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cve-cve-2026-109618/) [CVE record](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cve-cve-2026-109619/) [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-w8hw-w9fx-j79w/) [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-6wmf-4rv5-p3rp/) [php.net](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-net-advisory/) |
| Unauthenticated RCE over HTTP against Apache mod_php with default settings, before any application code runs [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/rce-modphp/) | PHP security team (GHSA, oss-security), php.net | confirmed | **A6** Established●●●●●● | 3/3 | [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-w8hw-w9fx-j79w/) [oss-security](https://refs.php.oct.2026.newsroom.sgit.ai/sources/openwall-oss-security-2026-10-21-6/) [php.net](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-net-advisory/) |
| The fix removes longjmp() for out-of-memory errors in favour of a delayed soft OOM at the next VM safe point and a hard OOM via _exit(); the changelog line is 'Avoid state corruption via bailout' [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/fix-bailout/) | PHP security team | confirmed | **A6** Established●●●●●● | 3/3 | [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-w8hw-w9fx-j79w/) [php.net](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-net-changelog-8/) [php-src](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-php-src-branch-7.4-backport/) |
| Updating is the only complete mitigation; the configuration measures reduce exposure to specific paths and do not make an installation safe [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/only-update/) | php.net; PHP security team | confirmed | **A6** Established●●●●●● | 3/3 | [php.net](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-net-advisory/) [oss-security](https://refs.php.oct.2026.newsroom.sgit.ai/sources/openwall-oss-security-2026-10-21-7/) [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-6wmf-4rv5-p3rp/) |
| Triggering the bug is much easier than turning it into code execution; the CVSS vector says attack complexity highFastly: 'most deployments may be safe from RCE. Do not assume this holds true for you.' Imperva: five demonstrated techniques, three via session upload progress; about 67 KB of memory disclosed per attack. [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/ac-high/) | Imperva; Fastly; the CVE record | confirmed | **A3** Echoed●●●○○○ opinion status overstated | 3/3 | [Imperva Threat Research](https://refs.php.oct.2026.newsroom.sgit.ai/sources/imperva-blog-php2shell/) [Fastly](https://refs.php.oct.2026.newsroom.sgit.ai/sources/fastly-blog-php2shell/) [CVE record](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cve-cve-2026-109618/) |
| Both bugs are in the C engine, not in PHP code: the allocator's longjmp-based bailout on out-of-memory, and request globals that survive a failed requestThe fix replaces bailout with a delayed error and an UnwindExit at a safe point, adds a hard limit that _exits, and resets the globals. See the code page. [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/fix-engine/) | php/php-src fix commit; the GitHub advisories | confirmed | **A6** Established●●●●●● | 3/3 | [php/php-src, read from a clone](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-php-src-fix-commit-3584a98bd/) [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-w8hw-w9fx-j79w/) [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-6wmf-4rv5-p3rp/) |
| In researchers' own tests, pre-authentication RCE was confirmed against WordPress, Drupal, Joomla, MediaWiki, Roundcube, Magento, phpMyAdmin, Nextcloud, Laravel, Symfony and WHMCSTwo researcher parties, no third-party reproduction in the vault. The demo videos were not downloaded. [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/wordpress-drupal/) | Calif; Wiz for WordPress and Drupal | reported | **A2** Reported●●○○○○ | 2/2 | [Calif](https://refs.php.oct.2026.newsroom.sgit.ai/sources/calif-php2shell/) [Wiz](https://refs.php.oct.2026.newsroom.sgit.ai/sources/wiz-blog-php2shell/) |
| None of the public proof-of-concept exploits reviewed by VulnCheck has the correct mechanism; a lab reproduction of the leaked PoC's precondition produced a clean 200The Hacker News says the same of the public code. Fastly: working RCE needs knowledge of the running binary's layout on x86_64. [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/pocs-wrong/) | rjmendez (detection author) citing VulnCheck; Huntress | reported | **A1** Weak signal●○○○○○ status overstated | 1/2 | [rjmendez, GitHub](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-rjmendez-phpup-2026/) [Huntress](https://refs.php.oct.2026.newsroom.sgit.ai/sources/huntress-php2shell-rapid-response/) |
| Patching the demonstrated paths does not make the bailout mechanism safe; more paths should be expectedA position, from a vendor; consistent with the Fediverse report of a third bug. [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/more-paths/) | Fastly | reported | **A2** Reported●●○○○○ opinion | 1/2 | [Fastly](https://refs.php.oct.2026.newsroom.sgit.ai/sources/fastly-blog-php2shell/) [oss-security](https://refs.php.oct.2026.newsroom.sgit.ai/sources/openwall-oss-security-109619-thread/) |
| Remote code execution is confirmed on PHP-FPMGHSA-w8hw (CVE-2026-109618): 'no complete FPM exploit has been demonstrated for this SAPI'. The Foundation blog: RCE 'was also confirmed on PHP-FPM through application-level code paths'. GHSA-6wmf (CVE-2026-109619): session lifecycle RCE 'validated against mod_php and FPM'. The accounts may refer to different CVEs. [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/rce-fpm/) | PHP Foundation blog; GHSA-6wmf for the session path | disputed | **A6** Established●●●●●● | 4/4 | [PHP Foundation](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-foundation-blog-security-release/) [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-6wmf-4rv5-p3rp/) [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-w8hw-w9fx-j79w/) [oss-security](https://refs.php.oct.2026.newsroom.sgit.ai/sources/openwall-oss-security-2026-10-21-6/) |
| All PHP versions from 5 onwards are affected by at least one of the flawsThe CVE records list only 8.2 to 8.5 with defaultStatus 'unaffected'. php.net published source backports for 7.4, 8.0 and 8.1, which implies they are affected. A scanner that trusts the CVE record will miss 7.4 to 8.1. [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/versions-old/) | NCSC-NL; Wiz ('>= 5.4'); CERT-FR (5.x, 6.x, 7.x, 8.0, 8.1) | disputed | **A3** Echoed●●●○○○ disputed | 3/4 | [NCSC-NL](https://refs.php.oct.2026.newsroom.sgit.ai/sources/ncsc-nl-advisories/) [Wiz on X](https://refs.php.oct.2026.newsroom.sgit.ai/sources/x-wiz-io-php2shell/) [CERT-FR](https://refs.php.oct.2026.newsroom.sgit.ai/sources/certfr-2026-ale-014/) [oss-security](https://refs.php.oct.2026.newsroom.sgit.ai/sources/openwall-oss-security-109619-thread/) |
| A web application firewall may provide some protection until systems are patchedSwiss BACS: 'Even a web application firewall alone is not sufficient.' Cloudflare says its rules blocked the traffic it saw and that attackers mutated payloads to get past them. [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/waf/) | CISA | disputed | **A6** Established●●●●●● | 3/3 | [CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-alert-php-20261021/) [BACS](https://refs.php.oct.2026.newsroom.sgit.ai/sources/ch-bacs-warnung-php/) [Cloudflare](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cloudflare-blog-php2shell-waf/) |
| The flaws are CVSS 10.0The PHP Foundation: 'a wrong CVSS score of 10.0 (the actual score is 9.2)'. Daubois traces it to a social post relayed by Phoenix Security and to watchTowr via Cyber Daily. [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/cvss-10/) | social posts on 20 October, relayed by a vendor and a news site | contradicted | refuted contradicted | 1/2 | [PHP Foundation](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-foundation-blog-security-release/) [Daubois](https://refs.php.oct.2026.newsroom.sgit.ai/sources/daubois-blog-php2shell-rumors/) |
| The 8.5.12 fix may be incomplete, or there is a third, different bugPer a Matrix channel, Canonical asked PHP and 'was told that it's unrelated and not a real issue'. Second-hand. Nothing from PHP on the list at capture. [fact timeline →](https://refs.php.oct.2026.newsroom.sgit.ai/facts/fix-incomplete/) | Fediverse posts relayed to oss-security by Aaron Rainbolt and Yves-Alexis Perez | unverified | **A1** Weak signal●○○○○○ opinion disputed | 0/1 | [oss-security](https://refs.php.oct.2026.newsroom.sgit.ai/sources/openwall-oss-security-109619-thread/) |

## What is still open
- Who first leaked the CVE IDs on 20 October, and where. The PHP Foundation does not say; a PHP security team member points to an anonymous Hacker News post, and Notebookcheck and Nguoi Quan Sat repeat that account. No copy of the post is in the vault.
- Whether the deleted Calif video is the one now embedded on Calif's own write-up. Calif's page does not mention the leak.
- Whether any site was actually compromised before it was patched or taken offline. Every claim of exploitation so far is of attempts, probes or honeypot hits, or, in CISA's Known Exploited Vulnerabilities listing of 26 October, of exploitation with no victim named; or, in Dream Research's report of 26 October, of 25 rooted servers with no victim or vendor named and no confirmation (one source, repeated by three outlets); the named cases do not state php2shell as the cause. Authorities in Singapore and Luxembourg now ask operators to look for traces; the answer will come from those searches, if it comes.
- Which sites were really taken offline, and why. The list now draws on more captured reports (Germany's hospitals and hosts, Morocco, Romania, Japan), but most are press accounts; few come from the organisations themselves (the Dutch government, Latvia's agency, Weird Gloop, the Charité's spokesman as quoted). A community tracker counts 51 listed and 50 back.
- Whether the 8.5.12 fix is complete. A Fediverse report of a third bug or incomplete fix reached oss-security on 21 October; PHP reportedly told Canonical it is unrelated. On 23 October PHP published an informational advisory for a separate flaw, CVE-2026-115560, in the session upload progress feature, reported by Cloudflare, SOCRadar and The Hacker News: it affects fully patched releases including 8.5.12, needs a rare session setting, will be fixed in the next regular release, and has session.upload_progress.enabled=0 as the mitigation; SOCRadar reports no exploitation and no severity score. PHP's advisory is not in the evidence vault, and whether this is the bug the Fediverse report described is not stated.

The full set of claims is on [every claim](../../claims/index.html); the ordered steps for a vulnerable system are on [if you run PHP](../../playbook/index.html). Other readers: [Curious reader](../everyone/index.html) · [Website owner](../site-owner/index.html) · [Project or programme manager](../pm/index.html) · [Board member or executive](../board/index.html) · [Security lead](../security/index.html) · [Journalist](../journalist/index.html) · [Security researcher](../researcher/index.html) · [Analyst or policy advisor](../analyst/index.html) · [CISO](../ciso/index.html) · [CTO](../cto/index.html) · [CFO](../cfo/index.html) · [Data protection officer](../dpo/index.html) · [Head of AppSec](../appsec/index.html) · [Developer](../developer/index.html) · [Communications team](../comms/index.html).


---
site v0.22.53 · data as of 2026-10-29T00:09Z · vault commit 6c07e190d81e · https://php.oct.2026.newsroom.sgit.ai/briefings/engineer/index.html
