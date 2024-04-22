## Incident Response Steps: DDoS Attack PLAYBOOK POD 22

### Step 1: Identify the Attack
- **Verification**:
  - Analyze network traffic using Wireshark to confirm DDoS attack patterns.
  - Check Splunk logs for unusual traffic patterns indicating a DDoS attack.
- **Asset Identification**:
  - Utilize Splunk to obtain IP addresses and network diagrams of targeted systems.
  - Identify targeted services such as Web Server, DNS, Mail Server, etc.
- **Attack Type Identification**:
  - Use Snort to detect and classify the type of DDoS attack (Volumetric, Amplification, Syn Flood, Protocol, etc.).
  - Investigate Snort alerts for details on malicious packets.

### Step 2: Contain the Attack
- **Mitigation**:
  - Implement Snort Rules to block incoming DDoS packet IP addresses.
  - Enforce rate-limiting to restrict packet volume from single IP addresses.
  - Explore DDoS defense options from Internet or Cloud Service providers (e.g., Scrubbing/Clean Pipe, Sinkholing, Null routing).
  - Redirect traffic to alternative servers if available.

### Step 3: Acquire Forensic Evidence for Root Cause Analysis
- **Evidence Collection**:
  - Capture network traffic with Wireshark, including packet captures and network flow data.
  - Analyze Splunk logs for historical data on the attack timeline and affected systems.
- **Root Cause Analysis**:
  - Utilize Splunk to identify vulnerabilities exploited during the attack.

### Step 4: Harden your Systems
- **System Hardening**:
  - Configure Snort rules in response to identified attack vectors.
  - Utilize Snort for real-time monitoring and detection of DDoS attack patterns.
  - Review and update Catalyst ticket logs for documentation of system hardening measures.

### Step 5: Notify Stakeholders and Report the Incident
- **Communication**:
  - Notify relevant stakeholders using Catalyst ticketing system about potential downtimes or compromised devices.
- **Reporting**:
  - Generate reports in Catalyst detailing the incident, including impact analysis and remediation efforts.
  - Document incident response steps in Catalyst for future reference and compliance purposes.
