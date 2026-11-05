# Nitesh AI Studio

A mobile-friendly image + reference-video motion transfer website using Runway Act-Two.

## What it does
- Upload one character image and one reference performance video.
- Upload both assets privately to Runway using ephemeral asset uploads.
- Submit a `character_performance` task using Act-Two with body control enabled.
- Poll task status and show the generated video when complete.
- Keep the API key on the server, never in browser JavaScript.

## Deploy on Render
1. Upload this project to a GitHub repository (do not upload any `.env` file or API key).
2. In Render, choose **New → Web Service**, connect the repository.
3. Runtime: Node. Build command: `npm install`. Start command: `npm start`.
4. Add the private environment variable `RUNWAYML_API_SECRET` with your Runway API key in Render's Environment tab.
5. Deploy. The public `onrender.com` URL is your website.

## Notes
- Runway API use requires an active API account and purchased API credits. Charges depend on Runway's current pricing and the generated task.
- Act-Two expects a recognizable character face and a reference performance video. Check Runway's current media requirements and limits before uploading.
- The ratio control maps to Act-Two's supported ratios. The output resolution is determined by Runway; the 1080p/4K selector in the starter interface is not a guarantee of output resolution.
- This is a starter deployment, not a hardened public SaaS product. Before opening it to the public, add user authentication, quotas, rate limits, persistent task storage, file retention controls, and privacy/consent notices.
