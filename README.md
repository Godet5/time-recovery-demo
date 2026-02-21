# Time Recovery Demo

Version: v1.1
Status: Live — Audio parked
Live URL: https://trd.dgf-creations.com
Branch: main

---

## What This Is

A client-facing interactive demo that shows what workflow automation
actually looks like from the customer's perspective.

This is not a landing page.
This is not a mockup.

It is a narrative demonstration of:
- Lead capture
- Automated booking
- Confirmation
- Intake
- Quote approval
- Invoice generation
- Payment
- Reschedule handling
- End-of-day owner dashboard
- Closing CTA with intake qualifier and calendar booking

The purpose is to make automation emotionally legible — and convert
that clarity into a booked conversation.

---

## Who This Is For

Service-based businesses that:
- Book manually
- Text customers between jobs
- Chase invoices
- Manage scheduling through phone calls

Examples:
- Pressure washing
- HVAC
- Roofing
- Plumbing
- Small contracting operations

---

## Closing Flow

The demo ends with a two-path CTA:

**Fast path** — ready buyers:
> Book a 20-Minute Workflow Audit → Google Calendar

**Qualifier path** — curious prospects:
> See My Business Applied → 3-question intake → Book Your Audit

Both paths land at the same calendar:
`https://calendar.app.google/rQQ1HoZEWjJjZwXC8`

---

## How To Run Locally

From the project root:

```bash
python3 -m http.server 8080
```

Open:

```
http://127.0.0.1:8080/ai-time-recovery/landing-demo.html
```

Note: Audio is currently parked (`AUDIO_ENABLED = false`).

---

## Audio Subsystem

The demo contains a fully implemented audio synchronization system:
- Blob-based audio loading with revoke on unload
- Drift correction (200ms cadence, 180ms threshold)
- Playback speed mirroring
- Scrubber synchronization with isSeeking guard
- Autoplay toast on browser policy block
- VO badge (ready/off state)
- Feature flag control (`AUDIO_ENABLED`)

To re-enable audio:
1. Place WAV file next to `landing-demo.html`
2. Set `AUDIO_ENABLED = true` in `landing-demo.html`
3. Serve the project folder

Source WAV: `~/downloads/20260219-215439_220450983.wav`

---

## Deployment

- **Platform**: Cloudflare Pages (GitHub OAuth — no secrets required)
- **Subdomain**: `trd.dgf-creations.com`
- **Deploy trigger**: Push to `main`
- **Build**: None (static HTML)
- **Root redirect**: `index.html` → `ai-time-recovery/landing-demo.html`

---

## Version History

- v1.1 — Live on trd.dgf-creations.com. CTA added: audit booking + intake qualifier. Calendar connected. Mobile viewport fixed.
- v1.0 — Initial release. Audio subsystem parked. Narrative arc finalized.

---

## Purpose

This repository exists as a standalone artifact.
It is intentionally isolated from experimental UI work.

It represents a deployable sales instrument.
