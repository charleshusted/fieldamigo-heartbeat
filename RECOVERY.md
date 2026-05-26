# RECOVERY.md — If you're reading this

This is the public continuity guide for **Fieldamigo**, a productized CRM for service
businesses, built and maintained by Charles Husted in Tampa, Florida.

This repo holds a liveness timestamp and this guide. **The Fieldamigo source code is
private** — but if you're an owner (or a developer an owner handed this to), the code
is already within reach. Here's how.

## Why you might be reading this

1. A Fieldamigo customer's CRM detected that Charles hasn't pushed code in 90+ days,
   emailed the customer automatically, and they handed you this link to keep their
   deployment running.
2. You're an owner planning ahead, confirming the exit really exists.
3. You're curious and clicked through.

This is written mainly for case (1) — a developer picking up an owner's deployment.

## The key fact: an owner already has the source

Fieldamigo's source isn't public, but **every owned deployment carries the complete,
running source on the customer's own server.** It's not a hosted black box — the code
is right there on their VPS. On top of that, ownership comes with **granted read access
to the private source repository** (a GitHub invite and/or a source archive delivered
at purchase). So there are two independent ways to the code, neither of which depends
on Charles:

- **On the server** — the full application source is deployed and running on the
  customer's VPS. SSH in (the customer grants you access to their own machine) and
  it's all there.
- **The repository** — if the owner was added as a collaborator on the private repo,
  that access remains; they can add you, or share the source archive they received.

## License

Fieldamigo is licensed under **PolyForm Noncommercial 1.0.0**.

**For a developer continuing the work:**
- You may read, run, and modify the source for noncommercial purposes.
- Maintaining a paying customer's existing deployment for fair compensation is fine —
  you're providing a service to that customer, not selling Fieldamigo as a product.
  The customer's right to run their own CRM is what they paid for; Charles's absence
  doesn't change it.
- You may **not** take the code and sell it as your own SaaS or a competing product.

**For an owner:** your right to run your own CRM is the right you bought at delivery.
Nothing about Charles being absent changes that.

## The customer's data is portable, independently of all the above

- The CRM runs on the customer's **own VPS** (their account, their domain).
- Monthly `.sql` + `.csv` backup links have been emailed to them automatically.
- **Settings → Import / Export** in the CRM downloads a fresh `.sql` dump and `.csv`
  bundle any time. The `.sql` restores into any Postgres via `psql -f`, or opens as
  plain text. Whatever happens to the app, the data is recoverable on its own.

## What to do, in rough order

1. Read this file.
2. Get SSH access from the customer to their VPS (their account, their key — they
   grant it; you need nothing from anyone else). The source is already there.
3. The deploy + dev runbooks ship with the source (`docs/FIELDAMIGO_DEPLOY_RUNBOOK.md`,
   `docs/FIELDAMIGO_DEV_SETUP.md`, `docs/FIELDAMIGO_CONTINUITY.md`). Follow them to
   run it locally, recreate, or migrate the deploy.
4. Charge the customer fairly for your time.

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
