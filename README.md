# ClientKit — Your Freelance Studio, Sorted

A single-file web app for beginner freelancers in India: track clients, price websites,
send invoices and never forget a follow-up. No account, no server — everything lives in
your browser's localStorage.

**Live:** https://abhiramunni.github.io/clientkit/

## What it does

- **Money at a glance** — four tiles show what's earned this month, what's waiting to be
  paid, what's overdue and what's still in the pipeline. A monthly income goal with a
  progress ring sits right underneath.
- **Client rolodex** — every client on a card (Lead → Pitched → Active → Done). Tap a
  card to open their file: projects with a stage stepper, invoices, notes and last
  contact. Advance a project stage in one tap.
- **Quote builder** — a 3-step wizard. Pick a site type (one-page ₹8,000 · multi-page
  ₹15,000 · online shop ₹30,000 · redesign ₹12,000), tick extras (logo, SEO, hosting,
  maintenance, copywriting), and get a total with an optional 18% GST toggle. Copy the
  quote text for WhatsApp/email, or save it straight as a Quoted project.
- **Invoices** — newest first, with status worked out from the due date (Draft / Sent /
  Paid / Overdue). Mark paid, mark sent, delete. Add an invoice by hand in ten seconds.
- **Follow-ups due** — auto-generated nudges: invoices past due, quotes unanswered for
  7+ days, leads you haven't pitched yet. One tap logs the follow-up as sent.
- **Plain-words guides** — pricing a website, what goes in a quote, getting paid on
  time, one-page contracts, GST for freelancers (indicative only — check with a CA),
  and following up without being pushy.
- **Privacy first** — copy a plain-text summary, remove the sample data, or erase
  everything (two-tap confirm). No data ever leaves the device.

Seeded with three real prospects from the author's own freelance outreach (Bokeh Ads,
Macaron Weddings, Jaseemography) plus clearly-marked sample clients, projects and
invoices so the money tiles demonstrate themselves — remove samples any time.

## Tech

- One self-contained `index.html` (HTML + CSS + vanilla JS, no build step, no backend).
- Fraunces + Inter, warm editorial palette (ivory paper, espresso ink, bronze/terracotta).
- Two AI-generated warm-editorial photos embedded as base64, with a slow Ken Burns drift.
- Full-screen cinematic intro (tap-to-skip; quick version on return visits) and a
  3-step onboarding coach.
- localStorage only. Works offline once loaded.

## QA

70/70 headless jsdom assertions pass (`node qa-test.js`), including hand-verified money
maths: earned ₹18,000 · waiting ₹25,000 · overdue ₹12,000 · pipeline ₹89,000; quote
maths one-page ₹8,000 + logo ₹3,000 + SEO ₹2,500 = ₹13,500 (₹15,930 with 18% GST);
mark-paid, follow-up, add-client, add-invoice, remove-samples and erase-all flows all
verified. `node --check` clean, zero uncaught JS errors, no pictographic emoji.

## License

MIT — use it, fork it, make it yours.
