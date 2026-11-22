# AutoClips AI

A free-first, browser-based video clipping starter that can be deployed as a static site on Vercel.

## Features
- Upload a local video and preview it
- Create multiple MP4 clips at selected durations
- Export 9:16 portrait clips or keep original aspect ratio
- Keyword-based title, description, tags and hashtags generator
- Browser-based Whisper Tiny speech transcription (first model download can be large)
- Timestamp-based highlight suggestions using transcript heuristics
- Caption text formatting and basic SRT export
- Browser-side FFmpeg processing; uploaded video is not sent to an app server

## Deploy to Vercel
1. Upload this folder to a GitHub repository.
2. Import the repository in Vercel.
3. Choose **Other** as the framework preset (static site), with no build command.
4. Set the output directory to `.` and deploy.

You can also deploy the folder with the Vercel CLI: `vercel --prod`.

## Important limitations
- Whisper Tiny speech-to-text runs locally in the browser after a large first-time model download. Highlight suggestions use simple transcript heuristics, not a trained virality predictor or scene understanding. Review all suggested clips before publishing.
- Captions can be downloaded as an SRT file; they are not burned into the exported MP4 in this version. SRT timing is estimated from text length, not aligned word-level timestamps.
- Browser FFmpeg is resource-intensive. Large or long videos may be slow or fail on phones with limited memory. Try a shorter/smaller MP4 if needed.
- The SEO generator is local keyword-based assistance, not a guarantee of rankings or virality.
- FFmpeg core is downloaded from jsDelivr on first use, so internet access is required to initialize the editor.
