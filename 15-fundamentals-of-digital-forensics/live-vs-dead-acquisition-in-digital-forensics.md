---
title: "Live vs Dead Acquisition in Digital Forensics"
subtitle: "Methods, tools, and critical decisions when collecting digital evidence from powered-on or powered-off systems"
description: "Learn how and when to perform live or dead acquisition of digital evidence, their technical and legal implications, tools used, and forensic best practices."
tags: ["cybersecurity", "digital forensics", "evidence acquisition", "live acquisition", "RAM memory", "chain of custody"]
authors: ["alesanchezr"]
---

In digital forensics, evidence acquisition is one of the most critical phases of the process. The quality of the subsequent analysis and the legal validity of the collected information depend on its correct execution.

There are two main approaches to acquiring digital evidence: **Live Acquisition and Dead Acquisition**.

Both methods have their own techniques, risks, benefits, and tools. This article will teach you in depth when to choose one or the other, how to do it correctly, and what mistakes to avoid. But first, let's agree on something basic yet fundamental: what exactly is digital evidence acquisition?

Imagine you are called to investigate a cybercrime. Maybe someone accessed a computer without permission, stole information, installed malware, or encrypted files with ransomware. Your mission is clear: understand what happened, how it happened… and, above all, preserve the evidence so it can be analyzed and even presented in court if necessary. This is where **digital evidence acquisition** comes into play.

## What is digital evidence acquisition?

Digital evidence acquisition is one of the most delicate and crucial tasks in any computer forensic investigation. It consists of copying, in an exact and unaltered manner, the information contained in a computer system—such as hard drives, RAM memory, system logs, or temporary files—for later analysis.

The main goal is not just to access the information, but to do so in a way that:

- 🛡️ Preserves the original state of the affected system.
- 🔍 Allows for detailed subsequent analysis without contaminating the evidence.
- ⚖️ Guarantees traceability and legal validity through a proper chain of custody.

> In other words: obtain an "untouchable" copy that reflects exactly how things were at the time of the incident, ready to be analyzed in a lab without risking modification of the original.

The way this acquisition is performed depends on the state of the system at the time it is found. This is where the key distinction comes in:

- **Live Acquisition:** when the system is powered on, active, and running.
- **Dead Acquisition:** when the system is powered off or is shut down in a controlled manner before collecting data.

Both methods are valid and widely used in digital forensics, but each carries different advantages, challenges, and risks, which are essential to understand in order to choose the right strategy for each situation.

## Live Acquisition

Live acquisition refers to the process of collecting digital evidence while the target system is powered on and operational.

This type of acquisition allows you to capture volatile information, that is, data residing in the system's temporary memory that disappears as soon as the device is powered off or restarted. Therefore, it is a fundamental technique when the analyst arrives at a scene where the incident is still ongoing or the system has not yet been tampered with.

Among the most important volatile data that can be captured are:

- Full RAM memory: contains processes, encryption keys, passwords in use, and malware payloads.
- Active processes: what is running at that exact moment, including malicious software.
- Logged-in users: active sessions, remote accesses.
- Network connections: IP addresses the system is communicating with.
- Open sessions and loaded scripts.
- Temporary encryption keys, which disappear once the system is powered off.

> **Note:** once you power off the system, all this information is lost forever. That’s why, when there is critical evidence in execution, this type of acquisition is prioritized.

### When is live acquisition used?

This method is applied when:

- The system cannot be powered off without risking the loss of volatile evidence.
- An active incident is underway, such as ransomware, persistent attacks, or real-time data exfiltration.
- There are signs of ongoing malicious activity, such as suspicious processes or connections to unknown servers.
- The device is an embedded system or has complex access (routers, mobile devices, IoT).

#### Examples of evidence collected and recommended tools

| Data Type                | Suggested Tools                                               |
|--------------------------|--------------------------------------------------------------|
| RAM memory               | Volatility, Belkasoft RAM Capturer, DumpIt, WinPMEM          |
| Active processes         | Sysinternals Process Explorer, pslist, tasklist, ps          |
| Network connections      | Wireshark, TCPView, netstat, Fiddler, CurrPorts              |
| Logged-in users          | who, w, query user, net session                              |
| Recent activity          | last, bash_history, RecentDocs, Prefetch, temp logs          |

---
These tools allow you to capture the system's volatile information without shutting it down, ensuring the current state of processes and connections is preserved. On the other hand, live acquisition is powerful but also carries risks if not performed carefully:

1. **Alteration of system state:** any action performed can modify files, memory, or key logs.
2. **Execution of code on the compromised device:** even opening a tool can change values in RAM or generate new logs.
3. **Legal risk:** if not properly documented, the evidence can be challenged for possible contamination.

For this reason, only trained personnel should perform live acquisition. It is not a method for improvisation.

### Best practices during live acquisition

- Document every step from the moment you arrive at the device.
- Calculate hashes (MD5, SHA-256) for any file or dump generated.
- Use portable tools from a forensic USB, without installing anything on the compromised system.
- Do not interact with suspicious software.
- Do not browse the system unnecessarily.
- Avoid actions that generate changes such as connecting to the internet, installing programs, or opening files.
- Run as few commands or scripts as possible.
- Last but not least, if conditions allow, first capture RAM (as it is the most volatile evidence) and then complement with a dead acquisition of the disk. This combination provides a comprehensive view of the system's state.

