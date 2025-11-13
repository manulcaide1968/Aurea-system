Aurea SYSTEM - PWA package

Files included:
- index.html           -> main app (user's UI)
- main-obf.js          -> obfuscated core JS (base64-encoded)
- service-worker.js    -> basic offline cache + install
- manifest.json        -> PWA manifest (app name, icons)
- icon-512.png / icon-192.png -> app icons

How to publish:
1. Upload the entire folder to a static host (Netlify, Vercel, GitHub Pages).
2. Open the URL from a mobile browser. On Android/Chrome, choose 'Add to Home screen'.
   On iOS/Safari, use 'Share -> Add to Home Screen' (note: service worker support is limited on iOS).
3. The app will run offline for cached resources.

Protection notes (important):
- The JS code is obfuscated (base64 + eval). This raises the difficulty of casual copying but does NOT fully prevent reverse-engineering.
- For strong protection, move core algorithm to a server (backend) and keep only a minimal frontend that calls your API.
- Consider licensing, NDA, and legal protection if you plan to commercialize the system.
