# network-noise-vs-real-threats-suricata

SOC-style alert triage lab analyzing Suricata IDS detections to separate false positives from real security risks.

## Asset Identification
A network sweep of the 192.168.8.0/24 subnet identified host ghostnode.ts.net at IP address 192.168.8.190, corresponding to the Raspberry Pi running the Suricata IDS sensor.

## Alert Analysis
Suricata generated alerts related to cryptocurrency mining domains and Telegram API usage. Investigation confirmed these alerts originated from the Pi itself and were associated with previously initiated lab activities, including incomplete crypto mining experiments and actively running Telegram bots.
Alerts were determined to be expected background network activity and did not warrant containment or remediation.

## Lessons Learned
This case highlights the importance of asset inventory and contextual awareness when triaging IDS alerts to avoid false positives.

**Indicators Reviewed**
- DNS queries to known mining pool domains
- TLS connections to Telegram API endpoints
- Source IP mapping to known lab infrastructure
