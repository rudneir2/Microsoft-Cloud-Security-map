# Microsoft cloud security services integrated (including Azure services, monitoring and Microsoft Defender services)

## Introduction

Microsoft has been working very hard to become the Company with the broadest and most intelligent set of Security solutions available on the Market. There are many facts and artifacts that prove that. From Security methodologies and frameworks like Zero Trust, Azure Security Benchmarks, Microsoft Compliance center, Azure public cloud Security services and Microsoft 365 Defender Security services, among many others, Microsoft delivers a complete set of Security solution to make your Company security posture much better!
From a threat perspective, Attackers has evolved along with new technologies and scenarios specially regarding public and hybrid cloud scenarios. You may have a very comprehensive understanding of how those threats works by looking at Mitre Att&ack matrix web page.
The idea of this architecture reference is putting Customer environment, threats, Azure Security services and Microsoft 365 Security services all together in an easy and simple way to understand how threats are related to Customer’s environment and how Security services works to protect Azure services, like Virtual Machines, Storage, Network, Application, Database, etc or Microsoft 365 services, like Office 365, Teams, OneDrive, etc and what are the Microsoft Security services that will provide an enhancement for a better security posture and threats mitigation.

![image](https://user-images.githubusercontent.com/97529152/151837839-ac8fde8c-bf34-4c7c-ab91-4bc755c63f6e.png)

## Potential use cases (how to use this diagram)

There are a couple of threats that are very common regardless of the industry segment, such as Ransonwares, DDOS attacks, Cross-site scripting, SQL injection, and much more. However, specific customers have specific concerns about a set of threats. This architecture reference may help you understand how to build several security layers for your environment and then combine multiple Microsoft security and monitoring services to work together and help you build out a security solution that will deliver a much better security posture.
This architecture reference will help you identify the best Microsoft security services combination for your main Security concerns.
It will also give you a big picture of Microsoft security services so that you can understand in an easy and simple way how they work together or in any combination you need.
Let’s review this Architecture reference for Microsoft cloud Security services in different steps so that you can understand all the elements on it.

## Customer environment and the most known threats

![image](https://user-images.githubusercontent.com/97529152/151838555-f69a1c45-0cb0-42e1-a3aa-4888fb936097.png)

It was considered on this diagram a very common Customer environment with an On-premises, Office 365 subscription and Azure subscription layer, also called hybrid environment. They were categorized according to the pillars of Microsoft Zero Trust: Network, Infrastructure, Endpoint, Application, Data and Identity. 
https://www.microsoft.com/en-us/security/business/zero-trust

In the bottom of the Architecture diagram, we have some of the most known cybersecurity threats used by Attackers in order to compromise Companies environment with malicious codes, phishing emails, malwares, Denial of Services (DOS) attacks and other attack vectors. They were categorized according to Tactics and Technics published by Mitre Att&ck matrix. 
https://attack.mitre.org/

### Components

1.	on-premises: it was considered in the diagram basic services such as Servers (VMs), Network appliances and services, Applications, Database and File server and ADDS (Active Directory Domain Service) that handle user’s credentials.

2.	Ofiice 365 environment: this environment contains traditional office applications including Word, Excel, PowerPoint, Outlook, OneNote and depending on the the plan purchased, may also include other apps such as OneDrive, Exchange, Sharepoint and Teams. It is represented on this diagram for an unique logo plus Azure AD, a cloud identity provider that is required to run Office 365.

3.	For Azure environment: this is the public cloud service that contains services very similar to on-premises, like Servers (VMs), Workstations (VDI), Network components (basically Virtual), services called PaaS like Web Apps, Databases and Storage service, where Companies don’t have to manage physical devices and Azure AD. This Azure AD will provide identity credentials for Azure services users, and it can be the same Azure AD used with Office 365. Azure AD is also called Azure Tenant.

4.	Most Common threats: the diagram represents only a few examples of threats. They are categorized according to Mitre Att&ck matrix. Attackers may use a specific threat to compromise a customer environment or use a combination of several threats, also called blended attack.

## Azure Security Services

Azure public cloud counts with several different Security services that protect its Network, Compute, Storage, Applications, Databases, and Identity services. An interesting fact is that some of them are free of costs, such as NSG (Network Security Group), Storage encryption, TLS/SSL, SAS token, and many others.

![image](https://user-images.githubusercontent.com/97529152/151838729-cbdb835b-3848-466d-b439-7380689fa8d7.png)

### Components

1.	Those Security services are “mapped” through Azure Security Benchmarks, currently in the version 3. The Azure Security Benchmark provides prescriptive best practices and recommendations to help improve the security of workloads, data, and services on Azure. The diagram shows a subset of those Azure security services and its control number according to Azure Security Benchmark reference page.
https://docs.microsoft.com/en-us/security/benchmark/azure/overview

2.	Azure Security services may also be found through Azure Security Baselines for specific Azure services. For example, if you want to understand how to apply Security to Azure Virtual Network or Azure Virtual Machines, you will find a specific set of recommended Security services for those specific services. This link shows an example of all Security services and best practices available for a Windows Virtual Machine.
https://docs.microsoft.com/en-us/security/benchmark/azure/baselines/virtual-machines-windows-security-baseline

## Microsoft 365 and Microsoft 365 Defender Security services

First off, Let’s demystify a couple of names regarding Microsoft and Office services.

Microsoft 365 and Office 365 are cloud-based services designed to help meet your organization's needs for robust security, reliability, and user productivity.
Microsoft 365 includes services like Power Automate, Forms, Stream, Sway and Office 365.

Office 365 includes several known services like Word, Excel, PowerPoint, Outlook, OneNote, SharePoint, Teams and OneDrive
Depending on the license you acquire for Microsoft 365 (https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-platform-service-description/office-365-plan-options), you may also get the Security services for Microsoft 365. These set of Security services are also called Microsoft 365 Defender. 

It is part of Microsoft 365 Defender:
- Microsoft Defender for Endpoint
- Microsoft Defender for Identity
- Microsoft Defender for Office 365
- Microsoft Defender for Cloud Apps

![image](https://user-images.githubusercontent.com/97529152/151839057-0975df46-6dc4-45d7-bff1-702a1ec6bb02.png)

### Components

1.	Microsoft Defender for endpoint
Microsoft Defender for Endpoint is an enterprise endpoint security platform designed to help enterprise networks prevent, detect, investigate, and respond to advanced threats. It will create a layer of protection for VMs running on Azure and on-premises. For more details about what it may protect, see it here: https://docs.microsoft.com/en-us/microsoft-365/security/defender-endpoint/microsoft-defender-endpoint?view=o365-worldwide

2.	Microsoft Defender for Cloud Apps
Microsoft Defender for Cloud Apps (formerly known as Microsoft Cloud Application Security or simply MCAS) is a Cloud Access Security Broker (CASB) that supports various deployment modes including log collection, API connectors, and reverse proxy. It provides rich visibility, control over data travel, and sophisticated analytics to identify and combat cyberthreats across all your Microsoft and third-party cloud services. In other words, it is going to provide protection and risk mitigation for Cloud Apps or even for some Apps running on-premises. It will also provide a protection layer for users that access those Apps.

It is very important not confuse it with the “Microsoft Defender for Cloud” that is a solution from Azure, formerly known as Azure Security Center, which provides recommendation and a security posture score for Servers, Apps, Storage accounts and other Azure resources. 
See more details on that page: https://docs.microsoft.com/en-us/defender-cloud-apps/what-is-defender-for-cloud-apps

3.	Microsoft Defender for Office 365
Microsoft Defender for Office 365 safeguards your organization against malicious threats posed by email messages, links (URLs), and collaboration tools. It will provide protection for email and collaboration. Depending on the license you have, you will be able to add post-breach investigation, hunting, and response, as well as automation, and simulation (for training). You may see more about the license options on this website: https://docs.microsoft.com/en-us/microsoft-365/security/office-365-security/overview?view=o365-worldwide

4.	Microsoft Defender for Identity
Microsoft Defender for Identity (formerly Azure Advanced Threat Protection, also known as Azure ATP) is a cloud-based security solution that leverages your on-premises Active Directory signals to identify, detect, and investigate advanced threats, compromised identities, and malicious insider actions directed at your organization. It will protect ADDS (Active Directory Domains Services) running on-premises. Even though this service runs on the cloud, it works to protect Identities on-premises.
If you need protection for identities provided by Azure AD, that runs natively on the cloud, you will have to consider Azure AD Identity Protection service.
See more details on that page: https://docs.microsoft.com/en-us/defender-for-identity/what-is

5.	Microsoft Endpoint Manager
Microsoft Endpoint Manager provides services for cloud and on-premises, including multiple services such as Microsoft Intune that allows you control features and settings on Android, Android Enterprise, iOS/iPadOS, macOS, and Windows 10 and 11 devices. It integrates with other services, including Azure Active Directory (AD), mobile threat defenders, ADMX templates, Win32 and custom LOB apps, and more.

Another known service that is now part of Microsoft Endpoint Manager is Configuration Manager, an on-premises management solution, that allow you to manage desktops, servers, and laptops that are on your network or internet-based. You can cloud-enable it to integrate with Intune, Azure Active Directory (AD), Microsoft Defender for Endpoint, and other cloud services. Use Configuration Manager to deploy apps, software updates, and operating systems. You can also monitor compliance, query, and act on clients in real time, and much more.
There are still other services that are part of Microsoft Endpoint Manager. To see all of them, look at this website: https://docs.microsoft.com/en-us/mem/endpoint-manager-overview

## Azure Monitoring services

Monitoring on Azure may seem confused at first sight, but they are not. Each Microsoft Azure monitoring service has its own importance in the entire Microsoft Security and Monitoring strategy.
There is couple of important services that will be presented in the next Architecture diagram. Some of those services are focused on capturing information from specific services such as network or apps. Some of them are core services, I mean, they can collect information from different services no matter what they are.

Those are the services:
- Log Analytics
- Azure Monitor
- Microsoft Defender for Cloud (aka Azure Security Center)
- Azure Sentinel
- Traffic Analytics (part of Network Watcher)
- Application Insights
- Storage Analytics






