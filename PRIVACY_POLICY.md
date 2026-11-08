# SoFarYetSoClose Privacy Policy

**Effective Date:** May 17, 2026
_Last updated: November 9, 2026_
**Version:** 1.4.0

SoFarYetSoClose ("we," "our," or "us") is an Android app. SoFarYetSoClose is a partner nudge app for Android that uses Firebase to support accounts, pairing, voice notes, and push notifications. This Privacy Policy explains what information the app collects, how it is used, and the choices you have. By installing or using SoFarYetSoClose you agree to the practices described below.

## Information We Collect

### Location Data
- SoFarYetSoClose does not collect location data.

### Account Information
- Signing in with Google is the only way into the app. There is nothing to fill in, and the app asks for no profile details of its own. Google supplies your email address and account identity to Firebase Authentication.
- Your account record in Firebase holds your Firebase user ID, partner ID, invite code, pairing time, and FCM push token.
- It also holds **your sleep window — the start and end times you set, and whether it is switched on — and your time zone offset from UTC in minutes.** Both exist for one feature: holding your partner's nudge until you are awake. The offset narrows down roughly where in the world you are, to the width of a time zone. Neither is used for anything else, shared with anyone else, or used to locate you more precisely.
- Nudge content (text nudges, emojis, and voice notes you record in the app), offline queue data, and app preferences may be associated with your account. A phrase you write yourself in the app is stored on your device and travels to Firebase as the text of any nudge you send with it.

### Device Information
- Device push token, notification preferences, offline queue state, and local app preferences may be stored locally or in Firebase.

## How We Use Your Information

### Location Sharing
- SoFarYetSoClose does not use your location.

### Account Management
- Create and manage accounts and partner pairings.
- Send nudges, emojis, voice notes, and push notifications between paired partners.
- Sync data and offline queue state across Firebase-backed services.

### Service Improvement
- Improve reliability, notification delivery, and sync behavior.
- We do not sell your relationship content or account data.

## Storage and Retention

### Data Storage
- Account, pairing, nudge, voice note audio, and push token data may be stored in Firebase services such as Firebase Authentication, Firestore, Storage, Cloud Functions, and Cloud Messaging.
- Offline queue and preferences may be stored locally using Room/DataStore.

### Data Retention
- Account and paired content are retained while your account is active. **The app has no button to delete a single nudge or voice note**, so deleting your account is the only way to remove your history through the app.
- **Voice notes have one retention control you set yourself**, under Settings: never, after 7 days, after 30 days, or once your partner has listened. **The default is never.** If you choose one of the others, a background job removes those audio files from Firebase Storage on that schedule.
- Local offline data remains until synced, deleted, app data is cleared, or the app is uninstalled.
- Firebase Analytics data is aggregated and kept 14 months; Firebase Crashlytics reports are kept 90 days. Both are Firebase defaults.

### Data Security
- On your device, your settings and your offline nudge queue sit in the app's private storage, protected by Android's application sandbox. The app does not add encryption of its own on top of that.
- In transit, every Google service named in this policy is reached over HTTPS/TLS.
- In Firebase, your data is encrypted at rest by Google, and Google's handling of what it receives is governed by Google's terms rather than ours.
- No Sudarshan Tech Labs server exists, so there is no third place holding your data: it is on your device, and it is in Google's Firebase.
- You should protect your device and your Google account with strong authentication, since your Google account is how you sign in.

## Data Sharing

### Family Groups
- SoFarYetSoClose does not use family groups unless explicitly described in this policy.
- If this app includes pairing, sharing, or collaboration features, data is shared only with the people or services required for the feature you choose.
- You control feature use through the app settings, permissions, account controls, or platform settings.

