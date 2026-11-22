# Wedding guest guide

Static guest information page for Shawn and Wendy, 28 November 2026. Open index.html or serve this directory with a static HTTP server. No build required.

## Requirements

- Replace RSVP with a mobile-friendly guide; no guest data collection or form submissions.
- Keep existing rose/cream styling, couple photos and Guestpix photo sharing.
- Show date, guest programme, venue information, directions and parking.
- No dress code section.
- Use only guest-facing events; omit preparations, vendor tasks, wedding party duties, private addresses and game mechanics.
- Clearly label provisional timings and missing logistics. Do not infer guest arrival from staff setup times.
- All guests use the main link. Tea ceremony timings are shared privately with relatives and are not shown on the page.
- All core programme information works without JavaScript.

## Before sending to guests

Confirm parking/drop-off, dinner reception/seating time, dinner finish time, hotel parking privileges, tea ceremony room and family arrival instructions. Confirm the existing date and Ocean Ballroom, Level 2. The working schedule lists lunch at 12:45 pm; confirm whether guests can eat earlier during wedding party photos (12:15-12:45 pm).

Each celebration combines its programme with the supplied venue address, responsive Google Maps embed and directions link. Church: Zion Presbyterian Church, 535 Upper Changi Rd, Singapore 486975. Dinner: Pan Pacific Singapore, 7 Raffles Blvd, Singapore 039595. Parking details are expandable. The share-generated map embeds require no API key.

The dinner travel section includes a portrait video guide outside the parking accordion. `resources/video/carpark-to-ballroom.mp4` is a 62-second, 720p H.264/AAC web copy (17.3 MB / 16.5 MiB), with fast-start metadata for streaming. Keep the original recording outside the repository. A lazy-loaded 39 KB JPEG provides the preview; JavaScript attaches the MP4 source only after a guest presses Watch. Native controls support playback and fullscreen, and the Open video link also works without JavaScript. The player reserves its portrait dimensions to avoid layout shifts.

The stylesheet and script URLs in `index.html` include a `?v=` version (the first 12 characters of the file's SHA-256 hash). Update the corresponding version whenever either file changes, so returning guests receive the matching assets rather than a cached previous version. The video preview also has an inline responsive width limit to prevent overflow if the stylesheet is unavailable.

The hotel travel link points to its official location information: https://www.panpacific.com/en/hotels-and-resorts/pp-marina/the-hotel.html

## Reminder plan

Send via existing WhatsApp chats: a short personalised message plus the webpage link. Include the date and relevant event start time in the message so guests do not have to open the page for essentials. A screenshot of the relevant programme card can be attached for guests who prefer an image; keep directions clickable in the message. Call relatives who need help arranging transport.

- 28 October 2026 (one month): date, invited events, approximate programme, venues and planning needs. Ask guests to message privately about changed plans, dietary or accessibility needs. Send relatives their relevant tea ceremony slot separately.
- 21 November 2026 (one week): confirmed arrival/seating times, exact venue/map pin, parking and drop-off instructions, family meeting points and a nominated day-of contact if available. Recheck the page before sending.
- Use the same link for both reminders and update it as logistics are confirmed. Send a direct correction if a major time or venue changes after the final reminder.
- Personalise for church-only, dinner-only or both; do not imply every recipient is invited to both.

## Copy-ready message drafts

Replace bracketed fields and include only events the recipient is invited to. These are drafts, not scheduled or sent messages.

### One month / friends

Hi [name]! One month to our wedding on Saturday, 28 November! We can't wait to celebrate with you at [church / dinner / both]. [Church ceremony: 10:30 am, Zion Presbyterian Church.] [Dinner celebration: first march-in at 7:45 pm, Pan Pacific Singapore, Ocean Ballroom, Level 2; arrival time to follow.] The programme and travel updates are here: [link]. If your plans or dietary/access needs have changed, please message us. Love, Shawn & Wendy

### One month / family

Hi [name]! Looking forward to celebrating with you on Saturday, 28 November. Your tea ceremony is planned for [time] at [venue]. We'll share the exact meeting point and arrival time privately. Our wedding programme is here: [link]. Please let us know if you need help arranging transport. Love, Shawn & Wendy

### One week / friends

Hi [name]! See you next Saturday, 28 November! Please arrive at [confirmed arrival time] for [invited event] at [venue and room]. [Ceremony / first march-in] starts at [time]. Directions: [map link]. Parking: [confirmed instructions]. All the details: [link]. If you need help on the day, contact [confirmed contact]. We can't wait to see you! Shawn & Wendy

### One week / family

Hi [name]! Our wedding is next Saturday, 28 November. For your tea ceremony, please meet at [exact meeting point] by [confirmed arrival time]; your ceremony is at [time]. Directions and parking: [confirmed instructions]. Your day's programme: [link]. For help on the day: [confirmed contact]. See you soon! Shawn & Wendy

## Legacy files

email.html and google-apps-script.js are retained as historical RSVP assets. The live index.html and script.js no longer use the RSVP endpoint. Existing external Apps Script deployments or stored responses have not been altered.

## Photo sharing

Guestpix is the selected wedding photo-sharing platform. The page uses the existing resources/qrcode/guestpix.jpeg QR image and supplied Guestpix album URL, with a direct link for guests browsing on their phones. Other trial providers and the Wedibox embed have been removed from the page. The QR and direct link work without JavaScript.
