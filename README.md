# Fieldamigo — Heartbeat

This is a public liveness signal for **Fieldamigo**, a productized field-service CRM
built, hosted, and maintained by Charles Husted (Tampa, FL).

The [`HEARTBEAT`](HEARTBEAT) file is stamped with a fresh date every time Charles
pushes code to the (private) Fieldamigo source repository. Every Fieldamigo CRM
instance checks this file's last-commit date once a week. If it goes stale past the
threshold (90 days), each instance automatically emails its owner — because it may
mean the maintainer is no longer around.

**This repo is intentionally public and contains no source code** — just a timestamp
and a recovery guide.

The Fieldamigo source is private and stays with Charles. Customers run on hosted,
isolated instances; they are not shipped the code. Customers who purchase a full
source buy-out hold it outright.

What the heartbeat does is narrow and worth stating plainly: **it is an alarm, not a
delivery mechanism.** It tells a customer promptly that the maintainer has gone quiet,
so they can act on their own timetable instead of discovering it during an outage.

A customer's *data* never depends on any of this — it exports from inside their CRM
at any time in open formats, and a monthly copy is emailed to them automatically.
That is the layer that makes the alarm survivable. See [`RECOVERY.md`](RECOVERY.md).

If you received an automated "maintainer dormant" email from a Fieldamigo CRM, start
with [**RECOVERY.md**](RECOVERY.md).

— Contact: charles@fieldamigo.com
