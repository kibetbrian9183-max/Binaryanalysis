# Primevest frontend (static site)
No build step. Files: index.html, config.js, vercel.json.

1. Deploy the backend first and copy its address.
2. Edit config.js: set window.PV.api to that address.
3. Deploy this folder to Vercel (framework: Other, no build command) or any static host.
   The host must serve index.html for /callback (vercel.json does this on Vercel).
4. Add primevestbinary.com under Vercel > Settings > Domains.
5. In the Deriv dashboard set the Redirect URL to https://primevestbinary.com/callback

Local test: `npx serve -s .` then open http://localhost:3000 (backend CORS must allow that origin).
