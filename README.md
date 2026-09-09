# Awesome-Security-Orchestration-Automation-n-Response

## Top Security Orchestration, Automation & Response (SOAR) Platforms



**A comprehensive ecosystem of SOAR platforms, security automation engines, incident-response orchestration systems and open-source alternatives**



*Open-source-first reference covering security orchestration, playbooks, alert enrichment, incident response, threat-intelligence automation, case management, remediation, workflow automation and autonomous SOC building blocks.*



**Last updated: September 2026**



Security Orchestration, Automation & Response (**SOAR**) platforms connect security tools and automate repetitive SOC workflows.



A typical SOAR platform receives an alert from a SIEM, EDR, XDR, email-security platform, cloud-security service or threat-intelligence source and then:



```text

Alert

  ↓

Normalize

  ↓

Enrich

  ↓

Correlate

  ↓

Investigate

  ↓

Decide

  ↓

Respond

  ↓

Document

  ↓

Close

```



Examples include **Cortex XSOAR, Splunk SOAR, Tines, Torq, Demisto, Swimlane, DFLabs, Google Security Operations SOAR, FortiSOAR and Siemplify**.



The SOAR market has increasingly divided into two models:



1. **Dedicated / independent SOAR** — platforms such as Tines, Torq and Swimlane.

2. **SOAR embedded inside larger security platforms** — including Cortex XSOAR/XSIAM, Splunk SOAR, Google Security Operations and Microsoft Sentinel automation.



Demisto is the predecessor of Palo Alto Networks' Cortex XSOAR, while Siemplify became the foundation of Google Security Operations' SOAR capability. DFLabs' IncMan lineage is also now part of the broader Sumo Logic Cloud SOAR history.



This README focuses particularly on **open-source alternatives**, including dedicated SOAR platforms, incident-response systems, threat-intelligence orchestration, observable-analysis engines and general-purpose workflow automation that can be combined into a full open-source SOC automation platform.



## Open-source emphasis



Open-source projects are divided into:



1. **Direct SOAR alternatives** — projects that provide playbooks, security orchestration or automated response.

2. **Incident-response platforms** — case-management systems that can form the operational core of a SOAR stack.

3. **Threat-intelligence automation** — systems for IOC collection, enrichment and sharing.

4. **Observable analysis and active response** — engines that allow automated investigation and response actions.

5. **General-purpose workflow automation** — automation engines suitable for security playbooks.

6. **Security automation building blocks** — SIEM, EDR, detection, policy, messaging and infrastructure automation components.



> **Important:** No single open-source project necessarily reproduces every capability of a large commercial SOAR platform. Enterprise SOAR products combine workflow engines with hundreds or thousands of integrations, case management, RBAC, audit, content packs, vendor support, analytics and increasingly AI/agentic functionality.



Contributions and corrections are welcome.



---



## Table of Contents



