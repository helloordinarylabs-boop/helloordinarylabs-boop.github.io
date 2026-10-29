---
permalink: /privacy-policy.html
---

# Privacy Policy for Fresh Note

**Effective Date:** October 25, 2026  
**Last Updated:** October 29, 2026

Fresh Note ("we," "our," or "us"), developed and maintained by **Ordinary Labs**, is committed to protecting your privacy and ensuring you have complete control over your personal data.

This Privacy Policy explains how Fresh Note (`com.ordinarylabs.freshnotes`) handles information when you use our mobile application on Android devices. This policy complies with Google Play Developer Policy requirements and applicable privacy laws, including the General Data Protection Regulation (GDPR) and the California Consumer Privacy Act (CCPA).

---

## 1. Developer and Contact Information

- **Developer Brand:** Ordinary Labs
- **Developer Contact Email:** [hello.ordinarylabs@gmail.com](mailto:hello.ordinarylabs@gmail.com)
- **Official Repository & Project Updates:** [https://github.com/helloordinarylabs](https://github.com/helloordinarylabs)

If you have questions, feedback, or requests regarding this Privacy Policy or your data, please contact us at [hello.ordinarylabs@gmail.com](mailto:hello.ordinarylabs@gmail.com).

---

## 2. Core Architecture: Local-First Privacy

Fresh Note is designed with a **privacy-by-default, local-first architecture**:

- **No Developer Servers:** Ordinary Labs does not own, operate, or host remote servers or cloud databases to store, inspect, process, or sell your notes.
- **On-Device Storage:** All notes, folder structures, tags, templates, attachments, and user preferences are stored directly on your device in a private SQLite database managed by Android Room.
- **Complete Ownership:** Your thoughts, writing, and personal records remain exclusively on your device under your direct physical and cryptographic custody.

---

## 3. Information We Collect and Process

### A. Notes and Content (User Data)
- **What is collected:** Plain text, Markdown notes, checklist items, folder names, and local file references created or imported by you.
- **How it is used:** Strictly to provide core note-taking and organization functionality within the app.
- **Where it is stored:** Exclusively in the local application sandbox on your device. We never transmit your notes to Ordinary Labs or any unauthorized third party.

### B. Biometric Authentication Data
- **What is processed:** Fingerprint or facial recognition verification when you enable "Lock Notebook Now" or app lock protection.
- **How it is handled:** Handled entirely by Android OS security hardware through official `BiometricPrompt` system APIs. Fresh Note **never** accesses, captures, stores, or transmits your actual biometric data, fingerprint images, or facial scans. Only a boolean success/failure signal is returned by the operating system.

### C. Cloud Backup and Restore (Google Drive)
- **What is collected:** If you voluntarily connect your Google Drive account, the app communicates with the Google Drive API.
- **Scope of Access:** The app requests minimal scoped access (`drive.appdata` / `drive.file`) strictly to read, write, and manage Fresh Note backup archives (`.backup`) created by the application.
- **Encryption:** Backup archives are encrypted on-device using symmetric AES encryption before being uploaded to your personal Google Drive storage.
- **No Intermediary:** Ordinary Labs operates no intermediate proxy servers. All communication occurs directly between your device and Google's authenticated endpoints. We never receive or store your Google account credentials or passwords.

### D. Advertising and Diagnostic Data (Google AdMob)
Fresh Note utilizes **Google AdMob** (publisher ID: `pub-6762588093607118`) to display advertisements in the free tier of the app. The Google Mobile Ads SDK may collect and process certain device information to provide and personalize ads, limit fraud, and track performance.
- **Identifiers Collected by AdMob:** Android Advertising ID (`AD_ID`), approximate IP address, and technical device identifiers (model, OS version).
- **Diagnostics:** Crash logs, app performance metrics, and ad interaction events.
- **Ad Deactivation via "Remove Ads":** When you purchase the optional, one-time "Remove Ads" in-app product, **all banner, native, and interstitial advertisements are completely deactivated**, and no further ad requests or ad-tracking events are initiated by the application.
- **Third-Party Policy:** For details on how Google processes ad data, visit [Google's Advertising Privacy & Terms](https://policies.google.com/technologies/ads) and [Google Privacy Policy](https://policies.google.com/privacy).
- **Opting Out:** You can reset or delete your Advertising ID, or opt out of personalized advertising at any time through your Android device settings:
  - *Android Settings → Google → Ads → Delete advertising ID* (or *Opt out of Personalized Ads*).

### E. In-App Purchases and Billing Information (Google Play Billing)
Fresh Note offers an optional one-time in-app purchase to remove advertisements permanently.
- **Payment Processing:** All purchase transactions, payment method verification, credit card processing, local currency conversion, and sales taxes are processed directly and securely by **Google Play** via the Google Play Billing Library.
- **No Financial Data Collected:** Ordinary Labs does **not** collect, view, process, or store your credit card numbers, bank account information, or billing address.
- **Data Accessed by Fresh Note:** The app only queries Google Play for the anonymous purchase token, product identifier (`remove_ads`), and purchase verification status to unlock your ad-free entitlement and verify/restore it across app restarts and device upgrades.
- **Google Play Terms:** All purchases are governed by the [Google Play Terms of Service](https://play.google.com/intl/en-US_us/about/play-terms/) and [Google Payments Privacy Notice](https://payments.google.com/legaldocument?family=privacy_notice).

---

## 4. Android System Permissions Requested

Fresh Note requests only permissions essential to its operation:

| Permission | Technical Name | Purpose & Justification |
| :--- | :--- | :--- |
| **In-App Billing** | `com.android.vending.BILLING` | Required to communicate with Google Play to facilitate the secure one-time purchase of "Remove Ads" and query/restore existing purchases. |
| **Biometric Lock** | `android.permission.USE_BIOMETRIC`<br>`android.permission.USE_FINGERPRINT` | Authenticates device ownership on-device to lock/unlock private notes. Biometric data never leaves hardware keystore. |
| **Network Access** | `android.permission.INTERNET`<br>`android.permission.ACCESS_NETWORK_STATE` | Allows rendering external Markdown images/links, syncing encrypted backups with Google Drive, verifying in-app billing with Google Play, and loading Google AdMob ads. |
| **Advertising ID** | `com.google.android.gms.permission.AD_ID` | Standard Google Play services permission required by the Google AdMob SDK for analytics, ad serving, and fraud prevention. |
| **Foreground Service / Wake Lock** | `android.permission.WAKE_LOCK`<br>`android.permission.FOREGROUND_SERVICE` | Ensures safe completion of user-initiated note backup, export, or restore tasks without data corruption. |

---

## 5. Third-Party Service Providers

We integrate minimal, reputable third-party services:

1. **Google Play In-App Billing:** For secure handling of one-time in-app purchases.  
   *Privacy Policy:* [https://payments.google.com/legaldocument?family=privacy_notice](https://payments.google.com/legaldocument?family=privacy_notice)
2. **Google Mobile Ads (AdMob):** For in-app advertisements in the free version.  
   *Privacy Policy:* [https://policies.google.com/privacy](https://policies.google.com/privacy)
3. **Google Play Services & Google Drive API:** For optional cloud backup and authentication.  
   *Privacy Policy:* [https://policies.google.com/privacy](https://policies.google.com/privacy)

We do not sell, rent, monetize, or broker your personal information or notes to data brokers, analytics farms, or third-party marketing services.

---

## 6. Data Retention, Deletion, and User Rights

You maintain absolute sovereignty over your data:

- **In-App Deletion:** You can delete individual notes, empty the Trash Bin, or use **Settings → Clear All Notes** to wipe the local database instantly.
- **Uninstalling the App:** Uninstalling Fresh Note permanently deletes the application sandbox and all local note data from your device storage.
- **In-App Purchases:** In-app purchase records are managed directly by Google Play. You can view your purchase history at any time in the Google Play Store app (*Google Play ➔ Profile icon ➔ Payments & subscriptions ➔ Budget & order history*). Purchases remain tied to your Google Account and are restored automatically upon reinstalling the app.
- **Google Drive Backup Deletion:** You can delete stored backups directly from inside Fresh Note via the Backup & Restore screen or by managing app data in your Google Drive account (*Google Drive Settings → Manage Apps → Fresh Note → Delete hidden app data*).
- **No Account Deletion Request Needed:** Because Ordinary Labs does not collect accounts, email registrations, or server-side user data, there is no server-side user record to delete.

---

## 7. Children's Privacy (COPPA & GDPR-K Compliance)

Fresh Note does not address anyone under the age of 13 (or under 16 in the European Economic Area). We do not knowingly collect or solicit personally identifiable information from children. If you are a parent or guardian and believe a child has provided us with personal data, please contact us at [hello.ordinarylabs@gmail.com](mailto:hello.ordinarylabs@gmail.com), and we will take immediate corrective action.

---

## 8. Data Security

We implement rigorous technical safeguards to protect your notes:
- **Application Sandbox:** Protected by Android's Linux kernel process isolation and SELinux policies.
- **Encryption in Transit:** All network requests to Google Drive and Google AdMob use industry-standard Transport Layer Security (TLS 1.3 / HTTPS).
- **Encrypted Archives:** All exported Google Drive backups are encrypted on-device before leaving your phone.
- **Screen Protection:** Users can enable "Screen Content Protection" in Settings to prevent app screenshots and hide note previews in the Android Recent Apps switcher.

---

## 9. Changes to this Privacy Policy

We may update this Privacy Policy periodically to reflect new features, operational practices, or legal requirements. When updates occur, the "Last Updated" date at the top of this document will be revised, and the updated version will be committed to our public repository. We encourage you to review this Privacy Policy periodically.

---

## 10. Contact Us

If you have any questions, suggestions, or concerns regarding this Privacy Policy, please reach out to us:

- **Entity:** Ordinary Labs
- **Email:** [hello.ordinarylabs@gmail.com](mailto:hello.ordinarylabs@gmail.com)
- **GitHub:** [https://github.com/helloordinarylabs](https://github.com/helloordinarylabs)
