## MedWise 0.0.1 (build 1) — test build

First test release of MedWise: medication reminders, medicine pack barcode scanning, interaction and allergy checks, an AI symptom checker, adherence reports and a clinical reference library.

### Downloads

| File | Who it's for |
|---|---|
| `MedWise-0.0.1+1-android.apk` | **Android testers** — download and install this one |
| `MedWise-0.0.1+1-ios-unsigned.ipa` | **iPhone testers** — must be sideloaded (see below) |
| `MedWise-0.0.1+1-android-playstore.aab` | Google Play upload only — cannot be installed on a phone |

### Installing on Android

1. Download `MedWise-0.0.1+1-android.apk` on your phone.
2. Open it. If asked, allow your browser or file manager to **install unknown apps**.
3. Tap **Install**.

### Installing on iPhone

This build is not signed by Apple, so it can't be installed by tapping it. Sign it with your own Apple ID using a free sideloading tool:

1. On a Mac or Windows PC, install **[Sideloadly](https://sideloadly.io)** (or **[AltStore](https://altstore.io)**).
2. Connect your iPhone with a cable and download `MedWise-0.0.1+1-ios-unsigned.ipa`.
3. Drag the `.ipa` into Sideloadly, enter your Apple ID, and click **Start**.
4. On the iPhone, go to **Settings → General → VPN & Device Management**, tap your Apple ID, and choose **Trust**.
5. On iOS 16 or later, turn on **Settings → Privacy & Security → Developer Mode** and restart when asked.

With a free Apple ID the app **stops opening after 7 days**. Sideload it again to renew it.

### Known limitations of this test build

- **Google Sign-In may not work on iPhone** when sideloaded, because the app gets a different bundle ID. Use email sign-in instead.
- **Notifications on iPhone** may be limited in sideloaded builds.

### Reporting problems

Please open an issue with your phone model, OS version, and steps to reproduce.

> MedWise is for information only and is not a substitute for professional medical advice.