### Third Parties
- Firebase/Google provides authentication, database, storage, cloud functions, and messaging services.
- **Firebase Crashlytics (Google)**: If the app crashes, a crash report is sent to Firebase Crashlytics. It can include the error details, device model, Android version, app version, and an installation identifier. No nudge text or relationship content is included. We use it only to find and fix bugs.
- **Firebase Analytics (Google)**: Aggregated usage events (which screens are opened and which features are used) together with device model, Android version, and app version. No nudge or message content is sent. We use it only to see which features are worth keeping.
- Google's handling of both is covered by the [Firebase Privacy Policy](https://firebase.google.com/support/privacy).
- Nudges and shared content are visible to your paired partner according to the app feature you use.
- **The text of a nudge travels in the push notification that tells your partner about it.** That means it passes through Firebase Cloud Messaging and can appear on your partner's lock screen.
- Two Firebase Cloud Functions run on Google's infrastructure when you send a nudge. They read the nudge to build that notification, check your partner's sleep window, and hold the notification until your partner is awake if needed. Their diagnostic logs record the nudge's ID, the two account IDs and the sleep window — not the nudge text, and not the audio.
- If you tap Share on a nudge or Share the app, the app sends plain text only (the nudge text or an app store link) to the Android share sheet, and the app you pick receives that text. The app does not share images, videos, or audio files this way.
- Copying a nudge or a phrase puts that text on your device's clipboard, where any app you paste into receives it.
- No relationship content is sold to advertisers or data brokers.

We do **not** share your data with:
- Data brokers
- Unrelated advertising networks, unless advertising is explicitly listed above for this app
- Third parties unrelated to the app features described in this policy

## Permissions Used

### Required Permissions

* **INTERNET**: Required for Firebase sync, voice notes, and messaging.
* **RECORD_AUDIO**: Used only to record voice notes you choose to send.
* **POST_NOTIFICATIONS, VIBRATE, FOREGROUND_SERVICE, FOREGROUND_SERVICE_REMOTE_MESSAGING**: Used for push notifications and background messaging.
* **SYSTEM_ALERT_WINDOW**: Used only for full-screen/overlay notification experiences when enabled. You grant it separately in Android settings, and the app works without it.

### Permissions added by Android libraries

The app declares the seven above. The finished build carries five more, declared by the libraries it is built on rather than by the app's own code. They appear in the permission list you see on the Play Store, so they are listed here for completeness:

* **ACCESS_ADSERVICES_AD_ID, ACCESS_ADSERVICES_ATTRIBUTION** and **com.google.android.gms.permission.AD_ID**: Android's Privacy Sandbox advertising APIs, declared by the Firebase Analytics library. **SoFarYetSoClose shows no advertising and contains no advertising SDK.** Those names appearing in a couples app's permission list would reasonably alarm anyone reading it, so to be explicit: they arrive with Analytics and are not used to show you ads.
* **ACCESS_NETWORK_STATE**: Declared by Firebase. Lets a library check whether a network exists before attempting to send; it grants no ability to use one.
* **WAKE_LOCK** and **RECEIVE_BOOT_COMPLETED**: Declared by Firebase Cloud Messaging and WorkManager. They are how Android delivers a push while the phone is idle, and re-registers scheduled work after a restart.

Verified against the merged manifest of the release build rather than the app's own manifest file.

### Optional Permissions

* Audio recording, overlay notification experiences, and notifications are controlled by you through app or Android settings.

## Your Rights and Controls

### Location Sharing Control
- No location sharing exists in SoFarYetSoClose.

### Account Management
- You can sign out, unpair from your partner, choose a voice-note auto-delete setting, or delete your account.
- Unpairing clears the pairing on both sides. **It does not delete the nudges either of you already received.**
- **There is no per-nudge delete in the app.** Deleting your account is the only way to remove your nudges and voice notes through the app; for anything narrower, email us.

### Data Access
- You can view your account, pairing, and nudge data in the app, and request access or deletion by email.

