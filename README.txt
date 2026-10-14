STUDYSYNC PRO — PWA PACKAGE

This package is based on your supplied `tracker 2.0.html` and uses your supplied logo.

FILES TO UPLOAD TO GITHUB
- index.html
- manifest.json
- sw.js
- icon-192.png
- icon-512.png

IMPORTANT: This is a PWA front-end package, not an Android APK.

PUBLISH / UPDATE ON YOUR EXISTING GITHUB REPOSITORY
1. Extract this ZIP on your Android device.
2. Open your existing GitHub repository: Tracker-2.0.
3. Upload these five files to the repository root.
4. If GitHub asks whether to replace existing files, choose the option to replace/commit the updated files.
5. Commit the changes.
6. Wait for GitHub Pages to redeploy, then reopen your published site in Chrome.
7. If the old version still appears, fully close/reopen Chrome or clear that site's cached data. If needed, change CACHE_NAME in sw.js to a new version before uploading.

INSTALL
- Open the published HTTPS site in Chrome.
- Wait for it to load while online.
- Chrome menu (⋮) > Install app / Add to Home screen.

LIVE TWO-PERSON STUDY ROOM — HONEST LIMITATIONS
The supplied HTML already includes a live-room feature using the public EMQX MQTT broker over secure WebSocket and an external MQTT library CDN. Two people can try entering the SAME room code while both are online and connected. This is not a dedicated private server, and this package does not provision or guarantee an always-available server.
- Live room sync requires internet and the external MQTT broker/CDN to be reachable.
- The offline cache lets the app shell open offline; it does NOT make live sync work offline.
- Room codes/topics are not private authentication. Use a long, hard-to-guess room code and do not share sensitive personal information.
- The displayed peer presence is best-effort; connection/broker restrictions can affect it.
- Data saved in localStorage remains per browser/device; this does not sync the task list itself between devices.

Before relying on the shared room, test with two devices: install/open both online, set different display names, enter the exact same unique room code, tap “Sync / Join Study Room”, and start one timer. Confirm the other device shows the peer. If it does not, the broker/CDN/network may be blocking the connection; a dedicated backend (e.g. authenticated Firebase/Supabase) would be needed for a more dependable private service.
