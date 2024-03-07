# SIEM-deploy-wazuh-agent-linux
## About wazuh
The Wazuh platform helps organizations and individuals protect their data assets through threat prevention, detection, and response. Besides, Wazuh is also employed to meet regulatory compliance requirements, such as PCI DSS or HIPAA, and configuration standards like CIS hardening guides. It is also a solution for users of IaaS (Amazon AWS, Azure, or Google Cloud) to monitor virtual machines and cloud instances.

Below you can find examples of some of the most common use cases of the Wazuh platform.


| Endpoint security | Threat intelligence | Security operations | Cloud security |
|----------|----------|----------|----------|
| Configuration assessment | Threat hunting | Incident response | Container security |
| Malware detection | Log data analysis | Regulatory compliance | Posture management |
| File integrity monitoring | Vulnerability detection | IT hygiene | Workload protection |

# Setting up
First I sigh up Wazuh in the cloud. I used their own cloud; it is free for a 14-day trial. After sigh in, I had to add an agent to it. For that, I used my Kali Linux system named as strom27 a default agent.

![Screenshot 2024-03-07 120612](https://github.com/Iamutsav27/SIEM-deploy-wazuh-agent-linux/assets/139797923/e71c761d-cf08-4579-ac64-94956ffe622e)

The Wazuh dashboard is the web user interface for data visualization and analysis. It includes out-of-the-box dashboards for security events, regulatory compliance (e.g., PCI DSS, GDPR, CIS, HIPAA, NIST 800-53), detected vulnerable applications, file integrity monitoring data, configuration assessment results, cloud infrastructure monitoring events, and others. It is also used to manage Wazuh configuration and to monitor its status.

![Screenshot 2024-03-07 161624](https://github.com/Iamutsav27/SIEM-deploy-wazuh-agent-linux/assets/139797923/7d056483-0eed-48c1-9749-259bd23e619a)

## Wazuh SCA module

Wazuh offers a Security Configuration Assessment (SCA) module that assists security teams to scan and detect misconfigurations within their environment. The Wazuh agent uses policy files to scan endpoints that it monitors. These files contain predefined checks to be carried out on each monitored endpoint.
- Security posture management: Wazuh SCA helps organizations ensure that their endpoints are configured securely. This minimizes vulnerabilities resulting from misconfigurations and reduces the risk of security breaches.
- Compliance monitoring: It allows organizations to assess and implement compliance with regulatory standards, best practices, and internal security policies.
- Continuous monitoring: Wazuh SCA continuously monitors the configuration of the endpoints and alerts when it discovers misconfigurations.

![Screenshot 2024-03-07 163427](https://github.com/Iamutsav27/SIEM-deploy-wazuh-agent-linux/assets/139797923/cb2d6d12-6d60-4926-877e-8a60e9028989)

This is for kali Linux and tell you how good you are, my score is 12% failed 14 of these. Let's jump into this report. Notice there in the breadcrumbs, I did jump into the security configuration assessment section and it'll tell me all the things I failed at. Let me actually sort by. It's gonna be a small list. And most of this is like default.


Let's get back to our agent dashboard here. Here on the menu we have security events showing you things like authentication failures, which could be brute force attacks. It'll show you top five alerts. It'll give you a list of security alerts.

![Screenshot 2024-03-07 172644](https://github.com/Iamutsav27/SIEM-deploy-wazuh-agent-linux/assets/139797923/adecf08b-b73a-4048-8f93-3b3a9c520865)

Here are some of the most useful features.

- Malware detection: Using a non-signature-based approach, this component is capable of detecting anomalies and the possible presence of rootkits. Also, it looks for hidden processes, hidden files, and hidden ports while monitoring system calls.
- Active response: This module runs automatic actions when threats are detected, triggering responses to block a network connection, stop a running process, or delete a malicious file. Users can also create custom responses when necessary and customize, for example, responses for running a binary in a sandbox, capturing network traffic, and scanning a file with an antivirus.
- Container security monitoring: This agent module is integrated with the Docker Engine API to monitor changes in a containerized environment. For example, it detects changes to container images, network configuration, or data volumes. Besides, it alerts about containers running in privileged mode and about users executing commands in a running container.

I realize that Wazuh is a powerful tool that will not only help to protect your own lab and your business, but it'll also teach you a ton about security, hacking, the blue team, and the fact that it's free and open source.
