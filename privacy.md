# Privacy Policy — College Buddy: Attendance

**Last updated: 23 July 2026**

This Privacy Policy explains how College Buddy ("the App", "we", "us") handles your information.

## TL;DR

Your attendance records, subjects, timetable, assignments and notes are yours. We do not have an account system, we never ask for your name or email, and we cannot read your data.

Three things do leave your device, and you should know about them:

1. **Ads.** Free users see ads from Google AdMob. Google's advertising SDK collects your device's advertising identifier and similar data. **Pro subscribers see no ads at all** — the ad code is never even started for them.
2. **Live Activity reminders.** So your class card can appear on the lock screen at the right moment, the App sends your upcoming class times and a device push token to our small server. No names, no attendance numbers.
3. **iCloud sync.** Your data syncs across *your own* devices through Apple's iCloud. It goes to your private iCloud account, which we cannot access.

Details on all three below.

---

## 1. Information We Do NOT Collect

We do not collect, request, or store:

- Your name, email address, phone number, or any account credentials
- Your attendance percentages or present/absent records (these never leave your device except into your own iCloud — see §6)
- Your location, contacts, microphone, or photo library
- Any payment or card details

The App has no login, no user profile, and no first-party analytics. We do not build a profile of you, and we do not sell data to anyone.

---

## 2. Information Stored on Your Device

The following is stored locally on your iPhone using Apple's standard storage APIs (`UserDefaults` and an App Group container):

- **Subjects** — names, attendance counts, thresholds, colours
- **Timetable** — your weekly class schedule
- **Assignments** — titles, due dates, status, notes
- **Attendance history** — a log of present/absent entries
- **Planner tasks** — your scheduled study tasks
- **Settings** — notification time, subscription status cache

You can delete all of it at any time via **Settings → Reset Semester**, or by uninstalling the App.

---

## 3. Advertising (Google AdMob)

**This section applies to free users only. If you subscribe to Pro, no ads are requested, the advertising SDK is never started, and nothing in this section happens.**

The free version of College Buddy shows ads supplied by **Google AdMob**, using the Google Mobile Ads SDK. Two formats are used:

- **Interstitial** — an occasional full-screen ad when you return to the App.
- **Rewarded** — an entirely optional ad you may choose to watch to unlock a single timetable scan. It never plays unless you tap to start it.

To serve these ads, Google may collect and process:

- Your device's **advertising identifier (IDFA)** and other device identifiers
- Device and general location information derived from your **IP address**
- **Ad interaction data** — which ads were shown, viewed, or tapped
- Diagnostic data such as crash and performance information

This data is used by Google for ad delivery, ad measurement, personalisation, and fraud prevention. Google acts as an independent controller of this data. Its handling is governed by:

