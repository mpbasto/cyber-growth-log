# 🦈 Wireshark

---

### 🔍 **Use Cases**

Wireshark is a powerful traffic analysis tool used for:

* **Troubleshooting network issues** (e.g., load failures, congestion).
* **Detecting security anomalies** (e.g., rogue hosts, strange ports, suspicious traffic).
* **Learning protocol details** (e.g., response codes, payloads).

> ⚠️ *Note:* Wireshark is **not** an Intrusion Detection System (IDS); it doesn't modify packets — just reads them. Analysis depends heavily on user skill.

---

### 🖥️ **Interface Overview**

Wireshark’s GUI includes five main sections:

1. **Toolbar** – Quick access to actions like filtering, sorting, exporting.
2. **Display Filter Bar** – Where users enter filter queries.
3. **Recent Files** – Easy access to previously viewed files.
4. **Capture Filters & Interfaces** – Defines what to capture and from which interface (e.g., eth0, lo).
5. **Status Bar** – Shows current profile, tool status, and packet counts.

---

### 📂 **Loading PCAP Files**

PCAP files (packet captures) can be loaded by:

* File menu
* Drag & drop file
* Double-clicking file

Once loaded, the screen displays:

* **Packet List Pane** – Overview of packets (source, destination, protocol, info).
* **Packet Details Pane** – In-depth breakdown of the selected packet.
* **Packet Bytes Pane** – Hex and ASCII view of the packet contents.

---

### 🎨 **Packet Colouring**

Wireshark uses colours to help spot anomalies or specific protocols:

* **Temporary colouring** – For current session only (via right-click or View → Conversation Filter).
* **Permanent colouring** – Saved to profile, persistent across sessions (set via View → Coloring Rules).
* You can customise colour rules using display filters.

---

### 📡 **Traffic Sniffing**

* **Blue shark icon** – Start capture
* **Red square** – Stop capture
* **Green arrow** – Restart capture
* Status bar shows interface and packet count.

---

### 🔗 **Merging PCAP Files**

* Merge multiple PCAPs via **File → Merge**
* Must save the new merged file before working with it.

---

### 🗂️ **Viewing File Details**

Helpful when working with multiple captures:

* View file info via **Statistics → Capture File Properties** or click the **PCAP icon** in the bottom left.
* Shows metadata like capture time, file hash, and interface details.
