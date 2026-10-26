# How do I know whether my site is affected?

> Research: collected from outside sources and what this site derives from them; every fact links to a saved copy of its source.

If the site runs on PHP (WordPress, Drupal, Joomla, Magento, MediaWiki, and Laravel all do) and the running PHP version is older than 8.5.12, 8.4.27, 8.3.36 or 8.2.35 without a distribution backport, it is affected. Check the version where the code runs, after the restart, not the package list. For bought-in products, the Dutch NCSC keeps an inventory of 674 products and their status.

Question · kept by the librarian · `librarian@php.newsroom`

# How do I know whether my site is affected?

How it was asked: The follow-up to 'can anything be done', asked by every site owner.

## The short answer

If the site runs on PHP (WordPress, Drupal, Joomla, Magento, MediaWiki, and Laravel all do) and the running PHP version is older than 8.5.12, 8.4.27, 8.3.36 or 8.2.35 without a distribution backport, it is affected. Check the version where the code runs, after the restart, not the package list. For bought-in products, the Dutch NCSC keeps an inventory of 674 products and their status.

To paste back where it was asked: the paragraph above and `https://php.oct.2026.newsroom.sgit.ai/questions/am-i-affected/index.html`

## The answer, with its sources

**Every PHP installation serving web requests is in scope**, says php.net: mod_php, PHP-FPM, php-cgi, FrankenPHP and LiteSpeed, with mod_php at highest risk. The flaw runs before any application code, so your own code is not the question. [php.net](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-net-advisory/) [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-w8hw-w9fx-j79w/)

**Fixed in** 8.5.12, 8.4.27, 8.3.36 and 8.2.35. Versions 7.4 to 8.1 are affected too and get no release from PHP. [php.net](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-net-advisory/) [php-src](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-php-src-branch-7.4-backport/) [oss-security](https://refs.php.oct.2026.newsroom.sgit.ai/sources/openwall-oss-security-109619-thread/)

**Check the running version** (`php -v` inside the container, or `phpinfo()` on the box) after restarting, and check vendors that bundle PHP. [NCSC-NL](https://refs.php.oct.2026.newsroom.sgit.ai/sources/ncsc-nl-php2shell/) [BACS](https://refs.php.oct.2026.newsroom.sgit.ai/sources/ch-bacs-warnung-php/)

**For products you did not build**, the NCSC-NL inventory lists 674 products: 206 vulnerable, 46 fixed, 418 under investigation and 3 not vulnerable when it was counted. [NCSC-NL](https://refs.php.oct.2026.newsroom.sgit.ai/sources/ncsc-nl-php2shell-software-list/)

## The pages that carry it
- [Affected systems: versions, deployments, applications, inventory](../../affected/index.html)
- [The NCSC-NL inventory: 674 products](../../affected/software.html)
- [If you run PHP: the steps, in order, with their sources](../../playbook/index.html)
- [Briefing for a developer: Is my code the problem, what do I change, and how do I check the box I deployed to?](../../briefings/developer/index.html)

Next question: [Should we take our site offline?](../take-offline/index.html) · [every question](../index.html). Nothing here is advice for your environment; the [php.net advisory](https://www.php.net/archive/2026.php#2026-10-21-5) and your national agency are the authorities.


---
site v0.22.22 · data as of 2026-10-25T09:35Z · vault commit 87795d121200 · https://php.oct.2026.newsroom.sgit.ai/questions/am-i-affected/index.html
