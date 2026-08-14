# Privacy Policy — College Buddy: Attendance

**Last updated: 14 August 2026**

**Applies to:** College Buddy for iOS (App Store) and College Buddy for Android (Google Play).

This Privacy Policy explains how College Buddy ("the App", "we", "us") handles your information. Where the two platforms behave differently, the difference is marked **iOS only** or **Android only**.

## TL;DR

Your attendance records, subjects, timetable, assignments and notes are yours. There is no account system, we never ask for your name or email, and we cannot read your data.

What leaves your device:

1. **Ads.** Free users see ads from Google AdMob. Google's advertising SDK collects your device's advertising identifier and similar data. **Pro subscribers see no ads at all** — the ad code is never started for them.
2. **Purchases.** Apple or Google processes payment and tells the App only whether Pro is active.
3. **iCloud sync — iOS only.** Your data syncs across *your own* Apple devices through your private iCloud account, which we cannot access.
4. **Live Activity reminders — iOS only.** Upcoming class times and a device push token go to our small server so the lock-screen card appears at the right moment. No names, no attendance numbers.

**On Android, items 3 and 4 do not happen at all.** There is no sync, no push server, and no first-party network connection of any kind.

Nothing else is transmitted. Timetable scanning runs entirely on your device.

---

## 1. Information We Do NOT Collect

We do not collect, request, or store:

- Your name, email address, phone number, or any account credentials
- Your attendance percentages or present/absent records
- Your location, contacts, microphone, or photo library
- Any payment or card details

The App has no login, no user profile, and no first-party analytics. We do not build a profile of you, and we do not sell data to anyone.

---

## 2. Information Stored on Your Device

Stored locally, using each platform's standard storage:

| | |
|---|---|
| **iOS** | `UserDefaults` and an App Group container |
| **Android** | Jetpack DataStore, in the App's private storage |

What is stored:

- **Subjects** — names, attendance counts, thresholds, colours
- **Timetable** — your weekly class schedule
- **Assignments** — titles, due dates, status, notes
- **Planner tasks** — titles, times, categories, repeat rules
- **History** — a log of each Present/Absent you record
- **Preferences** — reminder settings, default attendance requirement, whether Pro is active

This data never leaves your device except as described in §5 (iOS iCloud) and §6 (iOS Live Activities). **On Android it never leaves your device at all.**

---

## 3. Advertising (Free Users Only)

The free version shows ads supplied by **Google AdMob**. To do this, Google's Mobile Ads SDK collects and processes:

- Your device's **advertising identifier** — the Advertising ID on Android, or the IDFA on iOS
- Device and network information such as model, operating system version, language, and coarse region
- Ad interaction events — impressions and clicks

Google acts as an **independent data controller** for this information. We never see it, and we cannot link it to your attendance data.

