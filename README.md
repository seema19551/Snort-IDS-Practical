# 🛡️ Snort Network IDS Practical Implementation

## Project Overview

This repository documents the **successful implementation, configuration, and testing of Snort**, an industry-standard, open-source Network Intrusion Detection System (NIDS). The practical was conducted on a Linux environment and demonstrates fundamental skills in network security monitoring and analysis.

### 🎯 Key Objectives Demonstrated

The project successfully achieved the following core functionalities of Snort:

1.  **Installation & Setup:** Verification of the latest Snort version and successful system integration.
2.  **Configuration Validation (`-T`):** Testing the integrity and syntax of the main configuration file (`snort.conf`).
3.  **Passive Packet Sniffing (`-v`):** Running Snort as a network tap to capture and decode real-time TCP traffic.
4.  **IDS Mode Initialization (`-c`):** Launching Snort as a dedicated intrusion detection system, ready to process rules.
5.  **Configuration Review:** Examination and use of custom Port Variable definitions within `snort.conf`.

---

## 💻 Configuration and Rule Files

The following files are included for reference, capturing the setup used in the practical:

| File Name | Description |
| :--- | :--- |
| **`snort.conf`** | The primary configuration file, defining preprocessors, output plugins, and system variables. |
| **`local.rules`** | The custom rules file used to load detection logic during IDS mode. |

---

## 📸 Practical Evidence (Screenshots)

The screenshots below provide visual evidence of each stage of the Snort operation.

| Screenshot Name | Description | Command/Mode Demonstrated |
| :--- | :--- | :--- |
| **`snort_installation_version.jpg`** | Confirmation that **Snort version 2.9.20** is correctly installed and ready for use. | `sudo apt install snort` |
| **`snort_config_file_header.png`** | Snippet of `snort.conf`, verifying VRT rule package compatibility and structure. | `GNU nano /etc/snort/snort.conf` |
| **`snort_config_test_ports.jpg`** | Output showing defined network port variables (e.g., `HTTP_PORTS`) during the **Test Mode** execution. | `sudo snort -T -c /etc/snort/snort.conf` |
| **`snort_sniffer_mode_start.jpg`** | Snort initializing and successfully starting traffic acquisition in **Packet Dump Mode**. | `sudo snort -v -i <interface>` |
| **`snort_sniffer_mode_traffic.jpg`** | Captured output displaying decoded **TCP packet headers** and details in real-time. | *Continuation of Sniffer Mode* |
| **`snort_ids_mode_rules_read.png`** | Output showing Snort successfully initializing and parsing the rules file in **IDS Mode**. | `sudo snort -c /etc/snort/rules/local.rules` |

---

## ✨ Skills and Technologies

* **Technology:** Snort NIDS (Version 2.9.20)
* **Operating System:** Linux (Ubuntu/Debian)
* **Concepts:** Network Monitoring, Packet Analysis, Configuration Management, Command Line Interface (CLI) tools.

---
