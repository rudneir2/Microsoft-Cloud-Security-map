# Microsoft cloud security services integrated (including Azure services, monitoring and Microsoft Defender services)

## Introduction

Microsoft has been working very hard to become the Company with the broadest and most intelligent set of Security solutions available on the Market. There are many facts and artifacts that prove that. From Security methodologies and frameworks like Zero Trust, Azure Security Benchmarks, Microsoft Compliance center, Azure public cloud Security services and Microsoft 365 Defender Security services, among many others, Microsoft delivers a complete set of Security solution to make your Company security posture much better!
From a threat perspective, Attackers has evolved along with new technologies and scenarios specially regarding public and hybrid cloud scenarios. You may have a very comprehensive understanding of how those threats works by looking at Mitre Att&ack matrix web page.
The idea of this architecture reference is putting Customer environment, threats, Azure Security services and Microsoft 365 Security services all together in an easy and simple way to understand how threats are related to Customer’s environment and how Security services works to protect Azure services, like Virtual Machines, Storage, Network, Application, Database, etc or Microsoft 365 services, like Office 365, Teams, OneDrive, etc and what are the Microsoft Security services that will provide an enhancement for a better security posture and threats mitigation.

![image](https://user-images.githubusercontent.com/97529152/151837839-ac8fde8c-bf34-4c7c-ab91-4bc755c63f6e.png)

### Potential use cases (how to use this diagram)

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

![image](https://user-images.githubusercontent.com/97529152/151839345-941e00bc-21e2-42e0-be32-6ddd54f6227b.png)

### Components

1.	Azure Monitor will provide a collection of dashboards ready to be consumed and an Alert management system, among other things. You may check more about Azure Monitor services in this link: 
https://docs.microsoft.com/en-us/azure/azure-monitor/overview

2.	Microsoft Defender for Cloud (aka Azure Security Center) delivers a series of recommendations for VMs, Storage, Apps, etc, that helps you to be compliant with different regulatory standards such as ISO or PCI and at the same time offers a security score systems that helps you track how safe your environment are. See more about it in this link: 
https://docs.microsoft.com/en-us/azure/defender-for-cloud/defender-for-cloud-introduction

3.	Log analytics is definitely one of the most important services. It is the responsible for storing all the logs and alerts that will be used to create Alerts, Insights and Incidents. Basically, everything you ingest on Log Analytics will be available automatically to Azure Sentinel. You may check more about Log Analytics in this link: https://docs.microsoft.com/en-us/azure/azure-monitor/logs/log-analytics-overview

4.	Azure Sentinel works like a façade for Log Analytics. While log analytics stores all logs and alerts from different sources, like on-premises VMs, Azure VMs and Alerts from Microsoft 365 Defender Security services, among many others, Sentinel will offer APIs that will help to correlate all those logs so that you may have insights more accurately about what is going on in your environment avoiding false positives.
Azure Sentinel is the core of this whole Security and monitoring system that Microsoft Cloud offers.
More about Azure Sentinel: https://docs.microsoft.com/en-us/azure/sentinel/overview

### There are still a couple of others Monitoring services focused on specific resources. 

5.	Network Watcher provides tools to monitor, diagnose, view metrics, and enable or disable logs for resources in an Azure virtual network.
https://docs.microsoft.com/en-us/azure/network-watcher/network-watcher-monitoring-overview

6. 	Traffic Analytics, part of Network Watcher, works on top of NSG (Network Security Group) logs and offer lots of nice dashboards that are capable of agreeing different metrics from outbound and inbound connection in your Azure Virtual Network.
https://docs.microsoft.com/en-us/azure/network-watcher/traffic-analytics

7.	Application Insights, that is part of Azure Monitor, is focused on the application and provides extensible application performance management (APM) and monitoring for live web apps, including support for a wide variety of platform such as NET, Node.js, Java, and Python. See more about Application Insights in this website: 
https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview

8.	Azure Storage Analytics is a Storage service that is going to perform logging and provides metrics data for a storage account. You can use this data to trace requests, analyze usage trends, and diagnose issues with your storage account. See more about this service in this link:
https://docs.microsoft.com/en-us/azure/storage/common/storage-analytics

So, in this Architecture you see all those services together: Customer environment, Threats, Azure Security Services, Microsoft Defender Security Services and Azure Monitor services.

The key point in this architecture is Azure Sentinel as the solution that is going to connect all the logs and alerts provided by Azure Security Services, Microsoft Defender and Azure Monitor services.

It is out of scope on this document covering Sentinel in detail, however, just in a nutshell, after you have Sentinel implemented and receiving logs and alerts from all the sources we talked about it, the next step is mapping a set of queries that will inquire those logs for insights and evidences of IOCs (Indicators of Compromise). Once something is captured by Sentinel you will be able to investigate it or automate an action to mitigate or solve the incident, such as blocking an user or blocking an IP address in your firewall.

See more about Sentinel in this link:
https://docs.microsoft.com/en-us/azure/sentinel/


## How to access Azure Security, Monitoring and Microsoft 365 Defender services

As we covered many different Services, here it is information about how to access each of those Services:

**- Azure Security services**
All Azure Security services mentioned in the diagrams may be accessed through Azure Portal. Simply go to https://portal.azure.com and search for the service you are interested in.

### - Azure Monitor
Azure Monitor is a service that is available in all Azure subscription, so you only need to access Azure Portal at https://portal.azure.com and search for the service by typing “monitor”.

### Microsoft Defender for Cloud
Microsoft Defender for Cloud is also already available for anyone that access Azure Portal for the first time. To access it, go to Azure Portal at https://portal.azure.com and search for “Microsoft Defender for Cloud”.

### Log Analytics
To access Log Analytics, you will have to create the service as it doesn’t exist by default. Go to Azure Portal at https://portal.azure.com , search for “Log Analytics workspace” and then click on “Create”. After you create it, you will be able to access the service.

### Microsoft Sentinel
Azure Sentinel works on top of a Log Analytics workspace, so you will have to create first a Log Analytics workspace, then, search for “Sentinel” at Azure Portal, then create the service by choosing the Log Analytics workspace you want to have behind Microsoft Sentinel.

### Microsoft Defender for Endpoint
Microsoft Defender for Endpoint is part of Microsoft 365. You access the service through this URL: https://security.microsoft.com 
In the past you were able to access the service through https://securitycenter.windows.com 

### Microsoft Defender for Cloud Apps
Microsoft Defender for Endpoint is part of Microsoft 365. You access the service through this URL: https://portal.cloudappsecurity.com 

### Microsoft Defender for Office 365
Microsoft Defender for Office 365 is part of Microsoft 365. You access the service through this URL: https://security.microsoft.com that is the same portal used with Endpoint manager. In the past, you were able to access the service through https://protection.office.com 

### Microsoft Defender for Identity
Microsoft Defender for Identity is part of Microsoft 365. You access the service through this URL: https://portal.atp.azure.com . Remember, despite the fact that it is a cloud service, this service is responsible to protect Identities on-premises.

### Microsoft Endpoint Manager
Microsoft Endpoint Manager is the rebranded name for Intune, Configuration Manager and other services. You may access it through the portal https://endpoint.microsoft.com 

### Azure Network watcher
Azure Network watcher is part of Azure, so you just need to search for “Network watcher” at Azure portal,  https://portal.azure.com.

### Traffic Analytics
Traffic Analytics is part of Network watcher. You will find in the left menu once you start the Network watcher. It is a powerful Azure network monitor that works based on your Network Security Groups (NSG) implemented on your NICs or Subnets. To make it work, you will have to collect information from the NSGs. See it how to do it, in that document page: https://docs.microsoft.com/en-us/azure/network-watcher/network-watcher-nsg-flow-logging-portal

### Application Insight
Application Insight is part of Azure Monitor; however, you will have to create it in order to use it, according to the Application you want to monitor. For some applications built on Azure, such as Web Apps, you can create Application Insight directly from the Web Apps provisioning. So, to access it, you just need to search for “monitor” on Azure Portal, then, once in Monitor service, in the left menu, you will find “Applications”.

### Storage Analytics
Azure storage offers different types of storage under the same storage account technology. You may find blobs, files, table and queues on top of storage accounts. Storage analytics offers a broad range of metrics to use with those storages’ services. You will be able to access it, going to your Storage account at Azure Portal (https://portal.azure.com) , then setting “Diagnostic settings” on the left menu and choosing one log analytics workspace to send that information. Then, you may access some dashboard on “Insights” that you will see on the left menu. But you will also be able to access a series of workbooks on “workbooks” at the left menu, Metrics and Alerts for your storage account. Everything will be inside your storage account being monitored, in the left menu.


## How is the pricing for Microsoft Security services

Best way to get any of the Azure Security services prices is visiting Azure pricing calculator at https://azure.microsoft.com/en-us/pricing/calculator/

You will have to search for the service you are interested in and click on it to get all the variables that you provide you the price for the service.
Microsoft 365 Defender security services works with licenses. The link below shows all licensing requirements for Microsoft 365 Defender services.
https://docs.microsoft.com/en-us/microsoft-365/security/defender/prerequisites?view=o365-worldwide

