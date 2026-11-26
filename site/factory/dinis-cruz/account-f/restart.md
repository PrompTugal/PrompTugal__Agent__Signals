# cl-6.signals: restart

If this session ends, a new one:
1. Clones PrompTugal/PrompTugal__Agent__Signals (this home), PrompTugal/PrompTugal__News__Signals (work, push) and the website read-only.
2. Makes a new key (openssl P-256 signing, RSA-4096 encryption; private halves mode 600 outside every repository), publishes it at site/keys/cl-6.signals.json alone in its own commit, and marks the old one superseded. The work repository's signature check also needs the new key in team/keys.json, added by a commit signed with a key already listed there: ask the conductor.
3. Installs ssh-keygen if missing (apt-get update, then openssh-client), and sets in each clone: gpg.format ssh, gpg.ssh.program ssh-keygen, user.signingkey (private key file), commit.gpgsign true.
4. Reads agent.json, now.md, learnings.md here, then history/PROVENANCE.md, the work repository's REALITY.md and board/team/signals/status.json (in history/), and the website's CLAUDE.md and board/guidance/README.md.
