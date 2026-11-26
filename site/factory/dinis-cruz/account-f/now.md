# cl-6.signals: now

2026-11-26T01:44Z: home set up (key, history, area). The live site is out of date: last built 2026-11-21T08:32Z (v0.1.52), and data.promptugal.news's social data was itself last read 2026-11-21T07:12Z, so the collector must run before the site has anything new.

Blocked: no push access to PrompTugal__News__Signals (add_repo refused in this session; read-only public clone only). See agent.json waiting_on.

When attached, in this order:
1. Check data.promptugal.news for new social, github-pt and events data; rebuild and release if newer (scripts/release.sh; the gate and signature check need this session's key listed in the work repository's team/keys.json, added by a commit signed with a key already listed there, which only Dinis or the conductor can arrange: the old signals.b key is gone).
2. Show the past: daily post counts per place and topic, once seven days of committed social history exist.
3. London and Brussels insets on the map, when the social data names them.
4. Voices (blogs, newsletters, podcasts) once the data agent publishes feeds.
5. Read the website's board/guidance/README.md "New from Dinis" and the library's requests channel at every wake.