- Google's privacy policy: [policies.google.com/privacy](https://policies.google.com/privacy)
- How Google uses data from apps that use its services: [policies.google.com/technologies/partner-sites](https://policies.google.com/technologies/partner-sites)

**Android:** the App declares the `com.google.android.gms.permission.AD_ID` permission for this purpose. You can reset or delete your Advertising ID at any time in **Settings → Privacy → Ads**, which also lets you opt out of personalised advertising.

**iOS:** the App uses App Tracking Transparency. If you decline the prompt, the IDFA is not used.

**Pro removes advertising entirely.** For Pro users the ads SDK is never initialised, so no advertising identifier is read.

### Consent in the EEA, UK and Switzerland

**iOS** presents a Google User Messaging Platform consent message before personalised ads are served.

**Android** does not currently present a consent message. Until it does, users in those regions should treat the Android app as unsuitable if they do not wish Google to process the data described above, and may either opt out of personalised ads at the OS level or upgrade to Pro to remove advertising completely. We intend to add an in-app consent message to the Android version.

---

## 4. Timetable Scanning

The App can build your timetable from a photo or PDF you choose.

- The image is read using **Google ML Kit text recognition**, with the model **bundled inside the App**. Recognition happens **entirely on your device**.
- The image is **not uploaded**, not sent to us, and not sent to Google.
- The App requests no photo-library permission — you pick a single file through the system picker, and only that file is read.
- Only the recognised class names and times are saved, and only if you tap to confirm the import.

---

## 5. iCloud Sync — iOS only

Your subjects, timetable, assignments and planner sync between *your own* Apple devices through Apple's iCloud (CloudKit private database). It is your iCloud account; we have no access. You can disable it in iOS Settings.

**The Android app has no sync.** Data stays on the single device.

---

## 6. Live Activities and Notifications

**iOS.** So a class card can appear on your lock screen at the right time, the App sends upcoming class times and an anonymous device push token to a small server we operate on Cloudflare Workers. It holds no name, email, attendance figures, or advertising identifier, and entries expire automatically.

**Android.** Nothing equivalent happens. Class reminders and the in-class Present/Absent notification are produced by **local alarms scheduled on your device**. No push service, no server, no network connection. The App requests `POST_NOTIFICATIONS`, `SCHEDULE_EXACT_ALARM`, `RECEIVE_BOOT_COMPLETED` (to restore alarms after a restart) and `VIBRATE` solely for this.

---

## 7. Widgets, Watch and Home Screen

Home-screen widgets — and, on iOS, the Apple Watch app — read your subjects and timetable from local storage. This code runs locally and transmits nothing.

---

## 8. Subscriptions and In-App Purchases

College Buddy offers optional Pro subscriptions and a one-time Lifetime unlock.

| | |
|---|---|
| **iOS** | Apple StoreKit |
| **Android** | Google Play Billing |

- **Apple or Google** processes the transaction. You enter your payment details into their interface, not ours.
- **We receive only** a confirmation that an entitlement is active. It contains no name, email, payment details, or account ID.
- It is used solely to unlock Pro features and switch off advertising.

To manage or cancel:

- **iOS** — Settings → your name → Subscriptions → College Buddy. Refunds: [reportaproblem.apple.com](https://reportaproblem.apple.com)
- **Android** — Google Play → Menu → Payments & subscriptions → Subscriptions → College Buddy. Refunds: [support.google.com/googleplay](https://support.google.com/googleplay/answer/2479637)

---

## 9. Third-Party Services

| Service | Platform | Purpose | Privacy policy |
|---|---|---|---|
| **Google AdMob** | Both | Advertising for free users | [policies.google.com/privacy](https://policies.google.com/privacy) |
| **Google ML Kit** (bundled, on-device) | Both | Timetable text recognition | [policies.google.com/privacy](https://policies.google.com/privacy) |
| **Google User Messaging Platform** | iOS | Consent collection in the EEA/UK/Switzerland | [policies.google.com/privacy](https://policies.google.com/privacy) |
| **Google Play Billing** | Android | Subscriptions and purchases | [policies.google.com/privacy](https://policies.google.com/privacy) |
| **Google Play In-App Review** | Android | The optional "rate this app" prompt | [policies.google.com/privacy](https://policies.google.com/privacy) |
| **Apple StoreKit** | iOS | Subscriptions and purchases | [apple.com/legal/privacy](https://www.apple.com/legal/privacy/) |
| **Apple iCloud** | iOS | Sync across your own devices | [apple.com/legal/privacy](https://www.apple.com/legal/privacy/) |
| **Apple Push Notification service + our Cloudflare Worker** | iOS | Lock-screen Live Activities | [cloudflare.com/privacypolicy](https://www.cloudflare.com/privacypolicy/) |

We do not integrate Firebase, Facebook, Mixpanel, AppsFlyer, Adjust, or any other analytics or attribution SDK.

---

## 10. Google Play Data Safety Summary

For the Android app, this is what the Play Data safety declaration corresponds to:

| Data type | Collected | Shared | Purpose | Optional? |
|---|---|---|---|---|
| **Device or other IDs** (Advertising ID) | Yes | Yes — with Google | Advertising | Yes — not collected for Pro users |
| App activity, attendance, timetable, assignments | No | No | — | — |
| Personal info, location, contacts, photos, files | No | No | — | — |
| Financial info | No | No | Payment is handled entirely by Google Play | — |

Data is **encrypted in transit** (all SDK traffic uses HTTPS/TLS). Users can request deletion as described in §12.

---

## 11. Children's Privacy

College Buddy is intended for college and university students. It is not directed at children under 13, and we do not knowingly collect personal information from them.

Because the free version shows advertising that may use the advertising identifier, we recommend the App be used by those aged 13 and over (16 in some EEA countries). If you believe a child has used the App and you would like its data removed, uninstalling the App removes everything stored on the device; you may also contact us below.

---

## 12. Deleting Your Data

Because your data lives on your device, you control it directly:

- **In the App** — Settings → **Reset Semester** permanently deletes all subjects, attendance history, timetable entries, assignments and planner tasks.
- **Uninstalling** the App removes everything it stored.
- **iOS only** — uninstalling also clears your class times from our push server on next launch; to remove them immediately, delete the App.
- **Advertising data held by Google** — reset or delete your Advertising ID in your device settings, and direct any further request to Google using the links in §3.

We hold no server-side account for you, so there is no account for us to delete. If you would like written confirmation of any of the above, email us and we will respond within 7 days.

---

## 13. Data Security

Data on your device is protected by the platform's security model — device passcode or biometrics and full-disk encryption on both iOS and Android, plus Android's per-app private storage. All traffic to Google and (on iOS) to our push server is encrypted using HTTPS/TLS. We recommend keeping your device updated.

---

## 14. Your Rights

If you are in the EU, UK, California, India, or another jurisdiction with data protection law, you have rights of access, rectification, erasure, restriction, and objection.

Because we hold almost nothing about you, most of these you can exercise yourself:

- **Access / rectify** — your data is on your device; view and edit it directly in the App.
- **Erase** — see §12.
- **Object to advertising** — opt out of personalised ads in your device settings, decline the App Tracking Transparency prompt on iOS, or upgrade to Pro to remove ads entirely.
- **Google-held ad data** — Google is an independent controller of the advertising data described in §3; direct requests about it to Google.

For anything else, contact us below and we will respond within 7 days.

---

## 15. Changes to This Policy

If we change how the App handles data, we will update this Policy and the "Last updated" date. For material changes we will display a notice inside the App.

---

## 16. Contact

For privacy questions or concerns, email:

**raaghav.mehta.36@gmail.com**

We'll respond within 7 days.

---

*College Buddy is developed and operated by Raaghav Mehta, Sirsa, Haryana, India.*
