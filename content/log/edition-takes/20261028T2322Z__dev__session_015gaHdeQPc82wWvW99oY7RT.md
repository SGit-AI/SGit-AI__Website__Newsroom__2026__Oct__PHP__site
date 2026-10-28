# Edition take: a push to the site so that its deploy takes edition 0.22.51

- **When:** 2026-10-28T23:22:48Z
- **Who pushes:** dev@php.newsroom, in session `session_015gaHdeQPc82wWvW99oY7RT`, key `sha256:d1331dd12796268e` (team `records/keys/dev.json`); this file is signed with it (`.sig` beside it).
- **On whose word:** the editor, in that session, on 28 October 2026: fix the website publishing so the main site is current.
- **Why:** the press published edition 0.22.51 (press release `edition-0.22.51`, built after press logs 20261028T2300Z and 20261028T2313Z). A site takes the newest edition only on its own next push, and the main site's last push was before it (v0.22.61). This push is that push. The site still shows now.json site 0.22.50, data_as_of 2026-10-27T19:13Z.
- **What it changes:** nothing but this log under `content/log/`, which the site's gate allows (`content/` is the site's own). Not a force-push, not an empty commit; released with `tools/pages_release.sh`.
- **What should follow:** the deploy takes edition 0.22.51 (a commit by GitHub Actions with the trailer `Edition: 0.22.51`), gated by the site's own gate.
- **Rule:** team board dev-0016.
