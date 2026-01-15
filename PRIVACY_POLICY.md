# SoFarYetSoClose Privacy Policy

**Last Updated**: January 2025

This Privacy Policy describes how **Sudarshan Tech Labs** ("we", "our", or "us") collects, uses, and protects your information when you use the **SoFarYetSoClose** Android application ("the App", "our App", "the Service").

By using SoFarYetSoClose, you agree to the collection and use of information in accordance with this policy.

---

## 1. Information We Collect

### 1.1 Account Information

When you create an account, we collect:

* **Email Address**: Required for Firebase Authentication
  * Used for account creation and login
  * Stored securely by Firebase Authentication
  * Not shared with third parties
* **User ID**: Generated automatically by Firebase Authentication
  * Unique identifier for your account
  * Used to link your data across Firebase services

### 1.2 User Profile Data

We store the following information in Firebase Firestore:

* **Partner Information**:
  * Partner ID (if you are paired with a partner)
  * Pairing timestamp
  * Unique invite code (for pairing with your partner)
* **Sleep Schedule**:
  * Sleep start time (HH:mm format, default: 22:00)
  * Sleep end time (HH:mm format, default: 08:00)
  * Stored so your partner can respect your sleep window for delayed nudge delivery
* **FCM Token**: For push notifications
  * Automatically generated and updated by Firebase
  * Used only to send notifications to your device
  * Updated when you reinstall the app or clear app data

### 1.3 Nudge Data

When you send or receive nudges, we store:

* **Nudge Content**:
  * Nudge type (NUDGE, EMOJI, or VOICE)
  * Phrase text (if type is NUDGE)
  * Emoji (if type is EMOJI)
  * Timestamp
  * Sender user ID
  * Recipient user ID
* **Voice Notes** (if applicable):
  * Audio file (AAC format, ~160 KB max, 10 seconds max)
  * Stored securely in Firebase Storage
  * Only accessible by you and your paired partner
  * Can be auto-deleted based on your preferences

### 1.4 App Preferences (Local Storage)

The following data is stored locally on your device:

* **Notification Sound Preferences**: Your chosen notification sound
* **Voice Note Auto-Delete Settings**: Your preference for voice note deletion
* **Onboarding Status**: Whether you've completed onboarding (shown once)

### 1.5 Offline Queue Data (Local Storage)

When you're offline, pending nudges are stored locally:

* **Pending Nudges**: Queued in Room database on your device
  * Automatically synced when you're back online
  * Deleted after successful sync
  * Never transmitted until you're online

---

## 2. How We Use Your Information

### 2.1 Primary Uses

We use your information to:

* **Authenticate Your Account**: Verify your identity using Firebase Authentication
* **Enable Pairing**: Connect you with your partner using invite codes
* **Send and Receive Nudges**: Deliver nudges, emojis, and voice notes between partners
* **Deliver Push Notifications**: Notify you when you receive nudges from your partner
* **Respect Sleep Schedules**: Delay nudge delivery during your partner's sleep window
* **Provide App Features**: Enable all app functionality including history, settings, and account management

### 2.2 Data Sharing

* **With Your Partner**: 
  * Only nudges and voice notes are shared with your paired partner
  * Your sleep schedule is visible to your partner (for sleep-aware delivery)
  * Your email address is NOT shared with your partner
