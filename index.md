# PHP in October 2026: two critical security flaws, tracked as evidence

> Research: collected from outside sources and what this site derives from them; every fact links to a saved copy of its source.

PHP news for October 2026, led by the month's big story: two critical security flaws in PHP (CVE-2026-109618 and CVE-2026-109619, nicknamed php2shell). The current situation in plain words, the core facts with their evidence, what to do, and a briefing for every kind of reader.

Developing  ·  PHP news, October 2026  ·  [latest evidence 26 October 2026, 15:10 UTC](#checked)  ·  [last agent run 26 October 2026, 16:54 UTC](https://updates.php.oct.2026.newsroom.sgit.ai/views/loops/)

# Two serious security flaws in PHP, the software behind many of the world's websites

PHP is the software that WordPress and millions of other websites run on. A fix came out on 21 October 2026. Government cyber agencies have told organisations to install it now; the two US agencies add: take websites offline if you cannot. Phones and personal computers are not affected.

    What is happening nowExplain it from the startCheck your stackOn your phone

You may also see this called php2shell, or by its two official reference numbers, CVE-2026-109618 and CVE-2026-109619.

  JYour answer in thirty secondsfor Jordan, board member or executive
A critical flaw in software that runs many websites, fixed on 21 October. Every agency says update first; some say take systems offline if you cannot. As of 12:14 UTC on 26 October, the latest capture in the evidence vault, no named organisation has said it was broken into through this flaw, though attempts are widespread. Your questions are: do we know every system running PHP, are they updated and restarted, and who can pull a system offline and how fast.

Choose who you are in the bar above and this answer changes to fit.

Is there a fix?Yesinstall PHP 8.5.12, 8.4.27, 8.3.36 or 8.2.35How serious?Critical9.2 out of 10, both flawsDoes it reach you?Check your stackdescribe what you run and see what an attacker could reach in itAre attackers trying?Yesmillions of attempts, seen by one internet security companyAnyone confirmed hacked?Not yetno organisation, as of the latest checkWebsites taken offline28 reportssome one site, some a whole government; as a precautionOn the US 'used in attacks' list?Not yetthe US government's official list of flaws known to be used by attackersWhat do governments say?Update nowor take the website offline if you cannot; 16 agencies compared
This section v10 written in site [v0.22.30](https://team.php.oct.2026.newsroom.sgit.ai/admin/versions.html#v0.22.30) on 26 October 2026 · [history and changes, 9 earlier](https://updates.php.oct.2026.newsroom.sgit.ai/versions/front-glance/)

## Right now
as of 26 October 2026, 14:42 UTC, the latest page this site saved- A fix has been available since 21 October. Organisations that run websites on PHP are installing it. [php.net](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-net-advisory/)
- Every government cyber agency says: install the fix now. If you cannot, the US agencies say take the website offline; the UK puts that after temporary mitigations, and several European agencies say cut it off from the public internet first. [CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-alert-php-20261021/) [NCSC UK](https://refs.php.oct.2026.newsroom.sgit.ai/sources/ncsc-news-php/) [CERT-EU](https://refs.php.oct.2026.newsroom.sgit.ai/sources/certeu-sa-2026-018/) [NSA Cyber on X](https://refs.php.oct.2026.newsroom.sgit.ai/sources/nsa-x-2112903220209098897/)
- Attackers are trying to use the flaws, in large numbers: millions of attempts by one internet security company's count. As of 09:35 UTC on 25 October, no named organisation has said it was broken into through this flaw. The one security company that had claimed a successful break-in, Sophos, withdrew it; US banks and the large crypto platforms report none. [Matthew Prince, Cloudflare CEO on…](https://refs.php.oct.2026.newsroom.sgit.ai/sources/x-eastdakota-php2shell-stats/) [CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-kev-json/) [Paperjam](https://refs.php.oct.2026.newsroom.sgit.ai/sources/paperjam-article-php2shell-des-milliers-de-sites/) [Cyber Security News](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cybersecuritynews-critical-php2shell-exploit-code/) [American Banker](https://refs.php.oct.2026.newsroom.sgit.ai/sources/americanbanker-news-banks-dodge-early-damage-from-php2s/) [BTC-ECHO](https://refs.php.oct.2026.newsroom.sgit.ai/sources/btc-echo-news-krypto-boersen-akut-bedroht-kritisc/)
- The advice is moving from 'install the fix' to 'and check whether you were already broken into'. Singapore's and Luxembourg's authorities now say so. [CNA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/channelnewsasia-singapore-php-vulnerabilities-csa-singapore-firms-cybersecur/) [Paperjam](https://refs.php.oct.2026.newsroom.sgit.ai/sources/paperjam-article-php2shell-des-milliers-de-sites/)
- Some organisations took websites offline as a precaution: the Dutch government took its cyber agency's own site offline, and Dutch press reported the DigiD login down too. Almost all of them are back. [Rijksoverheid / NCSC-NL](https://refs.php.oct.2026.newsroom.sgit.ai/sources/rijksoverheid-ncsc-php-news/) [TPO.nl](https://refs.php.oct.2026.newsroom.sgit.ai/sources/tpo-nl-digid-offline/) [PHPocalypse Tracker](https://refs.php.oct.2026.newsroom.sgit.ai/sources/phpocalypse-tracker-sites-csv/) [Security.NL](https://refs.php.oct.2026.newsroom.sgit.ai/sources/securitynl-misbruik-gemeld/)

This section v7 written in site [v0.19.2](https://team.php.oct.2026.newsroom.sgit.ai/admin/versions.html#v0.19.2) on 25 October 2026 · [history and changes, 6 earlier](https://updates.php.oct.2026.newsroom.sgit.ai/versions/front-now/)

## The core facts, and the evidence for each
- confirmed two or more original sources agree
- reported one party says so; nobody has contradicted it
- disputed sources disagree
- unverified nobody has been able to check it
- confirmedThere are two flaws. Both are in PHP itself, underneath every website that uses it, and both are rated critical: 9.2 out of 10.[CVE record](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cve-cve-2026-109618/) [CVE record](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cve-cve-2026-109619/) [php.net](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-net-advisory/) [More →](flaws/index.html)
- confirmedSomeone anywhere on the internet, with no password, can use them against a website that has not installed the fix, and make its server run their own commands. Researchers proved this on the most traditional way of running PHP; for other setups it is likely but less certain.[PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-w8hw-w9fx-j79w/) [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-6wmf-4rv5-p3rp/) [PHP Foundation](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-foundation-blog-security-release/) [More →](flaws/index.html)
- confirmedThe fix is in PHP 8.5.12, 8.4.27, 8.3.36 and 8.2.35, released on 21 October 2026. Websites on PHP 8.1 or older have no ready-made fix.[php.net](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-net-advisory/) [php-src](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-php-src-branch-7.4-backport/) [More →](affected/index.html)
- reportedThe weak spot was first noticed in 2024 and left alone, because nobody could show it was dangerous. In August 2026, three research teams using AI tools showed that it was, and told the PHP project.[PHP Foundation](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-foundation-blog-security-release/) [Calif](https://refs.php.oct.2026.newsroom.sgit.ai/sources/calif-php2shell/) [Wiz](https://refs.php.oct.2026.newsroom.sgit.ai/sources/wiz-blog-php2shell/) [More →](discovery/index.html)
- confirmedThe plan was to announce the fix on 22 October. Word leaked out on 20 October, so it was released a day early.[PHP Foundation](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-foundation-blog-security-release/) [Daubois](https://refs.php.oct.2026.newsroom.sgit.ai/sources/daubois-blog-php2shell-rumors/) [More →](leak/index.html)
- reportedAttackers are trying, in large numbers: one internet security company reports millions of attempts, and Amazon reports a decoy server hit four days before the announcement. No named organisation has said it was broken into through these flaws, as of 09:35 UTC on 25 October, and the US government's official list of flaws known to be used in attacks did not include them when last checked.[Matthew Prince, Cloudflare CEO on…](https://refs.php.oct.2026.newsroom.sgit.ai/sources/x-eastdakota-php2shell-stats/) [THN](https://refs.php.oct.2026.newsroom.sgit.ai/sources/thehackernews-php2shell-4days/) [Paperjam](https://refs.php.oct.2026.newsroom.sgit.ai/sources/paperjam-article-php2shell-des-milliers-de-sites/) [CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-kev-json/) [CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-kev-catalog/) [More →](exploitation/index.html)
- confirmedEvery agency says install the fix. They disagree on what to do if you cannot: the US says take the website offline, the UK lists that as a last resort, several European agencies say cut it off from the public internet, and some say nothing about it.[CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-alert-php-20261021/) [NCSC UK](https://refs.php.oct.2026.newsroom.sgit.ai/sources/ncsc-news-php/) [CERT-EU](https://refs.php.oct.2026.newsroom.sgit.ai/sources/certeu-sa-2026-018/) [ACSC](https://refs.php.oct.2026.newsroom.sgit.ai/sources/acsc-alert-php/) [More →](agencies/index.html)
- confirmedThe headline '70% of the Internet' is not what it sounds like. It is roughly the share of websites whose server-side language is known that use PHP, which is what the same company's own article says; nobody has measured how many are actually at risk.[Wiz](https://refs.php.oct.2026.newsroom.sgit.ai/sources/wiz-blog-php2shell/) [Wiz on X](https://refs.php.oct.2026.newsroom.sgit.ai/sources/x-wiz-io-php2shell/) [Cloudflare](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cloudflare-blog-php2shell-waf/) [More →](numbers/index.html)

This section v6 written in site [v0.19.2](https://team.php.oct.2026.newsroom.sgit.ai/admin/versions.html#v0.19.2) on 25 October 2026 · [history and changes, 5 earlier](https://updates.php.oct.2026.newsroom.sgit.ai/versions/front-facts/)

## Latest
what changed on the site- 23 Oct, 10:03 UTCDie Presse: as of 12:03 Vienna time (10:03 UTC) on 23 October no successful attack via the PHP flaws was known in Austria. [Die Presse](https://refs.php.oct.2026.newsroom.sgit.ai/sources/diepresse-41383717-die-php-sicherheitsluecke-ist-a/)
- 23 Oct, 09:16 UTCJapan's RainForest reports that its honeypots recorded 21 php2shell-related requests from 14 different addresses: attempts, not break-ins. [voix](https://refs.php.oct.2026.newsroom.sgit.ai/sources/voix-business-cards-rainforest-ip-activity-an/)
- 23 Oct, 07:58 UTCIT Social: the update closes the flaw, but obliges a hunt for possible compromises; the published figures count attempts, not intrusions. [IT Social](https://refs.php.oct.2026.newsroom.sgit.ai/sources/itsocial-cybersecurite-cybersecurite-articles-php/)
- 23 OctAmerican Banker: no US bank or credit union has publicly reported a compromise, despite millions of attempts. [American Banker](https://refs.php.oct.2026.newsroom.sgit.ai/sources/americanbanker-news-banks-dodge-early-damage-from-php2s/)
- 22 Oct, 21:21 UTCSophos withdraws an earlier claim of a successful compromise: its data shows scanning and a few failed attempts, and a botnet payload it saw was blocked. [Cyber Security News](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cybersecuritynews-critical-php2shell-exploit-code/)

[Everything, in order →](timeline/index.html)

This section v5 written in site [v0.17.0](https://team.php.oct.2026.newsroom.sgit.ai/admin/versions.html#v0.17.0) on 24 October 2026 · [history and changes, 4 earlier](https://updates.php.oct.2026.newsroom.sgit.ai/versions/front-latest/)

## What nobody knows yet
- [Whether any website was actually broken into before it installed the fix.](impact/index.html)
- [Whether the fix is complete. A report on 21 October suggested it may not be; the PHP security team replied on the mailing list on 22 October, and this site will settle the question once that reply is saved here. Separately, on 23 October PHP published an advisory for another flaw, CVE-2026-115560, which affects fully patched releases and needs a rare session setting (reported by Cloudflare, SOCRadar and The Hacker News).](https://refs.php.oct.2026.newsroom.sgit.ai/code/)
- [Who leaked the news on 20 October, and where.](leak/index.html)
- [How many websites went offline, and why. The reports this site holds range from a single site to a whole government's platform; a community tracker lists about fifty sites that went dark and came back. Nobody has counted them all.](impact/index.html)
- [Where the 70% figure comes from. None of the pages that use it says how it was measured.](numbers/index.html)

This section v3 written in site [v0.17.0](https://team.php.oct.2026.newsroom.sgit.ai/admin/versions.html#v0.17.0) on 24 October 2026 · [history and changes, 2 earlier](https://updates.php.oct.2026.newsroom.sgit.ai/versions/front-unknown/)

### Ask about it

Answers cite the evidence on this site.
Questions readers ask

## How it unfolded
The full timeline2024An audit spots the out-of-memory weakness. Nobody can show it is exploitable, so it is left.Aug 2026Three teams using AI turn it into working attacks within three weeks and report them to PHP.20 OctThe secret leaks: the CVE numbers circulate two days early, with a wrong severity score.21 OctPHP releases the fix a day ahead of plan. Firewall vendors already have rules live.22 OctAgencies warn: update, or take systems offline. Sites go dark as a precaution.

## What governments advise
16 agencies
All say install the fix. They split on what to do if you cannot.
- 2 take offline
- 4 isolate or restrict
- 2 offline after other steps
- 6 no offline advice
- 2 not readable

[Every agency, in its own words →](agencies/index.html)

## Three ways to read this site
choose who you are in the bar above; the site takes you to yours
Briefing

The situation, the numbers that matter and what to ask: for decision makers and anyone new to the story.
Curious readerWebsite ownerBoard member or executiveProject or programme managerCFOCommunications team
Operations

What changed, what to do next and the state of the evidence, side by side: for people who patch and defend.
CISOCTOSecurity leadHead of AppSecPHP or platform engineerDeveloper
Analysis

The answer, the picture, then the evidence: for people who weigh sources, numbers and contradictions.
Data protection officerJournalistSecurity researcherAnalyst or policy advisor

## The briefing for you
How the readers are mapped
### I want to understand it

You heard about this on the news or from a colleague and want to know what it is and whether it touches you.
ACurious readerAlex · Plain EnglishWhat happened, does it affect me, and should I worry?4 reads · about 14 min Start →CWebsite ownerCasey · Plain EnglishMy website runs on WordPress or similar: am I affected, and what do I ask my host?4 reads · about 14 min Start →
### I make the decisions

You own a budget, a plan or a risk, and need what to decide, in what order, and what to ask your team.
JBoard member or executiveJordan · Plain EnglishAre we exposed, what is it costing us, and who owns the decision to pull a system?5 reads · about 18 min Start →TProject or programme managerTaylor · Plain EnglishWhat unplanned work does this create, who do I chase, and what do I tell stakeholders?5 reads · about 16 min Start →QCFOQuinn · Plain EnglishWhat is the financial exposure, what does downtime cost against breach cost, and will insurance respond?5 reads · about 17 min Start →MData protection officerMorgan · Some technicalWas personal data exposed, does this start a GDPR breach assessment or a 72-hour notification, and what do I document?6 reads · about 15 min Start →RCISORobin · Some technicalWhat is our exposure, what is our evidence we were not hit, and what do I tell the board?6 reads · about 17 min Start →ACTOAvery · Some technicalWhat does this cost us in engineering time, what breaks when we patch, and what do we change so the next one is a non-event?5 reads · about 21 min Start →
### I tell others

You write or speak about this, and need what is true, what is not, and who said it first.
RJournalistRowan · Some technicalWhich numbers hold up, who said what first, and what is still unverified?6 reads · about 13 min Start →RCommunications teamRiley · Plain EnglishWhat can we say that is true, what should we not say, and what will we be asked?5 reads · about 17 min Start →
### I run or build systems

You patch, configure, monitor or write code, and need versions, settings and signals.
SSecurity leadSam · Some technicalWhat do I patch first, what do I watch for, and when do I take something offline?5 reads · about 14 min Start →JHead of AppSecJamie · Deeply technicalWhich of our applications are in scope, which settings matter, and what do we add to the pipeline?5 reads · about 15 min Start →DPHP or platform engineerDrew · Deeply technicalWhich versions, which SAPIs, which settings, which commands?5 reads · about 18 min Start →LDeveloperLee · Some technicalIs my code the problem, what do I change, and how do I check the box I deployed to?4 reads · about 18 min Start →
### I study it

You research vulnerabilities or advise on policy, and need the evidence, the open questions and the precedent.
ASecurity researcherAsh · Deeply technicalWhat are the bug classes, what was demonstrated, and what is still open?5 reads · about 19 min Start →BAnalyst or policy advisorBlake · Some technicalHow did coordinated disclosure fail, and what does AI-assisted discovery change?6 reads · about 15 min Start →

## Stories: written here
signed, dated and kept as written; everything above is researchSomeone stole the bitcoin. What that does, and does not, tell us about php2shellHouse story · correspondent · 2026-10-26Has anyone actually been hacked through php2shell? What 525 sources say, five days onHouse story · correspondent · 2026-10-26What Wikipedia knows about being right: the principles, workflows and review habits this newsroom's agents should adoptHouse story · ontologist · 2026-10-25The editor, interviewed: Dinis Cruz on why this site existsInterview · the editor, in his own words
[All stories →](articles/index.html)

What else is going on Other vulnerabilities in the news this month, with the evidence that each is exploited beside the attention it gets: the SGit newsroom's Pulse, in a separate section, not about PHP. Pulse →

## How this site knows
543web pages saved as evidence, each with the time it was saved70statements checked: 20 confirmed, 10 disputed, 4 unverified68dated events, from 2024 to today16government agencies' advice compared
Every page this site relies on was saved at the moment it was read, with a fingerprint that proves it has not been altered since, so a fact can be checked even if the original page changes or disappears. Nothing here is advice for your own systems; for that, read [the PHP project's announcement](https://www.php.net/archive/2026.php#2026-10-21-5) and your national cyber agency. The site is put together by software agents working for one editor, Dinis Cruz; [how it works](method/index.html).

Latest evidence: [the evidence vault](https://refs.php.oct.2026.newsroom.sgit.ai/sources/), latest capture 26 October 2026, 14:42 UTC · [the source watch](https://refs.php.oct.2026.newsroom.sgit.ai/vaults/source-watch/), latest run 26 October 2026, 15:10 UTC · [the NCSC-NL inventory](patching/inventory/index.html), latest change read 23 October 2026, 12:50 UTC. Last agent run: 26 October 2026, 16:54 UTC (sherpa); [how the site is kept current, loop by loop](https://updates.php.oct.2026.newsroom.sgit.ai/views/loops/). Already know the vocabulary? [The specialist summary](summary/index.html) has the technical version of this page.


---
site v0.22.32 · data as of 2026-10-26T14:42Z · vault commit 2fc7e432584b · https://php.oct.2026.newsroom.sgit.ai/index.html