## Dead Acquisition

Dead acquisition is the process of collecting digital evidence **when the system is powered off**, or after it has been shut down in a controlled manner by the analyst. Unlike live acquisition, this technique focuses exclusively on **non-volatile** data, that is, data that remains persistently stored on the device even after it is powered off. The main types of evidence collected in this scenario include:

- Full forensic image of the hard drive.
- System and user files.
- System, network, and event logs.
- Configuration files and stored credentials.
- Program artifacts (history, prefetch, logs).

The goal is to obtain an exact copy of the disk or storage medium, without modifying anything, so it can be analyzed later in a controlled environment.

### When is dead acquisition used?

This type of acquisition is ideal when:

- The system was already powered off when the investigation began (e.g., during a seizure).
- It is possible to power off the system without risking the loss of critical information.
- There is suspicion of manipulation of persistent files and it is necessary to preserve the exact state of the disk.
- You are working under strict legal or judicial requirements.

#### Examples of tools used

| Type of Evidence              | Recommended Tools                             |
|-------------------------------|-----------------------------------------------|
| Disk image                    | FTK Imager, `dd`, Guymager                    |
| Access without modification   | Write blockers                                |
| Forensic image format         | `.E01` (EnCase), `.AFF`, `.dd`                |

These tools allow you to create a bit-by-bit image of the hard drive, ensuring that the original content is not altered. The use of write blockers is essential to protect the integrity of the medium during the process.

**Advantages**

- **Lower risk of altering evidence:** by working with the system powered off and using specialized tools, unintentional modification of files is avoided.
- **Ideal for legal environments:** this methodology is widely accepted in legal contexts, as it offers guarantees of integrity and reproducibility.
- **Allows detailed and repeatable analysis:** by working on an exact copy of the disk, analysts can examine artifacts without fear of compromising the original evidence.

**Limitations**

- **Volatile data is not captured:** all information that was in RAM, active processes, or network connections is lost when the system is powered off.
- **Loss of execution context:** if the device was powered off abruptly, important details such as active sessions, running malware, or encryption keys in memory may be missed.

For these reasons, when possible, it is recommended to **complement dead acquisition with a prior live acquisition**, especially if the system was powered on and contained critical information in execution.

> **Note:** Dead acquisition is a **safer and more controlled** technique, ideal for preserving evidence in formal investigations or post-incident analysis. However, its effectiveness depends on the relevant evidence being on the disk and not having lost key volatile information before shutdown.

## 🛡️ Chain of Custody and Legal Validity

One of the fundamental principles in digital forensics is ensuring that the collected evidence is **valid, intact, and legally admissible**. This depends not only on the tools used or the type of acquisition performed, but mainly on maintaining a **rigorous and well-documented chain of custody** from the very beginning.

The chain of custody is the **detailed record of the control, transfer, and handling of digital evidence**, from the moment it is collected until it is analyzed or presented to an authority. It is essential to demonstrate that the evidence: was not altered or contaminated during handling, was managed exclusively by authorized personnel, is associated with a reliable technical procedure, and is reproducible and verifiable by third parties.

### Key elements for maintaining an adequate chain of custody

Below are the actions and precautions that must be taken into account, both in live and dead acquisition:

1. **Record basic procedure data.** Accurately note:
    - Date and time of intervention start.
    - Full name and role of involved personnel.
    - Physical location of the device.
    - Initial state of the system (on, off, connected to network, etc.).

2. **Thorough documentation of every action.** Every action performed on the system or evidence must be recorded, including:
    - Commands executed.
    - Tools used (version, usage mode).
    - Storage media employed.
    - Relevant results obtained at the time.

3. **Use secure storage media**
    - Store memory dumps, forensic images, and collected files on reliable devices.
    - Use **encrypted USBs**, external hard drives with authentication, or storage on controlled servers.
    - Avoid using personal computers or shared media to transport evidence.

4. **Hash calculation and verification**
    For each forensic image, file, or dump, calculate:
    - Cryptographic hashes (preferably SHA-256, though MD5 is also accepted).
    - Hashes must be recorded immediately after acquisition and again at the time of analysis to verify integrity.
    - Any discrepancy between values invalidates the evidence.

5. **Use standardized forensic formats**
    Whenever possible, store images in containers recognized and validated by the forensic community:
    - `.E01` (EnCase)
    - `.AFF` (Advanced Forensic Format)
    - `.dd` (raw bit-by-bit dump)

    These formats allow encapsulation not only of the original data, but also additional information such as metadata, hashes, and acquisition process notes.

## Comparison: Live vs Dead Acquisition

| Characteristic             | Live Acquisition                      | Dead Acquisition                        |
|---------------------------|---------------------------------------|-----------------------------------------|
| System state              | Powered on                            | Powered off                             |
| Type of data collected    | Volatile (RAM, processes, connections)| Persistent (disk, files, logs)          |
| Risk of alteration        | High (requires active intervention)   | Low (with proper tools)                 |
| Legal value               | Admissible if well documented         | More robust for legal proceedings       |
| Required expertise        | High                                  | Medium                                  |
| Typical use               | Active incidents, malware in memory   | Post-mortem analysis, seized evidence   |

