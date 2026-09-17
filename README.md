# CIP-B105 Case Study 2 – Network Forensic Investigation

**Student:** Asmau Danzaria  
**Student ID:** 2617285  
**Course:** CIP-B105  
**Assessment:** Case Study 2  

## Overview

This repository contains my work for the CIP-B105 Case Study 2 assessment. The investigation involved examining supplied network capture evidence to identify and reconstruct relevant web activity, preserve supporting artefacts, and establish what could be concluded from the available traffic.

The main investigation focused on activity involving `www.willselfdestruct.com`. Packet and stream analysis was used to identify the client involved, examine the submitted HTTP data, correlate the network activity with a device, and assess available identity evidence.

## Investigation Summary

The supplied evidence was first inventoried and hashed before analysis. A working copy of the relevant Nitroba packet capture was then examined using Wireshark, TShark and supporting command-line tools.

The investigation identified HTTP activity between `192.168.15.4` and `www.willselfdestruct.com`. Frame 83601 contained a POST request to `/secure/submit`. Reconstruction of TCP stream 1707 recovered the submitted form data, including the recipient, subject and message.

Further analysis linked the source IP address to MAC address `00:17:f2:e2:c0:ce`. Traffic associated with the same client also contained Gmail-related identity artefacts referring to `jcoachj@gmail.com`. This evidence was correlated with the supplied Chemistry 109 roster and relevant packet timestamps.

The findings were based on the evidence available in the supplied captures. Where the traffic supported association rather than direct proof of a person's actions, this distinction was maintained in the final report.

## Tools Used

- Wireshark
- TShark
- capinfos
- md5sum
- sha256sum
- unzip
- Linux command-line utilities
- Python for URL-form decoding

## Repository Structure

- `CIP-B105-CS2_2617285_Asmau_Danzaria.pdf` – Final investigation report
- `codes/` – Commands and supporting code used during the investigation
- `reports/` – Generated analysis results, timelines and supporting records
- `screenshots/` – Selected screenshots documenting the investigation
- `README.md` – Repository overview

## Evidence Handling

Source evidence was preserved during the investigation and analysis was carried out on working copies. MD5 and SHA-256 hashes were recorded where required to support evidence integrity.

The repository is intended to document my investigation process and assessment work. Original or restricted evidence should not be redistributed where this is prohibited by the Academy.

## Key Areas Examined

The investigation covered:

- Evidence inventory and integrity verification
- Packet capture profiling
- HTTP request and POST analysis
- TCP stream reconstruction
- URL-encoded form decoding
- Source IP and MAC address correlation
- Identity-related HTTP and cookie artefacts
- Chemistry 109 roster correlation
- Incident timeline reconstruction
- Review of the additional supplied packet captures

## Note

This repository represents my individual assessment work. Conclusions in the accompanying report are based on the artefacts recovered during my examination of the supplied evidence and are limited to what those artefacts can reasonably support.
