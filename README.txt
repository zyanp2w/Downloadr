MEDIAFLOW PWA package

Upload these files to the ROOT of the existing Vercel frontend project:
- index.html (replace the current frontend index.html)
- manifest.json
- service-worker.js
- icons/ (folder)

Keep the existing frontend project configuration and backend deployment unchanged.
After redeploying, test:
1. https://YOUR-DOMAIN/manifest.json
2. https://YOUR-DOMAIN/service-worker.js
3. Open the site in Chrome on Android > menu (three dots) > Install app / Add to Home screen.

Important:
- This creates an installable PWA, not yet a standalone APK file.
- Once the PWA works, package it as an Android APK using a Trusted Web Activity workflow.
- The service worker deliberately does not cache /api/* responses or download requests.
