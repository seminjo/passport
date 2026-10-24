# Pass Port! - Airport Talk

A static HTML/CSS/JavaScript speaking-practice app based on the provided PRD.

## Implemented
- Start / Practice / Result screens
- Settings
- 5 immigration turns
- Korean translation toggle
- SpeechSynthesis (0.9 / 0.7)
- SpeechRecognition (`en-US`)
- Transcript display
- Key-word intelligibility check
- Recast → elicitation → chunking feedback
- No percentage/native-accent scoring
- Completion stars
- Result review + replay
- HTTPS / browser / microphone guidance
- No audio recording or saving

## Gemini
The app works fully without Gemini, as required by the PRD.
`script.js` includes a `getGeminiFeedback()` placeholder returning `null`.
Do not put a Gemini API key directly in client-side JavaScript. If needed later, connect that function to a secure Vercel Function/serverless endpoint. Fallback feedback will still work if Gemini fails.

## Local test
Speech recognition works best in Chrome. Use localhost:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Vercel
No Vite and no build step are required.
Recommended settings:
- Framework Preset: Other
- Build Command: empty
- Output Directory: empty
- Install Command: empty

The deployed URL must use HTTPS for microphone access.
