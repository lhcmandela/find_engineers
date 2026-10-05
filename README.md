# find_engineers

Find a verified, certified electrician or electrical engineer in Accra — for a repair today or a building project next month.

Starting with electrical work in Greater Accra, expanding later to architects, civil/structural engineers, plumbers and other building professionals.

See [docs/PRODUCT.md](docs/PRODUCT.md) for the full product spec: scope, features, business model and roadmap.

## Clickable demo

`index.html` is a working phone demo of the Phase 1 product. **Every person, rating and price in it is sample data**, and nothing leaves the phone.

What you can try:

| As a customer | As a professional (More → Switch to professional view) | As admin (More → Verification queue) |
|---|---|---|
| Pick a fault, see verified electricians nearby (sorted: available → rating → reply speed), send a request, watch it get accepted, mark it done, leave a review | Turn "Available now" on/off, accept an urgent job, send a quote on a project with the keypad | Tick each document as checked, approve or reject; approved people appear in search straight away |
| Post a project (e.g. new building wiring), receive three quotes, compare them, choose one | | Someone with no Energy Commission certificate can't be approved |

More → Colour lets you try four brand colours across the whole app.

**Run it:** open `index.html` in a browser (phone-sized window is best). It is a single file — React and Babel load from cdnjs, like Cashbook. On GitHub Pages it also installs to the home screen and opens offline.

The real app will be built in Python/Django (see the spec, section 11); this demo is the screen-by-screen target for it.
