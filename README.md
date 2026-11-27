# GAPB Android Messenger Project
**Made by Gaurav Raj**

## Features Included
- **Online & Offline Chatting**:
  - Online via Firebase Realtime Database + Firebase Cloud Messaging (`GapbMessagingService.kt`)
  - Offline P2P Mesh via Google Nearby Connections API (`NearbyChatManager.kt` — Bluetooth & Wi-Fi Direct)
- **End-to-End Encryption (E2EE)**: `E2EEncryptionManager.kt` using ECDH (`secp256r1`) + `AES/GCM/NoPadding`.
- **Chat Lock & Unlock**: `ChatLockManager.kt` with BiometricPrompt + encrypted 4-digit PIN (default `1234`, changeable in Settings).
- **Animated Phone Login / Sign-up**: `LoginScreen.kt` with pulsing logo and smooth OTP reveal.
- **File Sharing**: `ChatDetailScreen.kt` file picker + `NearbyChatManager.sendOfflineFile`.
- **Online/Offline Notifications + Vibration**: `NotificationHelper.kt` with high-priority notification channel and custom vibration waveform.
- **Share App (.apk) with Friends**: `ShareAppHelper.kt` using `FileProvider` to share the installed APK directly.
- **Developer Credit**: `Made by Gaurav Raj` displayed in `SettingsScreen.kt`.

## How to Build the `.apk` for Your Vivo Phone
1. Extract `GAPB_Android_Project.zip` on your computer.
2. Open **Android Studio** -> **Open** -> select the `GAPB_Android_Project` folder.
3. Let Gradle sync finish.
4. *(Optional for live cloud sync)*: Create a Firebase project, download `google-services.json` into `app/`, and uncomment `id("com.google.gms.google-services")` in `app/build.gradle.kts`.
5. Click **Build -> Build Bundle(s) / APK(s) -> Build APK(s)**.
6. Copy `app/build/outputs/apk/debug/app-debug.apk` to your Vivo Android phone and install it!
