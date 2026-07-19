# TryHackMe SOC Simulator — Phishing Unfolding

![Badge: 100% True Positive Rate](https://cdn-images.tryhackme.com/013c16b42db058985e5c7f307df4305d.png)

## Overview

This repo documents my completion of the **Phishing Unfolding** scenario in TryHackMe's **SOC Simulator**, earning the **"100% True Positive Rate"** badge.

The scenario places you inside a live, simulated SOC environment where alerts stream into a built-in SIEM (Splunk-based) in real time as a phishing attack unfolds across a corporate network. The job of the analyst is to triage each alert, determine whether it's a **true positive** or **false positive**, document findings in a case report, and escalate where the evidence warrants it — while new alerts keep arriving throughout the shift.

## Environment

- **SIEM**: Built-in simulator SIEM (Splunk-based) with case management for writing per-alert reports
- **Threat Intel**: An integrated TIP called TryDetectThis, used to check indicators (domains, hashes, senders) against known threat data
- **Alert volume**: Dozens of alerts, arriving on a timer, requiring prioritization by severity and age rather than working them in a fixed order

## Methodology

1. **Triage queue management** — prioritized unassigned alerts by severity first, then by oldest timestamp, since new alerts kept arriving mid-shift
2. **Evidence gathering per alert** — pulled email headers, sender domains, attachment hashes, and URLs referenced in each alert
3. **Threat intel correlation** — cross-checked indicators against TryDetectThis to confirm malicious infrastructure/senders
4. **Verdict + reporting** — classified each alert as true or false positive, documenting the reasoning in the case report tool
5. **Escalation calls** — flagged alerts that indicated an active/ongoing compromise (e.g. credential harvesting, payload delivery) for escalation
6. **Pattern recognition** — noticed several alerts were downstream effects of a single root-cause phishing email, and grouped/linked them rather than treating each as isolated

## Skills Demonstrated

- Phishing alert triage and true/false positive classification
- SIEM-based investigation workflow
- Threat intelligence correlation
- Incident documentation and escalation decision-making
- Working under a live, time-pressured alert stream

## Notes

In line with TryHackMe's room guidelines, this write-up focuses on methodology and process rather than reproducing specific alert content, flags, or full case report text from the room.
