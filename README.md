# TikTok Caption Downloader — Vercel prototype

## Deploy
1. Create a GitHub repository and upload this folder's contents.
2. Import the repository into Vercel.
3. Framework preset: Next.js. Build command: `npm run build`.
4. Deploy.

## Important
This is a browser-side prototype. It tries TikWM's public resolver directly from the browser and then fetches media directly. If the resolver/media host does not allow browser CORS, it will fail. It does not use Vercel serverless functions for video transfers, so it avoids Vercel function-duration limits, but browser memory and CORS still limit scale. It is not a guaranteed unlimited service.

For production-scale long-running jobs, use a separate queue/worker and object storage (for example, a VPS or container worker plus S3-compatible storage). Vercel should host the frontend/control panel only.

Caption source is whatever the resolver returns; verify it against the original TikTok post. The browser version currently does not embed cover artwork and cannot guarantee watermark removal.