* [SaaS/Hosted Platforms](#saashosted-platforms)

* [Open-Source SOAR Projects](#open-source-soar-projects)

* [Open-Source Incident Response & Case Management](#open-source-incident-response--case-management)

* [Open-Source Threat Intelligence Orchestration](#open-source-threat-intelligence-orchestration)

* [Open-Source Observable Analysis & Active Response](#open-source-observable-analysis--active-response)

* [Open-Source Workflow Automation Engines](#open-source-workflow-automation-engines)

* [Open-Source SOC / Security Automation Platforms](#open-source-soc--security-automation-platforms)

* [Additional Strong Open-Source Options](#additional-strong-open-source-options)

* [Commercial Platform → Open-Source Equivalents](#commercial-platform--open-source-equivalents)

* [Frameworks for Building Custom SOAR Platforms](#frameworks-for-building-custom-soar-platforms)

* [Reference Architecture](#reference-architecture)

* [Typical SOAR Workflow](#typical-soar-workflow)

* [Alert Enrichment Workflow](#alert-enrichment-workflow)

* [Automated Incident Response Workflow](#automated-incident-response-workflow)

* [Threat Intelligence Workflow](#threat-intelligence-workflow)

* [Phishing Response Workflow](#phishing-response-workflow)

* [Endpoint Isolation Workflow](#endpoint-isolation-workflow)

* [Capability Matrix](#capability-matrix)

* [Recommended Open-Source Stacks](#recommended-open-source-stacks)

* [What Is Still Difficult to Reproduce in Open Source?](#what-is-still-difficult-to-reproduce-in-open-source)

* [Why Open Source Is Interesting](#why-open-source-is-interesting)

* [How to Contribute](#how-to-contribute)

* [Disclaimer](#disclaimer)



---



# SaaS/Hosted Platforms



These are commercial, hosted or enterprise-oriented SOAR and security-automation platforms.



| Platform                                                                                          | Primary Model       | Main Strength                                           |

| ------------------------------------------------------------------------------------------------- | ------------------- | ------------------------------------------------------- |

| [Cortex XSOAR](https://www.paloaltonetworks.com/cortex/cortex-xsoar)                              | Enterprise SOAR     | Playbooks, case management and extensive integrations   |

| [Splunk SOAR](https://www.splunk.com/en_us/products/splunk-soar.html)                             | Enterprise SOAR     | Security automation integrated with Splunk              |

| [Tines](https://www.tines.com/)                                                                   | Cloud SOAR          | No-code security workflow automation                    |

| [Torq](https://torq.io/)                                                                          | Hyperautomation     | Low-code / AI-assisted security automation              |

| [Swimlane](https://swimlane.com/)                                                                 | Enterprise SOAR     | Low-code automation and case management                 |

| [DFLabs IncMan](https://www.dflabs.com/)                                                          | SOAR / IR           | Incident response automation                            |

| [Google Security Operations SOAR](https://cloud.google.com/security/products/security-operations) | SIEM/SOAR           | Google SecOps + SOAR + threat intelligence              |

| [Siemplify](https://cloud.google.com/security-operations)                                         | SOAR                | Former standalone SOAR platform, now Google SecOps SOAR |

| [FortiSOAR](https://www.fortinet.com/products/siem-soar/fortisoar)                                | Enterprise SOAR     | Fortinet Security Fabric integration                    |

| [IBM QRadar SOAR](https://www.ibm.com/products/qradar-soar)                                       | Enterprise SOAR     | Incident response and IBM ecosystem                     |

| [D3 Security](https://d3security.com/)                                                            | SOAR                | Automated incident response                             |

| [Rapid7 InsightConnect](https://www.rapid7.com/products/insightconnect/)                          | Workflow automation | Security orchestration                                  |

| [Sumo Logic Cloud SOAR](https://www.sumologic.com/solution/cloud-soar)                            | Cloud SOAR          | Cloud-native security automation                        |

| [Cyware Orchestrate](https://cyware.com/products/cyware-orchestrate)                              | SOAR                | Threat intelligence + orchestration                     |

| [Microsoft Sentinel](https://azure.microsoft.com/products/microsoft-sentinel)                     | SIEM + SOAR         | Automation rules + Logic Apps                           |

| [ServiceNow Security Operations](https://www.servicenow.com/products/security-operations.html)    | SecOps              | Incident and security workflow automation               |

| [OpenText ArcSight SOAR](https://www.opentext.com/)                                               | Enterprise SOAR     | ArcSight ecosystem                                      |

| [NetWitness](https://www.netwitness.com/)                                                         | Security operations | Detection + response automation                         |

| [D3 Smart SOAR](https://d3security.com/)                                                          | Enterprise SOAR     | Response automation                                     |

| [Palo Alto Cortex AgentiX](https://www.paloaltonetworks.com/)                                     | Agentic security    | AI-assisted SOC automation                              |



The 2026 SOAR market increasingly includes embedded SIEM/XDR automation and independent workflow platforms rather than treating SOAR as an isolated product category.



---



# Open-Source SOAR Projects



These are the most important open-source projects to investigate when building a SOAR platform without depending entirely on a proprietary product.



---



# 1. Shuffle



[GitHub](https://github.com/Shuffle/Shuffle)



Shuffle is one of the strongest direct open-source SOAR alternatives.



It provides:



* visual workflows

* security automation

* app integrations

* webhooks

* workflow execution

* sub-workflows

* API integrations

* SOC automation

* reusable workflows



Typical architecture:



```text

SIEM

 ↓

Shuffle

 ↓

Enrichment

 ↓

Decision

 ↓

Response

 ↓

Ticket / Case

```



Shuffle is particularly attractive as the central orchestration layer in an open-source SOC.



A real-world open-source SOC automation project demonstrates Shuffle coordinating Wazuh, DFIR-IRIS, OpenCTI and Cortex in an end-to-end alert-processing pipeline.



---



# 2. StackStorm



[GitHub](https://github.com/StackStorm/st2)



StackStorm is a powerful open-source event-driven automation platform.



It provides:



* sensors

* triggers

* rules

* actions

* workflows

* packs

* integrations

* Python automation

* REST APIs



Conceptually:



```text

Event

  ↓

Trigger

  ↓

Rule

  ↓

Workflow

  ↓

Action

```



StackStorm is broader than security SOAR, but its event-driven architecture makes it highly suitable for security automation.



---



# 3. TheHive



[GitHub](https://github.com/TheHive-Project/TheHive)



TheHive is primarily an open-source security incident-response and case-management platform rather than a pure SOAR engine.



It is useful for:



* incidents

* cases

* tasks

* observables

* investigations

* analyst collaboration

* incident workflows



It is particularly powerful when combined with:



```text

TheHive

 +

Cortex

 +

MISP

 +

Shuffle

```



---



# 4. Cortex



[GitHub](https://github.com/TheHive-Project/Cortex)



Cortex is an open-source observable-analysis and active-response engine.



It can analyze:



* IP addresses

* domains

* URLs

* email addresses

* hashes

* files

* other observables



Cortex exposes a REST API and can automate analysis through analyzers.



This makes it particularly useful as the **enrichment and action engine** inside a SOAR architecture.



---



# Open-Source Incident Response & Case Management



A complete SOAR implementation often needs a dedicated incident-management layer.



## TheHive



[GitHub](https://github.com/TheHive-Project/TheHive)



Strong for:



```text

Incident

 ↓

Case

 ↓

Tasks

 ↓

Observables

 ↓

Analysis

 ↓

Response

```



---



## DFIR-IRIS



[GitHub](https://github.com/dfir-iris/iris-web)



DFIR-IRIS is an open-source incident-response and case-management platform.



Useful for:



* cases

* incidents

* evidence

* observables

* tasks

* IOC management

* analyst collaboration

* incident tracking



It is an excellent alternative to the case-management component of larger SOAR platforms.



---



## OpenCTI



[GitHub](https://github.com/OpenCTI-Platform/opencti)



OpenCTI is an open-source cyber-threat-intelligence platform.



It provides:



* threat intelligence

* relationships

* observables

* indicators

* threat actors

* malware

* campaigns

* sightings

* enrichment



It is particularly valuable as the intelligence layer behind automated SOAR workflows.



---



## MISP



[GitHub](https://github.com/MISP/MISP)



MISP is one of the most important open-source threat-intelligence sharing platforms.



Useful for:



* IOC collection

* threat intelligence

* event correlation

* indicator sharing

* feeds

* organizations

* enrichment

* automation



MISP can be connected to Cortex, TheHive, Shuffle and other SOC components.



---



# Open-Source Threat Intelligence Orchestration



A typical threat-intelligence automation pipeline is:



```text

Indicator

   ↓

MISP / OpenCTI

   ↓

Cortex

   ↓

VirusTotal / WHOIS / DNS / Sandbox

   ↓

Risk

   ↓

SOAR

   ↓

Response

```



Important projects include:



* [MISP](https://github.com/MISP/MISP)

* [OpenCTI](https://github.com/OpenCTI-Platform/opencti)

* [Cortex](https://github.com/TheHive-Project/Cortex)

* [IntelOwl](https://github.com/intelowlproject/IntelOwl)

* [SpiderFoot](https://github.com/smicallef/spiderfoot)

* [Malwoverview](https://github.com/alexandreborges/malwoverview)

* [Yeti](https://github.com/yeti-platform/yeti)

* [OpenBAS](https://github.com/OpenBAS-Platform/openbas)



---



# IntelOwl



[GitHub](https://github.com/intelowlproject/IntelOwl)



IntelOwl provides an API-oriented intelligence-analysis framework.



It can aggregate analysis from multiple tools and services.



Potential SOAR use:



```text

Suspicious IP

     ↓

IntelOwl

     ↓

Multiple analyzers

     ↓

Aggregated intelligence

     ↓

SOAR decision

```



---



# SpiderFoot



[GitHub](https://github.com/smicallef/spiderfoot)



SpiderFoot is an automated OSINT reconnaissance platform.



It can be used by SOAR workflows for:



* domain investigation

* IP investigation

* DNS

* WHOIS

* infrastructure discovery

* threat intelligence enrichment



---



# Yeti



[GitHub](https://github.com/yeti-platform/yeti)



Yeti is an open-source threat-intelligence platform designed around observables, indicators and threat intelligence knowledge.



Useful as a threat-intelligence backend for security automation.



---



# OpenBAS



[GitHub](https://github.com/OpenBAS-Platform/openbas)



OpenBAS is an open-source breach and attack simulation platform.



It is not a conventional SOAR platform, but it can become part of an advanced security automation ecosystem.



Example:



```text

Detection

 ↓

SOAR

 ↓

OpenBAS

 ↓

Attack Simulation

 ↓

Validate Detection

 ↓

Improve Playbook

```



---



# Open-Source Observable Analysis & Active Response



These components can perform specific actions that SOAR platforms orchestrate.



## Cortex



```text

Observable

   ↓

Analyzer

   ↓

Result

```



Supported analysis concepts include:



* reputation

* malware analysis

* DNS

* WHOIS

* sandboxing

* threat intelligence

* URL analysis

* hash analysis



---



## Wazuh



[GitHub](https://github.com/wazuh/wazuh)



Wazuh is primarily an open-source security platform / SIEM-XDR system, but its alerting and active-response capabilities make it useful as a SOAR component.



Example:



```text

Wazuh Alert

    ↓

Webhook

    ↓

Shuffle

    ↓

Enrichment

    ↓

Firewall / Endpoint Action

```



---



## Suricata



[GitHub](https://github.com/OISF/suricata)



Suricata can provide:



* IDS

* IPS

* network security events

* EVE JSON

* automated alert triggers



It is a strong event source for SOAR.



---



## Zeek



[GitHub](https://github.com/zeek/zeek)



Zeek provides network telemetry and security events that can trigger automated workflows.



---



## Velociraptor



[GitHub](https://github.com/Velocidex/velociraptor)



Velociraptor is an advanced open-source endpoint visibility and digital-forensics platform.



SOAR integration can support:



```text

Alert

 ↓

Endpoint Query

 ↓

Collect Artifact

 ↓

Analyze

 ↓

Response

```



---



## osquery



[GitHub](https://github.com/osquery/osquery)



osquery provides SQL-based endpoint visibility.



A SOAR platform can execute queries automatically during investigations.



---



## GRR Rapid Response



[GitHub](https://github.com/google/grr)



GRR provides remote forensic and incident-response capabilities.



It can be used as an endpoint-response component in a larger SOC automation platform.



---



# Open-Source Workflow Automation Engines



SOAR does not necessarily require a security-specific workflow engine.



General-purpose open-source automation systems can provide the orchestration layer.



---



## n8n



[GitHub](https://github.com/n8n-io/n8n)



n8n provides:



* visual workflows

* webhooks

* API integrations

* conditional logic

* scheduled execution

* custom code

* credentials

* event-driven automation



It is not security-specific, but can be adapted for SOAR.



---



## Node-RED



[GitHub](https://github.com/node-red/node-red)



Node-RED provides event-driven visual workflow automation.



Excellent for:



* webhooks

* API orchestration

* MQTT

* IoT security

* lightweight SOC automation



---



## Windmill



[GitHub](https://github.com/windmill-labs/windmill)



Windmill provides developer-oriented workflows and automation.



Useful for:



* Python scripts

* TypeScript

* APIs

* jobs

* workflows

* internal security tooling



---



## Kestra



[GitHub](https://github.com/kestra-io/kestra)



Kestra is an open-source orchestration platform.



Useful for:



* event-driven workflows

* scheduled workflows

* API automation

* complex pipelines

* security automation



---



## Temporal



[GitHub](https://github.com/temporalio/temporal)



Temporal is a powerful workflow engine for durable execution.



It is especially valuable for security workflows where actions may take minutes, hours or days.



Example:



```text

Incident

 ↓

Approval

 ↓

Endpoint Isolation

 ↓

Wait for Analyst

 ↓

Credential Rotation

 ↓

Validation

 ↓

Close

```



---



## Apache Airflow



[GitHub](https://github.com/apache/airflow)



Airflow can orchestrate scheduled security jobs, enrichment pipelines and batch intelligence workflows.



---



## Dagster



[GitHub](https://github.com/dagster-io/dagster)



Dagster is useful for data-centric security workflows and threat-intelligence pipelines.



---



## Argo Workflows



[GitHub](https://github.com/argoproj/argo-workflows)



Excellent for Kubernetes-native security automation.



---



## Rundeck



[GitHub](https://github.com/rundeck/rundeck)



Rundeck provides operational runbook automation.



It can be useful for:



* response procedures

* infrastructure actions

* incident remediation

* privileged operational workflows



---



# Open-Source SOC / Security Automation Platforms



A complete open-source SOC can combine:



```text

SIEM

+

SOAR

+

Case Management

+

Threat Intelligence

+

Endpoint Response

+

Network Detection

+

Automation

```



Strong components include:



| Function            | Open-Source Projects            |

| ------------------- | ------------------------------- |

| SOAR                | Shuffle, StackStorm             |

| Incident Response   | TheHive, DFIR-IRIS              |

| Threat Intelligence | MISP, OpenCTI, Yeti             |

| Observable Analysis | Cortex, IntelOwl                |

| SIEM/XDR            | Wazuh, OpenSearch               |

| Network IDS         | Suricata, Zeek                  |

| Endpoint Response   | Velociraptor, osquery, GRR      |

| Malware Analysis    | CAPE, Cuckoo                    |

| Vulnerability       | Greenbone / OpenVAS             |

| Case Management     | TheHive, DFIR-IRIS              |

| Workflow            | n8n, Node-RED, Temporal, Kestra |

| Policy              | OPA, Kyverno                    |

| Identity            | Keycloak, OpenFGA               |

| Dashboards          | Grafana, OpenSearch Dashboards  |



---



# Additional Strong Open-Source Options



## SOAR / Automation



* [Shuffle](https://github.com/Shuffle/Shuffle)

* [StackStorm](https://github.com/StackStorm/st2)

* [n8n](https://github.com/n8n-io/n8n)

* [Node-RED](https://github.com/node-red/node-red)

* [Windmill](https://github.com/windmill-labs/windmill)

* [Kestra](https://github.com/kestra-io/kestra)

* [Temporal](https://github.com/temporalio/temporal)

* [Rundeck](https://github.com/rundeck/rundeck)

* [Apache Airflow](https://github.com/apache/airflow)

* [Dagster](https://github.com/dagster-io/dagster)

* [Argo Workflows](https://github.com/argoproj/argo-workflows)

* [Ansible](https://github.com/ansible/ansible)

* [Salt](https://github.com/saltstack/salt)



## Incident Response



* [TheHive](https://github.com/TheHive-Project/TheHive)

* [DFIR-IRIS](https://github.com/dfir-iris/iris-web)

* [Cortex](https://github.com/TheHive-Project/Cortex)

* [GRR](https://github.com/google/grr)

* [Velociraptor](https://github.com/Velocidex/velociraptor)

* [osquery](https://github.com/osquery/osquery)



## Threat Intelligence



* [MISP](https://github.com/MISP/MISP)

* [OpenCTI](https://github.com/OpenCTI-Platform/opencti)

* [Yeti](https://github.com/yeti-platform/yeti)

* [IntelOwl](https://github.com/intelowlproject/IntelOwl)

* [SpiderFoot](https://github.com/smicallef/spiderfoot)

* [OpenBAS](https://github.com/OpenBAS-Platform/openbas)



## Detection



* [Wazuh](https://github.com/wazuh/wazuh)

* [Suricata](https://github.com/OISF/suricata)

* [Zeek](https://github.com/zeek/zeek)

* [Falco](https://github.com/falcosecurity/falco)

* [Tetragon](https://github.com/cilium/tetragon)

* [Sigma](https://github.com/SigmaHQ/sigma)

* [YARA](https://github.com/VirusTotal/yara)



## Security Testing



* [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)

* [MITRE Caldera](https://github.com/mitre/caldera)

* [Infection Monkey](https://github.com/guardicore/monkey)

* [OpenBAS](https://github.com/OpenBAS-Platform/openbas)



## Malware Analysis



* [CAPE](https://github.com/kevoreilly/capemon)

* [Cuckoo Sandbox](https://github.com/cuckoosandbox/cuckoo)

* [YARA](https://github.com/VirusTotal/yara)



---



# Commercial Platform → Open-Source Equivalents



| Commercial / Hosted Platform          | Closest Open-Source Options               | Notes                                      |

| ------------------------------------- | ----------------------------------------- | ------------------------------------------ |

| **Cortex XSOAR**                      | Shuffle + TheHive + Cortex + MISP/OpenCTI | Strong modular replacement                 |

| **Demisto**                           | Shuffle + TheHive + Cortex                | Demisto is the predecessor of Cortex XSOAR |

| **Splunk SOAR**                       | Shuffle + StackStorm + Wazuh/OpenSearch   | Add SIEM and workflow components           |

| **Tines**                             | Shuffle + n8n + Node-RED                  | Strong workflow-oriented alternatives      |

| **Torq**                              | Shuffle + n8n + Temporal + StackStorm     | Event-driven automation                    |

| **Swimlane**                          | Shuffle + TheHive + DFIR-IRIS             | Workflow + case-management combination     |

| **DFLabs IncMan**                     | TheHive + DFIR-IRIS + Shuffle             | Incident-response oriented                 |

| **Google SOAR**                       | Shuffle + TheHive + Cortex + OpenCTI      | Strong modular alternative                 |

| **Siemplify**                         | Shuffle + TheHive + Cortex                | Siemplify is now part of Google SecOps     |

| **FortiSOAR**                         | Shuffle + StackStorm + Ansible            | Strong orchestration combination           |

| **IBM QRadar SOAR**                   | TheHive + DFIR-IRIS + Shuffle             | Case management + automation               |

| **Rapid7 InsightConnect**             | StackStorm + n8n + Shuffle                | Workflow-oriented                          |

| **Sumo Logic Cloud SOAR**             | Shuffle + TheHive + OpenCTI               | Cloud-independent open stack               |

| **Cyware Orchestrate**                | Shuffle + MISP + OpenCTI                  | Strong CTI-oriented combination            |

| **Microsoft Sentinel SOAR**           | Shuffle + StackStorm + Wazuh              | Add SIEM/workflow components               |

| **ServiceNow SecOps**                 | TheHive + DFIR-IRIS + n8n                 | Case/workflow alternative                  |

| **D3 Smart SOAR**                     | Shuffle + StackStorm + Temporal           | Workflow-centric alternative               |

| **Standalone SOAR**                   | Shuffle                                   | Closest direct OSS starting point          |

| **Security case management**          | TheHive / DFIR-IRIS                       | Strong open-source options                 |

| **Threat-intelligence orchestration** | MISP + OpenCTI + Cortex                   | Mature open-source combination             |



---



# Frameworks for Building Custom SOAR Platforms



A serious open-source SOAR platform can be assembled from several layers.



## 1. Event Ingestion



Sources:



```text

SIEM

EDR

XDR

Firewall

IDS

Email Security

Cloud Security

IAM

Threat Intelligence

Vulnerability Scanner

Ticketing

User Reports

```



Possible open-source components:



* Wazuh

* Suricata

* Zeek

* OpenSearch

* MISP

* OpenCTI

* TheHive

* DFIR-IRIS



---



# 2. Orchestration Engine



Choose one:



```text

Shuffle

StackStorm

Temporal

n8n

Node-RED

Windmill

Kestra

Argo Workflows

Rundeck

```



---



# 3. Case Management



```text

TheHive

DFIR-IRIS

```



---



# 4. Threat Intelligence



```text

MISP

OpenCTI

Yeti

IntelOwl

Cortex

```



---



# 5. Endpoint Response



```text

Velociraptor

osquery

GRR

Wazuh

```



---



# 6. Network Response



```text

Suricata

Zeek

pfSense

OPNsense

iptables/nftables

Cilium

```



---



# 7. Identity Response



A SOAR platform can automate:



```text

Disable User

Reset Password

Revoke Sessions

Revoke Tokens

Force MFA

Remove Group Membership

```



Possible open-source identity systems:



* [Keycloak](https://github.com/keycloak/keycloak)

* [Authentik](https://github.com/goauthentik/authentik)

* [OpenFGA](https://github.com/openfga/openfga)



---



# 8. Cloud Response



A playbook can automatically:



```text

Disable IAM key

Quarantine instance

Modify security group

Revoke session

Block IP

Create snapshot

Collect logs

```



Potential automation components:



* AWS CLI

* Azure CLI

* Google Cloud CLI

* Terraform

* OpenTofu

* Ansible



---



# 9. Communication



SOAR systems frequently integrate:



* Slack

* Mattermost

* Rocket.Chat

* Microsoft Teams

* email

* PagerDuty

* Opsgenie

* ticketing systems



Open-source communication alternatives include:



* [Mattermost](https://github.com/mattermost/mattermost)

* [Rocket.Chat](https://github.com/RocketChat/Rocket.Chat)



---



# 10. Policy & Authorization



Use:



* [Open Policy Agent](https://github.com/open-policy-agent/opa)

* [Kyverno](https://github.com/kyverno/kyverno)

* [OpenFGA](https://github.com/openfga/openfga)

* [Keycloak](https://github.com/keycloak/keycloak)



Example:



```text

IF severity = CRITICAL

AND action = endpoint_isolation

AND environment = production

THEN

    require analyst approval

```



---



# Reference Architecture



```mermaid

flowchart TD



    SIEM[SIEM / XDR]



    EDR[EDR / Endpoint]



    NET[Network Detection]



    EMAIL[Email Security]



    CLOUD[Cloud Security]



    IAM[Identity]



    TI[Threat Intelligence]



    INGEST[Event Ingestion]



    SOAR[SOAR Orchestrator]



    PLAYBOOK[Playbook Engine]



    ENRICH[Enrichment]



    DECISION[Decision / Policy]



    CASE[Case Management]



    RESPONSE[Response Actions]



    AUDIT[Audit / Evidence]



    DASH[Dashboard]



    SIEM --> INGEST

    EDR --> INGEST

    NET --> INGEST

    EMAIL --> INGEST

    CLOUD --> INGEST

    IAM --> INGEST

    TI --> INGEST



    INGEST --> SOAR

    SOAR --> PLAYBOOK



    PLAYBOOK --> ENRICH

    ENRICH --> DECISION



    DECISION --> CASE

    DECISION --> RESPONSE



    RESPONSE --> EDR

    RESPONSE --> NET

    RESPONSE --> IAM

    RESPONSE --> CLOUD

    RESPONSE --> EMAIL



    CASE --> AUDIT

    RESPONSE --> AUDIT



    AUDIT --> DASH

```



---



# Typical SOAR Workflow



```mermaid

flowchart LR



    ALERT[Security Alert]



    NORMALIZE[Normalize]



    ENRICH[Enrich]



    CORRELATE[Correlate]



    SCORE[Risk Score]



    DECIDE[Decision]



    RESPOND[Response]



    CASE[Create / Update Case]



    AUDIT[Audit]



    CLOSE[Close]



    ALERT --> NORMALIZE

    NORMALIZE --> ENRICH

    ENRICH --> CORRELATE

    CORRELATE --> SCORE

    SCORE --> DECIDE

    DECIDE --> RESPOND

    RESPOND --> CASE

    CASE --> AUDIT

    AUDIT --> CLOSE

```



---



# Alert Enrichment Workflow



```mermaid

flowchart TD



    ALERT[Incoming Alert]



    IOC[Extract IOC]



    TYPE[Determine IOC Type]



    CORTEX[Cortex]



    MISP[MISP]



    OPENCTI[OpenCTI]



    INTEL[Threat Intelligence]



    SCORE[Risk Score]



    CASE[Update Case]



    ALERT --> IOC

    IOC --> TYPE



    TYPE --> CORTEX

    TYPE --> MISP

    TYPE --> OPENCTI



    CORTEX --> INTEL

    MISP --> INTEL

    OPENCTI --> INTEL



    INTEL --> SCORE

    SCORE --> CASE

```



---



# Automated Incident Response Workflow



```mermaid

flowchart TD



    ALERT[High Severity Alert]



    VERIFY[Verify Alert]



    ENRICH[Enrich]



    DECISION{Confirmed Incident?}



    CASE[Create Case]



    ISOLATE[Isolate Endpoint]



    DISABLE[Disable Account]



    BLOCK[Block IOC]



    COLLECT[Collect Evidence]



    NOTIFY[Notify SOC]



    CLOSE[Close / Escalate]



    ALERT --> VERIFY

    VERIFY --> ENRICH

    ENRICH --> DECISION



    DECISION -->|No| CLOSE

    DECISION -->|Yes| CASE



    CASE --> ISOLATE

    CASE --> DISABLE

    CASE --> BLOCK

    CASE --> COLLECT



    ISOLATE --> NOTIFY

    DISABLE --> NOTIFY

    BLOCK --> NOTIFY

    COLLECT --> NOTIFY



    NOTIFY --> CLOSE

```



---



# Threat Intelligence Workflow



```mermaid

flowchart LR



    IOC[IOC]



    MISP[MISP]



    OPENCTI[OpenCTI]



    CORTEX[Cortex]



    INTELOWL[IntelOwl]



    VT[Threat Intelligence APIs]



    SCORE[Risk Scoring]



    SIEM[SIEM]



    SOAR[SOAR]



    IOC --> MISP

    IOC --> OPENCTI

    IOC --> CORTEX

    IOC --> INTELOWL

    IOC --> VT



    MISP --> SCORE

    OPENCTI --> SCORE

    CORTEX --> SCORE

    INTELOWL --> SCORE

    VT --> SCORE



    SCORE --> SIEM

    SCORE --> SOAR

```



---



# Phishing Response Workflow



```mermaid

flowchart TD



    EMAIL[Reported Phishing Email]



    PARSE[Parse Email]



    IOC[Extract URLs / Domains / Hashes]



    TI[Threat Intelligence]



    MALWARE[Sandbox / Malware Analysis]



    DECISION{Malicious?}



    DELETE[Delete Similar Emails]



    BLOCK[Block IOC]



    CASE[Create Incident]



    USER[Notify User]



    REPORT[Security Report]



    EMAIL --> PARSE

    PARSE --> IOC

    IOC --> TI

    TI --> MALWARE

    MALWARE --> DECISION



    DECISION -->|No| REPORT

    DECISION -->|Yes| CASE



    CASE --> DELETE

    CASE --> BLOCK

    CASE --> USER



    DELETE --> REPORT

    BLOCK --> REPORT

    USER --> REPORT

```



---



# Endpoint Isolation Workflow



```mermaid

flowchart TD



    ALERT[EDR Alert]



    ENRICH[Threat Intelligence]



    SCORE[Risk Score]



    DECISION{High Risk?}



    APPROVAL{Approval Required?}



    ISOLATE[Isolate Endpoint]



    COLLECT[Collect Forensics]



    ANALYZE[Analyze]



    REMEDIATE[Remediate]



    RESTORE[Restore Endpoint]



    CLOSE[Close Case]



    ALERT --> ENRICH

    ENRICH --> SCORE

    SCORE --> DECISION



    DECISION -->|No| CLOSE

    DECISION -->|Yes| APPROVAL



    APPROVAL -->|Yes| ISOLATE

    APPROVAL -->|No| ISOLATE



    ISOLATE --> COLLECT

    COLLECT --> ANALYZE

    ANALYZE --> REMEDIATE

    REMEDIATE --> RESTORE

    RESTORE --> CLOSE

```



---



# SOAR Playbook Structure



A reusable playbook can be represented as:



```text

playbook/

│

├── trigger

│

├── normalize

│

├── enrich

│   ├── reputation

│   ├── threat-intelligence

│   └── asset-context

│

├── decision

│   ├── severity

│   ├── confidence

│   └── business-impact

│

├── approval

│

├── response

│   ├── isolate

│   ├── block

│   ├── disable

│   └── revoke

│

├── evidence

│

├── notification

│

└── close

```



---



# SOAR Playbook Categories



A mature SOC can automate many recurring workflows.



## Identity



```text

Impossible Travel

Brute Force

MFA Fatigue

Compromised Account

Privilege Escalation

Suspicious OAuth Application

```



## Endpoint



```text

Malware

Ransomware

Suspicious Process

EDR Alert

Persistence

Credential Dumping

```



## Network



```text

C2 Communication

Port Scan

DNS Tunneling

Malicious IP

Lateral Movement

```



## Email



```text

Phishing

Malicious Attachment

Malicious URL

Business Email Compromise

Credential Harvesting

```



## Cloud



```text

Exposed Storage

Compromised IAM

Suspicious API Call

Public Security Group

Cryptomining

```



---



# SOAR Automation Levels



A useful maturity model is:



```text

Level 1

---------

Manual response



        ↓



Level 2

---------

Enrichment automation



        ↓



Level 3

---------

Workflow automation



        ↓



Level 4

---------

Decision automation



        ↓



Level 5

---------

Automated response



        ↓



Level 6

---------

Cross-platform orchestration



        ↓



Level 7

---------

Adaptive / AI-assisted automation



        ↓



Level 8

---------

Agentic SOC

```



Automation should increase only when the organization has sufficient confidence, testing, observability and rollback capability.



---



# Human-in-the-Loop Automation



Not every response should be fully automatic.



A mature SOAR architecture can implement:



```text

Low Risk

   ↓

Automatic



Medium Risk

   ↓

Analyst Approval



High Risk

   ↓

Senior Approval



Critical

   ↓

Emergency Response

```



Example:



```text

Block malicious IP

        ↓

Automatic



Disable production administrator

        ↓

Human approval



Delete cloud infrastructure

        ↓

Multiple approvals

```



This reduces the risk of an incorrect automated decision causing a production outage.



---



# SOAR Audit Trail



Every automated action should ideally record:



```text

Incident ID

Playbook ID

Playbook Version

Trigger

Timestamp

Analyst

Automation

Action

Target

Result

Approval

Error

Rollback

```



Example:



```json

{

  "incident": "INC-2026-00124",

  "playbook": "phishing-response",

  "version": "3.2",

  "action": "isolate_endpoint",

  "target": "HOST-001",

  "approved_by": "analyst@example",

  "status": "success"

}

```



---



# SOAR Failure Handling



Automation must assume that integrations fail.



```mermaid

flowchart TD



    ACTION[Execute Action]



    SUCCESS{Successful?}



    RETRY[Retry]



    FALLBACK[Fallback Action]



    ESCALATE[Escalate to Analyst]



    AUDIT[Record Failure]



    ACTION --> SUCCESS



    SUCCESS -->|Yes| AUDIT

    SUCCESS -->|No| RETRY



    RETRY --> SUCCESS



    RETRY -->|Repeated Failure| FALLBACK



    FALLBACK --> ESCALATE

    ESCALATE --> AUDIT

```



Possible failure modes include:



```text

API timeout

Rate limit

Authentication failure

Expired token

Invalid IOC

Target unavailable

Permission denied

Partial execution

Rollback failure

```



---



# Capability Matrix



| Capability          | Cortex XSOAR | Splunk SOAR |            Tines |             Torq |         Swimlane |            Shuffle |       StackStorm |          TheHive |        DFIR-IRIS |

| ------------------- | -----------: | ----------: | ---------------: | ---------------: | ---------------: | -----------------: | ---------------: | ---------------: | ---------------: |

| SOAR orchestration  |            ✅ |           ✅ |                ✅ |                ✅ |                ✅ |                  ✅ |                ✅ |               ⚠️ |               ⚠️ |

| Visual workflows    |            ✅ |           ✅ |                ✅ |                ✅ |                ✅ |                  ✅ |               ⚠️ |               ⚠️ |               ⚠️ |

| Security playbooks  |            ✅ |           ✅ |                ✅ |                ✅ |                ✅ |                  ✅ |                ✅ |               ⚠️ |               ⚠️ |

| Case management     |            ✅ |           ✅ |                ✅ |                ✅ |                ✅ |                 ⚠️ |               ⚠️ |                ✅ |                ✅ |

| Threat intelligence |            ✅ |           ✅ |                ✅ |                ✅ |                ✅ |   Via integrations | Via integrations | Via integrations | Via integrations |

| Observable analysis |            ✅ |    Via apps | Via integrations | Via integrations | Via integrations |   Via integrations | Via integrations |       Via Cortex | Via integrations |

| API automation      |            ✅ |           ✅ |                ✅ |                ✅ |                ✅ |                  ✅ |                ✅ |                ✅ |                ✅ |

| Webhooks            |            ✅ |           ✅ |                ✅ |                ✅ |                ✅ |                  ✅ |                ✅ |                ✅ |                ✅ |

| Python automation   |            ✅ |           ✅ |               ⚠️ |               ⚠️ |               ⚠️ |           Via apps |                ✅ | Via integrations | Via integrations |

| Approval workflows  |            ✅ |           ✅ |                ✅ |                ✅ |                ✅ |             Custom |           Custom |           Custom |           Custom |

| RBAC                |            ✅ |           ✅ |                ✅ |                ✅ |                ✅ | Limited / evolving |                ✅ |                ✅ |                ✅ |

| Audit trail         |            ✅ |           ✅ |                ✅ |                ✅ |                ✅ |                  ✅ |                ✅ |                ✅ |                ✅ |

| Open source         |            ❌ |           ❌ |                ❌ |                ❌ |                ❌ |                  ✅ |                ✅ |               ✅* |                ✅ |

| Self-hosted         |            ✅ |           ✅ |                ❌ |                ❌ |                ✅ |                  ✅ |                ✅ |               ✅* |                ✅ |

| SIEM integration    |            ✅ |      Native |         Via APIs |         Via APIs |         Via APIs |                  ✅ |                ✅ | Via integrations | Via integrations |

| Endpoint response   |            ✅ |    Via apps | Via integrations | Via integrations | Via integrations |   Via integrations | Via integrations | Via integrations | Via integrations |

| Workflow engine     |       Native |      Native |           Native |           Native |           Native |             Native |           Native |          Limited |          Limited |



`*` Capabilities, licensing and deployment models can change; verify current project documentation before production deployment.



---



# Recommended Open-Source Stacks



## 1. Best Overall Open-Source SOAR Stack



```text

Wazuh

   +

Shuffle

   +

TheHive

   +

Cortex

   +

MISP

   +

OpenCTI

```



Architecture:



```text

Wazuh

  ↓

Shuffle

  ↓

Cortex / MISP / OpenCTI

  ↓

TheHive

  ↓

Response

```



This is one of the strongest starting points for a complete open-source SOC automation environment.



---



# 2. Enterprise-Style Open-Source SOC



```text

Wazuh

    +

Shuffle

    +

TheHive

    +

Cortex

    +

MISP

    +

OpenCTI

    +

Velociraptor

    +

Suricata

    +

Zeek

    +

DFIR-IRIS

    +

Keycloak

    +

OpenSearch

```



This provides:



* SIEM

* SOAR

* case management

* CTI

* endpoint response

* network detection

* investigation

* identity

* search



---



# 3. Lightweight SOAR



```text

Shuffle

   +

Wazuh

   +

TheHive

```



Excellent for:



* small SOCs

* labs

* universities

* MSSPs

* security research

* internal security teams



---



# 4. Threat-Intelligence-Centric SOC



```text

MISP

   +

OpenCTI

   +

Cortex

   +

Shuffle

   +

TheHive

```



Strong for organizations where CTI and IOC enrichment are central to incident response.



---



# 5. Incident-Response-Centric SOC



```text

TheHive

   +

Cortex

   +

DFIR-IRIS

   +

Velociraptor

   +

Shuffle

```



Strong for:



* DFIR

* incident response

* endpoint investigations

* evidence collection

* case management



---



# 6. General-Purpose Automation Stack



```text

StackStorm

   +

Ansible

   +

TheHive

   +

MISP

   +

Wazuh

```



Useful when the SOC wants deep infrastructure automation rather than only security-specific playbooks.



---



# 7. Developer-Friendly Security Automation



```text

n8n

   +

Gitleaks

   +

Wazuh

   +

OpenCTI

   +

Slack / Mattermost

```



Useful when security engineering teams want low-code automation.



---



# 8. Kubernetes-Native SOAR



```text

Argo Workflows

      +

Wazuh

      +

OpenSearch

      +

OpenCTI

      +

MISP

      +

Kubernetes

```



Useful for cloud-native SOC environments.



---



# 9. Durable Security Automation



```text

Temporal

   +

TheHive

   +

Cortex

   +

MISP

   +

Velociraptor

```



Particularly useful when workflows can take hours or days and need durable state.



---



# 10. Maximum Open-Source Coverage



```text

                   ┌───────────────┐

                   │    Wazuh      │

                   │     SIEM      │

                   └───────┬───────┘

                           ↓

                   ┌───────────────┐

                   │    Shuffle    │

                   │     SOAR      │

                   └───────┬───────┘

                           ↓

             ┌─────────────┼─────────────┐

             ↓             ↓             ↓

          Cortex         MISP         OpenCTI

             │             │             │

             └─────────────┼─────────────┘

                           ↓

                      TheHive

                           ↓

             ┌─────────────┼─────────────┐

             ↓             ↓             ↓

       Velociraptor     Suricata        Zeek

             │             │             │

             └─────────────┼─────────────┘

                           ↓

                      Response

```



---



# Example SOC Repository



A complete open-source SOAR repository could look like:



```text

soc-automation/

│

├── playbooks/

│   ├── phishing/

│   ├── malware/

│   ├── ransomware/

│   ├── compromised-account/

│   ├── impossible-travel/

│   ├── suspicious-login/

│   ├── malicious-ip/

│   └── cloud-incident/

│

├── integrations/

│   ├── siem/

│   ├── edr/

│   ├── firewall/

│   ├── email/

│   ├── identity/

│   ├── cloud/

│   └── threat-intelligence/

│

├── enrichment/

│   ├── cortex/

│   ├── misp/

│   ├── opencti/

│   └── intelowl/

│

├── response/

│   ├── isolate-endpoint/

│   ├── disable-user/

│   ├── block-ip/

│   ├── quarantine-email/

│   └── revoke-token/

│

├── policies/

│   ├── approval.rego

│   ├── severity.rego

│   └── production.rego

│

├── tests/

│   ├── phishing/

│   ├── malware/

│   └── ransomware/

│

└── README.md

```



---



# Playbook-as-Code



SOAR platforms increasingly benefit from treating playbooks as version-controlled artifacts.



Example:



```yaml

name: suspicious_login_response



trigger:

  type: siem.alert

  severity:

    - high

    - critical



steps:



  - name: enrich_user

    action: identity.lookup



  - name: enrich_ip

    action: cortex.analyze



  - name: threat_intelligence

    action: misp.lookup



  - name: risk_score

    action: risk.calculate



  - name: approval

    condition: risk > 80



  - name: revoke_sessions

    action: identity.revoke_sessions



  - name: create_case

    action: thehive.create_case

```



Advantages:



* Git version control

* peer review

* testing

* rollback

* change history

* CI/CD

* reproducibility



---



# SOAR Testing



A mature SOAR environment should test playbooks before production.



```text

Playbook

   ↓

Unit Test

   ↓

Integration Test

   ↓

Simulation

   ↓

Staging

   ↓

Production

```



Useful testing components include:



* [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)

* [MITRE Caldera](https://github.com/mitre/caldera)

* [OpenBAS](https://github.com/OpenBAS-Platform/openbas)

* synthetic SIEM alerts

* mock APIs

* test tenants

* sandbox environments



---



# SOAR + MITRE ATT&CK



SOAR playbooks can map actions to MITRE ATT&CK techniques.



Example:



```text

Alert:

Credential Dumping



        ↓



ATT&CK:

T1003



        ↓



SOAR:

1. Enrich endpoint

2. Collect forensic artifacts

3. Isolate host

4. Identify account

5. Reset credentials

6. Search for lateral movement

7. Create case

```



This enables:



* coverage measurement

* response mapping

* detection engineering

* purple-team validation



---



# SOAR + Detection Engineering



The strongest SOC architecture closes the loop:



```mermaid

flowchart LR



    DETECT[Detection]



    ALERT[Alert]



    SOAR[SOAR]



    RESPONSE[Response]



    RESULT[Outcome]



    LEARN[Lessons Learned]



    RULE[Improve Detection]



    PLAYBOOK[Improve Playbook]



    DETECT --> ALERT

    ALERT --> SOAR

    SOAR --> RESPONSE

    RESPONSE --> RESULT



    RESULT --> LEARN

    LEARN --> RULE

    LEARN --> PLAYBOOK



    RULE --> DETECT

    PLAYBOOK --> SOAR

```



This transforms SOAR from a simple automation system into a **continuous security-operations improvement loop**.



---



# What Is Still Difficult to Reproduce in Open Source?



Even with Shuffle, StackStorm, TheHive, Cortex, MISP and OpenCTI, several commercial capabilities remain difficult to reproduce as one integrated product.



## 1. Huge Integration Ecosystems



Commercial platforms can provide large libraries of pre-built integrations, often covering:



```text

SIEM

EDR

XDR

Firewall

Email

IAM

Cloud

Threat Intelligence

Ticketing

Vulnerability

SASE

Network

Identity

SaaS

```



An open-source implementation often requires:



```text

API knowledge

+

Connector development

+

Authentication management

+

Testing

+

Maintenance

```



---



# 2. Enterprise Content Packs



Commercial SOAR platforms often provide pre-built:



```text

Playbooks

Integrations

Dashboards

Incident Types

Fields

Automations

Documentation

```



Open-source platforms may require the SOC to create and maintain much of this content.



---



# 3. Case Management + SOAR Integration



Commercial platforms typically unify:



```text

Alert

+

Case

+

Playbook

+

Investigation

+

Evidence

+

Response

+

Audit

```



Open source often requires multiple projects.



For example:



```text

Shuffle

+

TheHive

+

Cortex

+

MISP

```



---



# 4. High-Quality Integrations



An API connector is easy to write.



A production-grade connector must handle:



```text

Authentication

Rate limits

Pagination

Retries

Timeouts

Version changes

Errors

Permissions

Audit

Idempotency

```



This creates substantial long-term maintenance.



---



# 5. Enterprise RBAC



Complex organizations may require:



```text

SOC Analyst

Senior Analyst

Incident Commander

Threat Hunter

SOC Manager

Security Engineer

Platform Administrator

Auditor

```



with different permissions.



Open-source systems can implement this, but it often requires multiple components.



---



# 6. Compliance



Enterprise customers may require:



```text

SOC 2

ISO 27001

PCI DSS

HIPAA

NIST

FedRAMP

GDPR

```



Open-source software can support the technical controls, but deploying open-source software does not automatically make the resulting SOC compliant.



---



# 7. Agentic SOC



Modern commercial platforms increasingly add:



```text

AI Triage

AI Investigation

AI Playbook Generation

AI Decision Support

Autonomous Enrichment

Agentic Response

```



Reproducing this safely requires more than connecting an LLM to a workflow engine.



A production agentic SOC needs:



```text

Tool permissions

+

Guardrails

+

Confidence thresholds

+

Human approval

+

Audit

+

Rollback

+

Prompt security

+

Data isolation

```



---



# Why Open Source Is Interesting



The most interesting open-source opportunity is not simply to build another playbook editor.



It is to create a modular:



> **Open-Source Security Operations Automation Platform**



combining:



```text

Detection

+

Orchestration

+

Threat Intelligence

+

Case Management

+

Endpoint Response

+

Network Response

+

Identity Response

+

Cloud Response

+

Policy

+

Audit

```



A possible architecture is:



```text

                     Security Events

                           │

         ┌─────────────────┼─────────────────┐

         ↓                 ↓                 ↓

       Wazuh            Suricata            Zeek

         │                 │                 │

         └─────────────────┼─────────────────┘

                           ↓

                        Shuffle

                           │

             ┌─────────────┼─────────────┐

             ↓             ↓             ↓

          Cortex          MISP         OpenCTI

             │             │             │

             └─────────────┼─────────────┘

                           ↓

                       Decision

                           │

                  ┌────────┴────────┐

                  ↓                 ↓

              TheHive          DFIR-IRIS

                  │                 │

                  └────────┬────────┘

                           ↓

                       Response

                           │

          ┌────────────────┼────────────────┐

          ↓                ↓                ↓

      Velociraptor      Identity         Cloud

          │                │                │

          └────────────────┼────────────────┘

                           ↓

                         Audit

```



---



# Best Open-Source Projects by Use Case



| Use Case                     | Recommended Projects                    |

| ---------------------------- | --------------------------------------- |

| Direct SOAR                  | Shuffle, StackStorm                     |

| Security workflow automation | Shuffle, StackStorm, n8n                |

| Durable automation           | Temporal                                |

| Incident management          | TheHive, DFIR-IRIS                      |

| Observable analysis          | Cortex                                  |

| Threat intelligence          | MISP, OpenCTI, Yeti                     |

| Threat enrichment            | Cortex, IntelOwl, SpiderFoot            |

| SIEM                         | Wazuh, OpenSearch                       |

| Network detection            | Suricata, Zeek                          |

| Endpoint response            | Velociraptor, osquery, GRR              |

| Malware analysis             | CAPE, Cuckoo                            |

| Vulnerability management     | Greenbone / OpenVAS                     |

| Security testing             | Atomic Red Team, MITRE Caldera, OpenBAS |

| Infrastructure response      | Ansible, Salt, Rundeck                  |

| Low-code automation          | n8n, Node-RED, Shuffle                  |

| Kubernetes workflows         | Argo Workflows                          |

| Policy                       | OPA, Kyverno                            |

| Identity                     | Keycloak, OpenFGA                       |

| Dashboards                   | Grafana, OpenSearch Dashboards          |

| Communication                | Mattermost, Rocket.Chat                 |



---



# Recommended Open-Source Shortlist



If the objective is to build a serious open-source alternative to the commercial platforms listed at the beginning of this README, the first projects to investigate are:



## Tier 1 — Direct SOAR



1. [Shuffle](https://github.com/Shuffle/Shuffle)

2. [StackStorm](https://github.com/StackStorm/st2)



## Tier 2 — Incident Response



3. [TheHive](https://github.com/TheHive-Project/TheHive)

4. [DFIR-IRIS](https://github.com/dfir-iris/iris-web)

5. [Cortex](https://github.com/TheHive-Project/Cortex)



## Tier 3 — Threat Intelligence



6. [MISP](https://github.com/MISP/MISP)

7. [OpenCTI](https://github.com/OpenCTI-Platform/opencti)

8. [Yeti](https://github.com/yeti-platform/yeti)

9. [IntelOwl](https://github.com/intelowlproject/IntelOwl)



## Tier 4 — General Workflow Engines



10. [n8n](https://github.com/n8n-io/n8n)

11. [Node-RED](https://github.com/node-red/node-red)

12. [Windmill](https://github.com/windmill-labs/windmill)

13. [Kestra](https://github.com/kestra-io/kestra)

14. [Temporal](https://github.com/temporalio/temporal)

15. [Rundeck](https://github.com/rundeck/rundeck)



## Tier 5 — SOC Infrastructure



16. [Wazuh](https://github.com/wazuh/wazuh)

17. [Suricata](https://github.com/OISF/suricata)

18. [Zeek](https://github.com/zeek/zeek)

19. [Velociraptor](https://github.com/Velocidex/velociraptor)

20. [osquery](https://github.com/osquery/osquery)



---



# Practical Fully Open-Source Reference Stack



A serious open-source SOAR implementation could use:



```text

                           Wazuh

                             │

                             ↓

                          Shuffle

                             │

        ┌────────────────────┼────────────────────┐

        ↓                    ↓                    ↓

      Cortex                MISP                OpenCTI

        │                    │                    │

        └────────────────────┼────────────────────┘

                             ↓

                          TheHive

                             │

                ┌────────────┼────────────┐

                ↓            ↓            ↓

          Velociraptor    Identity       Cloud

                │            │            │

                └────────────┼────────────┘

                             ↓

                           Audit

                             ↓

                          Grafana

```



This provides a modular approximation of the capabilities found across:



* Cortex XSOAR

* Splunk SOAR

* Tines

* Torq

* Swimlane

* DFLabs

* Google Security Operations SOAR

* Siemplify

* FortiSOAR



without requiring a single proprietary SOAR platform.



---



# Open-Source SOAR Maturity Model



```text

                 OPEN-SOURCE SOC AUTOMATION



Level 1

Manual SOC

    ↓

Level 2

IOC Enrichment

    ↓

Level 3

Basic Playbooks

    ↓

Level 4

Incident Automation

    ↓

Level 5

Cross-Tool Orchestration

    ↓

Level 6

Automated Response

    ↓

Level 7

Policy-Governed Automation

    ↓

Level 8

Adaptive / AI-Assisted SOC

```



The most important transition is from:



```text

Automation

```



to:



```text

Controlled Automation

```



where every high-impact action has:



* authorization

* audit

* confidence

* rollback

* exception handling



---



# Conclusion



The SOAR ecosystem has evolved from traditional playbook automation into a broader security-operations automation layer.



The architecture can be understood as:



```text

                   SOAR

                    │

       ┌────────────┼────────────┐

       ↓            ↓            ↓

 Orchestration   Intelligence   Response

       │            │            │

    Shuffle       MISP        Velociraptor

    StackStorm    OpenCTI     Identity

    Temporal      Cortex      Firewall

    n8n            Yeti        Cloud

       │            │            │

       └────────────┼────────────┘

                    ↓

               Case Management

                    │

             ┌──────┴──────┐

             ↓             ↓

          TheHive       DFIR-IRIS

```



For organizations seeking an open-source alternative, there is no requirement to reproduce an entire commercial platform in one project.



A better strategy is to combine specialized components:



```text

Shuffle

+

TheHive

+

Cortex

+

MISP

+

OpenCTI

+

Wazuh

+

Velociraptor

+

Suricata

+

Zeek

```



The most important open-source projects to evaluate first are therefore:



> **Shuffle + StackStorm + TheHive + Cortex + MISP + OpenCTI + DFIR-IRIS + Wazuh + Velociraptor.**



The most interesting opportunity is to build a unified platform around these components that provides:



```text

Detect

 ↓

Normalize

 ↓

Enrich

 ↓

Correlate

 ↓

Investigate

 ↓

Decide

 ↓

Approve

 ↓

Respond

 ↓

Audit

 ↓

Learn

```



That architecture can provide a surprisingly capable open-source foundation for a modern SOC and can reproduce a substantial portion of the functionality traditionally associated with commercial SOAR platforms.



---



# How to Contribute



Useful contributions include:



* adding new SOAR integrations

* creating reusable playbooks

* adding SIEM integrations

* adding EDR integrations

* improving threat-intelligence connectors

* adding response actions

* documenting approval workflows

* creating automated tests

* adding MITRE ATT&CK mappings

* improving case-management integrations

* adding incident-response templates

* documenting deployment architectures

* adding Kubernetes deployments

* improving observability

* adding security policies

* documenting human-in-the-loop controls

* creating realistic SOC simulations



Pull requests are welcome.



---



# Disclaimer



This README is an ecosystem overview rather than a security certification, product endorsement or guarantee of production readiness.



Open-source availability, licensing, integrations and project activity can change.



Before deploying an open-source SOAR platform, evaluate:



* project maintenance

* license

* security posture

* authentication

* RBAC

* secrets management

* integration reliability

* API compatibility

* auditability

* workflow testing

* rollback capabilities

* failure handling

* scalability

* HA architecture

* data retention

* compliance requirements

* incident-response procedures



**SOAR automation can cause real operational changes.**



Actions such as:



```text

Disable Account

Isolate Endpoint

Block IP

Revoke Token

Delete Email

Modify Firewall

Terminate Cloud Instance

```



should therefore be protected by appropriate:



```text

Authentication

+

Authorization

+

Approval

+

Confidence

+

Audit

+

Rollback

```



> **Open source makes it possible to construct a powerful SOAR ecosystem from Shuffle, StackStorm, TheHive, Cortex, MISP, OpenCTI, DFIR-IRIS, Wazuh and many other projects. The greatest challenge is no longer simply executing automation—it is creating trustworthy, observable, policy-controlled automation that can safely act on production security incidents.**
