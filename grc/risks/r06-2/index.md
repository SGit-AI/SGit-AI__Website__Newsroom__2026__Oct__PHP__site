# R06-2: Essential and financial entities miss their reporting clocks

> Research: collected from outside sources and what this site derives from them; every fact links to a saved copy of its source.

Because NIS2 asks for an early warning within 24 hours and DORA for major-incident reports on its own schedule, an entity that cannot tell a precautionary outage from an incident may report late or not at all, resulting in a regulatory finding on top of the incident.

[Risks](../index.html) / [R06 A compromise becomes a reportable breach](../../../grc/risks/r06/index.html) / R06-2

# R06-2: Essential and financial entities miss their reporting clocks

Because NIS2 asks for an early warning within 24 hours and DORA for major-incident reports on its own schedule, an entity that cannot tell a precautionary outage from an incident may report late or not at all, resulting in a regulatory finding on top of the incident.

[Explore the graph from this risk](../../explore/index.html#focus=risk:r06-2) · [What the graph is missing](../../gaps/index.html)

**Rating** **12** high · **Likelihood** 3 Possible · **Impact** 4 Major · **Kind** Compliance · **Acceptance** not recorded

**Basis.** Precautionary shutdowns may themselves meet the significance tests; the evidence does not say how entities classified them.

## The path

The risk sits in the middle. To its left, the stories that tell it, the roles and team members that act on it, and every stakeholder that carries part of it. To its right, what it arises from, the vulnerability behind that, the part of the fix that addresses it and the code the fix changed. Every line is an edge in the graph; every node is a link; hover for the full name. Vulnerabilities, stories and team members include those of the risk this one is part of; roles include those of the risks above and beneath it.

## Who carries it

One risk, assigned to every stakeholder that carries part of it, with the part each plays.

| Stakeholder | Part | Why | Its register |
|---|---|---|---|
| [Critical infrastructure providers](../../../grc/stakeholders/critical-infra/index.html) | **owner** | Essential entities under NIS2. | 2 risks |
| [Banks, insurers and financial entities](../../../grc/stakeholders/finance/index.html) | **owner** | Under DORA. | 1 risk |
| [EU and member-state CERTs](../../../grc/stakeholders/eu-agencies/index.html) | **regulator** | Receive the reports. | 5 risks |
| [CISO](../../../grc/stakeholders/ciso/index.html) | **treater** | Classifies the event. | 2 risks |

## What it arises from
- **Exploitation that cannot yet be seen.** Honeypots and edge networks see attempts; nobody has shown a compromise, and KEV waits for one. Absence of evidence is read as safety.

## The evidence

| Claim | Status | Fact-check | Sources |
|---|---|---|---|
| [As of 09:35 UTC on 25 October, no named organisation has said it was compromised through php2shell. Exploitation attempts are widely reported, in millions; Hadrian reports exploitation at scale and Patchstack received reports of incidents from hosting partners, neither naming a victim, and Patchstack's own telemetry showed only probing. Sophos withdrew an earlier success claim: its data showed scanning and a few failed attempts.](https://refs.php.oct.2026.newsroom.sgit.ai/facts/no-confirmed-compromise/) | reported | **A4** Corroborated●●●●○○ | [CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-kev-json/) [CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-alert-php-20261021/) [Huntress](https://refs.php.oct.2026.newsroom.sgit.ai/sources/huntress-php2shell-rapid-response/) [Amazon](https://refs.php.oct.2026.newsroom.sgit.ai/sources/aws-security-blog-madpot/) [SecurityWeek](https://refs.php.oct.2026.newsroom.sgit.ai/sources/securityweek-first-attempts-sensors/) [SecurityWeek](https://refs.php.oct.2026.newsroom.sgit.ai/sources/securityweek-exploitation-days-before/) [Recorded Future](https://refs.php.oct.2026.newsroom.sgit.ai/sources/recordedfuture-php2shell/) [Imperva Threat Research](https://refs.php.oct.2026.newsroom.sgit.ai/sources/imperva-blog-php2shell/) [Weird Gloop](https://refs.php.oct.2026.newsroom.sgit.ai/sources/weirdgloop-blog-php2shell/) [Paperjam](https://refs.php.oct.2026.newsroom.sgit.ai/sources/paperjam-article-php2shell-des-milliers-de-sites/) [PCMag](https://refs.php.oct.2026.newsroom.sgit.ai/sources/pcmag-news-hackers-already-trying-to-exploit-serious-php-flaw/) [IT Social](https://refs.php.oct.2026.newsroom.sgit.ai/sources/itsocial-cybersecurite-cybersecurite-articles-php/) [Lupa.cz](https://refs.php.oct.2026.newsroom.sgit.ai/sources/lupa-cvut-cyber-attack/) [Yahoo! News Japan](https://refs.php.oct.2026.newsroom.sgit.ai/sources/yahoo-jp-gmo-fx-login-leak/) [産経ニュース](https://refs.php.oct.2026.newsroom.sgit.ai/sources/sankei-dmm-service-halt/) [INTERNET Watch](https://refs.php.oct.2026.newsroom.sgit.ai/sources/impress-watch-valtec/) [The Verge](https://refs.php.oct.2026.newsroom.sgit.ai/sources/the-verge-php2shell-websites-down/) [Cyber Security News](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cybersecuritynews-critical-php2shell-exploit-code/) [American Banker](https://refs.php.oct.2026.newsroom.sgit.ai/sources/americanbanker-news-banks-dodge-early-damage-from-php2s/) [The Next Web](https://refs.php.oct.2026.newsroom.sgit.ai/sources/the-next-web-php2shell-no-confirmed-breaches/) [Die Presse](https://refs.php.oct.2026.newsroom.sgit.ai/sources/diepresse-41383717-die-php-sicherheitsluecke-ist-a/) [voix](https://refs.php.oct.2026.newsroom.sgit.ai/sources/voix-business-cards-rainforest-ip-activity-an/) [Haber.com](https://refs.php.oct.2026.newsroom.sgit.ai/sources/haber-teknoloji-siber-guvenlik-baskanligi-ndan/) |
| [The Dutch government took NCSC.nl offline as a precaution, with no active misuse seen yet; Dutch press reported DigiD, MijnOverheid and Overheid.nl offline too](https://refs.php.oct.2026.newsroom.sgit.ai/facts/nl-offline/) | reported | **A4** Corroborated●●●●○○ | [Rijksoverheid / NCSC-NL](https://refs.php.oct.2026.newsroom.sgit.ai/sources/rijksoverheid-ncsc-php-news/) [TPO.nl](https://refs.php.oct.2026.newsroom.sgit.ai/sources/tpo-nl-digid-offline/) |

## Treatments

| Treatment | Status | Where |
|---|---|---|
| Classify a precautionary shutdown against the reporting thresholds on the day | missing | [Impact: taken offline versus compromised](../../../impact/index.html) |

## The standards that govern it

| Framework | Control | What it asks | Family |
|---|---|---|---|
| [NIS2](../../frameworks/nis2/index.html) | [Art.23](../../frameworks/nis2/index.html#c-art-23) | Reporting significant incidents: early warning in 24 hours, notification in 72 hours, final report in a month | Law and regulation |
| [NIS2](../../frameworks/nis2/index.html) | [Art.20](../../frameworks/nis2/index.html#c-art-20) | Governance: management bodies approve and oversee the risk-management measures and can be held liable | Law and regulation |
| [DORA](../../frameworks/dora/index.html) | [Art.19](../../frameworks/dora/index.html#c-art-19) | Reporting major ICT-related incidents | Law and regulation |
| [DORA](../../frameworks/dora/index.html) | [Art.10](../../frameworks/dora/index.html#c-art-10) | Detection of anomalous activities | Law and regulation |
| [NIST SP 800-53](../../frameworks/nist80053/index.html) | [IR-6](../../frameworks/nist80053/index.html#c-ir-6) | Incident reporting | Frameworks and control catalogues |

## The stories that tell it
- No story on this site tells this risk yet.

On this site: [Impact: taken offline versus compromised](../../../impact/index.html) · [What sixteen agencies actually advise](../../../agencies/index.html)


---
site v0.22.20 · data as of 2026-10-25T09:35Z · vault commit 87795d121200 · https://php.oct.2026.newsroom.sgit.ai/grc/risks/r06-2/index.html
