# ClipForge AI — video repurposing prototype

## What this version does
- Lets visitors upload a local video or paste a link.
- Embeds supported YouTube URLs in the page so the source video can be watched without downloading it first.
- Plays direct MP4/WebM links when the source host permits browser playback.
- Creates local draft cuts from a local/directly playable source, with editable caption text and suggested editable titles.
- Provides platform aspect-ratio presets and browser text-to-speech.

## Publish on GitHub Pages
1. Extract this folder.
2. Upload/replace `index.html`, `style.css`, `app.js`, and `README.md` in the root of your repository.
3. Commit the changes to `main`.
4. Keep GitHub Pages set to **Deploy from a branch → main → /(root)**.

## Important: what is not AI-powered yet
YouTube embeds are preview-only in this static version. A YouTube page URL does not expose the source media file to the browser's video editor. The browser also cannot reliably fetch and process arbitrary TikTok/Instagram/social-media URLs due to host restrictions and cross-origin controls.

This version does **not** yet automatically download/import social videos, analyze the whole video to find the best moments, transcribe audio, create word-timed captions, or use a language model to write genuinely context-aware titles/captions. The title suggestions are simple local templates based on the topic/transcript text, not AI output. The existing clip generator uses evenly spaced draft cuts, so do not describe those cuts as AI-selected highlights.

To deliver the full requested product, ClipForge needs a backend that can securely ingest supported source media, extract audio/video, run speech-to-text, analyze segments for hook/story/payoff, generate titles/captions with an AI model, render subtitle overlays, and return downloadable clips. This requires an API key and a server or hosted video-processing service; never put a private API key in `app.js` or any public GitHub repository. GitHub Pages alone cannot run that backend.

## Privacy
Local uploaded videos are processed in the browser by the prototype. Embedded YouTube previews are loaded from YouTube's privacy-enhanced embed domain. No AI service is called by this version.
