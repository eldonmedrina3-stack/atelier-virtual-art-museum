ATELIER — Virtual Art Museum (PWA)

FILES
- index.html: the museum website and artist submission form
- manifest.webmanifest: installable app information
- sw.js: service worker for app-shell offline caching
- icons/: app icons

RUN LOCALLY
A PWA's install and offline features require HTTPS or localhost; opening index.html directly as file:// is not enough.
Quick local server (if Python is installed):
  1. Open the project folder.
  2. In the folder address bar type cmd and press Enter.
  3. Run: py -m http.server 8000
  4. Open http://localhost:8000 in Chrome or Edge.

PUBLISH FOR INSTALLATION ON LAPTOP AND PHONE
1. Create a GitHub account and a new public repository named atelier-art-museum.
2. Upload index.html, manifest.webmanifest, sw.js, and the icons folder, preserving the folder structure.
3. In repository Settings > Pages, select Deploy from a branch, choose main and /(root), then Save.
4. Wait for GitHub Pages to publish. Open the HTTPS website URL in Chrome/Edge on laptop or Chrome on Android.
5. Use the Install button or browser menu > Install app / Add to Home screen.
   On iPhone, open the HTTPS site in Safari, tap Share, then Add to Home Screen.

ARTIST SUBMISSIONS — IMPORTANT
This starter edition stores artworks in IndexedDB in the current browser/device. Uploaded images and artwork details remain on that device/browser. They are not automatically visible to other visitors or synced to another phone/computer.
Export backup downloads a JSON backup; Import backup restores it in another browser/device. For a real public exhibition where all artists can upload and every visitor sees the same works, connect a hosted backend/database and add authentication, moderation, storage rules, and abuse protection. Do not collect sensitive information in this local demo.

OFFLINE
The service worker caches the app shell after the first visit. External sample images are hosted by Unsplash and may require internet; uploaded artwork stored in this browser remains available locally.
