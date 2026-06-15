# LeadHearth — faceless AI lead-gen for home-services businesses

A neutral-brand, AI-operated service that helps local home-services businesses (HVAC,
roofing, plumbing, electrical, etc.) win more booked jobs — by reactivating their own past
customers via email, optimizing their Google Business Profile, automating reviews, and
following up on new leads instantly. Pricing is a setup fee plus pay-per-booked-job, so the
service only earns when the client does.

> **Status: pre-build.** This repo currently contains only the Phase 0 setup materials.
> The application (landing page, audit generator, outreach + fulfillment engines) is built
> in sandbox after Phase 0 is complete and is reviewed before anything goes live.

## Start here
- **`docs/phase-0-setup-checklist.md`** — the legal/accounts/domains setup that unblocks the
  build (the only steps that require you personally). Do the critical-path items first.
- **`.env.example`** — every API key the app will need, with pointers to where each comes from.

## Guardrails
- Email only (no SMS) — keeps us within CAN-SPAM and out of TCPA/A2P 10DLC.
- Reactivation emails go only to a client's **own** past customers, with unsubscribe + physical
  address on every send.
- Nothing customer-facing ships without automated compliance checks **and** explicit human approval.