### GDPR Rights (EU Users)
If you are in the European Union, you have additional rights:
- **Right to Access**: Request a copy of your personal data
- **Right to Rectification**: Correct inaccurate data
- **Right to Erasure**: Request deletion of your data
- **Right to Restrict Processing**: Limit how we use your data
- **Right to Data Portability**: Receive your data in a portable format
- **Right to Object**: Object to certain types of processing

To exercise these rights, contact us using the methods in the Contact Us section.

### Permissions
- You can revoke Android permissions in Android Settings -> Apps -> SoFarYetSoClose -> Permissions.
- The overlay permission is granted and revoked separately, in Android Settings -> Apps -> SoFarYetSoClose -> Display over other apps.
- Revoking required permissions may prevent related features from functioning.

## Children's Privacy

- Our app is **not intended for children under 13**.
- We do not knowingly collect data from children under 13.
- If you are a parent or guardian and believe your child has provided personal information, please contact us to request deletion.
- Parents and guardians should supervise children's use of apps that store personal content.

## Security

- Local data is protected by Android's application sandbox. SoFarYetSoClose is an Android app only; there is no web or browser version of it.
- Network communication uses HTTPS/TLS where applicable.
- Third-party services named in this policy provide their own security controls and privacy policies.
- You are responsible for protecting your device and your Google account credentials.
- We do not sell your personal data.

## Changes to This Policy

We may update this Privacy Policy to reflect new features, legal requirements, or changes in our practices. Significant changes will be:
- Noted in the app release notes or repository when applicable
- Reflected with a new "Last updated" date
- Communicated in the app or project page if the change is significant

The "Last updated" date at the top of this policy indicates when revisions occurred. Continued use of the app after changes constitutes acceptance of the updated policy.

## Contact Us

If you have questions about this Privacy Policy, wish to request data deletion, or have privacy concerns:

* **GitHub Repository:** https://github.com/SUDARSHANCHAUDHARI/sofaryetsoclose-privacy-policy
* **Email:** sunny.sudarshan@gmail.com
* **Main App Repository:** https://github.com/SUDARSHANCHAUDHARI/SoFarYetSoClose

We will respond as quickly as possible, typically within 48 hours.

## Data Deletion

### How to Delete Your Account:
You have **multiple options** to delete your account and associated data:

#### Option 1: In-App Deletion
1. Open SoFarYetSoClose
2. Go to **Settings**, then **Account**
3. Tap **Delete Account**
4. Confirm

This removes your account record in Firebase — the pairing, the invite code, the sleep window, the time zone offset and the push token — every nudge you sent or received, and every voice note you uploaded. Your partner is unpaired and can pair with someone else afterwards.

**One thing it does not yet remove: the sign-in record itself**, which is the entry in Firebase Authentication holding your email address. Deleting your account from inside the app signs you out and leaves that record in place. An app update that removes it in the same step is in progress; until it ships, email us as in Option 2 and we will delete it. We would rather say this plainly than let you believe it is already gone.

#### Option 2: Email Deletion Request
Send an email to: **sunny.sudarshan@gmail.com**
- Subject: "Data Deletion Request - SoFarYetSoClose"
- Include: The email/account identifier used in the app, if any
- We will process deletion requests as quickly as possible, typically within 48 hours for acknowledgement

#### Option 3: Clearing the App's Local Data
1. Android Settings > Apps > SoFarYetSoClose > Storage > Clear Data, or uninstall the app
2. This removes the app's local copy — settings and the offline queue — from your device only. It does not delete anything from Firebase, so use Option 1 or Option 2 for that.

There is no deletion form on this page. This page is a static document with no scripts and no forms; email is how a request reaches us.

### What Gets Deleted:
- Your account record in Firebase, including the pairing, the invite code, the sleep window, the time zone offset and the push token
- Every nudge you sent or received
- Every voice note you uploaded to Firebase Storage
- The app's local settings and offline queue, when you clear app data or uninstall
- The sign-in record holding your email address — today by email request, see Option 1

