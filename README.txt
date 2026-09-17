GAME NIGHT TRACKER — INSTALLABLE WEB APP
==========================================

This folder is a Progressive Web App (PWA). On Android, Chrome can
install it to your home screen so it opens full-screen like a real
app, with an icon, no browser bar, and offline support.

IMPORTANT: For the install prompt and offline caching to work
properly, these files need to be served over HTTPS — opening
index.html directly by double-clicking it (file://) will still run
the tracker fine, but Chrome won't treat it as an installable app.

FASTEST WAY TO HOST IT (free, ~2 minutes): GitHub Pages
--------------------------------------------------------
1. Create a free GitHub account if you don't have one.
2. Create a new repository (e.g. "game-night-tracker").
3. Upload all 5 files in this folder to the repo:
     index.html
     manifest.json
     service-worker.js
     icon-192.png
     icon-512.png
4. Go to the repo's Settings -> Pages.
5. Under "Branch", choose "main" and folder "/ (root)", then Save.
6. GitHub gives you a URL like:
     https://YOUR-USERNAME.github.io/game-night-tracker/
   Open that on your Android phone in Chrome.

OTHER FREE OPTIONS
-------------------
- Netlify Drop: netlify.com/drop — drag this folder in, get an
  instant HTTPS URL, no account required for a quick test.
- Vercel, Cloudflare Pages, or any static host works the same way.

INSTALLING ON ANDROID
-----------------------
1. Open the hosted URL in Chrome on your phone.
2. Tap the three-dot menu -> "Add to Home screen" (or Chrome may
   show an "Install app" banner automatically).
3. Confirm. You'll get a home-screen icon that opens the tracker
   full-screen, like a native app.

DATA STORAGE
-------------
Once installed this way, the tracker saves your wins, drink counts,
and zest notes using your browser's local storage on that phone —
it stays put across sessions, but it's tied to that browser/device,
not synced anywhere else.

WANT AN ACTUAL COMPILED .APK INSTEAD?
---------------------------------------
That requires the Android SDK and Gradle build tools, which aren't
available in the environment used to generate this. If you want to
go that route, ask and a full Android Studio project (a thin WebView
wrapper around this same tracker) can be put together for you to
open in Android Studio and build/install yourself.
