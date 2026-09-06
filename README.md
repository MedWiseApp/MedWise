# MedWise

**MedWise** is a mobile health companion that helps people understand their symptoms, manage their medications, scan drug packaging, and reference trusted clinical guidelines — all from one app.

It is a mobile app with an AI-powered backend to turn three everyday frictions — *"what could this be?"*, *"did I take my medication?"*, and *"what am I actually holding in my hand?"* — into a few taps.

---

## Demo

<p align="center">
  <video src="docs/media/MedWiseAppDemo.mp4" width="360" controls muted playsinline>
    Your browser does not support inline video — <a href="docs/media/MedWiseAppDemo.mp4">download the demo</a>.
  </video>
</p>

📽️ **[Watch the app demo](docs/media/MedWiseAppDemo.mp4)** — a full walkthrough of the AI diagnosis flow, medication reminders, pack scanner, and clinical library.

---

## What MedWise does

MedWise is organized around five sections, reachable from the bottom navigation bar:

### 🏠 Home
A daily dashboard: an adherence ring showing how consistently the user is taking their medications, a current streak, a week-at-a-glance bar chart, today's upcoming doses, and a recent-activity feed — so the state of a user's health routine is visible at a glance.

### 🩺 Diagnosis (AI)
The core AI feature. The user describes their symptoms and body area; MedWise first **suggests related symptoms** a clinician would probe (as tappable chips) to refine the input, then returns a **ranked, probability-scored list of possible conditions**, each with:
- an ICD-10 code and confidence tag (e.g. *High / Moderate / Low*),
- suggested first-line treatment and recommended tests,
- red-flag warnings to watch for.

Results can arrive as a single response or **stream in card-by-card** for a faster perceived response. A pre-LLM safety gate screens for emergencies (chest pain, stroke signs, anaphylaxis, suicidal ideation, etc.) — if triggered, the request short-circuits straight to an emergency banner instead of a diagnosis. Every result carries a medical disclaimer, and a visible quota meter shows how many AI queries remain on the user's plan. Past sessions are saved and can be revisited, with follow-up questions supported for upgraded users.

### 📦 Pack Scanner
Point the camera at a medicine box's barcode or 2D data matrix to instantly read its **batch number and expiry date** — fully offline, since that data is encoded directly in the barcode. The product's identity (name, manufacturer, dosing) is then resolved from a lookup service and filled in once available. Results are clearly labeled by source: an official registry match shows verified dosing information, while a web-search fallback is presented as an unconfirmed claim — MedWise never blurs the line between the two.

### 💊 Medicine & Reminders
Add medications with custom dosing schedules and get local notifications when it's time to take them, including a full-screen ringing alarm mode with snooze. The screen tracks an adherence streak, a visual calendar, and an exportable report — and surfaces the next several upcoming doses without silently truncating a busy schedule.

### 📚 Library
A searchable reference library of clinical decision rules, emergency protocols, dosing calculators, and general health guidelines, organized by category with bookmarking for quick access to frequently used documents.

### Account & Personalization
Email/password and Google sign-in, phone OTP, biometric unlock, and a guided onboarding flow. The app is fully localized into **8 languages** (English, Spanish, French, Arabic, Turkish, Dutch, Portuguese, Russian) and supports free and premium subscription tiers with in-app purchases that raise the AI-diagnosis quota.

---

## How it's built

MedWise is split across two repositories (private, closed-source):

- **Mobile app** — iOS & Android, using Cloud services, on-device barcode/data-matrix scanning, local notifications for reminders, and in-app purchases for subscriptions.


This repository hosts only the public-facing description and demo media for MedWise — the application and backend source code are maintained in private repositories.

---

## License

This repository is licensed under the [MIT License](LICENSE).
