# Why is this such big news?

> Research: collected from outside sources and what this site derives from them; every fact links to a saved copy of its source.

Four things at once: the flaws are in PHP itself, which runs a large share of the web; they were found with AI help; the coordinated disclosure leaked a day early, so the fix shipped under pressure; and the NSA, CISA and NCSC told organisations that could not patch to take systems offline, which is why government, council and police sites went dark.

Question · kept by the librarian · `librarian@php.newsroom`

# Why is this such big news?

How it was asked: 'Article about this in The Times as well, so it's big news.'

## The short answer

Four things at once: the flaws are in PHP itself, which runs a large share of the web; they were found with AI help; the coordinated disclosure leaked a day early, so the fix shipped under pressure; and the NSA, CISA and NCSC told organisations that could not patch to take systems offline, which is why government, council and police sites went dark.

To paste back where it was asked: the paragraph above and `https://php.oct.2026.newsroom.sgit.ai/questions/why-big-news/index.html`

## The answer, with its sources

**Where the flaw is.** In the PHP engine, so it affects any PHP site regardless of the application on top, rated 9.2 out of 10. [CVE record](https://refs.php.oct.2026.newsroom.sgit.ai/sources/cve-cve-2026-109618/) [php.net](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-net-advisory/)

**How it was found.** Calif, OpenAI and Wiz each found it with frontier AI models in August; the same root cause had been seen in a 2024 audit and left unfixed. [Calif](https://refs.php.oct.2026.newsroom.sgit.ai/sources/calif-php2shell/) [PHP Foundation](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-foundation-blog-security-release/) [Wiz](https://refs.php.oct.2026.newsroom.sgit.ai/sources/wiz-blog-php2shell/)

**How disclosure broke.** The CVE IDs leaked on 20 October with a wrong 10.0 score, a demonstration video was published and deleted, and the release was brought forward a day. [PHP Foundation](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-foundation-blog-security-release/) [Daubois](https://refs.php.oct.2026.newsroom.sgit.ai/sources/daubois-blog-php2shell-rumors/)

**What the agencies said.** The NSA's post was viewed 10.1 million times at capture; councils, the Met Police, the OBR and government sites in the Netherlands, Finland, France and Latvia went offline as a precaution. [NSA Cyber on X](https://refs.php.oct.2026.newsroom.sgit.ai/sources/nsa-x-2112903220209098897/) [LBC](https://refs.php.oct.2026.newsroom.sgit.ai/sources/lbc-uk-websites-offline/) [Rijksoverheid / NCSC-NL](https://refs.php.oct.2026.newsroom.sgit.ai/sources/rijksoverheid-ncsc-php-news/) [CERT.LV](https://refs.php.oct.2026.newsroom.sgit.ai/sources/certlv-php-preventive/)

## The pages that carry it
- [PHP in October 2026: two critical security flaws, tracked as evidence](../../index.html)
- [Who found php2shell, and what the AI did](../../discovery/index.html)
- [How the coordinated disclosure broke](../../leak/index.html)
- [The timeline, 2024 to the latest capture](../../timeline/index.html)
- [In context: php2shell against Kaminsky, Heartbleed, Shellshock, Log4Shell and the last PHP RCE](../../context/index.html)

Next question: [We are on PHP 7.4, 8.0 or 8.1. Is there a patch?](../old-php/index.html) · [every question](../index.html). Nothing here is advice for your environment; the [php.net advisory](https://www.php.net/archive/2026.php#2026-10-21-5) and your national agency are the authorities.


---
site v0.22.40 · data as of 2026-10-26T17:09Z · vault commit 1dceaa1dfa7f · https://php.oct.2026.newsroom.sgit.ai/questions/why-big-news/index.html
