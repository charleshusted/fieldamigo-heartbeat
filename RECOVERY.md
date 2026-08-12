# RECOVERY.md — If you're reading this

This is the public continuity guide for **Fieldamigo**, a productized CRM for service
businesses, built, hosted, and maintained by Charles Husted in Tampa, Florida.

This repo holds a liveness timestamp and this guide. **The Fieldamigo source code is
private and is not shipped to customers** — Fieldamigo runs as a hosted, isolated
instance per business. That is deliberate, and it is why the emphasis below falls on
the customer's *data*, which is unconditionally theirs, rather than on the code, which
is not.

## Why you might be reading this

1. A Fieldamigo customer's CRM detected that Charles hasn't pushed code in 90+ days,
   emailed the customer automatically, and they handed you this link to keep their
   instance running.
2. You're an owner planning ahead, confirming the exit really exists.
3. You're curious and clicked through.

This is written mainly for case (1) — a developer picking up a customer's instance.

## The key fact: the customer's data is already in their hands

Before anything else, and independently of everything below: **the data is safe and
portable, and always was.**

- **Settings → Import / Export** in the CRM downloads a fresh `.sql` dump and a `.csv`
  bundle at any time. The `.sql` restores into any Postgres via `psql -f`, or opens as
  plain text in any editor. The `.csv` bundle is every table, zipped.
- Monthly `.sql` + `.csv` backup links have been emailed to the customer automatically
  all along, so a recent copy already exists in their inbox.
- The instance is single-tenant — one database, one application, one set of backups,
  nothing entangled with another business.

Whatever happens to the application, the business records are recoverable on their own,
in open formats, with no cooperation required from anyone.

## What about the source code?

Be clear-eyed about this, because it's the part people most want a neat answer to.

Fieldamigo is hosted. The source is **not** on the customer's server and was not sold
to them, unless they purchased a **full source buy-out** — in which case they already
hold it outright and can hand it to you today. Ask which applies; it's the first
question worth answering.

If they did not buy it out, the source is not automatically available to you, and this
guide will not pretend otherwise. The route is:

1. **Contact Charles** — `charles@fieldamigo.com`.
2. If Charles is genuinely unreachable, contact his estate or next of kin. The source
   is an asset with an owner; that owner is who can license or release it.
3. In the meantime, the customer is not stuck. Everything in the section above is
   already theirs, and a competent developer can run a business off exported data
   while the licensing question is settled.

The honest summary: **the data is guaranteed, the code is not.** If the customer needs
a guarantee on the code itself, the buy-out is how they get one, and it's available to
purchase at any time — including before any of this becomes urgent.

## License

Fieldamigo is licensed under **PolyForm Noncommercial 1.0.0**.

**For a developer continuing the work:**
- You may read, run, and modify the source for noncommercial purposes.
- Maintaining a paying customer's existing instance for fair compensation is fine —
  you're providing a service to that customer, not selling Fieldamigo as a product.
  The customer's right to keep their shop running is what they paid for; Charles's
  absence doesn't change it.
- You may **not** take the code and sell it as your own SaaS or a competing product.

**For a customer:** your right to keep running your own shop's CRM is the right you
paid for. Nothing about Charles being absent changes that.

## What to do, in rough order

1. Read this file.
2. Secure the customer's data first — have them pull a fresh `.sql` + `.csv` export
   from **Settings → Import / Export**, or retrieve the latest monthly email bundle.
   Do this before touching anything else; it costs minutes and removes all urgency.
3. Settle the source question (see above): if the customer bought it out, they hand it
   to you now; if not, contact Charles or his estate. Don't block step 2 on this.
4. The deploy + dev runbooks ship with the source
   (`docs/FIELDAMIGO_DEPLOY_RUNBOOK.md`, `docs/FIELDAMIGO_DEV_SETUP.md`,
   `docs/FIELDAMIGO_CONTINUITY.md`). Follow them to run it locally, recreate the
   instance, or migrate the deployment onto infrastructure the customer controls.
5. Charge the customer fairly for your time.

## Charge them fairly

These are small-business owners who chose Fieldamigo because they were tired of being
gouged by SaaS subscriptions. Don't gouge them — and don't undercharge; you're doing
real work. Honor the transparency the relationship was built on.

## Who to contact

- Charles Husted — Tampa, Florida — `charles@fieldamigo.com`.
- If Charles isn't reachable: the customer who handed you this is your point of truth.
  Their needs are concrete and immediate; everything else is procedural.

---

*This guide lives in the public heartbeat repo and is updated as the continuity story
evolves. Reading it does not by itself mean Charles is gone — it's simply where the
recovery information lives if it's ever needed.*
