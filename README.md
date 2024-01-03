---
description: >-
  Technologies used: Wazuh, TheHive, Shuffle, VirusTotal (OSINT), Sysmon logs,
  Mimikatz attack
---

# SOC Automation Project

In this project, I created a Home Lab to simulate a Security Operations Center (SOC) environment in which it will perform automation. The goal of this Home Lab project is to explore how a SOC analyst would investigate alerts and any detections caught in my SIEM. \
\
I have created a diagram that can be found in this project folder describing how my Home Lab will be setup, but here it is as well:

<figure><img src=".gitbook/assets/SOCAutomationProjectDiagram.jpg" alt=""><figcaption></figcaption></figure>

As you can see, I will be using a Windows 10 machine in VirtualBox as my virtual machine and it will represent the Wazuh Agent. Wazuh Management receives events from the Wazuh agent which then sends alerts to Shuffle.&#x20;

Shuffle will use open source intelligence (OSINT) to enrich the indicators of compromise (IOCs) and send the alerts to our case management, TheHive.&#x20;

Shuffle will then send an email to us (the SOC analyst) with details about the alert and ask the analyst what action(s) need to be taken, if any. The action(s) will be sent back to Shuffle, which will send it to the Wazuh Manager. The Wazuh Manager will instruct the Wazuh agent to perform the action(s).







<figure><img src=".gitbook/assets/image.png" alt=""><figcaption><p>Shuffle workflow</p></figcaption></figure>
