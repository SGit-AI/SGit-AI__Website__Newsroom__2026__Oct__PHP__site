# Do our developers need to change our code?

> Research: collected from outside sources and what this site derives from them; every fact links to a saved copy of its source.

No. Both bugs are in the C engine that runs PHP, not in PHP code, and the demonstrated attack runs before any application code. The fix is updating the PHP runtime and restarting it. What developers can do is check the version on the machines they deploy to and rebuild container images.

Question · kept by the librarian · `librarian@php.newsroom`

# Do our developers need to change our code?

How it was asked: Asked by managers handed the headline.

## The short answer

No. Both bugs are in the C engine that runs PHP, not in PHP code, and the demonstrated attack runs before any application code. The fix is updating the PHP runtime and restarting it. What developers can do is check the version on the machines they deploy to and rebuild container images.

To paste back where it was asked: the paragraph above and `https://php.oct.2026.newsroom.sgit.ai/questions/change-code/index.html`

## The answer, with its sources

**The bugs are in the engine.** The fix commit changes the allocator's out-of-memory handling and the request globals in php-src, 389 files. [php/php-src, read from a clone](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-php-src-fix-commit-3584a98bd/) [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-w8hw-w9fx-j79w/) [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-6wmf-4rv5-p3rp/)

**Before your code runs.** The mod_php exploit was demonstrated with default settings before any application code runs. [PHP](https://refs.php.oct.2026.newsroom.sgit.ai/sources/github-ghsa-w8hw-w9fx-j79w/) [oss-security](https://refs.php.oct.2026.newsroom.sgit.ai/sources/openwall-oss-security-2026-10-21-6/) [php.net](https://refs.php.oct.2026.newsroom.sgit.ai/sources/php-net-advisory/)

## The pages that carry it
- [Briefing for a developer: Is my code the problem, what do I change, and how do I check the box I deployed to?](../../briefings/developer/index.html)
- [The code: where php2shell lives and what the fix does](https://refs.php.oct.2026.newsroom.sgit.ai/code/)
- [The fix, mapped to the code](https://refs.php.oct.2026.newsroom.sgit.ai/review/)

Next question: [Can anything be done to fix it, or do we just have to wait for updates?](../fix-or-wait/index.html) · [every question](../index.html). Nothing here is advice for your environment; the [php.net advisory](https://www.php.net/archive/2026.php#2026-10-21-5) and your national agency are the authorities.


---
site v0.22.42 · data as of 2026-10-26T17:09Z · vault commit 1dceaa1dfa7f · https://php.oct.2026.newsroom.sgit.ai/questions/change-code/index.html
