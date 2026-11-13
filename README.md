# SIEM Home Lab

A home lab I'm building to practice SOC analyst skills: collecting logs, writing detections, and investigating simulated attacks. I'm building it alongside the TryHackMe SOC Level 1 path (my notes are in [soc-level-1-notes](https://github.com/HersiAhmed/soc-level-1-notes)).

## The goal

```
┌────────────────────────┐            ┌──────────────────────────────┐
│  Windows 11 VM         │   logs     │  Ubuntu VM                   │
│  "the victim"          │ ─────────► │  Splunk (indexer + search)   │
│  Sysmon + forwarder    │  port 9997 │  "the SOC's SIEM"            │
└────────────────────────┘            └──────────────────────────────┘
```

Generate realistic attacker activity on Windows, send the logs to Splunk, and build detections that catch it, mapped to MITRE ATT&CK.

## Progress

| Part | What I built | Status |
|---|---|---|
| [01](01-building-the-siem-server.md) | Ubuntu VM, Linux setup, Splunk installed as a service | ✅ Done |
| [02](02-windows-victim-and-switching-hypervisors.md) | Windows victim VM, VirtualBox troubleshooting, move to VMware | ✅ Done |
| 03 | Connect the VMs on one network | ⏳ Next |
| 04 | Sysmon + Splunk forwarder | |
| 05 | Attack simulations + detections | |
| 06 | Dashboard | |

## Lab specs

| | |
|---|---|
| **Host** | Windows 11 Home, Intel Core Ultra 9, 32 GB RAM |
| **Hypervisor** | VMware Workstation Pro 26H1 (the lab started on VirtualBox 7.2; see Part 02) |
| **SIEM server** | Ubuntu 26.04.1 LTS, 8 GB RAM, 4 CPUs, 80 GB disk |
| **SIEM** | Splunk Enterprise 10.6.1.1 |
| **Victim endpoint** | Windows 11 Enterprise Evaluation, 6 GB RAM, 2 CPUs, 64 GB disk |
