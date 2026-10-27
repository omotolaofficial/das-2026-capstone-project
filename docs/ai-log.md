# AI Log

## Build 1 — Event Ticketing Domain Core

- **What I asked AI to help with:** Implement the event inventory, booking rules, booking references, FIFO waitlist, demo, and lookup benchmark.
- **What I reviewed:** The booking-capacity rules, sold-out booking rejection, cancellation flow, waitlist order, and booking lookup.
- **What I tested:** `npm run demo` and `npm run benchmark`.
- **What the tests showed:** The demo refused a booking when insufficient seats remained, accepted a booking that fitted the remaining capacity, and showed Chidi as next on the waitlist after Ada cancelled. The benchmark showed that `Map.get()` was substantially faster than `Array.find()` for the tested lookups.
- **My learning:** A `Map` supports efficient lookup by key, while a FIFO queue serves the person who joined first. I should test edge cases rather than assume generated code is correct.
