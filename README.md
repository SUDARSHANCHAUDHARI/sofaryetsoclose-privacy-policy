# SoFarYetSoClose — Privacy Policy

**Effective Date:** 2026-03-21
**Last Updated:** 2026-03-21
**Version:** 1.0.0

Published by **Sudarshan Tech Labs** | https://sudarshantechlabs.com | sudarshantechlabs@gmail.com

---

SoFarYetSoClose is a long-distance connection app for Android. It helps people stay connected over distance through shared content and real-time communication features. The App uses Firebase Authentication for secure accounts and Firebase Firestore and Storage for data sync.

---

## Data Collection

### Account Information

| Data | Purpose | Storage |
|---|---|---|
| Email address | Account identification | Firebase Authentication |
| Display name | Profile display | Firebase Authentication, Firestore |
| Google account info (if Google Sign-In used) | Authentication only | Firebase Authentication |
| Authentication session tokens | Maintain secure sign-in | Firebase Authentication |
| FCM push token | Deliver notifications | Firebase Cloud Messaging |

### App Content

| Data | Purpose | Storage |
|---|---|---|
| User-generated content (messages, posts, shared items) | Core app functionality | Firebase Firestore |
| Audio recordings | In-app audio features | Firebase Storage |
| Media files (images, videos shared in-app) | Content sharing | Firebase Storage |
| App preferences | Personalisation | DataStore and EncryptedSharedPreferences on your device |

### Analytics and Crash Data

| Data | Purpose | Storage |
|---|---|---|
| App usage events (screens visited, features used) | App improvement | Firebase Analytics |
| Device model, OS version, app version | Analytics context | Firebase Analytics |
| Crash stack traces (no personal content) | App stability | Firebase Crashlytics |

---

## How We Use Your Data

| Purpose | Data Used |
|---|---|
| Authenticate you securely | Firebase Authentication |
| Store and sync your content | Firebase Firestore and Storage |
| Deliver push notifications | Firebase Cloud Messaging |
| Record and share audio | Firebase Storage |
| Improve app quality | Firebase Analytics (aggregated) |
| Fix crashes | Firebase Crashlytics |

---

## Data Storage and Security

- **Authentication:** Firebase Authentication with Google's secure infrastructure
- **Content:** Firebase Firestore and Storage with encryption in transit (HTTPS/TLS) and at rest
- **Firestore security rules:** Your content is accessible only to you and users you connect with
- **Local preferences:** Stored in EncryptedSharedPreferences on your device
- **Background messaging:** Foreground service runs for real-time message delivery

## Data Retention

| Data | Retention |
|---|---|
| Account and Firestore content | Until you delete your account |
| Firebase Storage files | Until you delete them or your account |
| Firebase Analytics | Aggregated, 14 months (Firebase default) |
| Firebase Crashlytics | 90 days (Firebase default) |

---

## Data Sharing

We do not sell your data. Content is shared only with users you connect with in-app. Data is processed by:

- **Google Firebase (Authentication, Firestore, Storage, Messaging, Analytics, Crashlytics):** https://firebase.google.com/support/privacy
- **Google (Google Sign-In):** https://policies.google.com/privacy

---

## Account Deletion

You have the right to delete your account and all associated data at any time.

### Option 1 — In-App Deletion
1. Open SoFarYetSoClose
2. Go to **Settings**
3. Tap **Account**
4. Tap **Delete Account**
5. Confirm the deletion

### Option 2 — Email Request
Send an email to **sudarshantechlabs@gmail.com** with:
- Subject: **SoFarYetSoClose Account Deletion Request**
- Your registered email address

We will process your request within 30 days.

### What Gets Deleted
- ✅ Firebase Authentication account
- ✅ All Firestore content (messages, posts, shared items)
- ✅ All Firebase Storage files (audio, media)
- ✅ Push notification token

### What May Remain
- Aggregated, anonymised Firebase Analytics data
- Firebase Crashlytics reports (no personal content)

---

## Permissions Explained

| Permission | Why It Is Needed |
|---|---|
| `INTERNET` | Required for all Firebase services |
| `RECORD_AUDIO` | Record audio messages |
| `POST_NOTIFICATIONS` | Deliver message and activity notifications |
| `VIBRATE` | Haptic feedback for notifications |
| `SYSTEM_ALERT_WINDOW` | Display overlay alerts when App is backgrounded |
| `FOREGROUND_SERVICE` | Run real-time messaging service in background |
| `FOREGROUND_SERVICE_REMOTE_MESSAGING` | Required service type for messaging foreground service |

---

## Your Rights and Controls

- **Delete content:** Delete individual items within the App
- **Delete account:** See Account Deletion section above
- **Disconnect notifications:** Disable in Android Settings > Apps > SoFarYetSoClose > Notifications

---

## Children's Privacy

SoFarYetSoClose is not directed at children under 13. We do not knowingly create accounts for children under 13. If we become aware that a child under 13 has registered, we will delete the account promptly.

---

## Changes to This Policy

We may update this Privacy Policy from time to time. We will notify you of significant changes via:

- In-app notification
- Updated policy date on this page

Continued use of SoFarYetSoClose after changes become effective constitutes your acceptance of the updated policy.

---

## Contact Us

For privacy questions, data access requests, or account deletion:

- **Email:** sudarshantechlabs@gmail.com
- **Developer:** sunny.sudarshan@gmail.com
- **Website:** https://sudarshantechlabs.com
- **Response Time:** Within 48 hours

---

## GDPR Rights (EU Users)

If you are in the European Economic Area, you have the right to:

- **Access** — Request a copy of your personal data
- **Rectification** — Correct inaccurate data
- **Erasure** — Request deletion of your data
- **Restrict Processing** — Limit how we use your data
- **Data Portability** — Receive your data in a portable format
- **Object** — Object to certain types of processing

To exercise these rights, contact us at the details above.

---

## Play Store Data Safety Summary

| Data type | Collected | Shared | Purpose |
|---|---|---|---|
| Email address | Yes | No | Account authentication |
| User content | Yes | Connected users only | App functionality |
| Audio recordings | Yes | Connected users only | App functionality |
| App interactions | Yes (Firebase Analytics) | No | Analytics |
| Crash logs | Yes (Crashlytics) | No | App stability |

---

---

**This privacy policy complies with:**
- Google Play Store requirements
- GDPR (General Data Protection Regulation)
- CCPA (California Consumer Privacy Act)

**Last reviewed:** 2026-03-21
