# Privacy Policy — TaptiRaksha (ताप्ती रक्षा)

**Version:** 1.1  
**Effective Date:** October 14, 2026  
**Developer:** Shrikrishna Sunildatta Narvekar (operating publicly as Shrikrishna S Narvekar)  
**Contact Email:** `narvekarshrikrishna@gmail.com`  
**Application Name:** TaptiRaksha (ताप्ती रक्षा)  
**Package Name:** `com.taptiraksha.app`  
**Official Hosted URL:** [https://narvekarshrikrishna-wq.github.io/TapRaksha/privacy/](https://narvekarshrikrishna-wq.github.io/TapRaksha/privacy/)  

---

> [!IMPORTANT]
> **Government Independence Disclaimer:**  
> TaptiRaksha is an independent life-safety application developed by **Shrikrishna S Narvekar**. It is **not** a government-issued application and is **not affiliated with, authorized by, or endorsed by** the Government of India, India Meteorological Department (IMD), National Disaster Management Authority (NDMA), SACHET (NDMA), or the Central Pollution Control Board (CPCB). All meteorological and environmental figures are derived from public data endpoints and open biometeorological algorithms.

---

## 1. Executive Summary

* **No User Accounts:** There is no registration, login, phone number verification, or server-side account profile.
* **Zero Advertisements:** The application contains no advertising SDKs, ad trackers, or banner networks.
* **Zero Commercial Telemetry:** No analytics SDKs (such as Firebase Analytics, Mixpanel, or Adjust), no third-party crash reporters (such as Firebase Crashlytics or Sentry), and no tracking pixels or advertising IDs.
* **100% On-Device Personal Health Data:** Your age, occupation, health profile, medications, optional reproductive health status, hydration logs, and checklist ticks are stored **exclusively** on your device in private, sandboxed local storage (`AppDatabase` Room database and encrypted DataStore). They are **never transmitted** off your device to any server.

---

## 2. Information Stored Locally on Your Device

The following personal inputs are processed and stored solely in sandboxed app storage on your device (`android:allowBackup="false"`):

1. **Selected District:** Preferred work or home district (chosen from 700+ offline Indian districts).
2. **Age Band:** Age bracket (e.g., <18, 18–44, 45–64, 65+ years) used exclusively to calibrate physiological heat-stress thresholds on-device.
3. **Occupation & Work Details:** Work intensity cohort (outdoor agricultural/construction, delivery/transport, indoor shaded, etc.), work shift timings, and split-shift preferences.
4. **Health Conditions:** Self-declared categories including cardiovascular disease, chronic kidney disease (CKD), diabetes, hypertension, and respiratory flags.
5. **Medicine Categories:** Anticholinergics, diuretics, antihypertensives, and psychiatric medications (used solely to adjust hydration rate and dehydration risk models locally).
6. **Optional Sex Option:** Female / Male / Other.
7. **Optional Body Build:** Small, Medium, Heavy (used to calibrate estimated body surface area heat-exchange rates).
8. **Optional Reproductive Status:** Pregnancy trimester, breastfeeding status, and active period (menstruation) status.
9. **Indoor Heat Check:** User observations regarding indoor heat retention and ventilation.
10. **Hydration & Shade Logs:** Water intake timestamps, shade break records, and reminder interval settings.
11. **Checklist & Alert History:** Next 4 hours "Be Ready" checklist items marked as packed, dismissed alerts, and advisory acknowledgements.
12. **Cached Environmental Data:** Locally cached weather forecasts, AQI observations, and alert bulletins to enable complete offline functionality during network outages.
13. **Appearance Settings:** Theme selection (Light/Dark/System), font scaling, and animation speed preferences.

---

## 3. Information Transmitted Off Your Device

To provide accurate heat-stress forecasts and air-quality monitoring, the application communicates over encrypted HTTPS only when network connectivity is available:

* **Approximate District Center Coordinates:** Sent via HTTPS to **Open-Meteo GmbH** (`api.open-meteo.com`) to retrieve hourly meteorological forecasts (temperature, relative humidity, dew point, solar radiation, and wind speed). Device GPS coordinates are never transmitted; only pre-calculated district center or coarse user-approved coordinates are sent.
* **District, State, or Station Identifiers:** Sent to public environmental endpoints (Central Pollution Control Board / public data gateways) to fetch ambient AQI.
* **Standard Network Metadata:** Standard HTTPS headers (such as IP address) processed ephemerally by server gateways to complete network transmission.

> [!NOTE]
> **Strict Isolation Guarantee:**  
> Your profile answers, age, occupation, health conditions, medicine categories, pregnancy, breastfeeding, period status, packed checklist, and first-aid interactions are **never sent to any server**.

---

## 4. Permissions Requested & System Usage

TaptiRaksha requests only standard, Play-compliant permissions strictly necessary to operate offline-first:

| Permission | Type | Justification / Technical Usage |
|:---|:---|:---|
| `INTERNET` | Install-time | Fetch meteorological, alert, and air quality data over secure HTTPS. |
| `ACCESS_NETWORK_STATE` | Install-time | Detect network connectivity to dynamically switch between `LIVE` and `CACHED` status badges. |
| `ACCESS_COARSE_LOCATION` | Optional runtime | Determine the approximate district when the user taps "Find my district". Never requested in the background. Manual district selection works 100% offline without granting location permission. |
| `POST_NOTIFICATIONS` | Optional runtime (Android 13+) | Deliver optional hydration reminders, rest-break prompts, and severe heat screening alerts. |
| `VIBRATE` | Install-time | Provide tactile feedback for emergency alerts on supported devices. |
| `WAKE_LOCK` | Install-time (Standard Library) | Merged automatically by AndroidX WorkManager to ensure scheduled hydration reminder tasks complete execution without premature termination. |
| `RECEIVE_BOOT_COMPLETED` | Install-time (Standard Library) | Merged automatically by AndroidX WorkManager to reschedule background hydration reminders after device restart. |

### Prohibited Permissions
TaptiRaksha **does not declare or use**:
- Precise location (`ACCESS_FINE_LOCATION`)
- Background location (`ACCESS_BACKGROUND_LOCATION`)
- Automated calling (`CALL_PHONE` or `ACTION_CALL`)
- Exact alarms (`SCHEDULE_EXACT_ALARM` or `USE_EXACT_ALARM`)
- Full-screen intents (`USE_FULL_SCREEN_INTENT`)
- Notification policy access (`ACCESS_NOTIFICATION_POLICY`)
- Battery optimization whitelist bypass (`REQUEST_IGNORE_BATTERY_OPTIMIZATIONS`)
- Camera, microphone, contacts, SMS, or external storage access

---

## 5. Notification Privacy & Safeguards

* **User Control:** All notifications are entirely optional and can be toggled in app Settings or Android system settings.
* **Standard Battery-Friendly Scheduling:** Water and shade reminders utilize standard Android `WorkManager` approximate timing. They do not use exact alarms and do not bypass device battery optimizations.
* **Respect for System Audio & DND:** Heat alerts respect device volume and Do Not Disturb (DND) modes.
* **Sensitive Privacy Invariant:** Notifications **never** mention or display personal medical or reproductive details (e.g., pregnancy, period, medicines, diabetes, or kidney disease). Forecast alerts and hydration reminders use strictly generic, public-safety phrasing.

---

## 6. Data Retention, Auto-Expiry & Deletion

* **User-Initiated Purge:**
  - **Profile → "Clear my answers":** Instantly and permanently wipes all profile answers (age, occupation, health conditions, medicines, reproductive status) from the device's Room database.
  - **Settings → "Clear cached data":** Purges cached weather forecasts, AQI observations, and alert history.
* **Automatic Expiry:** Active period (menstruation) status automatically expires on-device after the configured duration (1 to 7 days) via timestamp comparison.
* **App Uninstallation:** Completely and permanently removes all sandboxed Room databases, DataStore preferences, and cache files from the user's device.

---

## 7. Children's Privacy

TaptiRaksha is designed for the general working population and does not knowingly collect, transmit, or request any personally identifiable information from children under the age of 13 (or applicable local age threshold). If an age band under 18 is selected in the personal profile, that choice is stored 100% locally on the device solely to adapt occupational heat-safety and hydration guidance. If a parent or guardian wishes to clear any locally saved information, tapping *Profile → Clear my answers* or uninstalling the app permanently purges all stored inputs immediately.

---

## 8. Emergency Services & Dialer Protocol

TaptiRaksha provides quick-access buttons for Indian emergency helplines:
* **112:** National Unified Emergency Response Support System (Police, Fire, Medical)
* **108:** Emergency Medical Ambulance Services
* **102:** Free Janani Shishu Suraksha Karyakram (JSSK) ambulance service where available for pregnancy-related emergencies

**Security Guarantee:**  
All emergency buttons use standard Android `Intent.ACTION_DIAL`. The application opens the system dialer with the number pre-filled. **The application never places phone calls automatically and never transmits user location automatically.**

---

## 9. Medical & Clinical Disclaimer

> [!WARNING]
> **Not a Medical Device:**  
> TaptiRaksha is not a certified medical device and does not diagnose, treat, cure, or prevent any medical condition or illness. It provides general heat-stress guidance calculated using published biometeorological algorithms.  
> **Never** discontinue or alter prescribed medications or physician-directed fluid restriction limits based on app recommendations. Always consult a qualified medical practitioner, pharmacist, ASHA/ANM health worker, or employer safety officer for individualized clinical advice.

---

## 10. Data Sources & Third-Party Attribution

* **Numerical Weather Prediction:** Open-Meteo GmbH ([open-meteo.com](https://open-meteo.com/)) under Creative Commons Attribution 4.0 International (CC BY 4.0).
* **Ambient Air Quality Data:** Central Pollution Control Board (CPCB) ground Continuous Ambient Air Quality Monitoring Stations (CAAQMS) and public government data portals.
* **Heat Wave & Disaster Protocols:** India Meteorological Department (IMD) thresholds, National Disaster Management Authority (NDMA) Heat Action Plan guidelines, and National Centre for Disease Control (NCDC) / NPCCHH clinical guidelines.

---

## 11. Developer Contact & Public Verification

For privacy inquiries, security audits, or compliance questions:

* **Developer:** Shrikrishna Sunildatta Narvekar (operating publicly as Shrikrishna S Narvekar)
* **Contact Email:** `narvekarshrikrishna@gmail.com`
* **Application:** TaptiRaksha (ताप्ती रक्षा)
* **Package Name:** `com.taptiraksha.app`
* **Public GitHub Repository:** [https://github.com/narvekarshrikrishna-wq/TapRaksha](https://github.com/narvekarshrikrishna-wq/TapRaksha)
* **Hosted Privacy Policy:** [https://narvekarshrikrishna-wq.github.io/TapRaksha/privacy/](https://narvekarshrikrishna-wq.github.io/TapRaksha/privacy/)
