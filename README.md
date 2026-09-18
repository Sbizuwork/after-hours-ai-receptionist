# 📞 After-Hours AI Receptionist

> An AI receptionist for small service businesses. It answers the calls the owner can't — after closing time, between clients, on weekends — answers FAQs, books appointments, and texts the owner a summary.

🚧 **Status: building in the open, spec first.** The full product spec lives below. Working code is coming next — the thinking is published before the code.

## The Problem

Small service businesses — nail salons, barbershops, auto shops, cleaning companies — lose bookings every day to unanswered calls. The owner is with a client, it's after closing time, it's the weekend: the phone rings, nobody picks up, and the caller books with whoever answers.

For a first-time buyer who just acquired the business from a retiring owner, every lost booking is margin they can't afford to lose — and they can't afford a full-time receptionist either.

## The Solution

An AI receptionist that answers the business's calls 24/7:

- Greets callers and answers common questions (hours, prices, services)
- Books, reschedules, and cancels appointments
- Takes messages for anything it can't handle
- Texts the owner a summary of every after-hours interaction

Setup is a 10-minute onboarding: answer questions about your services, prices, and hours — no technical skill needed. The bar: a first-time owner can set it up between clients.

## Planned Demo

"Hana just bought a nail salon. It's 9pm and she's home. A customer calls the salon…"

The demo will show one continuous story: the call answered, a pricing question handled, an appointment booked, and Hana getting the text summary in the morning — no human intervention.

## How It Will Work

- **Conversation engine** — intent matching over a business knowledge base (greeting, hours, pricing, services, booking, reschedule/cancel, message-taking, graceful fallback). Architected so a real LLM can replace the demo engine later.
- **Knowledge base** — services, prices, hours, policies. Owner-editable in plain language via a simple form (v1).
- **Booking** — books into its own calendar; the owner is notified of every booking.
- **Owner dashboard** — every after-hours interaction summarized: who called, what they wanted, what got booked.

## Decisions So Far

- **Voice-first, SMS fallback.** The receptionist answers calls; missed calls fall back to text.
- **Web-simulated demo first.** No telephony account, no real number, no cost — the portfolio demo runs in the browser. Real telephony (Twilio) is the v2 story.
- **Narrow vertical over generic.** Appointment-based service businesses, not "AI receptionist for everyone." Specificity is the differentiator.
- **Form-based knowledge editing for v1.** Conversational editing ("we changed our hours") is a fast follow.

## Roadmap

- [x] Product spec (this README)
- [ ] Working demo — web-based simulated call
- [ ] Owner onboarding flow (10-minute setup)
- [ ] Owner dashboard with call summaries
- [ ] Knowledge base editor
- [ ] Real telephony integration (v2)

## Built With (planned)

Plain HTML/CSS/JS — no build step, no backend, no API keys for the demo. A zero-cost, zero-friction portfolio demo.

## Why This Exists

Part of a build-in-public series: practical AI tools for the "silver tsunami" — the wave of small businesses changing hands as baby-boomer owners retire. Each project is one plug-and-play tool a non-technical new owner can actually use.
