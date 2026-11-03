# Privacy Policy for Musafir (مسافر)

**Effective Date:** November 3, 2026  
**Last Updated:** November 3, 2026  
**Developer:** Mohammed Raees Mackdoom  
**Contact:** [mackdoom.dev@gmail.com](mailto:mackdoom.dev@gmail.com)

---

## 1. Overview
**Musafir (مسافر)** is an Android mobile application created by **Mohammed Raees Mackdoom** to serve the Muslim community as a comprehensive daily companion and prayer automation tool. The primary feature of the app is to automatically mute/silence the device when entering a masjid during congregational prayer times and restore the normal ringtone volume upon leaving.

The app also provides:
- Live Masjid Prayer & Jamaat schedules sourced from `masjidboardlive.com`
- 16-Line and 12-Line Holy Quran reader with customizable bookmarks and Khatmah tracker
- Salaah Streak & Qadha counter with ongoing prayer check notifications
- Digital Tasbeeh Counter with haptic feedback
- Qibla Compass Finder
- Nearby Halaal Restaurants directory

---

## 2. Sensitive Permissions & Purpose (Google Play Disclosures)

To perform automatic silencing without requiring you to manually remember to silence your phone, the application requests specific Android permissions:

| Android Permission | Purpose & Benefit |
| :--- | :--- |
| `ACCESS_FINE_LOCATION` & `ACCESS_COARSE_LOCATION` | Determines proximity to selected masjids and calculates Qibla direction relative to True North. |
| `ACCESS_BACKGROUND_LOCATION` | Enables geofences to detect when you enter or leave a masjid while your device is locked in your pocket. **Only active during prayer windows.** |
| `ACCESS_NOTIFICATION_POLICY` | Manages Do Not Disturb (DND) / Ringer state to toggle between Silent/Vibrate and Normal ringtone volume. |
| `POST_NOTIFICATIONS` | Displays active silencing status, Friday Al-Kahf reminders, and prayer check notifications (Yes/No response for Salaah streak and Qadha tracking). |
| `SCHEDULE_EXACT_ALARM` | Optimizes battery life by keeping location monitoring dormant outside prayer windows. |
| `RECEIVE_BOOT_COMPLETED` | Re-registers your geofences and prayer alarms when your phone restarts. |
| `FOREGROUND_SERVICE` & `FOREGROUND_SERVICE_LOCATION` | Performs a brief 1-minute high-accuracy verification upon entering a boundary to avoid false triggers while driving past. |

### 🔒 Background Location Transparency
- **No Location Tracking:** We do **NOT** track, record, or upload your coordinates.
- **On-Device Geofencing:** Your coordinates are processed entirely by Android's internal `GeofencingClient` on your physical device. No remote servers ever receive your location.
- **Battery-Saving Windows:** Geofences are only scheduled around active prayer times (e.g., 15 minutes before Jamaat until 30 minutes after). Outside these windows, location monitoring is idle.

---

## 3. Third-Party Services
The application accesses external APIs solely to fetch publicly available data requested by the user:
- **MasjidBoardLive (masjidboardlive.com):** Fetches public daily prayer & Jamaat timetables for supported masjids. No personal information is transmitted.
- **OpenStreetMap / Overpass API:** Searches for public masjid locations or halaal restaurants near a queried location.

---

## 4. Data Storage & Security
- All user configurations, custom masjids, Qadha tallies, Salaah streaks, bookmarks, and Tasbeeh counts are stored locally in private application sandbox storage (`SharedPreferences`).
- No personal user data is ever sold, leased, or transmitted to any third party.

---

## 5. Data Deletion
Users have total control over their data:
- You can edit, clear, or reset any counter, streak, or monitored masjid directly in the app.
- You can revoke permissions anytime via Android *Settings > Apps > Musafir > Permissions*.
- Clearing App Storage or uninstalling the app permanently purges all saved data from your device.

---

## 6. Contact Information
For questions or support regarding this Privacy Policy:
- **Developer:** Mohammed Raees Mackdoom
- **Email:** [mackdoom.dev@gmail.com](mailto:mackdoom.dev@gmail.com)
- **GitHub:** [https://github.com/musafirapp](https://github.com/musafirapp)
