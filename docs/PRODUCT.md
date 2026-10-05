# find_engineers — Product Spec (v0.1)

_Status: decided for launch, revisit after the first 2 months of real usage._

## 1. One-line pitch

**Find a verified, certified electrician or electrical engineer in Accra — for a repair today or a building project next month.**

Longer term: the trusted place in Ghana to assemble the professionals you need to build, fix, or maintain a building (architects, civil/structural, electrical, plumbing, and more).

## 2. Why this, and why not just "another artisan app"

Generic "book a handyman" platforms already exist in Ghana:

- **GHartisans** — run by the Youth Employment Agency, location-based booking for carpentry, plumbing, electrical, with in-app payment. ([ghartisans.yea.gov.gh](https://ghartisans.yea.gov.gh))
- **JACK-SP** — Accra app (2019) covering dozens of trades, with photo ID cards for providers. ([Citi Newsroom](https://citinewsroom.com/?p=483416))
- **Fixam** and others on the app stores.

Competing head-on with a free government app across every trade is a losing fight. Our edge is **professional credentials and engineering work**:

1. **Verification that actually means something.** Electrical wiring in Ghana legally requires Energy Commission certification under the Electrical Wiring Regulations 2011 (L.I. 2008), and over 14,000 electricians and inspectors have been certified. ([GNA](https://gna.org.gh/2023/04/energy-commission-certifies-14000-electricians-inspectors-nationwide/)) Engineers register with the Engineering Council under Act 819. ([GhaLII](https://ghalii.org/akn/gh/act/2011/819)) We show these credentials as badges, checked by us.
2. **Engineers, not just artisans.** Design work (load calculations, wiring diagrams, solar sizing, inspections for the Energy Commission's periodic inspection requirement) is underserved by handyman apps.
3. **Founder expertise.** The founder is an electrical engineer — can judge quality, write the right job categories, and recruit the first professionals personally.

## 3. Launch scope (Phase 1)

| Decision | Choice | Reason |
|---|---|---|
| Trades | **Electrical only** (electricians + electrical engineers) | Founder's field; the clearest legal credential to verify; one trade done well beats ten done badly |
| Location | **Greater Accra** | Founder is there; density makes "nearby today" possible |
| Job types | **Both** repairs ("Fix") and projects ("Build") | Same professionals serve both; repairs bring frequent traffic, projects bring value |
| Customer price | **Free** | Remove every barrier to the first requests |
| Professional price | **Free at launch** | A marketplace with no customers can't charge pros; charge once we deliver them work |
| Payments | **Not through the platform yet** — customer pays the pro directly | Escrow means disputes, refunds, and payment regulation; prove demand first |
| Platform | **Mobile-first website** (installable as a PWA) | Works on every phone, no app-store approval; native apps come later |
| Sign-in | **Phone number + SMS code** | Phone-first market; email is optional |

## 4. Who uses it

**Customer — "Fix" (urgent repair).** Homeowner, tenant, shop owner. "Half my house has no light." Wants someone nearby, trustworthy, today.

**Customer — "Build" (planned project).** Someone building or renovating: full wiring of a new house, rewiring, solar/inverter install, generator changeover, a wiring inspection. Wants 2–3 quotes from qualified people and to compare them.

**Professional.** Certified electrician (domestic/commercial) or registered electrical engineer. Wants a steady flow of real jobs and a profile that proves they're legit.

**Admin (founder at launch).** Verifies credentials, removes bad actors, watches quality.

## 5. Core features (MVP)

### Customer
- **Describe the problem by picking, not typing**: categories such as no power / partial outage, breaker keeps tripping, sparking or burning smell, sockets & switches, lighting, prepaid meter issues, new wiring, rewiring, solar & inverter, generator & changeover, inspection/certificate, appliance installation (AC, water heater). Optional photo + short note.
- **Location**: neighbourhood picker (e.g. East Legon, Madina, Tema Comm. 25) and optional GhanaPost GPS address.
- **Urgency**: Emergency (now) / This week / Planning.
- **Fix flow**: see matching verified pros near you (badges, rating, jobs done, "available now") → send request → pro accepts → phone/WhatsApp contact unlocked for both.
- **Build flow**: post a project brief → up to 3 pros respond with a quote → compare → choose.
- **Safety tips** while waiting for emergency jobs (e.g. switch off the main breaker) — written by the founder.
- **Review** after the job: only possible if a real request exists between that customer and pro.

### Professional
- Profile: photo, trade level (electrician / electrical engineer), categories offered, areas served, photos of past work, years of experience.
- Upload credentials: Ghana Card, Energy Commission certificate number, Engineering Council registration (engineers).
- **Available now** toggle for emergency jobs.
- Request inbox: accept / decline; respond to project briefs with a quote.
- Notifications via SMS (WhatsApp later).

### Admin
- Verification queue: check credentials (Energy Commission's public database / "Certified Electrician" app; Engineering Council), approve or reject, award badges.
- Suspend accounts, see reported issues, basic stats.

### Badges
- **ID verified** — Ghana Card checked.
- **EC Certified** — Energy Commission wiring certificate checked.
- **Registered Engineer** — Engineering Council registration checked.
- Unverified pros **cannot** receive requests. Quality over quantity.

## 6. Matching rule (v1, simple on purpose)

For a request: pros who are **verified** + offer that **category** + serve that **area**; for emergencies also **available now**. Sort by: available now → rating → response speed → jobs completed. No clever algorithm until we have data.

## 7. Money (how this becomes a business)

- **Phase 1 (launch):** free for everyone. Goal is proof that people use it.
- **Phase 2:** optional **protected payment** via mobile money (Paystack supports MoMo and split payments to sub-accounts): customer pays in, money released to the pro when the job is confirmed done (or per milestone for projects). We keep a **commission (~10%)** on these jobs. Customers get a reason to pay through us (protection); pros get a reason to accept it (guaranteed payment, more jobs).
- **Later options:** featured placement for pros, paid inspection/certificate bookings, B2B accounts for estate developers and property managers.

## 8. Success measures for the first 2 months

- 30+ verified professionals across at least 10 Accra neighbourhoods.
- 100+ job requests.
- 70%+ of emergency requests accepted within 1 hour.
- Average rating ≥ 4.3 and repeat customers appearing.

If requests come but aren't accepted → recruit more pros. If pros join but no requests → focus on customer marketing. The numbers tell us which.

## 9. Roadmap

1. **Phase 1 — Electrical, Accra.** Everything above.
2. **Phase 2 — Payments & quotes.** Protected MoMo payments, commission, milestone payments for projects, WhatsApp notifications.
3. **Phase 3 — More disciplines + "Build a house" planner.** Add architects, civil/structural engineers, plumbers, quantity surveyors. A guided planner: "I want to build a 3-bedroom house" → shows which professionals are needed at each stage (drawings → structure → wiring & plumbing design → construction → inspection) and lets the customer hire each in turn.
4. **Phase 4 — Apps & expansion.** Android and iOS apps (or the PWA in the stores), Kumasi and Takoradi.

## 10. Risks and how we handle them

| Risk | Mitigation |
|---|---|
| Customers and pros meet once, then skip the platform | Accept it in Phase 1; Phase 2 payment protection and reviews give a reason to stay |
| Bad or fake professionals | Manual verification, request-linked reviews only, quick suspension |
| Not enough pros early | Founder recruits personally (school/industry network, certified electrician associations) |
| Free government app competes | Stay focused on credentials and engineering work they don't emphasise |
| Founder time | Keep Phase 1 small; Django's built-in admin covers the admin tools |

## 11. Technical direction (for the build)

- **Backend:** Python + **Django** (admin panel free out of the box, mature auth, ORM).
- **Database:** PostgreSQL (SQLite while developing).
- **Frontend:** Django templates + HTMX + Tailwind CSS — mobile-first, no separate JavaScript app needed yet.
- **SMS/OTP:** a Ghanaian-friendly SMS provider (e.g. Hubtel, Arkesel, or mNotify) — choose at build time.
- **Payments (Phase 2):** Paystack (MoMo + card).
- **Hosting:** a simple PaaS (Render, Railway, or similar) to start.

## 12. Open questions (not blocking Phase 1)

- Product name and brand (find_engineers is the working name).
- Exact commission rate and when to switch it on.
- Whether to separate "electrician" and "electrical engineer" into different search paths or one list with filters.
