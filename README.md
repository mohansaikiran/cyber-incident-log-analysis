# Cyber Incident Log Analysis

### Overview
This repository documents a cybersecurity incident response simulation completed as part of the Deloitte Australia Cyber Job Simulation on Forage.
The scenario involves investigating a suspected data breach of a client's manufacturing status dashboard by analysing web activity logs from the internal telemetry system.

### Scenario
A major news outlet has published sensitive information about the client's production status, including halted assembly lines and impacted factories.
The client suspects that the new internal status board (telemetry dashboard) has been breached and has engaged the cyber team to investigate the source of the leak.

### Objectives
The main goals of this exercise are:
1. Determine whether a hacker could access the manufacturing status dashboard directly from the internet (without VPN access).
2. Analyse the web_activity.log / web_requests.log file for suspicious behaviour.
3. Identify potential automated scraping of the API and the user account/host involved.
4. Explain the likely attack path and make recommendations to the client.

### Key Findings
1. The status dashboard is hosted on the intranet and is only reachable from internal IP addresses (or via VPN), so there is no direct internet access path.
2. Normal users follow a pattern: login → load dashboard resources → perform a limited number of ad‑hoc API requests for specific factories/machines.
3. One internal IP shows highly regular, repeated API calls to multiple factories at exact hourly intervals, indicating scripted/automated scraping using valid credentials.
