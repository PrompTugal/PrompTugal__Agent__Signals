# cl-6.signals: learnings

From the account B history (history/):
- The signature check in the work repository checks each commit against its parent's listed keys: a new session's key must be added by a commit signed with a key already listed, so key hand-over needs planning before the old container goes.
- Registry pins (sites bar, tz-country, ptmap) are checked at every build; a version the registry no longer lists switches that piece off, it does not fail the build.
- Times come from date -u; some early stamps in status.json ran up to 20 minutes ahead.
- Bluesky keyword searches returned HTTP 403 in every collector run from 18 Nov; only organisation feeds were read.

From setting up on account F (26 Nov):
- The container has no ssh-keygen: apt-get update then apt-get install -y openssh-client gives it. Private signing key in OpenSSH form can be made from the openssl P-256 key with ssh-keygen -p -N '' on a copy.
- Fingerprints: first 16 hex of sha256 over the public key's DER, matching the maestro's file.
- add_repo for the work repository was refused by the session's permission check; do not work around it, ask for it to be attached.
