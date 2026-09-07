# Privacy Policy

*Last updated: September 7, 2026 (Application Version 1.0.28 / Build 29)*

We place fundamental importance on respecting the privacy and protecting the personal data of users of our mobile application **AirTourer**.

This Privacy Policy details how your information is handled, in strict compliance with the General Data Protection Regulation (GDPR - Regulation EU 2016/679), the European Artificial Intelligence Act (AI Act - Regulation EU 2024/1689), as well as privacy and security guidelines established by the **Apple App Store** and **Google Play Store**.

---

## 1. Data Controller

Personal data processing within the scope of the application is operated under the responsibility of:

- **Publisher / Developer**: `AirTourer`
- **Location**: `Lille, France`
- **Official Contact Email / DPO**: `airtourer.app@gmail.com`
- **Official Website**: [https://riff4.github.io](https://riff4.github.io)

---

## 2. Geolocation Data Processing & Ephemeral Server Requests

Access to your device's geographical position is governed by strict, transparent technical and legal privacy safeguards:

- **Real-Time Local Processing (Device RAM)**: Continuous tracking of your position (displaying your location pin on the interactive map, real-time distance calculations for step-by-step guidance and thematic tours, heading compass) is performed exclusively in your smartphone's random access memory (RAM).
- **Ephemeral Search Queries (HTTPS / TLS)**: When you search for points of interest (POIs) nearby, pan or zoom the map, or explore stages of a curated tour, the geographic coordinates of the center of the viewed area and the search radius are transmitted ephemerally over a secure, encrypted connection (HTTPS / TLS) to our hosted database (**Supabase / PostgreSQL PostGIS**). This transmission's sole purpose is to query the spatial index to return the corresponding list of heritage monuments and audioguides.
- **Zero Storage / Zero History / Immediate Purge**: These coordinates are **NEVER stored on disk or in the database**, never written to log files, never linked to any user profile or identifier (no user account exists in the application), and never sold or shared with third parties. As soon as the SQL query completes and results are returned to the client, coordinates are immediately purged from server memory. This processing strictly qualifies as **Ephemeral Processing** under the Google Play Data Safety specifications.
- **No Background Location Tracking**: The application does not request and does not use background location permissions (`ACCESS_BACKGROUND_LOCATION`). As soon as the application is minimized or closed, all GPS signal polling ceases immediately.
- **User Control & Choice**: You may grant or decline location access upon opening the app or at any time in your device's operating system settings. Declining location permissions does not prevent browsing POI details, exploring guided tours, or listening to unlocked audio guides.

---

## 3. Zero-Account Model & Secure Local Storage (SecureStore)

AirTourer applies a strict *Privacy by Design* principle:

- **No Sign-up / No Account Required**: No user account, email address, password, or profile creation is ever requested to access the application's features.
- **Local Encrypted Storage (SecureStore)**: Necessary application state data is stored exclusively on your device within encrypted local storage (*SecureStore*). This includes:
  - Your remaining free audio listening credits / token balance;
  - Identifiers (IDs) of unlocked points of interest;
  - Unlocked exploration badges and milestones (e.g., 50, 88, 300 explored POIs);
  - Your interface and audio language preferences (French / English).
- This data remains strictly stored on your physical device and is never transmitted to remote servers.

---

## 4. AI Transparency & User Feedback (EU AI Act 2024/1689)

In compliance with the European Artificial Intelligence Act (Regulation EU 2024/1689):

- **No Training on User Data**: No personal data, location data, or listening history is ever used, shared, or sold to train or fine-tune third-party artificial intelligence models.
- **Error & Feedback Reporting (POI Feedback)**: When reporting a historical inaccuracy or audio issue via the report button on a place's card, only the information strictly necessary to review the issue (POI ID and user-provided description text) is transmitted. This reporting is handled anonymously, without collecting any personal identifying information.

---

## 5. Advertising, Consent Management & `app-ads.txt` (Google AdMob & Google UMP)

The application provides a non-intrusive monetization model based on rewarded video ads:

- **AdMob Rewarded Video Ads**: Users can choose to watch an optional short rewarded video ad provided by Google AdMob to receive **5 free audio credits** per completed video.
- **Official Advertising Transparency (`app-ads.txt`)**: This website hosts the official [app-ads.txt](https://riff4.github.io/app-ads.txt) file complying with IAB standards to transparently verify the application's advertising inventory.
- **GDPR Consent via Google UMP (CMP)**: For users located in the European Union (EU), United Kingdom (UK), and European Economic Area (EEA), consent is gathered and managed via the **Google User Messaging Platform (UMP)**, an IAB TCF-certified Consent Management Platform (CMP).
- **Review or Revoke Consent Anytime**: You can review, modify, or revoke your advertising consent preferences at any time directly within the application via the **"Settings" (Paramètres)** screen.

---

## 6. Background Audio Playback (Foreground Service)

- **`FOREGROUND_SERVICE_MEDIA_PLAYBACK` Permission**: The application uses this Android permission strictly for media playback.
- **Purpose**: To allow users to continue listening to cultural audio guides while their device screen is locked/turned off or while the application is minimized during a walk or tour.
- This foreground service performs no GPS tracking, no audio recording, and no background personal data collection.

---

## 7. Data Recipients & Processors

Your personal data is **never sold, leased, or transferred** to third parties for marketing or commercial purposes.

Technical service providers involved in operating the service are:
- **Supabase Inc.**: For hosting the PostgreSQL / PostGIS database that stores the POI catalog and guided tours, and ephemerally processes spatial search queries via HTTPS/TLS.
- **Google Ireland Limited**: For delivering rewarded video advertisements (Google AdMob) and managing regulatory consent (Google UMP CMP).
- **GitHub Pages (GitHub, Inc.)**: For hosting the static legal information website and the `app-ads.txt` file.

---

## 8. Data Retention Periods

- **Geolocation coordinates & POI search queries**: **0 seconds** (ephemeral real-time processing in volatile RAM on the smartphone and transient RAM execution on the PostgreSQL server during the query only; no storage on disk, no logs, no history).
- **Local Application Data (SecureStore)**: Retained on your physical device until you reset application data or uninstall the application.

---

## 9. Your Rights (GDPR Compliance)

Under European data protection regulations (GDPR - Regulation EU 2016/679), you hold the following rights:

- **Right of access and information** (Art. 15 GDPR): To know how your data is handled.
- **Right to erasure** (Art. 17 GDPR): To permanently delete your local data by resetting the app or uninstalling it from your device.
- **Right to withdraw consent** (Art. 21 GDPR): To adjust GPS location permissions in your device settings and advertising consent choices in the in-app Settings screen.

### Exercising Your Rights
For any questions or requests regarding your privacy:  
👉 **`airtourer.app@gmail.com`**

Maximum legal response time: **30 days**.

If you believe your rights have not been respected, you may file a complaint with the competent supervisory authority:  
**CNIL (Commission Nationale de l'Informatique et des Libertés - France)**  
Website: [https://www.cnil.fr](https://www.cnil.fr)

---

## 10. Store Compliance (Apple App Store & Google Play Store)

This Privacy Policy fully complies with major application store guidelines:
- **Apple App Store Privacy Guidelines**: Transparent live GPS usage without IDFA tracking, no user profiling, strict adherence to user privacy.
- **Google Play User Data Policy**: Clear disclosure of ephemeral location processing (*Ephemeral Processing* without persistent logging or disk storage in the Data Safety section), disclosure of the *Foreground Service Media Playback* permission, Google UMP / CMP compliance for ads, transparent AI-assisted content disclosure, and no background location permission (`ACCESS_BACKGROUND_LOCATION` not requested).

---

## 11. Changes to This Privacy Policy

We reserve the right to update this Privacy Policy as our services evolve or to maintain compliance with legal requirements. The latest revision date at the top of this document will be updated accordingly.
