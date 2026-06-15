# Phase 0 — Setup Checklist (do these to unblock the build)

These are the **only items I can't do for you**: forming a legal entity, opening financial
accounts, and creating provider accounts that require your identity/payment method. Do the
**critical-path** items first — they have multi-day/multi-week lead times and gate everything
else. Everything marked _(I wire it)_ just needs the account created + a key handed to me.

Working brand name: **"LeadHearth"** — replace with whatever you prefer before buying domains.

---

## A. Critical path — start TODAY (longest lead times)

- [ ] **1. Form the LLC** (~$0–300 depending on state; many use a single-member LLC).
  - Options: file directly with your state's Secretary of State (cheapest), or use a
    formation service (Stripe Atlas ~$500 incl. Delaware C-corp — overkill here; LLC is fine).
  - Recommendation: home-state single-member LLC filed directly, or a service like Northwest/
    ZenBusiness (~$0 + state fee) if you want it hands-off.
  - **Lead time: 1 day–2 weeks** depending on state. **This blocks the bank + Stripe.**
- [ ] **2. Get an EIN** from the IRS (free, online, ~10 min once the LLC exists):
  https://www.irs.gov/businesses/small-businesses-self-employed/apply-for-an-employer-identification-number-ein-online
- [ ] **3. Open a business bank account** (free options: Mercury, Found, Bluevine; or a local
  bank). Needs LLC docs + EIN. **Lead time: same day–3 days.**
- [ ] **4. Pick the brand name + buy domains** (~$50 total):
  - 1 **brand domain** (e.g. `leadhearth.com`) — used for the website + client-facing email.
  - 2–3 **separate outreach domains** (e.g. `leadhearth.co`, `gethearthleads.com`) — used
    ONLY for cold email so the brand domain's reputation is never at risk.
  - Registrar: Cloudflare or Namecheap.
- [ ] **5. Start email warmup immediately** on the outreach domains via the cold-email tool
  (Section C). **Warmup takes ~2 weeks**, so starting now is the single biggest schedule win.
- [ ] **6. Google Workspace** on the brand domain (~$7/user/mo) for `info@`/`team@` mailboxes.

---

## B. Money rails

- [ ] **7. Stripe account** (https://stripe.com) under the LLC + business bank.
  - Complete identity/business verification fully (reduces the risk of holds when revenue scales).
  - I'll wire Checkout (setup fee) + metered/usage billing (per-result). _(I wire it — I just
    need the API keys.)_
  - **Lead time: same day, but verification can take a few days.**

---

## C. Provider accounts → API keys (create the account, paste the key into `.env`)

For each, create the account, grab the key, and add it to `.env` (template in `.env.example`).
All are pay-as-you-go or free-tier; total ≈ within the $500 tooling budget.

- [ ] **8. Anthropic API** (the AI brain) — https://console.anthropic.com → API key. ~$60–80/mo.
- [ ] **9. Cold-email sending tool** — **SmartLead** or **Instantly** (~$30–40/mo). Handles
  sending, warmup, inbox rotation, reply tracking. Connect the outreach domains here. _(I wire it.)_
- [ ] **10. Transactional email for fulfillment** — **Resend** or **SendGrid** (free tier to start).
  Used to send reactivation/review emails **from each client's own verified domain**. _(I wire it.)_
- [ ] **11. Google Cloud / Places API** — for the visibility-audit data. Free tier covers early
  volume. https://console.cloud.google.com → enable Places API → API key. _(I wire it.)_
- [ ] **12. AI voice agent** — **Vapi** (https://vapi.ai) or **Retell** — usage-based (~$30–50/mo)
  for the faceless sales/booking calls. _(I wire it.)_
- [ ] **13. Supabase** (Postgres DB, free tier) — https://supabase.com → project URL + keys. _(I wire it.)_
- [ ] **14. Vercel** (hosting, free tier) — https://vercel.com → connect this GitHub repo. _(I wire it.)_

---

## D. Compliance basics (I build the safeguards; you confirm the facts)

- [ ] **15. A physical mailing address** for the LLC (required in every cold/marketing email by
  CAN-SPAM). A virtual business address (e.g. from the bank or a service) is fine.
- [ ] **16. Confirm the rule we operate under:** email only, no SMS (keeps us out of TCPA/A2P
  10DLC entirely). Reactivation emails go ONLY to a client's **own** past customers. I'll bake
  unsubscribe + physical address + truthful headers into every template; you approve them.

---

## Budget recap (tooling ≈ $500; legal is separate)
| Bucket | Est. |
|---|---|
| Domains (brand + outreach) | ~$50 |
| Email warmup/sending + Workspace | ~$60 |
| Anthropic API (month 1) | ~$60–80 |
| Google Places API | ~$0–30 |
| AI voice (usage) | ~$30–50 |
| Reserve: data enrichment / small ad test | ~$200 |
| Vercel + Supabase + Stripe | $0 upfront (Stripe per-txn) |
| **Legal (LLC/EIN/bank) — separate** | **~$0–300 (you fund)** |

## Phase 0 is "done" when:
1. LLC + EIN + business bank exist. 2. Stripe verified. 3. Brand + outreach domains bought and
**warmup started**. 4. All keys in Section C are in `.env`. Hand me the keys (or grant access)
and I'll wire everything and build Phase 1 in sandbox for your review — nothing goes live until
you approve it.