### Data Retention After Deletion:
- **Immediate:** account access may stop or deletion may be queued depending on the service
- **Up to 30 days:** cloud data may be removed from active systems unless a shorter period is legally required
- **Backups/logs:** limited backup or security logs may remain for a short period under provider policies

To request deletion of your data:

1. Open SoFarYetSoClose, if installed
2. Delete local content or clear app/site data where applicable
3. Contact support via email: sunny.sudarshan@gmail.com
4. Request account/data deletion and include enough detail for us to identify the app and any account, if one exists
5. We will confirm what data can be deleted and complete the request according to the retention terms above

## Firebase and Google Services

The app uses all of the following:

- Firebase Authentication, through Google Sign-In
- Firebase Firestore
- Firebase Storage
- Firebase Cloud Messaging
- Firebase Cloud Functions
- Firebase Analytics
- Firebase Crashlytics

Please review relevant third-party privacy policies:

- [Google Privacy Policy](https://policies.google.com/privacy)
- [Firebase Privacy Policy](https://firebase.google.com/support/privacy)
- [Google Play Terms](https://play.google.com/about/play-terms/)

## About SoFarYetSoClose

SoFarYetSoClose is built with privacy in mind. The app is built with:
- Kotlin and Jetpack Compose
- Firebase backend services
- Room/DataStore for offline/local state
- Push notifications and partner pairing features

The app collects only the data needed for the features described in this policy, and local-first features keep data on your device whenever possible.

---

**Last Updated:** November 9, 2026

---

## Recent Updates (Version 1.4.0 - November 9, 2026)

- **Disclosed the sleep window and the time zone offset.** Both are stored in Firebase and read by a Cloud Function so a nudge can be held until your partner is awake. Neither had ever been mentioned, and the time zone offset narrows your location to the width of a time zone, so it is now named rather than left in a field list.
- **Said that the text of a nudge travels in the push notification**, so it passes through Firebase Cloud Messaging and can appear on a lock screen, and described what the two Cloud Functions read and log.
- **Disclosed the voice-note auto-delete setting** — never, 7 days, 30 days, or after your partner listens — and that it defaults to never.
- **Corrected the deletion section.** Deleting your account from inside the app does not yet remove the sign-in record holding your email address; it signs you out and leaves that record. The policy now says so and tells you to email us until the app update lands. Also removed "Option 3: Web Deletion", which described a deletion form that has never existed on this page.
- **Said there is no per-nudge delete in the app**, in place of "delete content where supported". A reader could have believed a single voice note could be withdrawn.
- **Listed the permissions Android libraries merge in.** The app declares seven; the finished build carries twelve plus `com.google.android.gms.permission.AD_ID`. The Privacy Sandbox entries arrive with Firebase Analytics, and the entry states plainly that the app shows no advertising and has no advertising SDK.
- **Replaced the boilerplate security sentence** claiming protection by controls available on "Android, the browser, Firebase, Google, GitHub, or other services". There is no browser version of this app and no GitHub service in it. The section now says where data actually sits. The browser and GitHub references elsewhere in the document went with it.
- **Said the app asks for no profile details**, in place of "display/profile details you provide". Google Sign-In is the only route in and the app writes no profile of its own.
- **Added Firebase Analytics and Crashlytics to the services list**, which named only five of the seven Firebase products in use.

## Recent Updates (Version 1.3.0 - November 2, 2026)

- **Named Firebase Crashlytics and Firebase Analytics** and set out what each receives. This entry is recorded late: the change shipped under version 1.3.0 without a changelog note.

## Recent Updates (Version 1.2.0 - October 19, 2026)

- **Replaced general "media" wording with voice notes, the only media the app records or uploads, and described the plain-text Share option.**
- **Listed a single contact email.**

## Recent Updates (Version 1.1.0 - May 17, 2026)

- **Aligned policy with the shared privacy-policy structure.**
- **Clarified Firebase account/pairing data, partner sharing, media/audio features, offline queue, and notifications.**
