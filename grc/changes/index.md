# What changed in the risk graph, release by release

> Research: collected from outside sources and what this site derives from them; every fact links to a saved copy of its source.

The php2shell risk graph compared between any two releases: nodes and edges added and removed, bases changed, gaps opened and closed; computed from git at every release.

[GRC](../../grc/index.html) · [Risks](../../grc/risks/index.html) · [Stakeholders](../../grc/stakeholders/index.html) · [Frameworks](../../grc/frameworks/index.html) · [The graph](../../grc/graph/index.html) · [Explore](../../grc/explore/index.html) · [Gaps](../../grc/gaps/index.html) · [Changes](../../grc/changes/index.html) · [From the network](../../grc/network/index.html)

# What changed in the risk graph, release by release

The graph is rebuilt at every release. This page compares two releases of it: the nodes and edges added and removed, the edges whose basis changed (from inferred to confirmed, say), and the gaps that opened or closed. 190 releases carry a graph; 11 of them changed it. Pick any two below; the default is the latest change.

## v0.22.45 → v0.22.46

| Measure | v0.22.45 | v0.22.46 | Change |
|---|---|---|---|
| Nodes | 732 | 740 | +8 |
| Edges | 1,366 | 1,375 | +9 |
| Edges known as source | 264 | 273 | +9 |
| Edges known as code | 287 | 287 | same |
| Edges known as inferred | 815 | 815 | same |
| Gap: Controls joined to no code or test that implements them | 95 | 95 | same |
| Gap: Code with no owner one step away | 16 | 16 | same |
| Gap: Code no test reaches | 9 | 9 | same |
| Gap: Risks no story tells | 14 | 14 | same |
| Gap: Risks with no treatment | 0 | 0 | same |
| Gap: Risks with no owner | 0 | 0 | same |
| Gap: Vulnerabilities no test reaches | 0 | 0 | same |
| Gap: Edges inferred by an agent, not yet checked | 815 | 815 | same |

### Nodes added: 8

8 source
- [Arista Networks](../../grc/explore/index.html#focus=source:arista-security-advisory-0200) source
- [Broadcom (Symantec) Security](../../grc/explore/index.html#focus=source:broadcom-security-broadcom-php2shell-response) source
- [CISA KEV](../../grc/explore/index.html#focus=source:cisa-kev-kev-catalog-page) source
- [Craft CMS (Pixel & Tonic)](../../grc/explore/index.html#focus=source:craft-cms-craft-cloud-and-php2shell) source
- [NETGEAR](../../grc/explore/index.html#focus=source:netgear-000070960) source
- [Salesforce](../../grc/explore/index.html#focus=source:salesforce-general-message-20000267) source
- [Splunk](../../grc/explore/index.html#focus=source:splunk-svd-2026-1013) source
- [The Hacker News](../../grc/explore/index.html#focus=source:the-hacker-news-cisa-confirms-php2shell-exploitation) source

### Edges added: 11

11 *cites*
- As of 17:15 UTC on 28 October, no named organisation has sai *cites* Arista Networks source
- As of 17:15 UTC on 28 October, no named organisation has sai *cites* Broadcom (Symantec) Security source
- As of 17:15 UTC on 28 October, no named organisation has sai *cites* CISA KEV source
- As of 17:15 UTC on 28 October, no named organisation has sai *cites* Craft CMS (Pixel & Tonic) source
- As of 17:15 UTC on 28 October, no named organisation has sai *cites* NETGEAR source
- As of 17:15 UTC on 28 October, no named organisation has sai *cites* Salesforce source
- As of 17:15 UTC on 28 October, no named organisation has sai *cites* Splunk source
- As of 17:15 UTC on 28 October, no named organisation has sai *cites* The Hacker News source
- The UK's NCSC, the NSA and their counterparts in the EU and *cites* CERT-FR (ANSSI) source
- The UK's NCSC, the NSA and their counterparts in the EU and *cites* UK National Cyber Security Centre (NCSC) source
- The UK's NCSC, the NSA and their counterparts in the EU and *cites* US National Security Agency (NSA) source

### Edges removed: 2
- The flaws were disclosed on 22 October 2026 *cites* BBC News
- The UK's NCSC, the NSA and their counterparts in the EU and *cites* BBC News

## Every release that changed the graph

| Release | Against | Nodes | Edges | Bases | Gaps | Nodes / edges after |
|---|---|---|---|---|---|---|
| [v0.22.46](#from=0.22.45&to=0.22.46) 2026-10-27 | v0.22.45 | +8 −0 | +11 −2 | 0 | +0 −0 | 740 / 1,375 |
| [v0.22.43](#from=0.22.42&to=0.22.43) 2026-10-27 | v0.22.42 | +2 −0 | +6 −0 | 0 | +0 −0 | 732 / 1,366 |
| [v0.22.34](#from=0.22.33&to=0.22.34) 2026-10-26 | v0.22.33 | +2 −0 | +2 −0 | 0 | +0 −0 | 730 / 1,360 |
| [v0.22.25](#from=0.22.24&to=0.22.25) 2026-10-26 | v0.22.24 | +1 −0 | +1 −0 | 0 | +0 −0 | 728 / 1,358 |
| [v0.19.3](#from=0.19.2&to=0.19.3) 2026-10-25 | v0.19.2 | +1 −0 | +1 −0 | 0 | +0 −0 | 727 / 1,357 |
| [v0.15.19](#from=0.15.18&to=0.15.19) 2026-10-24 | v0.15.18 | +2 −0 | +2 −0 | 0 | +0 −0 | 726 / 1,356 |
| [v0.14.30](#from=0.14.29&to=0.14.30) 2026-10-24 | v0.14.29 | +3 −0 | +3 −0 | 0 | +0 −0 | 724 / 1,354 |
| [v0.13.0](#from=0.12.1&to=0.13.0) 2026-10-24 | v0.12.1 | +1 −1 | +1 −1 | 0 | +0 −0 | 721 / 1,351 |
| [v0.12.1](#from=0.12.0&to=0.12.1) 2026-10-24 | v0.12.0 | +8 −0 | +8 −0 | 0 | +0 −0 | 721 / 1,351 |
| [v0.10.13](#from=0.10.12&to=0.10.13) 2026-10-23 | v0.10.12 | +271 −0 | +504 −0 | 839 | +0 −9 | 713 / 1,343 |
| [v0.6.0](#from=&to=0.6.0) 2026-10-22 | the first graph | +442 −0 | +839 −0 | 0 | +143 −0 | 442 / 839 |

How it is made: every release commits the graph the build wrote ([data/grc-graph.json](https://data.php.oct.2026.newsroom.sgit.ai/latest/grc-graph.json)). `admin/build/grc_history.py` compares each release's graph with the one before and keeps what changed in [data/grc-history.json](https://data.php.oct.2026.newsroom.sgit.ai/latest/grc-history.json), written once per release, at its own build. The gaps are counted with today's rules ([data/grc-gaps.json](https://data.php.oct.2026.newsroom.sgit.ai/latest/grc-gaps.json)) over each release's graph, so every pair is measured the same way. An edge is the same edge when its start, verb and end are the same. Graphs before v0.10.13 recorded no basis on an edge. Comparing two releases that are not next to each other replays the changes between them in your browser.


---
site v0.22.51 · data as of 2026-10-28T17:15Z · vault commit 75668aedfb6d · https://php.oct.2026.newsroom.sgit.ai/grc/changes/index.html
