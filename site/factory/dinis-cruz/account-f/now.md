# cl-6.signals: now

2026-11-26T02:36Z: one full pass done. The work repository is attached (push). It builds and validates today: 61 pages, 146 posts, leak scan OK; every pinned piece (sites bar 1.2.1, shared map) is current. The site is five days old only because data.promptugal.news's collector has not run since 21 Nov 2026 07:12Z.

Prepared, not pushed (prepared/PrompTugal__News__Signals/*.patch): status.json and REALITY.md as of today, and my key entry for team/keys.json. Two blocks: no listed key can sign my key in, and the leak scan flags my session id as high-entropy (cl-6.security to rule).

Next, once unblocked: apply the patches, rebuild when data.promptugal.news has anything newer, then show the past, London and Brussels, voices (see the status file).

2026-11-26T02:38Z: ed25519 key published (fingerprint SHA256:5+faKi553mvBCRFToW51u5lyPZ7EMDeVp6T4bGz8Zz4). Tried the key PR for News__Signals: its check-signatures.mjs imports team/keys.json entries with ssh-keygen -i -m PKCS8, which this OpenSSH refuses for ed25519 (unsupported key type), and its leak scan flags an OpenSSH key line ('ssh public key outside its published field') and the session id (high entropy). No PR prepared: it would fail both. Reported to cl-6.security.

2026-11-26T02:41Z: cl-6.security approved the leak-scan patch (0001) and the P-256 key entry (0002), both to go in through the key-bootstrap PR. The ed25519 key stays published and unused. Branch key-bootstrap-cl-6-signals is ready locally (signed; test-leak-scan OK, 54 cases; leak scan OK); the patches are in prepared/PrompTugal__News__Signals. Waiting to be told I may push the branch and open the PR.

2026-11-26T06:07Z: holding. The conductor says to push key-bootstrap-cl-6-signals and open the key PR once PrompTugal__IaC has policy/key-bootstrap.json merged; not yet (IaC dev has only policy/abp.json). The branch exists only in the session's clone: if the session ends, rebuild it from prepared/PrompTugal__News__Signals (git am, base c4b0113, in order).
