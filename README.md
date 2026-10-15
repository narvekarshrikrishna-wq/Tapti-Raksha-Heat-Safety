# Tapti-Raksha-Heat-Safety
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Privacy Policy — TaptiRaksha</title>
  <style>
    :root {
      --bg: #ffffff;
      --text: #1a1a1a;
      --card-bg: #f8f9fa;
      --border: #e5e7eb;
      --primary: #c2410c;
      --accent: #0369a1;
      --alert-bg: #fef2f2;
      --alert-border: #ef4444;
      --info-bg: #f0fdf4;
      --info-border: #22c55e;
    }
    @media (prefers-color-scheme: dark) {
      :root {
        --bg: #121212;
        --text: #e5e5e5;
        --card-bg: #1e1e1e;
        --border: #333333;
        --primary: #fb923c;
        --accent: #38bdf8;
        --alert-bg: #2d1515;
        --alert-border: #ef4444;
        --info-bg: #142a1b;
        --info-border: #22c55e;
      }
    }
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      line-height: 1.6;
      color: var(--text);
      background-color: var(--bg);
      margin: 0;
      padding: 16px;
    }
    .container {
      max-width: 820px;
      margin: 0 auto;
      padding: 16px 0;
    }
    header {
      border-bottom: 2px solid var(--border);
      padding-bottom: 16px;
      margin-bottom: 24px;
    }
    h1 {
      font-size: 1.85rem;
      margin: 0 0 8px 0;
      color: var(--primary);
    }
    .meta {
      font-size: 0.95rem;
      color: #6b7280;
    }
    h2 {
      font-size: 1.35rem;
      margin-top: 32px;
      margin-bottom: 12px;
      color: var(--accent);
      border-bottom: 1px solid var(--border);
      padding-bottom: 6px;
    }
    p, li {
      font-size: 1rem;
    }
    ul {
      padding-left: 24px;
    }
    li {
      margin-bottom: 8px;
    }
    .box {
      background-color: var(--card-bg);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 16px;
      margin: 16px 0;
    }
    .alert-box {
      background-color: var(--alert-bg);
      border-left: 4px solid var(--alert-border);
      padding: 14px 16px;
      margin: 16px 0;
      border-radius: 4px;
    }
    .info-box {
      background-color: var(--info-bg);
      border-left: 4px solid var(--info-border);
      padding: 14px 16px;
      margin: 16px 0;
      border-radius: 4px;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin: 16px 0;
      font-size: 0.95rem;
    }
    th, td {
      border: 1px solid var(--border);
      padding: 10px 12px;
      text-align: left;
    }
    th {
      background-color: var(--card-bg);
      font-weight: 600;
    }
    footer {
      margin-top: 48px;
      padding-top: 20px;
      border-top: 1px solid var(--border);
      font-size: 0.9rem;
      color: #6b7280;
      text-align: center;
    }
    code {
      background: var(--card-bg);
      padding: 2px 6px;
      border-radius: 4px;
      font-size: 0.9em;
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>Privacy Policy — TaptiRaksha</h1>
      <div class="meta">
        <strong>Version:</strong> 1.1<br>
        <strong>Last updated:</strong> October 14, 2026<br>
        <strong>Developer:</strong> Shrikrishna S Narvekar
      </div>
    </header>

    <div class="alert-box">
      <strong>Independence Disclaimer:</strong> TaptiRaksha is an independent project developed by <strong>Shrikrishna S Narvekar</strong>. It is not affiliated with or endorsed by the Government of India, IMD, NDMA, SACHET or CPCB.
    </div>

    <h2>1. Short Version</h2>
    <div class="info-box">
      <strong>No account. No ads. No analytics. No selling data.</strong><br>
      Your health and profile answers stay on your phone.<br>
      The app uses weather, alert and air-quality sources to show heat-safety guidance.
    </div>

    <h2>2. What Stays on Your Phone</h2>
    <p>The following personal data is stored exclusively in your phone's encrypted private local storage (Room database and Android DataStore) and is never transmitted off your device:</p>
    <ul>
      <li><strong>Selected district:</strong> Your preferred work or home district.</li>
      <li><strong>Age band:</strong> E.g., &lt;18, 18–44, 45–64, 65+ years.</li>
      <li><strong>Occupation and work details:</strong> Work intensity cohort, shift timings, split-shift preferences.</li>
      <li><strong>Health condition categories:</strong> Cardiovascular, chronic kidney disease, diabetes, hypertension, respiratory flags.</li>
      <li><strong>Medicine categories:</strong> Anticholinergics, diuretics, antihypertensives, etc.</li>
      <li><strong>Optional sex option:</strong> Female / Male / Other.</li>
      <li><strong>Optional body build:</strong> Build categories affecting heat exchange rate.</li>
      <li><strong>Optional reproductive health status:</strong> Pregnancy trimester, breastfeeding status, period (menstruation) status.</li>
      <li><strong>Optional room heat check:</strong> Indoor heat observations.</li>
      <li><strong>Reminder settings &amp; hydration logs:</strong> Water intake timestamps, shade break records, custom intervals.</li>
      <li><strong>Notification preferences &amp; alert history:</strong> Heat alerts acknowledged or dismissed.</li>
      <li><strong>Packed checklist ticks:</strong> Next 4 hours "Be Ready" checklist items marked as packed.</li>
      <li><strong>Cached weather, AQI, forecast and alert data:</strong> Local copies allowing offline operation.</li>
      <li><strong>Appearance settings:</strong> Dark mode preference, font scale, animation speed controls.</li>
    </ul>

    <h2>3. What Leaves Your Phone</h2>
    <p>Only technical parameters strictly required to fetch weather and air-quality data leave your phone:</p>
    <ul>
      <li><strong>Approximate location or district centre coordinates:</strong> Sent via secure HTTPS to open meteorological services (Open-Meteo) to retrieve temperature, humidity, solar radiation, and wind.</li>
      <li><strong>District, state, or station identifier:</strong> Sent to public environmental endpoints (CPCB / open data) to fetch ambient AQI.</li>
      <li><strong>Standard technical network metadata:</strong> Standard HTTPS network headers (such as IP address) processed ephemerally by server gateways to complete network transmission.</li>
    </ul>
    <div class="alert-box">
      <strong>Zero Sensitive Data Transmission:</strong> Your profile answers, health conditions, medicine categories, pregnancy, breastfeeding, period status, packed checklist and first-aid activity are never sent to any server by TaptiRaksha.
    </div>

    <h2>4. Permissions Table</h2>
    <p>TaptiRaksha requests only the minimum Play-compliant permissions necessary to operate offline-first:</p>
    <table>
      <thead>
        <tr>
          <th>Permission</th>
          <th>Type</th>
          <th>Why It Is Needed</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><code>INTERNET</code></td>
          <td>Install-time</td>
          <td>Fetch weather, alert and AQI data over secure HTTPS.</td>
        </tr>
        <tr>
          <td><code>ACCESS_NETWORK_STATE</code></td>
          <td>Install-time</td>
          <td>Know whether data can be refreshed or whether cached offline data should be displayed.</td>
        </tr>
        <tr>
          <td><code>ACCESS_COARSE_LOCATION</code></td>
          <td>Optional runtime</td>
          <td>Find approximate district when user taps "Find my district". Never requested in background. Manual district selection works 100% offline without location.</td>
        </tr>
        <tr>
          <td><code>POST_NOTIFICATIONS</code></td>
          <td>Optional runtime (Android 13+)</td>
          <td>Deliver optional water/shade reminders and high heat alerts.</td>
        </tr>
        <tr>
          <td><code>VIBRATE</code></td>
          <td>Install-time</td>
          <td>Optional vibration for notifications on supported devices.</td>
        </tr>
        <tr>
          <td><code>WAKE_LOCK</code></td>
          <td>Install-time (Standard Library)</td>
          <td>Merged automatically by AndroidX WorkManager to ensure scheduled hydration tasks complete execution.</td>
        </tr>
        <tr>
          <td><code>RECEIVE_BOOT_COMPLETED</code></td>
          <td>Install-time (Standard Library)</td>
          <td>Merged automatically by AndroidX WorkManager to reschedule background hydration reminders after a device reboot.</td>
        </tr>
      </tbody>
    </table>
    <p>
      TaptiRaksha does not use precise location, camera, microphone, contacts, files, SMS or phone-call permission.<br>
      Emergency buttons open the dialer only and never place calls automatically.
    </p>

    <h2>5. Notifications</h2>
    <ul>
      <li>Notifications are entirely optional and can be toggled in app Settings or Android system settings.</li>
      <li>Water and shade reminders use standard Android WorkManager and are approximate, not exact alarms.</li>
      <li>Heat alerts respect your device's volume and Do Not Disturb (DND) settings; if your phone is on Silent or DND, you may not hear alerts.</li>
      <li><strong>Privacy Guarantee:</strong> Notifications never include pregnancy, period, medicine, or health-condition details. Reminders and forecast alerts use generic safety text only.</li>
    </ul>

    <h2>6. Data Retention and Deletion</h2>
    <p>Your data stays on your phone until you clear it or uninstall the app. You have full control:</p>
    <ul>
      <li><strong>Profile &rarr; Clear my answers:</strong> Erases your age, occupation, health categories, medicines, and reproductive health inputs.</li>
      <li><strong>Settings &rarr; Clear cached data:</strong> Purges cached weather forecasts, AQI observations, and alert history.</li>
      <li><strong>Automatic Expiry:</strong> Period status automatically expires after its active duration (configurable or default 7 days).</li>
      <li><strong>App Uninstall:</strong> Completely removes all local Room database tables and DataStore preferences from your device.</li>
    </ul>

    <h2>7. Children's Privacy</h2>
    <p>TaptiRaksha is designed for the general working population and does not knowingly collect, transmit, or request any personally identifiable information from children under the age of 13 (or applicable local age threshold). If an age band under 18 is selected in the personal profile, that choice is stored 100% locally on the device solely to adapt occupational heat-safety and hydration guidance. If a parent or guardian wishes to clear any locally saved information, tapping <em>Profile &rarr; Clear my answers</em> or uninstalling the app permanently purges all stored inputs immediately.</p>

    <h2>8. Emergency Services &amp; Calling</h2>
    <p>The app provides quick-access emergency buttons for:</p>
    <ul>
      <li><strong>112:</strong> National Emergency Response Support System (Police, Fire, Ambulance).</li>
      <li><strong>108:</strong> Emergency Medical Ambulance Services.</li>
      <li><strong>102:</strong> Free Janani Shishu Suraksha Karyakram (JSSK) ambulance service where available for pregnancy-related emergencies.</li>
    </ul>
    <p>All emergency buttons use standard Android <code>Intent.ACTION_DIAL</code>. The app opens your device dialer with the number pre-filled. The app does not contact emergency services automatically and does not share location automatically.</p>

    <h2>9. Medical Disclaimer</h2>
    <div class="alert-box">
      <strong>Not a Medical Device:</strong> TaptiRaksha is not a medical device and does not diagnose, treat, cure or prevent any illness. It provides general heat-safety guidance.<br><br>
      Do not change prescribed medicines or fluid limits based on the app. Always consult your doctor, pharmacist, ASHA/ANM health worker, or employer safety officer for individualized medical advice.
    </div>

    <h2>10. Data Sources and Attribution</h2>
    <ul>
      <li><strong>Weather Model &amp; Forecast:</strong> Open-Meteo GmbH (<a href="https://open-meteo.com/" target="_blank" rel="noopener">open-meteo.com</a>).</li>
      <li><strong>Ambient AQI:</strong> Central Pollution Control Board (CPCB) monitoring station feeds and verified public gateways.</li>
      <li><strong>Public Disaster Warnings:</strong> IMD / NDMA / SACHET public alert gateways when active.</li>
      <li><strong>Biometeorological &amp; Occupational Protocols:</strong> National Programme on Climate Change and Human Health (NPCCHH / NCDC), National Disaster Management Authority (NDMA) Heat Action Plan guidelines.</li>
    </ul>
    <p>Data source availability can change. The app shows timestamps and source labels so users can judge freshness.</p>

    <h2>11. Contact Details</h2>
    <p>For inquiries, open-source audit questions, or feedback regarding this Privacy Policy:</p>
    <p>
      <strong>Developer:</strong> Shrikrishna Sunildatta Narvekar (operating publicly as Shrikrishna S Narvekar)<br>
      <strong>Email:</strong> <a href="mailto:narvekarshrikrishna@gmail.com">narvekarshrikrishna@gmail.com</a><br>
      <strong>Project:</strong> TaptiRaksha (ताप्ती रक्षा)<br>
      <strong>Hosted Policy URL:</strong> <a href="https://narvekarshrikrishna-wq.github.io/TapRaksha/privacy/" target="_blank" rel="noopener">https://narvekarshrikrishna-wq.github.io/TapRaksha/privacy/</a>
    </p>

    <footer>
      &copy; 2026 Shrikrishna S Narvekar · TaptiRaksha (ताप्ती रक्षा) · Independent Open-Source Heat Safety
    </footer>
  </div>
</body>
</html>
