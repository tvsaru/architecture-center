---
title: "Enterprise Cloud Adoption: Cloud Native - Security Management Policy"
description: What is Cloud Native - Security Management Policy?
author: BrianBlanchard
ms.date: 10/03/2018
---

# Enterprise Cloud Adoption: What is Cloud Native - Security Management Policy?

Security Management is one of the [Five Disciplines of Cloud Governance](../overview.md). This discipline focuses on general security topics including protection of the network, digital assets, data, etc... As outlined in the [policy review guide](policy-compliance/what-is-a-cloud-policy-review.md), the Enterprise Cloud Adoption framework is building out three levels of **sample policy** for each of the five disciplines: Cloud-Native, Enterprise, and Cloud Design Principle Compliant. This article is the Cloud-Native, Sample Policy for the Security Management Discipline.

> [!NOTE]
> Microsoft is in no position to dictate corporate or IT policy. This article is provided as a means of triggering thoughts during an internal policy review. It is assumed that this policy will be extended, validated, and tested against corporate policy before attempting to use a policy like this sample. Any use of this sample policy, as is, should be discouraged.

## Policy Alignment

This sample policy is meant to synthesize a Cloud Native scenario, meaning the tools and platforms provided by Azure are sufficient to mitigate business risks regarding a deployment. In this scenario, it is assumed that simple configuration of the default Azure services will provide sufficient asset protection.

## Cloud security and compliance

Security is integrated into every aspect of Azure, offering unique security advantages derived from global security intelligence, sophisticated customer-facing controls, and a secure, hardened infrastructure. This powerful combination helps protect your applications and data, support your compliance efforts, and provide cost-effective security for organizations of all sizes. This approach creates a strong starting position for any security policy, but does not negate the need for equally strong security practices related to the security services being used.

### Built-in security controls

It’s hard to maintain a strong security posture when security controls are not intuitive and need to be configured separately. Azure includes built-in security controls across a breadth of services that help you protect data and workloads quickly and manage risk across hybrid environments. Integrated partner solutions let you easily transition existing protections to the cloud.

### Cloud Native Identity Policies

Identity is becoming the new boundary layer for security, taking over that role from the traditional network-centric perspective. Network perimeters have become increasingly porous, and that perimeter defense cannot be as effective as it was before the explosion of bring your own device (BYOD) and cloud applications. Azure identity management and access control enable seamless, secure access to all your apps. 

A sample cloud native policy for Identity across cloud and on-premises directories, could include requirements like the following:

* Authorized access to resources with role-based access, multi-factor authentication, and single sign-on
* Quick mitigation of user identities suspected of compromise
* Just-in-time, just-enough access granted on a task-by-task basis to limit exposure of over-privileged admin credentials
* Extended user identity and access to policies across multiple environments through Azure Active Directory

While it is important to understand [Identity Management](../identity-management/) in the context of Security Management, the [Five Disciplines of Cloud Governance](../overview.md) calls out [Identity Management](../identity-management/) as its own discipline, separate from security management. 

### Network Access Policies

Network control includes the configuration, management, and securing of network elements such as virtual networking, load balancing, DNS, and gateways. The controls provide a means for services to communicate and interoperate. Azure includes a robust and secure networking infrastructure to support your application and service connectivity requirements. Network connectivity is possible between resources located in Azure, between on-premises and Azure hosted resources, and to and from the internet and Azure.

A cloud native policy for Network Controls might include requirements like the following:

* Hybrid connections to on-prem resources (While technically possible in Azure), might not be allowed in a cloud native policy. Should a hybrid connection prove neccessary, a more robust Enterprise Security Policy sample would be a more relevent reference
* Users can establish secure connections to and within Azure using virtual networks and network security groups
* Native Windows Azure Firewall protects hosts from malicious network traffic by limited port access. A good example of this policy would be the requirement to block (or not enable) traffic directly to a VM over RDP - TCP/UDP port 3389
* Services like Web Application Firewall and Azure DDoS Protection safeguard and ensure app availability safeguards for virtual machines running in azure. These features should not be disabled or misused.

### Data protection

One of the keys to data protection in the cloud is accounting for the possible states in which your data may occur, and what controls are available for each state. For the purpose of Azure data security and encryption best practices, recommendations focus on the following data states:

* Data encryption controls are built into services from virtual machines to storage and SQL Database
* As data moves between clouds and customers, it can be protected using industry-standard encryption protocols
* Azure Key Vault enables users to safeguard and control cryptographic keys and other secrets used by cloud apps and services
* Azure Information Protection will help classify, label, and protect your sensitive data in apps

While these features are built into Azure, each of the above requires configuration and could increase costs. Alignment of each Cloud Native feature with a [data classification strategy](what-is-date-governance.md) is highly suggested.

### Security Monitoring

Security monitoring is a proactive strategy that audits your resources to identify systems that do not meet organizational standards or best practices. Azure Security Center provides unified security management and advanced threat protection across hybrid cloud workloads. With Security Center, you can apply security policies across your workloads, limit your exposure to threats, and detect and respond to attacks, including:

* Unified view of security across all on-premises and cloud workloads with Azure Security Center
* Continuous monitoring and security assessments to ensure compliance and remediate any vulnerabilities
* Interactive tools and contextual threat intelligence for streamlined investigation
* Extensive logging and integration with existing security information

### Extending Cloud Native Policies

Using the cloud can take some of the security burden off your shoulders. Microsoft provides physical security for Azure datacenters and helps protect the cloud platform against infrastructure threats such as a DDoS attack. Given that Microsoft has thousands of cybersecurity specialists working on security every day, the resources brought to bear against attackers are considerable. In fact, while organizations once worried about whether the cloud was secure, most now understand that given the level of investment that vendors such as Microsoft make in people and specialized infrastructure, the cloud is actually more secure than most on-premises datacenters.

Even with this investment in Cloud Native Security Management, it is suggested that any Security Management policy extend the default Cloud Native policies. The following are examples of extended policies that should be considered, even in a Cloud Native environment:

* Secure VMs. Security should be everybody’s number-one priority, and doing it effectively requires several things. You must assess your security state, protect against security threats, and then detect and respond rapidly to threats that occur.
* Protect VM contents. Setting up regular automatic backups is essential to protect against user errors. This isn’t enough, though; you must also make sure that your backups are safe from ransomware attacks and available when you need them.
* Monitor VMs and applications. This pattern encompasses several tasks, including getting insight into the health of your VMs, understanding interactions among them, and establishing ways to monitor the applications these VMs run. All of these are essential to keep your applications running around the clock.

## Next steps

Now that you've reviewed the sample Security Management policy for Cloud Native solutions, return to the [policy review guide](policy-compliance/what-is-a-cloud-policy-review.md) to start building on this sample to create your own policies for cloud adoption.

> [!div class="nextstepaction"]
> [Build your own policies using the Policy Review Guide](policy-compliance/what-is-a-cloud-policy-review.md)