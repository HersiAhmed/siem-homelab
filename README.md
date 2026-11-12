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
| 02 | Windows victim VM + lab network | ⏳ Next |
| 03 | Sysmon + Splunk forwarder | |
| 04 | Attack simulations + detections | |
| 05 | Dashboard | |

## Lab specs

| | |
|---|---|
| **Host** | Windows 11 Home, Intel Core Ultra 9, 32 GB RAM |
| **Hypervisor** | Oracle VirtualBox 7.2 |
| **SIEM server** | Ubuntu 26.04.1 LTS, 8 GB RAM, 4 CPUs, 80 GB disk |
| **SIEM** | Splunk Enterprise 10.6.1.1 |
