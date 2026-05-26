# Fieldamigo — Heartbeat

This is a public liveness signal for **Fieldamigo**, a productized field-service CRM
built and maintained by Charles Husted (Tampa, FL).

The [`HEARTBEAT`](HEARTBEAT) file is stamped with a fresh date every time Charles
pushes code to the (private) Fieldamigo source repository. Every deployed Fieldamigo
CRM checks this file's last-commit date once a week. If it goes stale past the
threshold (90 days), each CRM automatically emails its owner — because it may mean
the maintainer is no longer around.

**This repo is intentionally public and contains no source code** — just a timestamp
and a recovery guide. The Fieldamigo source itself is private; access to it is granted
to customers who own their deployment (see [`RECOVERY.md`](RECOVERY.md)).

If you received an automated "maintainer dormant" email from your CRM, start with
[**RECOVERY.md**](RECOVERY.md).

— Contact: charles@fieldamigo.com
