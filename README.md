# ReFS Research 🚀

A deep dive into **ReFS** – Microsoft's **Resilient File System**, designed to overcome the limits of traditional file systems. Built with **data integrity** and **scalability** in mind, ReFS is about handling **large datasets**, protecting against **corruption**, and ensuring **reliability** in the toughest environments.

---

## What makes ReFS different?

- **Resilience**: Protects against data corruption with built-in integrity streams and self-healing.
- **Scalability**: Supports volumes up to **35 PB** (yes, petabytes) and handles **millions of files** with ease.
- **Performance**: Optimized for **large-scale data** environments – no compromises on speed or efficiency.
- **No Downtime**: Works with **Storage Spaces** for continuous availability, even in the event of hardware failure.

---

## Why ReFS could be the future of file systems ⚡

ReFS is more than just another file system – it's designed for the demands of **cloud storage**, **big data**, and **high-performance workloads**. As we move towards an era where data is measured in **petabytes** and uptime is non-negotiable, ReFS could be the foundation for **next-gen infrastructures**:

- **Cloud-Ready**: Ideal for data centers, virtual machines, and highly available applications.
- **Self-Healing**: Automated error detection and correction – because data should just work.
- **Built for Scale**: With file system limits that leave **NTFS** in the dust, ReFS is poised to handle tomorrow’s storage challenges today.

---

## Purpose

This repository is a resource for **digital forensics professionals** and **incident responders** to understand and analyze ReFS, specifically in:

- 🔍 **Forensic Investigations**: Gain insights into file system metadata, timestamps, and object IDs to reconstruct events.
- 🛡️ **Incident Response**: Track how ReFS manages file creation, modification, and deletion – vital in understanding malicious activity or file tampering.
- 🧩 **File Recovery**: Learn how ReFS handles data integrity and self-healing, helping in data recovery from corrupted or damaged systems.
- 🔐 **Data Integrity Analysis**: Dive deep into how ReFS detects and corrects data corruption using integrity streams, and how this impacts investigations.
  
---

The Filesystem's Boot Sector Starts As Follows:

<img width="563" alt="image" src="https://github.com/user-attachments/assets/e3432e03-d538-4afa-bcad-39b0340e7819">
<br><i>The Hex of The Boot Sector</i><br><br>

| Offset | Value        | Description                    |
|--------|--------------|--------------------------------|
| x00    | 3 bytes      | JMP Instructions               |
| x03    | 4 bytes      | File System Name               |
| x07    | 9 bytes      | Reserved (Must be '00')        |
| x16    | 4 bytes      | Identity - FSRS (signature)    |
| x20    | 2 bytes      | Length of FSRS                 |
| x22    | 2 bytes      | Checksum of FSRS               |
| x24    | 8 bytes      | Total Sectors                  |
| x32    | 4 bytes      | Bytes per Section              |
| x36    | 4 bytes      | Sectors Per Cluster            |
| x40    | 16 bytes     | Unknown (Research ongoing)     |
| x56    | 8 bytes      | Serial Number                  |


---
🙏 Thank You & References

This repository wouldn’t be possible without the invaluable research and contributions from the forensics and file system communities. Special thanks to the researchers and developers who have explored the depths of ReFS and shared their findings.

Key References:

- "Reverse engineering of ReFS"

  Authors: Rune Nordvik, Henry Georges, Fergus Toolan, Stefan Axelsson

  Available at: https://www.sciencedirect.com/science/article/pii/S1742287619301252

- "Forensic analysis of the Resilient File System (ReFS) journaling"

  Authors: Seonho Lee, Jungheum Park, Hyunuk Hwang, Seungyoung Lee, Sangjin Lee, Doowon Jeong

  Available at: https://www.sciencedirect.com/science/article/pii/S2666281721000342


- https://www.resilientfilesystem.co.uk/
  Author: Andrew Head

- https://www.ntfs.com/refs-architecture.htm


