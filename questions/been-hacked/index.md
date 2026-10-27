# Has anyone actually been hacked?

> Research: collected from outside sources and what this site derives from them; every fact links to a saved copy of its source.

Not that any named organisation has said, as of 00:45 UTC on 27 October, the latest capture in the evidence vault. Attack attempts are real and in the millions at Cloudflare alone, Amazon saw one on a honeypot four days before disclosure, and two security vendors are reported as saying it is being exploited, without naming any victim (other reports of the same vendors describe attempts). CISA added both flaws to its exploited-vulnerabilities list on 26 October, which means it has evidence of exploitation, but it names no victim. The sites that went offline say they did it as a precaution.

Question · kept by the librarian · `librarian@php.newsroom`

# Has anyone actually been hacked?

How it was asked: The Times' standfirst: 'Hackers could seize control of online stores and steal passwords'.

## The short answer

Not that any named organisation has said, as of 00:45 UTC on 27 October, the latest capture in the evidence vault. Attack attempts are real and in the millions at Cloudflare alone, Amazon saw one on a honeypot four days before disclosure, and two security vendors are reported as saying it is being exploited, without naming any victim (other reports of the same vendors describe attempts). CISA added both flaws to its exploited-vulnerabilities list on 26 October, which means it has evidence of exploitation, but it names no victim. The sites that went offline say they did it as a precaution.

To paste back where it was asked: the paragraph above and `https://php.oct.2026.newsroom.sgit.ai/questions/been-hacked/index.html`

## The answer, with its sources

**Attempts: yes.** Cloudflare's chief executive reported millions of exploit attempts across its network by the early hours of 22 October; Amazon saw an attempt on a honeypot on 17 October; Latvia saw automated attempts, none successful. [Matthew Prince, Cloudflare CEO on…](https://refs.php.oct.2026.newsroom.sgit.ai/sources/x-eastdakota-php2shell-stats/) [Amazon](https://refs.php.oct.2026.newsroom.sgit.ai/sources/aws-security-blog-madpot/) [CERT.LV](https://refs.php.oct.2026.newsroom.sgit.ai/sources/certlv-php-preventive/)

**Successful break-ins: none named.** As of 00:45 UTC on 27 October no named organisation has said it was compromised through php2shell, and the four named cases in the press (Valtec, ČVUT, GMO, DMM) either were retracted or state no php2shell cause; two security vendors, Hadrian and Patchstack, are reported as saying it is being exploited, without naming a victim, while other reports of the same vendors describe attack attempts, not compromises. CISA's alert of 21 October said it had not observed exploitation; on 26 October CISA added both CVEs to its Known Exploited Vulnerabilities catalog, which takes evidence of exploitation, naming no victim: exploited, but no organisation named as compromised. Huntress saw none on its partners' systems. This is a statement about the evidence so far, and it will change. [CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-alert-php-20261021/) [CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-kev-json/) [CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-alert-kev-20261026/) [Huntress](https://refs.php.oct.2026.newsroom.sgit.ai/sources/huntress-php2shell-rapid-response/) [The Register](https://refs.php.oct.2026.newsroom.sgit.ai/sources/the-register-hackers-pile-on-php2shell/) [Insurance Business](https://refs.php.oct.2026.newsroom.sgit.ai/sources/insurance-business-au-asiapac-attacks-begin/) [Security.NL](https://refs.php.oct.2026.newsroom.sgit.ai/sources/securitynl-misbruik-gemeld/) [BleepingComputer](https://refs.php.oct.2026.newsroom.sgit.ai/sources/bleepingcomputer-amazon-4-days-before/) [INTERNET Watch](https://refs.php.oct.2026.newsroom.sgit.ai/sources/impress-watch-valtec/) [Lupa.cz](https://refs.php.oct.2026.newsroom.sgit.ai/sources/lupa-cvut-cyber-attack/) [Yahoo! News Japan](https://refs.php.oct.2026.newsroom.sgit.ai/sources/yahoo-jp-gmo-fx-login-leak/) [産経ニュース](https://refs.php.oct.2026.newsroom.sgit.ai/sources/sankei-dmm-service-halt/)

**The offline sites were precautions.** Weird Gloop, the Dutch government's DigiD and the NCSC-NL itself, Finland's Valtori and Oxford City Council all describe taking sites down to be safe, not after a breach. A UK minister said there was no breach of Budget security after the OBR site was affected. [Weird Gloop](https://refs.php.oct.2026.newsroom.sgit.ai/sources/weirdgloop-blog-php2shell/) [Rijksoverheid / NCSC-NL](https://refs.php.oct.2026.newsroom.sgit.ai/sources/rijksoverheid-ncsc-php-news/) [Yle](https://refs.php.oct.2026.newsroom.sgit.ai/sources/yle-finland-government-sites-shut/) [Oxford Chronicle](https://refs.php.oct.2026.newsroom.sgit.ai/sources/oxfordchronicle-councils-offline/) [East Anglian Daily Times](https://refs.php.oct.2026.newsroom.sgit.ai/sources/eadt-minister-budget-no-breach/)

**The caveat.** A clean log does not prove a clean system (JPCERT), and the last PHP core flaw, in 2024, was exploited one day after disclosure. Absence of a confirmed victim after two days is a fact about two days; authorities in Singapore and Luxembourg now ask operators to look for traces of a break-in. [JPCERT/CC](https://refs.php.oct.2026.newsroom.sgit.ai/sources/jpcert-at260033/) [Akamai Security Research](https://refs.php.oct.2026.newsroom.sgit.ai/sources/akamai-blog-cve-2024-4577-one-day/) [CISA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cisa-kev-json/) [CNA](https://refs.php.oct.2026.newsroom.sgit.ai/sources/channelnewsasia-singapore-php-vulnerabilities-csa-singapore-firms-cybersecur/) [Paperjam](https://refs.php.oct.2026.newsroom.sgit.ai/sources/paperjam-article-php2shell-des-milliers-de-sites/)

## The pages that carry it
- [Exploitation signals, in order](../../exploitation/index.html)
- [Impact: taken offline versus compromised](../../impact/index.html)
- [Every claim, with its status and sources](../../claims/index.html#no-confirmed-compromise)

Next question: [Do I need to change my passwords?](../passwords/index.html) · [every question](../index.html). Nothing here is advice for your environment; the [php.net advisory](https://www.php.net/archive/2026.php#2026-10-21-5) and your national agency are the authorities.


---
site v0.22.43 · data as of 2026-10-27T00:45Z · vault commit 24f0b0e22666 · https://php.oct.2026.newsroom.sgit.ai/questions/been-hacked/index.html
