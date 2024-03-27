# Penetration Testing

PT is the process of evaluating the security posture of a computer system, network or application.

## Phases of PT:

### 1) Reconnaissance

* **Purpose**: The reconnaissance phase involves gathering information about the target system, network, or organization. This information can include details about the network topology, domain names, IP addresses, employee names, email addresses, and more.
* **Techniques**: Reconnaissance techniques can be passive (e.g., searching publicly available information, social media profiling, WHOIS lookup) or active (e.g., network scanning, port scanning, DNS enumeration).
* **Outcome**: The goal is to gather as much information as possible to understand the target environment's architecture, potential entry points, and attack surface.

### 2) Scanning and Enumeration

* **Purpose**: In the scanning phase, the penetration tester actively scans the target network or systems to identify live hosts, open ports, and running services. This phase helps in identifying potential targets for further investigation and exploitation.
* **Techniques**: Network scanning tools like Nmap, port scanners, vulnerability scanners, and enumeration tools are commonly used in this phase.
* **Outcome**: The outcome of this phase is a comprehensive understanding of the target's network topology, available services, and potential vulnerabilities.

### 3) Vulnerability Assessment

* **Purpose**: The vulnerability assessment phase involves identifying and assessing vulnerabilities present in the target systems and applications. This phase aims to identify weaknesses that could be exploited by attackers to gain unauthorized access or disrupt operations.
* **Techniques**: Vulnerability scanning tools are used to identify known vulnerabilities, misconfigurations, and weak security controls. This can include scanning for software vulnerabilities, weak passwords, insecure configurations, and missing patches.
* **Outcome**: The outcome of this phase is a list of identified vulnerabilities along with their severity ratings, potential impact, and recommended remediation actions.

### 4) Exploitation

* **Purpose**: The exploitation phase involves attempting to exploit identified vulnerabilities to gain unauthorized access to the target systems or sensitive data. This phase simulates real-world attacks and assesses the effectiveness of existing security controls.
* **Techniques**: Exploitation techniques can vary depending on the nature of the vulnerabilities discovered. This may include exploiting software vulnerabilities, misconfigurations, weak authentication mechanisms, or other weaknesses.
* **Outcome**: The outcome of this phase is successful exploitation of vulnerabilities, leading to unauthorized access, privilege escalation, or other compromise scenarios.

### 5) Reporting

* **Purpose**: The reporting phase involves documenting the findings, analysis, and recommendations resulting from the penetration test. A comprehensive report provides stakeholders with valuable insights into the security posture of the organization and guidance on remediation efforts.
* **Content**: The penetration test report typically includes an executive summary, methodology, findings, risk assessment, recommendations, and any supporting evidence or documentation.
* **Outcome**: The outcome of this phase is a detailed penetration test report that highlights identified vulnerabilities, their potential impact on the organization, and actionable recommendations for improving security posture.
