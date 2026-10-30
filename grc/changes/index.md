# What changed in the risk graph, release by release

> Research: collected from outside sources and what this site derives from them; every fact links to a saved copy of its source.

The php2shell risk graph compared between any two releases: nodes and edges added and removed, bases changed, gaps opened and closed; computed from git at every release.

[GRC](../../grc/index.html) · [Risks](../../grc/risks/index.html) · [Stakeholders](../../grc/stakeholders/index.html) · [Frameworks](../../grc/frameworks/index.html) · [The graph](../../grc/graph/index.html) · [Explore](../../grc/explore/index.html) · [Gaps](../../grc/gaps/index.html) · [Changes](../../grc/changes/index.html) · [From the network](../../grc/network/index.html)

# What changed in the risk graph, release by release

The graph is rebuilt at every release. This page compares two releases of it: the nodes and edges added and removed, the edges whose basis changed (from inferred to confirmed, say), and the gaps that opened or closed. 193 releases carry a graph; 12 of them changed it. Pick any two below; the default is the latest change.

## v0.22.52 → v0.22.53

| Measure | v0.22.52 | v0.22.53 | Change |
|---|---|---|---|
| Nodes | 740 | 744 | +4 |
| Edges | 1,375 | 1,379 | +4 |
| Edges known as source | 273 | 277 | +4 |
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

### Nodes added: 4

4 source
- [CyPro](../../grc/explore/index.html#focus=source:cypro-php2shell-exploit-roots-firewalls) source
- [Dream Research](../../grc/explore/index.html#focus=source:dreamgroup-chained-php2shell-roots-25-servers) source
- [The Hacker News](../../grc/explore/index.html#focus=source:the-hacker-news-thehackernews-php2shell-roots-25-s) source
- [The Next Web](../../grc/explore/index.html#focus=source:the-next-web-php2shell-cisa-kev-dream-25-servers) source

### Edges added: 4

4 *cites*
- As of 17:13 UTC on 29 October, no named organisation has sai *cites* CyPro source
- As of 17:13 UTC on 29 October, no named organisation has sai *cites* Dream Research source
- As of 17:13 UTC on 29 October, no named organisation has sai *cites* The Hacker News source
- As of 17:13 UTC on 29 October, no named organisation has sai *cites* The Next Web source

## Every release that changed the graph

| Release | Against | Nodes | Edges | Bases | Gaps | Nodes / edges after |
|---|---|---|---|---|---|---|
| [v0.22.53](#from=0.22.52&to=0.22.53) 2026-10-29 | v0.22.52 | +4 −0 | +4 −0 | 0 | +0 −0 | 744 / 1,379 |
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
site v0.22.54 · data as of 2026-10-29T17:13Z · vault commit cd9375f1aefd · https://php.oct.2026.newsroom.sgit.ai/grc/changes/index.html
