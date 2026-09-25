# SAGARMATHA — RANZANA website

Four static pages for 有限会社サガラマタ:

- `index.html` — Home, restaurant introduction, LINE, and reservation invitation
- `about.html` — supplied representative message, values, and company overview
- `access.html` — both shops, opening hours, phone numbers, descriptions, and map links
- `reservation.html` — a two-shop slideshow with shop-specific booking and delivery links

Open `index.html` in a modern browser, or serve this directory with a local HTTP server. The EN/日本語 switch carries its choice across pages. The reservation slideshow can be switched using the shop buttons, arrow buttons, arrow keys, or a horizontal swipe. All images are in `assets/`; no build step is required.

## Uploading to Manus

Upload the entire `SAGARMATHA` folder, including `vendor/budoux-ja-parser.js`, `script.js`, and `styles.css`. Each HTML page loads the local BudouX Japanese parser before the site script. The site parses rendered Japanese text when the page loads and again after language changes, so phrase-aware wrapping works at desktop and mobile widths without npm, a CDN, or configuration in Manus. The parser is BudouX 0.9.2; its Apache 2.0 license is in `vendor/BUDOUX-LICENSE.txt`.

The Hino shop uses its supplied LINE, Tabelog, Rakuten Gurunavi, Uber Eats, 出前館, and Rocket Now links. The Hachioji shop uses its supplied Uber Eats, 出前館, and Rocket Now links. Hachioji reservations are by phone because no booking-platform URL was supplied for that shop. Hot Pepper is omitted for both shops because no direct URL was supplied.

Shop names, addresses, hours, telephone numbers, and the representative message come from `sagarmatha PROMPT.md` provided by the owner. The Hachioji Rocket Now URL had an accidental leading `E` before `https`; the site uses the valid `https` URL.
