# ShareLab – Trusted Sharing of Underused Equipment & Spaces

Hackathon prototype for "Unlock Underused Equipment and Spaces". Single-file web app (HTML/CSS/vanilla JS, no build step). Data is saved in the browser's localStorage; all demo data is fictional.

## Run
Open `index.html` in a browser, or host it with GitHub Pages (Settings → Pages → Deploy from branch `main`, folder `/root`).

## Test the full journey (no credentials needed)
Use the "Demo account" dropdown at the top.
1. **Aarav (user)** → Discover. Laser Cutter shows ✗ "Laser Safety not on file". Open Profile, submit "Laser Safety".
2. **Admin** → Profile → Verification queue → Verify.
3. **Aarav** → Discover → Laser Cutter → Request booking.
4. **Meera (user)** → request the same slot → goes to the **waiting list** automatically.
5. **Kiran (manager)** → Requests: sorted by fair-use priority, with automatic checks. Approve with a reason (or reject/waitlist; reason is required).
6. **Aarav** → My bookings → Check in (record condition) → Return (choose a worse condition to trigger an auto damage flag).
7. **Kiran** → Resources & incidents → Resolve the incident. Cancel a booking to see waitlist promotion.
8. Any role → "Full history" on a booking, or the **Audit trail** tab.
Also: owners can list new resources (Resources tab), and "Simulate overdue" triggers a delay incident and a notification.

## Features
Listings with rules, location, supervision and deposit · search and category filter · eligibility checks on verified certificates · admin/manager verification · conflict detection and waiting list · fair-use limits (6h/week/resource) and priority by recent usage · approve/reject/waitlist with required reasons · check-in and return condition records · automatic damage flag (human review, no automatic penalties) · incident reporting and resolution · notifications · role-based views (user, owner, manager, admin) · full audit trail.

## Limitations
Browser-only storage (no real backend or login), simulated notifications, no payments, one institution. Future: Supabase/Postgres backend, SSO, email/SMS, photo evidence, AI matching and document review with human sign-off.

## Disclosure
No templates or external libraries. Built with AI assistance (Claude).
