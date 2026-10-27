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

Operations · data as of 26 October 2026, 17:09 UTC

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
      storyv0.22.34 · 2026-10-26
### [Someone stole the bitcoin. What that does, and does not, tell us about php2shell](../articles/steal-my-bitcoin/index.html)
storyv0.22.34 · 2026-10-26
### [Has anyone actually been hacked through php2shell? What 525 sources say, five days on](../articles/has-anyone-been-hacked/index.html)
factreportedv0.22.34 · 2026-10-26
### [As of 14:42 UTC on 26 October, no named organisation has said it was compromised through php2shell. Exploitation attempts are widely reported, in millions; Hadrian reports exploitation at scale and Pa](https://refs.php.oct.2026.newsroom.sgit.ai/facts/no-confirmed-compromise/)
CISACISAHuntressAmazonfrontv0.22.31 · 2026-10-26
### [Stories: written here](../index.html#stories)
frontv0.22.30 · 2026-10-26
### [Front page: at a glance](../index.html#glance)
factconfirmedv0.22.29 · 2026-10-26
### [The fixes were scheduled for 14:00 UTC on 21 October and were published between 13:31 and 13:35 UTC](https://refs.php.oct.2026.newsroom.sgit.ai/facts/release-time/)
oss-securityDauboisCERT-FRCERT-EUstoryv0.21.0 · 2026-10-25
### [What Wikipedia knows about being right: the principles, workflows and review habits this newsroom's agents should adopt](../articles/what-wikipedia-knows-about-being-right/index.html)
questionv0.19.2 · 2026-10-25
### [Has anyone actually been hacked?](../questions/been-hacked/index.html)
frontv0.19.2 · 2026-10-25
### [Front page: right now](../index.html#now)
frontv0.19.2 · 2026-10-25
### [Front page: the core facts](../index.html#facts)
frontv0.17.0 · 2026-10-24
### [Front page: what nobody knows yet](../index.html#unknown)
frontv0.17.0 · 2026-10-24
### [Front page: latest](../index.html#latest)
questionv0.14.8 · 2026-10-24
### [Is PHP really the software behind most websites?](../questions/most-websites/index.html)
storyv0.14.24 · 2026-10-24
### [The risk graph, before and after: what changed from one reader's five ideas](../articles/the-risk-graph-before-and-after/index.html)

Mark an item read with its circle: it fades, and leaves when you choose to hide read items. It comes back only if what it says changes.

### How sure are we?
- 20 confirmed
- 36 reported
- 7 disputed
- 3 contradicted
- 4 unverified

[The fact-check](../factcheck/index.html)

### Events per day, October
12171819202122
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
site v0.22.41 · data as of 2026-10-26T17:09Z · vault commit 1dceaa1dfa7f · https://php.oct.2026.newsroom.sgit.ai/ops/index.html
