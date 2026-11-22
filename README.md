# AutoClips AI

A browser-based video clipping and captions/SEO helper.

## Deploy to Vercel

1. Extract this ZIP.
2. Upload the **contents of the `autoclips-ai` folder** to the root of your GitHub repository (not the ZIP file itself).
3. In Vercel, set Root Directory to `.` if `index.html` is at the repository root.
4. Redeploy the `main` branch.

The video engine uses FFmpeg.wasm loaded from jsDelivr. The browser needs internet access to download the FFmpeg JavaScript and WebAssembly files on first use. Video processing runs locally in the browser; large videos may require substantial phone memory and processing time.
