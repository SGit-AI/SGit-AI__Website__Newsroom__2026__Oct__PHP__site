# Operations: what changed, what to do next, how sure we are

> Research: collected from outside sources and what this site derives from them; every fact links to a saved copy of its source.

The home for people who patch and defend: the next three actions, everything that changed newest first with what you have read marked, and the state of the evidence as charts: facts by status, events per day, exploitation signals, fixed versions.

SOperationsfor Sam, security lead

Your reading path
- [Your briefing](../briefings/security/index.html)
- [If you run PHP](../playbook/index.html)
- [Exploitation signals](../exploitation/index.html)
- [Detection and defence](../defence/index.html)
- [The agencies](../agencies/index.html)

    If you run PHPstepsCheck your stackPatching: who gets a fixThe two flawsExploitation signalsDetection and defenceThe agencies16Every claim70The code

Operations · data as of 29 October 2026, 00:09 UTC

# What changed, what to do next, and how sure we are

Internet-facing mod_php first, then FPM, then everything else. Where patching slips, apply php.net's temporary settings and record that each blocks a known path only. Alert on PHP workers spawning shells or fetching tools. Decide now who calls isolate or offline, and when.

## Your next three actions
The whole playbook1
### Patch internet-facing first

mod_php, then FPM, then the rest. Restart every worker; rebuild every image; check the running version after the restart.
2
### Bound the known paths

session.upload_progress off, low post_max_size, fatal_error_backtraces off on 8.5, pm.max_requests on FPM. Each blocks a path; none is a fix.
3
### Watch the process tree

Alert on a PHP worker spawning a shell or a downloader. A clean access log proves nothing about the host.

## What changed, newest first
Release by release
      storyv0.22.53 · 2026-10-29
### [Has anyone actually been hacked through php2shell? What 525 sources say, five days on](../articles/has-anyone-been-hacked/index.html)
storyv0.22.53 · 2026-10-29
### [A vendor says a campaign rooted 25 servers, two days before we saw it. What the report says, and what it leaves open](../articles/dream-research-rooted-25-servers/index.html)
questionv0.22.53 · 2026-10-29
### [Has anyone actually been hacked?](../questions/been-hacked/index.html)
frontv0.22.53 · 2026-10-29
### [Stories: written here](../index.html#stories)
frontv0.22.53 · 2026-10-29
### [Front page: right now](../index.html#now)
frontv0.22.53 · 2026-10-29
### [Front page: the core facts](../index.html#facts)
factreportedv0.22.53 · 2026-10-29
### [As of 00:09 UTC on 29 October, no named organisation has said it was compromised through php2shell. That the flaws are exploited is now CISA's position: on 26 October it added both CVEs to its Known E](https://refs.php.oct.2026.newsroom.sgit.ai/facts/no-confirmed-compromise/)
CISACISAHuntressAmazonfrontv0.22.51 · 2026-10-28
### [Front page: at a glance](../index.html#glance)
storyv0.22.51 · 2026-10-27
### [How a push reaches the pages: the six repositories, the edition, and why one push still waits for another](../articles/how-a-push-reaches-the-pages/index.html)
storyv0.22.46 · 2026-10-27
### [Someone stole the bitcoin. What that does, and does not, tell us about php2shell](../articles/steal-my-bitcoin/index.html)
frontv0.22.46 · 2026-10-27
### [Front page: latest](../index.html#latest)
factdisputedv0.22.46 · 2026-10-27
### [The UK's NCSC, the NSA and their counterparts in the EU and Australia advise taking systems offline where patching is not feasible](https://refs.php.oct.2026.newsroom.sgit.ai/facts/offline-allies/)
ACSCCERT-EUNCSC-NLACN / CSIRT Italiafactdisputedv0.22.46 · 2026-10-27
### [There is no evidence yet that hackers have exploited the flaw](https://refs.php.oct.2026.newsroom.sgit.ai/facts/no-exploitation/)
BBC NewsAmazonCISAfactcontradictedv0.22.46 · 2026-10-27
### [The flaws were disclosed on 22 October 2026](https://refs.php.oct.2026.newsroom.sgit.ai/facts/disclosure-22oct/)
php.netphp-src

Mark an item read with its circle: it fades, and leaves when you choose to hide read items. It comes back only if what it says changes.

### How sure are we?
- 20 confirmed
- 35 reported
- 9 disputed
- 2 contradicted
- 4 unverified

[The fact-check](../factcheck/index.html)

### Events per day, October
1217181920212226
Red: from the leak on 20 October. [The timeline](../timeline/index.html)

### Exploitation signals
- 2026-10-17Amazon: One exploit attempt against a MadPot honeypot from a commercial anonymisation network, four days bef
- 2026-10-17Amazon: One exploit attempt against a MadPot honeypot from an IP on a commercial anonymisation network, geol
- 2026-10-20 to 21Cloudflare: 'We observed attack traffic targeting our customers' after the leak, and attackers 'mutating the att
- 2026-10-21T02:00ZAmazon: Proof-of-concept attempts begin, then six hours of attempts from anonymised infrastructure; 'multipl

[Every signal](../exploitation/index.html) · [No named compromise: the evidence](../compromise/index.html)

### Fixed in
8.5.128.4.278.3.368.2.35
8.1 and older: source backports only. [Affected systems](../affected/index.html)


---
site v0.22.53 · data as of 2026-10-29T00:09Z · vault commit 6c07e190d81e · https://php.oct.2026.newsroom.sgit.ai/ops/index.html
