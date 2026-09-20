# Rion Assistant Android v1.2

Rion Assistant is an Android assistant prototype for chat, voice commands, and video-edit planning.

## Architecture
Android app -> your HTTPS backend -> AI provider.

**Never put an AI API key inside the Android APK.** Keep secrets in the backend environment.

## Included
- AI chat UI with backend-ready service
- Voice input (Nepali)
- Video picker
- Natural-language video edit planner
- Shorts/Reels edit presets
- Backend example (Node.js/Express) with environment-based API key
- Mock mode so the app can be tested without an API key

## Build
Open the `android` folder in Android Studio and run the app.

For the backend:
1. `cd backend`
2. `npm install`
3. Copy `.env.example` to `.env`
4. Put your provider API key in `.env`
5. `npm start`

Then set the Android backend URL in `ApiConfig.kt`.

This project is a safe starter scaffold: the video editor currently creates an edit plan; native Media3/FFmpeg processing can be connected next.


## 📱 Build APK using only your phone

This version includes a GitHub Actions workflow, so you do not need Android Studio or a PC.

1. Create/sign in to a GitHub account on your phone.
2. Create a new repository (for example `psk-ai`).
3. Upload the **contents** of this ZIP to the repository (the `.github` folder must also be uploaded).
4. Open the repository's **Actions** tab.
5. Open **Build Rion Assistant APK** and tap **Run workflow** (or push to `main` to trigger it).
6. When the workflow finishes, open the completed run and download the artifact named **PSK-AI-debug-apk**.
7. Extract the artifact ZIP. Inside is `app-debug.apk`.
8. Tap the APK and install it.

For a real release, use an HTTPS backend URL and proper app signing. Do not put private AI API keys in the APK.
