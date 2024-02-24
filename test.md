## Style Sheet Test Page
> **First Published:** *2024-01-26,* **Revised:** *2024-02-23 (v1.0.5) See Appendix A*<br>&copy;**Copyright:** ***2024 Thomas R Schmidt, Wildwood IL USA***

#### Table Testing

| Type | Model | Firmware | Web Version | Purchased |
| ---- | ----- | -------- | ----------- | --------- |
| Outdoor Mini-Dome (4) | DS-2CD-2543-G0-IS | v5.5.61 b180718<br>v5.6.820 b220519<br>v5.6.821 b230831 | v4.0.1 b180626<br>v4.0.1 b220610 | 3 in 2018<br>1 in 2023 |
| Indoor Cube w/PIR | DS-2CD-2422-FWD-IW | v5.5.0 b170725 | v4.0.1 b170711 | 2018  |
| Outdoor PTZ Mini-Dome | DS-2DE-3404-W-DE | v5.7.4 b221130<br>v5.8.1 b231108 | v4.0.1 b220121 | 2024 |
| NVR | DS-7604-NI-Q1 | v4.32.110 b211009 | v4.0.1 b210914 | 2024 |

---

| Date | Version | Code Changes | Doc Changes |
| ---- | ------- | ------------ | ----------- |
| 2024-01-26 | 1.0.0 | First Published - First Release | |
| 2024-02-05 | 1.0.1 | Remove Ping and use GET timeout errors for online state of Camera<br>Test first ever HE driver update using HPM | |
| 2024-02-06 | 1.0.2 | Add link to User Guide on device driver page, courtesy of jtp10181 | |
| 2024-02-07 | 1.0.3 | Remove link to UG from top of driver page due to<br>overlay issue when viewing device on a phone.<br>Minor debug logging improvements. | |
| 2024-02-13 | 1.0.3 | New web site design implemented |
| 2024-02-22 | 1.0.4 | **Report:** GET Error 405 - Method Not Allowed<br>**Fix:** Update old Hikvision IPMD url paths to ISAPI paths.<br>- Affected features: Basic Motion, Alarm Out trigger, IO Status.<br>- Required to support newer cameras. May break older cams. | |
| 2024-02-23 | 1.0.5 | **Report:** NullPointerException: Cannot invoke method toUpperCase()<br>**Fix:**Check for null camera name and set to default value before using | |
| 2024-02-23 | 1.0.5 | **Change:** Alarm Server: Log "Unknown" events for reporting to tr-systems. | Camera Configuation<br>Resources for Development |

---

End of Document