- [Google Privacy Policy](https://policies.google.com/privacy)
- [How Google uses information from sites or apps that use our services](https://policies.google.com/technologies/partner-sites)

### Your controls

- **App Tracking Transparency.** On first use, iOS asks whether College Buddy may track you across other companies' apps and websites. If you decline, the advertising identifier is not available for tracking. You can change this any time in **iPhone Settings → Privacy & Security → Tracking**.
- **EEA, UK and Switzerland.** Before any ad is requested, we show a Google-certified consent message that lets you consent or refuse. You can withdraw consent at any time via the privacy options in the App.
- **Remove ads entirely.** Upgrading to Pro removes all advertising permanently.

---

## 4. Live Activity Push Notifications (our server)

To make a class Live Activity appear on your lock screen at the moment a class begins, the App communicates with a small server we operate (a Cloudflare Worker at `college-buddy-push.raaghavmehta.workers.dev`).

**What is sent**, each time you open the App:

- An **Apple push token** for Live Activities (a random device-scoped identifier issued by Apple)
- Your **upcoming classes for the next 7 days** — subject name, subject colour, start time, end time
- Your **time zone** and the App's bundle identifier

**What is *not* sent:** your name, email, any account identifier, your attendance percentages, your present/absent history, your assignments, your planner tasks, or your notes.

This information exists solely so the server knows *when* to send a push. Each upload replaces the previous one entirely, so if you delete classes or use **Reset Semester**, the server's copy is cleared on your next app open. The push token is issued by Apple, is specific to your installation, and becomes invalid if you delete the App.

Local class reminders (§5) do not involve this server at all.

---

## 5. Notifications

If you enable class reminders or attendance alerts, the App schedules **local notifications** on your device using Apple's `UserNotifications` framework. These are generated and delivered entirely by your iPhone — no server is involved.

Lock-screen **Live Activities** may additionally be delivered by push, as described in §4.

You can disable notifications at any time via **iPhone Settings → Notifications → College Buddy**, or inside the App under **Settings**.

---

## 6. iCloud Sync

Your **subjects, timetable, assignments, attendance history, and planner tasks** sync between your own Apple devices using Apple's iCloud key-value storage (`NSUbiquitousKeyValueStore`).

This data goes to **your private iCloud account**, not to us. We have no ability to read, access, or recover it. It is governed by [Apple's Privacy Policy](https://www.apple.com/legal/privacy/). You can disable it in **iPhone Settings → your name → iCloud**.

---

## 7. Timetable Scanner (Camera and Photos)

The Pro timetable scanner reads a printed timetable from your camera, photo library, or a PDF. **All text recognition happens on your device** using Apple's on-device Vision framework. The image and the recognised text are never uploaded to us or to any third party. The photo is discarded once you finish the import.

---

## 8. Widgets and Apple Watch

Home-screen widgets and the Apple Watch app read your subjects and timetable from the App Group container on your device. This code runs locally and transmits nothing.

---

## 9. Subscriptions and In-App Purchases

College Buddy offers optional Pro subscriptions and a one-time Lifetime unlock through Apple's StoreKit framework. When you make a purchase:

- **Apple** processes the transaction. You enter your Apple ID and payment details into Apple's interface, not ours.
- **We receive only** a verified receipt from Apple confirming whether you have an active subscription. It contains no name, email, payment details, or Apple ID.
- The receipt is used solely to unlock Pro features and to switch off advertising.

To manage or cancel, go to **iPhone Settings → tap your name → Subscriptions → College Buddy**. For refunds, visit [reportaproblem.apple.com](https://reportaproblem.apple.com).

---

## 10. Third-Party Services

College Buddy integrates:

| Service | Purpose | Privacy policy |
|---|---|---|
| **Google AdMob** (Google Mobile Ads SDK) | Advertising for free users | [policies.google.com/privacy](https://policies.google.com/privacy) |
| **Google User Messaging Platform** | GDPR consent collection in the EEA/UK/Switzerland | [policies.google.com/privacy](https://policies.google.com/privacy) |
| **Apple StoreKit** | Subscriptions and purchases | [apple.com/legal/privacy](https://www.apple.com/legal/privacy/) |
| **Apple iCloud** | Sync across your own devices | [apple.com/legal/privacy](https://www.apple.com/legal/privacy/) |
| **Apple Push Notification service + our Cloudflare Worker** | Lock-screen Live Activities | [cloudflare.com/privacypolicy](https://www.cloudflare.com/privacypolicy/) |

We do not integrate Firebase, Facebook, Mixpanel, AppsFlyer, Adjust, or any other analytics or attribution SDK.

---

## 11. Children's Privacy

College Buddy is intended for college and university students. It is not directed at children under 13, and we do not knowingly collect personal information from them.

Because the free version shows advertising that may use the advertising identifier, we recommend the App be used by those aged 13 and over (16 in some EEA countries). If you believe a child has used the App and you would like its data removed, deleting the App removes everything stored on the device; you may also contact us at the address below.

---

## 12. Data Security

Data on your device is protected by Apple's iOS security model — device passcode, Face ID / Touch ID, and full-disk encryption. Data in transit to our push server and to Google is encrypted using HTTPS/TLS. We recommend keeping your iPhone updated.

---

## 13. Your Rights

If you are in the EU, UK, California, or another jurisdiction with data protection law, you have rights of access, rectification, erasure, restriction, and objection.

Because we hold almost nothing about you, most of these you can exercise yourself:

- **Access / rectify** — your data is on your device and in your own iCloud; you can view and edit it directly in the App.
- **Erase** — use **Settings → Reset Semester**, or uninstall the App. This also clears your class times from our push server on next launch. To remove them immediately, delete the App.
- **Object to advertising** — decline the App Tracking Transparency prompt, refuse consent in the EEA/UK/Switzerland message, or upgrade to Pro to remove ads entirely.
- **Google-held ad data** — because Google is an independent controller of the advertising data described in §3, requests about that data should be directed to Google using the links in that section.

For anything else, contact us below and we will respond within 7 days.

---

## 14. Changes to This Policy

If we change how the App handles data, we will update this Policy and the "Last updated" date. For material changes we will display a notice inside the App.

---

## 15. Contact

For privacy questions or concerns, email:

raaghav.mehta.36@gmail.com

We'll respond within 7 days.

---

*College Buddy is developed and operated by Raaghav Mehta, Sirsa, Haryana, India.*
