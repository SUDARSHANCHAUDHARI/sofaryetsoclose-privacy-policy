# Privacy Policy — SoFarYetSoClose

**Last updated:** 2026-03-21
**Effective date:** 2026-03-21

This Privacy Policy describes how **Sudarshan Tech Labs** ("we", "us", or "our") handles information in the **SoFarYetSoClose** Android application ("the App").

---

## 1. About This App

SoFarYetSoClose is a communication app that keeps people connected over distance. It uses Firebase Authentication for accounts, Firebase Firestore and Storage for data sync, and Firebase Cloud Messaging for notifications.

---

## 2. Data We Collect

### 2.1 Account Information

| Data | Purpose | Storage |
|---|---|---|
| Email address | Account identification | Firebase Authentication |
| Display name | Profile display | Firebase Authentication, Firestore |
| Google account info (if Google Sign-In used) | Authentication | Firebase Authentication |
| Authentication tokens | Secure sign-in | Firebase Authentication |

### 2.2 App Content and Usage Data

| Data | Purpose | Storage |
|---|---|---|
| User-generated content | Core app functionality | Firebase Firestore |
| Media files | Content sharing | Firebase Storage |
| Audio recordings | In-app audio features | Firebase Storage |
| App preferences and settings | Personalisation | DataStore (on-device), EncryptedSharedPreferences |
| Push notification tokens | Deliver notifications | Firebase Cloud Messaging |

### 2.3 Analytics and Crash Data

| Data | Purpose | Storage |
|---|---|---|
| App usage events | Improve user experience | Firebase Analytics |
| Crash reports (device info, stack trace) | App stability | Firebase Crashlytics |

---

## 3. How Data Is Used

- To authenticate users and manage accounts via Firebase Authentication
- To sync content and data across sessions via Firestore
- To deliver push notifications via Firebase Cloud Messaging
- To store media and audio files via Firebase Storage
- To improve app quality through aggregated analytics
- To diagnose and fix crashes via Crashlytics

---

## 4. Data Sharing

We do not sell your data. Content in the App is shared only as required by the app's functionality (e.g., with connected users). Analytics and crash data is processed by Google Firebase.

Third-party services used:
- **Google Firebase (Auth, Firestore, Storage, Messaging, Analytics, Crashlytics):** https://firebase.google.com/support/privacy
- **Google Sign-In:** https://policies.google.com/privacy

---

## 5. Permissions Explained

| Permission | Reason |
|---|---|
| `INTERNET` | Required for Firebase services |
| `RECORD_AUDIO` | Record audio within the app |
| `POST_NOTIFICATIONS` | Deliver push notifications |
| `VIBRATE` | Haptic feedback for notifications |
| `SYSTEM_ALERT_WINDOW` | Display overlay alerts when the app is in background |
| `FOREGROUND_SERVICE` | Run background service for real-time features |
| `FOREGROUND_SERVICE_REMOTE_MESSAGING` | Background messaging service type |

---

## 6. Data Retention

| Data | Retention |
|---|---|
| Account and Firestore data | Until you delete your account |
| Firebase Storage files | Until you delete them or your account |
| Firebase Analytics | Aggregated, 14 months (per Firebase policy) |
| Firebase Crashlytics | 90 days (per Firebase policy) |

---

## 7. Your Rights

You have the right to:
- Access your data within the App
- Delete individual content within the App
- Delete your account and all associated data (see below)
- Contact us for a data export at sudarshantechlabs@gmail.com

---

## 8. Account Deletion

To delete your account and all associated data:

1. Open the App
2. Go to **Settings > Account > Delete Account**

Or contact us at **sudarshantechlabs@gmail.com** with the subject "SoFarYetSoClose Account Deletion Request".

All Firestore data, Storage files, and your Authentication account will be permanently deleted within 30 days.

---

## 9. Children's Privacy

SoFarYetSoClose is not directed at children under 13. We do not knowingly collect personal information from children. If we become aware that a child under 13 has created an account, we will delete it promptly.

---

## 10. Data Security

- Authentication is handled by Firebase Authentication
- All data in transit is encrypted via HTTPS/TLS
- Firebase Firestore security rules restrict data access to authenticated owners
- Local preferences are stored using EncryptedSharedPreferences
- Release builds use code obfuscation (ProGuard/R8)

---

## 11. Changes to This Policy

We will notify you of significant changes by updating the "Last updated" date. Continued use of the App constitutes acceptance.

---

## 12. Contact

**Sudarshan Tech Labs**
Official website: https://sudarshantechlabs.com
Company email: sudarshantechlabs@gmail.com
Developer contact: sunny.sudarshan@gmail.com

---

## Play Store Data Safety Summary

| Data type | Collected | Shared | Purpose |
|---|---|---|---|
| Email address | Yes | No | Account authentication |
| User content | Yes | No (except connected users) | App functionality |
| Audio recordings | Yes | No | App functionality |
| App interactions | Yes (Firebase Analytics) | No | Analytics |
| Crash logs | Yes (Crashlytics) | No | App stability |

---

*This policy applies to the SoFarYetSoClose Android application published by Sudarshan Tech Labs.*
