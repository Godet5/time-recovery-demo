# Time Recovery Demo

Version: v1.0
Status: Audio parked
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

The purpose is to make automation emotionally legible.

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
- Blob-based audio loading
- Drift correction
- Playback speed mirroring
- Scrubber synchronization
- Autoplay guard
- Feature flag control

To re-enable audio:
1. Place WAV file next to `landing-demo.html`
2. Set `AUDIO_ENABLED = true`
3. Serve the project folder

---

## Version History

- v1.0 — Initial release. Audio subsystem parked. Narrative arc finalized.

---

## Purpose

This repository exists as a standalone artifact.
It is intentionally isolated from experimental UI work.

It represents a deployable sales instrument.
