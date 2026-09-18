# After-Hours AI Receptionist — Mini-PRD (pre-build spec)

Status: spec approved 2026-09-18. Decisions: voice-first with SMS fallback concept, web-simulated demo (no real telephony), form-based knowledge-base editing for v1. Code build paused — spec published first.

## Problem
Small service businesses — nail salons, barbershops, auto shops, cleaning companies — lose bookings every day to unanswered calls. The owner is with a client, it's after closing time, it's the weekend: the phone rings, nobody picks up, and the caller books with whoever answers. For a first-time buyer who just acquired the business from a retiring owner, every lost booking is margin they can't afford to lose — and they can't afford a full-time receptionist either.

## Target user
First-time owner-operators of small service businesses bought from retiring owners. Non-technical. The bar: "can I set this up between clients?"

## Solution
An AI receptionist that answers the business's calls 24/7. It greets callers, answers common questions (hours, prices, services), books / reschedules / cancels appointments, takes messages for anything it can't handle — then texts a summary to the owner. Setup is a 10-minute onboarding: answer questions about your services, prices, and hours, and you have a receptionist.

## Demo story
"Hana just bought a nail salon. It's 9pm and she's home. A customer calls the salon..." Show: the call answered, a pricing question handled, an appointment booked, and Hana getting the text summary in the morning. One continuous story, no human intervention.

## Scope — in for v1
- Voice conversation: greet, answer FAQs from the business knowledge base, handle booking / reschedule / cancel, take messages
- Owner onboarding: ~10-minute setup flow (services, prices, hours, policies) in plain language
- Owner notifications: text or email summary of every after-hours interaction
- Editable knowledge base: the owner updates hours, prices, or policies without technical skill

## Scope — out for v1
- Real telephony (Twilio number): prototype demos through a web-based simulated call
- Payments or deposits at booking time
- Multi-location support
- Deep integrations with existing booking systems (books into its own calendar; owner gets notified instead)

## What "working" looks like
1. A stranger can "call" the demo salon and complete a booking with zero human help.
2. The owner can set it up in about 10 minutes with no technical skill.
3. Every interaction produces an owner-facing summary.

## Open questions for the owner (X)
1. Voice-first or SMS-first? Proposal: voice-first for the receptionist, SMS as the fallback for missed calls (pairs with the "missed-call text-back" sibling idea).
2. Real phone number for the demo (Twilio, small ongoing cost) or web simulation? Proposal: web simulation for the portfolio; real telephony is the v2 story.
3. Knowledge base editing: conversational ("we changed our hours to 9-6") or a simple form? Proposal: form for v1, conversational edit as a fast follow.

## Initial tradeoffs
- Web-simulated call keeps the prototype demoable in a portfolio with no telephony cost, no real number, and no telephony account. Real phone integration is the obvious v2 and a good "next steps" story.
- Narrow vertical (appointment-based service businesses) over a generic receptionist. Specificity is the differentiator — generic AI receptionists already exist.
- Booking into its own calendar rather than integrating with Square/Acuity/etc. Integrations are a v2; the v1 proves the conversation and the booking logic.
