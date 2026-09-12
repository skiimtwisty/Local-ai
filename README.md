# Pocket Companion (phone-first local AI PWA)

A static progressive web app that runs a small language model locally in Safari using WebLLM/WebGPU. No paid model API or message counter is required after the model is downloaded.

## What it has
- Local browser LLM (default: Llama 3.2 1B q4)
- Persistent conversation history and pinned memory
- Editable companion name/personality
- 18+ adult-character mode (consenting fictional adults only)
- iPhone speech synthesis for spoken replies
- Push-to-talk using Safari SpeechRecognition when available
- Optional avatar image stored locally in browser storage
- Installable PWA / Add to Home Screen

## Fastest way to put it on an iPhone
The app needs to be served over HTTPS for WebGPU/PWA/microphone behavior to be reliable. Any static host works.

### GitHub Pages
1. Create a new GitHub repository.
2. Upload the contents of this folder to the repository root.
3. In the repository, open **Settings > Pages**.
4. Choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. Open the Pages address in Safari on the iPhone.
6. Tap **Share > Add to Home Screen**.
7. Open the installed app, tap the gear, then **Download / load local model**.

The first model download is large. Use Wi-Fi and keep Safari open during the initial load.

## Notes
- The default 1B model is intentionally small enough to have a chance on phones. Its intelligence/roleplay quality will be below large cloud models such as Grok.
- If the default model fails from memory pressure, select the Qwen 0.5B fallback.
- Apple's built-in speech voices are used for TTS, so spoken replies do not consume API minutes.
- Speech recognition may require Siri/Dictation and microphone permission.
- A future version can point at a custom MLC/WebLLM-compatible roleplay model if a phone-sized one proves stable on the target iPhone.

## Privacy
Chat history, settings, and avatar stay in the browser's local storage. Model inference is local after model assets have been fetched/cached. Initial model/library downloads come from external CDNs/model hosting.