* **With Firebase Services**:
  * All data is stored in Firebase (Google's secure infrastructure)
  * Firebase services are used for authentication, database, storage, and notifications
  * Firebase complies with Google's privacy policies and security standards
* **With Third Parties**:
  * We do NOT sell, rent, or share your data with third parties
  * We do NOT use your data for advertising purposes
  * We do NOT track you across apps or websites

---

## 3. Third-Party Services

### 3.1 Firebase Services (Google)

We use the following Firebase services:

* **Firebase Authentication**: Secure user authentication
  * Privacy Policy: [Firebase Privacy](https://firebase.google.com/support/privacy)
  * Google Privacy Policy: [Google Privacy](https://policies.google.com/privacy)
* **Firebase Firestore**: Cloud database for user and nudge data
  * Data is encrypted in transit (HTTPS/TLS) and at rest
  * Stored in Google Cloud infrastructure
  * Accessible only by authenticated users
* **Firebase Storage**: Secure storage for voice notes
  * Audio files are encrypted
  * Accessible only by you and your paired partner
* **Firebase Cloud Messaging (FCM)**: Push notifications
  * Used to deliver nudge notifications
  * Token stored securely in Firestore
  * No personal data is transmitted in notifications

### 3.2 Google Play Services (Optional)

* **Google Play Billing**: For future in-app purchases (if implemented)
* **Analytics**: Aggregated, anonymized usage statistics (if enabled)
  * No personally identifiable information is collected

---

## 4. Permissions Explained

### 4.1 Required Permissions

| Permission              | Purpose                          | Why Needed                                    |
| ------------------------ | -------------------------------- | --------------------------------------------- |
| **INTERNET**             | Connect to Firebase services     | Required for authentication, data sync, and notifications |
| **RECORD_AUDIO**         | Record voice notes               | Required to record 10-second voice messages   |
| **POST_NOTIFICATIONS**   | Send push notifications          | Required to notify you when you receive nudges |

### 4.2 Privacy Controls

You have full control over your data:

* ✅ **Account Deletion**: Delete your account and all data anytime (Settings → Account → Delete Account)
* ✅ **Unpairing**: Unpair from your partner anytime (Settings → Account → Unpair)
* ✅ **Notification Control**: Enable/disable notifications in device settings
* ✅ **Voice Note Control**: Choose auto-delete preferences for voice notes (Never, After 7/30 days, After partner listens)
* ✅ **Sleep Schedule**: Customize your sleep window anytime in Settings

---

## 5. Data Storage & Retention

### 5.1 Where Data is Stored

* **Firebase Firestore**: User profiles, nudges, pairing information
  * Stored in Google Cloud infrastructure
  * Encrypted in transit and at rest
* **Firebase Storage**: Voice note audio files
  * Stored securely in Google Cloud Storage
  * Encrypted and access-controlled
* **Local Device**: App preferences, offline queue (Room database)
  * Stored on your device only
  * Not synced to cloud

### 5.2 Data Retention

* **User Account**: Retained until you delete your account
* **Nudges**: Retained until you delete your account
* **Voice Notes**: 
  * Stored until you delete your account
  * Can be auto-deleted based on your preferences:
    * Never
    * After 7 days
    * After 30 days
    * After partner listens (placeholder - requires listened status tracking)
* **Offline Queue**: Deleted after successful sync
* **FCM Token**: Retained until you delete your account or uninstall the app

### 5.3 Data Deletion

When you delete your account:

1. All your user data is deleted from Firestore
2. All your nudges are deleted from Firestore
3. All your voice notes are deleted from Firebase Storage
4. Your partner is automatically unpaired
5. Your FCM token is removed
6. Local app data is cleared

**Note**: Deletion is permanent and cannot be undone. Your partner will be notified that you have unpaired.

---

## 6. Security Measures

### 6.1 Data Protection

We implement industry-standard security measures:

* ✅ **Encryption**: All data is encrypted in transit (HTTPS/TLS) and at rest
* ✅ **Authentication**: Secure Firebase Authentication with email/password
* ✅ **Access Control**: Firestore security rules ensure only you and your partner can access your data
* ✅ **Secure Storage**: Voice notes stored securely in Firebase Storage with access controls
* ✅ **Regular Updates**: Security patches and updates applied regularly

### 6.2 Security Rules

Firestore security rules enforce:

* Users can only read/write their own user document
* Users can only read nudges sent to them or from them
* Users can only upload voice notes to their own folder
* Partner access is limited to paired users only
* All operations require authentication

---

## 7. Your Rights

### 7.1 Data Control

You have the right to:

* **View Your Data**: Access all your nudges and profile in the app
* **Edit Your Data**: Update sleep schedule, notification preferences
* **Delete Your Data**: Delete individual nudges or your entire account
* **Unpair**: Unpair from your partner anytime
* **Export**: Request your data export (contact us at sudarshantechlabs@gmail.com)

### 7.2 GDPR Rights (EU Users)

If you're in the European Union, you have additional rights under GDPR:

* ✅ **Right to Access**: View all your personal data
* ✅ **Right to Rectification**: Edit inaccurate data
* ✅ **Right to Erasure**: Delete your account and all data ("Right to be Forgotten")
* ✅ **Right to Data Portability**: Request your data export in a portable format
* ✅ **Right to Object**: Control how your data is used
* ✅ **Right to Restrict Processing**: Limit how we process your data

**How to Exercise Your Rights**: 
* Use the app's built-in features in Settings
* Contact us directly at sudarshantechlabs@gmail.com
* We will respond within 30 days

### 7.3 CCPA Rights (California Users)

If you're in California, you have additional rights under CCPA:

* ✅ **Right to Know**: Know what personal information we collect
* ✅ **Right to Delete**: Request deletion of your personal information
* ✅ **Right to Opt-Out**: Opt-out of sale of personal information (we don't sell data)
* ✅ **Right to Non-Discrimination**: We won't discriminate for exercising your rights

---

## 8. Children's Privacy

SoFarYetSoClose is intended for users who are 18 years of age or older. We do not knowingly collect personal information from children under 18.

If you are a parent or guardian and believe your child has provided us with personal information, please contact us immediately. We will delete such information from our servers.

---

## 9. International Data Transfers

Your data may be transferred to and stored in servers located outside your country of residence. Firebase services are hosted in Google Cloud data centers worldwide.

By using the App, you consent to the transfer of your data to these servers. We ensure that appropriate safeguards are in place to protect your data in accordance with this Privacy Policy.

---

## 10. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. We will notify you of any changes by:

* Updating the "Last Updated" date at the top of this policy
* Posting the new Privacy Policy in the app
* Sending you an in-app notification (for significant changes)

Your continued use of the App after any changes constitutes your acceptance of the new Privacy Policy.

---

## 11. Contact Us

If you have any questions about this Privacy Policy or our data practices, please contact us:

* **Email**: sudarshantechlabs@gmail.com
* **Developer Email**: sunny.sudarshan@gmail.com
* **Website**: <https://sudarshantechlabs.com>
* **GitHub**: [SoFarYetSoClose Repository](https://github.com/SUDARSHANCHAUDHARI/SoFarYetSoClose)

**Response Time**: We aim to respond to privacy-related inquiries within **48 hours**.

---

## 12. About Sudarshan Tech Labs

**SoFarYetSoClose** is developed and published by **Sudarshan Tech Labs**.

* **Company**: Sudarshan Tech Labs
* **Website**: <https://sudarshantechlabs.com>
* **Email**: sudarshantechlabs@gmail.com
* **Developer**: Sudarshan Kishor Chaudhari
* **Developer Email**: sunny.sudarshan@gmail.com
* **GitHub**: [@SUDARSHANCHAUDHARI](https://github.com/SUDARSHANCHAUDHARI)

---

## 13. Legal Basis for Processing (GDPR)

For users in the European Union, we process your personal data based on:

* **Consent**: You consent to data processing by using the App
* **Contractual Necessity**: Processing is necessary to provide the App's services
* **Legitimate Interests**: To improve the App and ensure security

You can withdraw your consent at any time by deleting your account.

---

## 14. Data Breach Notification

In the event of a data breach that may affect your personal information, we will:

* Notify you within 72 hours (if required by law)
* Provide details about the breach
* Explain steps we're taking to address it
* Offer guidance on protecting your information

---

## 15. Complaints

If you have a complaint about how we handle your personal information, you can:

* Contact us directly at sudarshantechlabs@gmail.com
* File a complaint with your local data protection authority (for EU users)
* File a complaint with the California Attorney General (for California users)

---

**Last Updated**: January 2025

**Version**: 1.0

---

**Made with ❤️ by Sudarshan Tech Labs**

_Privacy is not a feature - it's a fundamental right._
