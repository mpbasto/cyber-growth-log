# 🧠 TryHackMe: Networking > Wireshark: The Basics

📅 Date: 2025-08-06
📍 Modules Covered:

- Packet Dissection
- Packet Navigation
- Packet Filtering

---

## 🛠️ What I Worked On/ Learned

- Dissecting a packet means breaking down its details by decoding each protocol and its fields. Wireshark uses the OSI model layers to organise packet info
- Wireshark assigns a unique number to each packet in a capture to help navigating, referencing and tracking events within large packet sets
- Default time format: "Seconds Since Capture Start". You can switch to UTC format via **View → Time Display Format** for clearer event correlation.
- Two main types of filters: Capture (applied before packet collection to limit what is captured) and Display (applied after capture to control what's shown from already captured data)
- Golden rule: _“If you can click on it, you can filter and copy it."_

### Expert Info

Wireshark highlights potential issues based on packet behavior.

Categories have different severities:

- Chat (Blue) – Informational

- Note (Cyan) – Notable events

- Warn (Yellow) – Warnings

- Error (Red) – Serious issues

Common Expert Info Groups:

| Group          | Info                        |
| -------------- | --------------------------- |
| **Checksum**   | Errors in checksum.         |
| **Malformed**  | Malformed packets           |
| **Deprecated** | Use of outdated protocols   |
| **Comment**    | Presence of packet comments |

Access via bottom status bar or **Analyze → Expert Information**.

---

## ⚠️ What I Struggled With

- Understanding the use of `chmod` and how the number system works (`755`, `644`, etc).
- The difference between **absolute** and **relative** paths tripped me up occasionally.

---

## ✅ Wins, Surprises, and Next Steps

### 🎉 Wins

- Using Expert Information view to better understand a capture.

### 🤯 Surprises

- Exporting files that have been transferred through the wire is easier than I thought through Wireshark.
