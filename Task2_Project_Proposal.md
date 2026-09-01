# Securing Generative AI in a Managed Service Provider Environment

**John Brent Petty**

Western Governors University

D833 Cybersecurity Information and Assurance Capstone

John Jamison

April 6, 2026

Task 2: Project Proposal

# Background

This project takes place within a mid-sized managed service provider (MSP), referred to as Front Range Managed Services (FRMS), which supports multiple small-to-medium business clients. Employees, including help desk technicians and support staff, routinely access client systems for troubleshooting, remote support, and issue resolution. The organization operates within a Microsoft-based environment that includes Microsoft 365, Azure Active Directory, Microsoft Defender for Endpoint, remote monitoring and management (RMM) tools, and a centralized ticketing system.

As part of daily operations, employees are increasingly using generative AI tools, such as AI-assisted troubleshooting platforms and Microsoft Copilot, to improve efficiency and reduce resolution times. These tools are often used during documentation, problem analysis, and live support interactions involving client systems.

While these tools provide operational benefits, their adoption has outpaced the implementation of formal security controls, monitoring mechanisms, and usage policies. The organization currently lacks AI-specific governance controls, Data Loss Prevention (DLP) policies for AI interactions, and formal monitoring of employee use of generative AI tools. This creates a gap between productivity gains and the organization's ability to manage emerging cybersecurity risks associated with generative AI usage (National Institute of Standards and Technology, 2023; National Institute of Standards and Technology, 2018).

# Problem

The unmanaged use of generative AI tools within the Front Range Managed Services (FRMS) environment introduces significant cybersecurity risks, particularly related to the exposure of sensitive client data. Employees may unintentionally input confidential information—such as system configurations, logs, or client-specific details—into AI platforms without full awareness of how that data is stored, processed, or potentially reused (National Institute of Standards and Technology, 2023).

The organization currently lacks formal governance controls, Data Loss Prevention (DLP) policies, and monitoring mechanisms specific to generative AI usage. This creates a risk of data leakage, prompt injection attacks, and unauthorized data exposure, which may impact the confidentiality, integrity, and availability of client information (Center for Internet Security, 2021; National Institute of Standards and Technology, 2023).

In an MSP environment where employees routinely access multiple client systems, this risk is amplified due to the volume and sensitivity of data handled during daily operations. Without a structured framework to control and monitor AI interactions, the organization is unable to effectively mitigate these emerging cybersecurity threats or ensure compliance with client security requirements and industry standards (National Institute of Standards and Technology, 2018).

# Scope

The scope of this project includes endpoint devices used by MSP employees, such as workstations and laptops, as well as the applications and services through which generative AI tools are accessed. This includes browser-based AI platforms and integrated tools such as Microsoft Copilot.

In-scope systems include Windows 10/11 endpoints, Microsoft 365 services, Azure Active Directory, and endpoint security tools such as Microsoft Defender for Endpoint. Network activity related to AI usage, including web traffic to AI platforms, is also considered within scope.

The project focuses on systems used for client support activities, including help desk operations, remote troubleshooting sessions, and documentation workflows. This includes environments accessed through remote monitoring and management (RMM) tools and ticketing systems where client-related data may be handled.

Data within scope includes client-related information such as system configurations, logs, and other potentially sensitive or proprietary information processed during support interactions.

This project is limited to securing the FRMS internal environment and employee interactions with generative AI tools. Client-owned systems, third-party environments outside of MSP control, and non-AI-related security controls are considered out of scope.

# Stakeholders

The IT and help desk teams are primary stakeholders, as they are the primary users of generative AI tools for troubleshooting, documentation, and client support. They are responsible for adopting the new controls, following acceptable use policies, and providing feedback on usability and workflow impact.

The security team is responsible for designing, implementing, and monitoring the technical controls, including Data Loss Prevention (DLP), endpoint security configurations, and centralized logging. This group will also be responsible for tuning policies, investigating alerts, and ensuring the ongoing effectiveness of the solution.

MSP leadership and management are key stakeholders, as they provide strategic direction, approve resource allocation, and ensure alignment with business objectives. They are also responsible for policy approval and enforcement across the organization.

Clients are indirect but critical stakeholders, as the MSP handles sensitive client data. They have a vested interest in ensuring their information is protected and influence security requirements through contractual obligations and expectations.

Compliance and legal stakeholders ensure that the use of generative AI tools aligns with regulatory requirements, contractual obligations, and data protection standards.

Finally, all MSP employees are stakeholders, as they are required to follow established policies and complete training to ensure secure use of generative AI technologies.

# Risk Assessment

The risk assessment approach used in this project is informed by established cybersecurity frameworks and guidance from the National Institute of Standards and Technology (NIST) and the Center for Internet Security (CIS). This methodology evaluates risk by analyzing threat sources, identifying vulnerabilities, and assessing likelihood and impact to determine overall risk severity within the organization. NIST Special Publication 800-30 provides a structured methodology for identifying threats, vulnerabilities, likelihood, and impact when conducting risk assessments (NIST, 2012). This framework supports the evaluation of risks such as data leakage and prompt injection within the MSP environment.

The NIST Cybersecurity Framework emphasizes the importance of identifying, protecting, detecting, and responding to cybersecurity risks, particularly in environments handling sensitive data (NIST, 2018). Additionally, the NIST Artificial Intelligence Risk Management Framework highlights emerging risks associated with AI systems, including data exposure, misuse, and lack of governance controls (NIST, 2023).

The CIS Critical Security Controls further reinforce the need for data protection, access control, monitoring, and user awareness to reduce the likelihood of security incidents (CIS, 2021). These controls align with the identified risks by emphasizing the importance of implementing technical safeguards such as Data Loss Prevention (DLP), centralized logging, and endpoint monitoring.

These sources informed the risk identification and analysis process by providing a structured approach to evaluating threats and their potential impact on confidentiality, integrity, and availability. They also guided the selection of appropriate technical and governance-based controls to mitigate the identified risks and improve the organization's overall security posture.

## Risk #1

**Risk Description:** Sensitive client data may be exposed through employee use of generative AI tools, where confidential information is unintentionally submitted in prompts.

**Threat Source/Event:** Internal users (employees) inputting sensitive data into generative AI platforms such as Microsoft Copilot or browser-based AI tools during troubleshooting, documentation, or analysis.

**Vulnerability:** The organization lacks Data Loss Prevention (DLP) controls, AI-specific governance policies, and monitoring mechanisms to detect or prevent the transmission of sensitive data to AI platforms.

**Potential Impact:** Exposure of client data could result in loss of confidentiality, regulatory non-compliance, reputational damage, and potential contractual or legal consequences. In an MSP environment, this risk is amplified due to access to multiple client environments and sensitive data sets.

**Likelihood Assessment:** High – Employees regularly use AI tools during daily operations, and without technical controls or clear governance, it is highly likely that sensitive data could be unintentionally submitted.

**Severity Assessment:** High – A data exposure event involving client information could result in significant business impact, including legal liability, loss of client trust, and financial penalties (National Institute of Standards and Technology, 2012; National Institute of Standards and Technology, 2023).

## Risk #2

**Risk Description:** Generative AI tools may produce manipulated or misleading outputs due to prompt injection or adversarial input, leading to incorrect recommendations or actions by employees.

**Threat Source/Event:** Malicious or untrusted input introduced into generative AI tools, including prompt injection attacks or compromised data sources that influence AI-generated responses.

**Vulnerability:** The organization lacks validation controls, monitoring, and user awareness related to AI-generated output, allowing employees to trust and act on AI responses without verification.

**Potential Impact:** Employees may follow incorrect or manipulated guidance, resulting in misconfigurations, service disruptions, or improper handling of client systems. This could impact system integrity and availability, and may lead to operational downtime or security incidents.

**Likelihood Assessment:** Medium – While prompt injection requires specific conditions, the increasing reliance on AI tools and lack of user awareness increases the likelihood of exposure to manipulated outputs.

**Severity Assessment:** High – Incorrect actions based on AI-generated output could result in system outages, security misconfigurations, or compromised client environments, leading to significant operational and reputational impact (National Institute of Standards and Technology, 2012; National Institute of Standards and Technology, 2023).

# Objectives

The objectives of this project are to design and implement a secure framework for generative AI usage within a managed service provider (MSP) environment that reduces cybersecurity risk while maintaining operational efficiency. Specifically, the project aims to:

- Implement Data Loss Prevention (DLP) controls to detect and prevent the transmission of sensitive data into generative AI tools.
- Establish monitoring and logging capabilities to provide visibility into employee interactions with AI platforms.
- Develop and enforce governance policies that define acceptable use of generative AI within the organization.
- Reduce the risk of data leakage, prompt injection, and unauthorized data exposure associated with AI usage.
- Align the solution with established cybersecurity frameworks such as the NIST Cybersecurity Framework and CIS Critical Security Controls.
- Improve employee awareness of secure AI usage practices through training and policy guidance.

The desired end state is a controlled and monitored environment in which generative AI tools can be used securely, sensitive data is protected, and all AI-related interactions are governed by enforceable policies and supported by centralized visibility (National Institute of Standards and Technology, 2018; Center for Internet Security, 2021).

# Technical Solution

The proposed solution implements a combination of technical and governance-based controls to manage the secure use of generative AI tools within the managed service provider (MSP) environment. This solution leverages existing Microsoft security technologies to provide Data Loss Prevention (DLP), endpoint monitoring, and centralized logging to reduce the risk of sensitive data exposure and misuse of AI tools.

Microsoft Purview will be used to implement Data Loss Prevention (DLP) policies that identify and prevent the transmission of sensitive data into generative AI platforms. These policies will detect data types such as personally identifiable information (PII), system configurations, and client-specific technical data. When sensitive data is detected, actions such as blocking, alerting, or user notification will be triggered to prevent unauthorized data exposure.

Microsoft Defender for Endpoint will provide visibility into endpoint-level activity and enforce controls related to AI usage. This includes monitoring access to AI tools through browsers and applications, identifying risky behavior, and restricting access to unauthorized or unapproved AI platforms.

Microsoft Sentinel will serve as the centralized logging and monitoring solution, aggregating data from DLP policies, endpoint activity, and user interactions. This enables correlation of events, detection of suspicious patterns, and investigation of potential policy violations or attempted data exfiltration related to AI usage.

In addition to technical controls, the solution includes the development of governance policies and acceptable use guidelines that define how employees can securely interact with generative AI tools. User training will reinforce these policies and promote awareness of risks such as data leakage and prompt injection.

This integrated approach ensures that generative AI usage is controlled, monitored, and aligned with cybersecurity best practices while maintaining operational efficiency within the MSP environment.

## Standards and Regulations

The proposed solution aligns with established cybersecurity frameworks and industry standards to ensure a structured and compliant approach to managing generative AI risks within the MSP environment.

The NIST Cybersecurity Framework (CSF) provides a foundation for identifying, protecting, detecting, and responding to cybersecurity risks. This solution supports these functions by implementing Data Loss Prevention (DLP) controls to protect sensitive data, monitoring tools to detect potential misuse, and centralized logging to support incident response activities (NIST, 2018).

NIST Special Publication 800-53 provides a comprehensive set of security and privacy controls that guide the implementation of access control, system monitoring, and data protection mechanisms. The use of Microsoft Purview, Defender for Endpoint, and Sentinel aligns with these control families by enforcing data protection, audit logging, and continuous monitoring (NIST, 2020).

The NIST Artificial Intelligence Risk Management Framework (AI RMF) addresses risks specific to AI systems, including data exposure, misuse, and lack of governance. This project aligns with the AI RMF by implementing governance policies, monitoring AI interactions, and reducing the risk of unintended data disclosure (NIST, 2023).

The CIS Critical Security Controls (Version 8) further support this solution by emphasizing data protection, access control, and security monitoring. Controls related to data protection and logging directly align with the implementation of DLP policies and centralized monitoring within the MSP environment (CIS, 2021).

By aligning with these frameworks, the proposed solution ensures that generative AI usage is managed in a secure, compliant, and industry-recognized manner.

## Integration

The proposed solution integrates with the existing Microsoft-based infrastructure within the MSP environment to provide seamless security control implementation without significant disruption to operations. Microsoft Purview, Microsoft Defender for Endpoint, and Microsoft Sentinel work together to create a unified security framework for managing generative AI usage.

Endpoint devices serve as the primary point of interaction, where employees access generative AI tools through browsers or integrated applications such as Microsoft Copilot. Microsoft Defender for Endpoint monitors these endpoints, providing visibility into user activity and enforcing device-level security controls.

Microsoft Purview integrates with endpoint and cloud services to apply Data Loss Prevention (DLP) policies that inspect user interactions with AI tools. When sensitive data is detected in prompts or submissions, policies can block the action, generate alerts, or notify users in real time.

All activity related to DLP enforcement and endpoint monitoring is forwarded to Microsoft Sentinel, where logs are centralized for analysis. Sentinel enables correlation of events across systems, allowing the organization to detect patterns of misuse, investigate incidents, and maintain audit visibility.

This integration ensures a continuous flow of data from user interaction to enforcement and monitoring, enabling real-time protection, centralized visibility, and coordinated incident response across the MSP environment.

## Reporting

The proposed solution provides comprehensive audit trail and reporting capabilities through centralized logging and monitoring using Microsoft Sentinel and Microsoft Purview. All user interactions with generative AI tools, including attempts to transmit sensitive data, are captured and recorded to ensure visibility and accountability.

Microsoft Purview generates logs related to Data Loss Prevention (DLP) policy enforcement, including blocked actions, alerts, and user notifications. These logs provide insight into attempted data transfers and policy violations involving generative AI tools.

Microsoft Defender for Endpoint contributes additional telemetry related to endpoint activity, including access to AI platforms, application usage, and potentially risky behavior. This data enhances visibility into how AI tools are being accessed and used across the organization.

Microsoft Sentinel aggregates logs from Purview and Defender for Endpoint into a centralized Security Information and Event Management (SIEM) platform. This enables correlation of events, detection of suspicious patterns, and investigation of potential incidents. Sentinel also supports alerting, dashboards, and reporting capabilities that provide real-time and historical insights into AI usage and associated risks.

These audit and reporting capabilities support compliance requirements, incident response efforts, and continuous monitoring by providing a clear and traceable record of user activity and security events related to generative AI usage.

## Justification

The proposed solution is preferred over alternative approaches because it leverages existing Microsoft security tools within the MSP environment, providing a cost-effective and integrated method for managing generative AI risks. By utilizing Microsoft Purview, Defender for Endpoint, and Sentinel, the organization can implement comprehensive Data Loss Prevention (DLP), monitoring, and logging capabilities without introducing significant complexity or requiring additional third-party solutions.

Compared to a policy-only approach, this solution provides enforceable technical controls that actively prevent sensitive data exposure rather than relying solely on user compliance. It also improves visibility into user behavior and potential risks through centralized monitoring and logging, which would not be achievable through governance measures alone.

Alternative solutions, such as standalone DLP or third-party AI monitoring tools, may introduce additional costs, integration challenges, and operational overhead. In contrast, the Microsoft-based solution integrates seamlessly with the organization's existing infrastructure, reducing implementation complexity and enabling faster deployment.

This approach provides a balanced combination of security, usability, and cost efficiency while aligning with industry best practices. It ensures that generative AI tools can be used productively without compromising the confidentiality, integrity, or availability of sensitive client data.

## Cost

The estimated cost for implementing the proposed solution within Front Range Managed Services (FRMS) includes both initial implementation costs and ongoing operational expenses. These costs are based on the use of Microsoft security technologies already present within the organization's environment, which reduces the need for additional third-party solutions.

Initial implementation costs are estimated to range from approximately \$8,000 to \$15,000. These costs include configuration of Data Loss Prevention (DLP) policies within Microsoft Purview, onboarding and tuning of Microsoft Defender for Endpoint, integration with Microsoft Sentinel, and labor costs associated with IT and security personnel responsible for deployment and testing.

Ongoing operational costs are estimated to range from \$2,000 to \$6,000 per month. These costs primarily include Microsoft licensing, data ingestion and retention within Microsoft Sentinel, continuous monitoring and maintenance, and periodic updates to policies and controls.

Because the solution leverages existing Microsoft infrastructure, costs are significantly lower than implementing standalone or third-party solutions. This approach provides a cost-effective method for improving security while maintaining operational efficiency and scalability within the FRMS environment.

**Table 1: Cost Breakdown for Proposed Solution**

| **Cost Category**        | **Description**                                              | **Estimated Cost**    |
| ------------------------ | ------------------------------------------------------------ | --------------------- |
| Microsoft Purview (DLP)  | Data classification and DLP policy enforcement               | Included / Licensing  |
| Defender for Endpoint    | Endpoint monitoring and control                              | Included / Licensing  |
| Microsoft Sentinel       | SIEM logging, ingestion, and analysis                        | \$1,000–\$3,000/month |
| Implementation Labor     | Security engineers and IT staff configuration and deployment | \$5,000–\$10,000      |
| Training & Documentation | User training sessions and policy development                | \$1,000–\$2,000       |
| Maintenance & Monitoring | Ongoing tuning, monitoring, and updates                      | \$1,000–\$3,000/month |

# Timeline

The implementation of secure generative AI controls within the MSP environment will follow a structured, phase-based approach to ensure controlled deployment, minimal disruption to operations, and effective risk mitigation. The total estimated timeline for implementation is approximately 10 weeks.

**Phase 1: Assessment and Requirements Analysis (2 weeks)**

This phase involves evaluating current AI usage within the organization, identifying how employees interact with generative AI tools, and determining the types of data being shared. Stakeholder input will be gathered from IT, security, and management teams to define requirements and prioritize risks.

**Phase 2: Solution Design (2–3 weeks)**

During this phase, the technical and governance framework will be developed. Data Loss Prevention (DLP) policies will be defined using Microsoft Purview, endpoint monitoring controls will be designed using Defender for Endpoint, and logging requirements will be established using Microsoft Sentinel. Acceptable use policies and employee guidelines will also be created.

**Phase 3: Implementation and Configuration (3–4 weeks)**

The designed controls will be deployed in a controlled environment. DLP policies will be implemented to detect and prevent sensitive data transmission, endpoint controls will be configured, and logging pipelines will be established within Microsoft Sentinel.

**Phase 4: Testing and Validation (1–2 weeks)**

The solution will be tested to ensure effectiveness. This includes validating DLP policy enforcement, confirming logging and monitoring capabilities, and identifying any gaps or operational issues. Feedback from users will be collected to refine the solution.

**Phase 5: Deployment and User Training (1–2 weeks)**

Following successful testing, the solution will be fully deployed across the FRMS environment. Employees will receive training on secure AI usage practices, and policies will be formally enforced.

**Phase 6: Monitoring and Continuous Improvement (Ongoing)**

Ongoing monitoring will be conducted using Microsoft Sentinel to track AI usage and detect potential security incidents. Policies and controls will be regularly reviewed and updated based on emerging threats and user behavior.

## Resources

The successful implementation of this project requires a combination of personnel, technology, and organizational support. Key personnel include security engineers responsible for designing and implementing Data Loss Prevention (DLP) policies, IT administrators responsible for configuring endpoint controls and managing system integration, and help desk staff who will adopt and provide feedback on the solution.

Technical resources include Microsoft Purview for DLP and data classification, Microsoft Defender for Endpoint for endpoint monitoring and enforcement, and Microsoft Sentinel for centralized logging, monitoring, and analysis. Existing infrastructure such as Microsoft 365, Azure Active Directory, and endpoint devices will also support the implementation.

Additional resources include training materials and documentation to ensure employees understand acceptable use policies and secure AI practices. Support from leadership and management is also required to approve policies, allocate resources, and ensure organization-wide adoption of the solution.

## Dependencies

The success of this project depends on several key factors within the MSP environment. First, appropriate Microsoft licensing must be in place to support Microsoft Purview, Defender for Endpoint, and Microsoft Sentinel capabilities. Without the required licensing tiers, certain Data Loss Prevention (DLP), monitoring, and logging features may not be available.

Proper endpoint configuration is also required to ensure that devices are onboarded to Microsoft Defender for Endpoint and integrated with Microsoft Purview and Sentinel. This includes ensuring that all relevant systems are correctly configured for policy enforcement and telemetry collection.

User cooperation and adherence to policies are critical dependencies. Employees must follow acceptable use guidelines and participate in training to ensure that generative AI tools are used securely and appropriately.

Organizational support from leadership is also required to approve policies, allocate resources, and enforce compliance across the organization. Without management support, adoption and enforcement of the solution may be limited.

Finally, network connectivity and system integration between Microsoft services must be maintained to ensure continuous monitoring, logging, and enforcement of security controls.

## Risk Mitigation

The proposed solution mitigates the identified risks by implementing a combination of technical controls, monitoring capabilities, and governance policies designed to reduce the likelihood and impact of generative AI-related threats.

For Risk #1 (data leakage), Data Loss Prevention (DLP) policies implemented through Microsoft Purview will detect and prevent the transmission of sensitive client data into generative AI tools. These controls reduce the likelihood of accidental data exposure by blocking or alerting on unauthorized data sharing.

Microsoft Defender for Endpoint further mitigates this risk by monitoring endpoint activity and restricting access to unapproved AI platforms, reducing the attack surface and limiting opportunities for data exfiltration.

For Risk #2 (prompt injection and AI misuse), centralized logging and monitoring through Microsoft Sentinel enables the detection of suspicious patterns, anomalous behavior, and potential policy violations. This improves the organization's ability to identify and respond to threats that could impact system integrity or availability.

Governance policies and user training also play a critical role in risk mitigation by increasing employee awareness of secure AI usage practices and reducing reliance on unverified AI-generated outputs.

Together, these controls reduce both the likelihood and severity of the identified risks, providing a layered defense that improves the overall security posture of the MSP environment.

## Security Benefits

The proposed solution enhances the organization's security posture by reducing the risk of sensitive data exposure associated with generative AI usage. Data Loss Prevention (DLP) policies help protect confidential information, while endpoint monitoring and centralized logging improve visibility into user activity. The implementation of governance policies and monitoring capabilities strengthens the organization's ability to detect, prevent, and respond to AI-related threats, supporting the protection of confidentiality, integrity, and availability.

## Operational Impact

The solution is designed to integrate with existing Microsoft infrastructure, minimizing disruption to daily operations. Employees can continue to use generative AI tools to improve efficiency, while security controls operate in the background to enforce safe usage. Although minor workflow adjustments and user training will be required, the overall impact is expected to be manageable and balanced by improved guidance and clearer usage policies.

## Business Impact

The implementation of secure AI controls improves client trust by demonstrating a commitment to protecting sensitive information. It also reduces the risk of regulatory non-compliance, legal liability, and reputational damage associated with data exposure incidents. By enabling the secure use of generative AI technologies, the organization can continue to innovate and improve service delivery while maintaining a strong security and compliance posture.

# Conclusion

The increasing use of generative AI tools within the managed service provider (MSP) environment introduces significant cybersecurity risks that must be addressed to protect sensitive client data. This project presents a comprehensive solution that combines Data Loss Prevention (DLP), endpoint monitoring, centralized logging, and governance policies to manage these risks effectively.

By leveraging Microsoft Purview, Defender for Endpoint, and Microsoft Sentinel, the proposed solution provides a practical and integrated approach to securing AI usage without disrupting operational efficiency.

This approach reduces the risk of data leakage, improves visibility into user activity, and strengthens the organization's ability to detect and respond to potential threats. Additionally, it aligns with established cybersecurity frameworks and industry standards, ensuring a structured and compliant implementation.

Overall, the solution enables FRMS to adopt generative AI technologies securely while maintaining the confidentiality, integrity, and availability of sensitive information and supporting long-term operational and business success.

# References

Center for Internet Security. (2021). _CIS Critical Security Controls (Version 8)._ <https://www.cisecurity.org/controls/v8>

National Institute of Standards and Technology. (2012). _Guide for conducting risk assessments (NIST SP 800-30 Rev. 1)._ <https://doi.org/10.6028/NIST.SP.800-30r1>

National Institute of Standards and Technology. (2018). _Framework for improving critical infrastructure cybersecurity (Version 1.1)._ <https://doi.org/10.6028/NIST.CSWP.04162018>

National Institute of Standards and Technology. (2020). _Security and privacy controls for information systems and organizations (NIST SP 800-53 Rev. 5)._ <https://doi.org/10.6028/NIST.SP.800-53r5>

National Institute of Standards and Technology. (2023). _Artificial Intelligence Risk Management Framework (AI RMF 1.0)._ <https://doi.org/10.6028/NIST.AI.100-1>

Microsoft. (2023a). _Microsoft Purview Data Loss Prevention documentation._ <https://learn.microsoft.com/en-us/purview/dlp-learn-about-dlp>

Microsoft. (2023b). _Microsoft Defender for Endpoint documentation._ <https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint>

Microsoft. (2023c). _Microsoft Sentinel documentation._ <https://learn.microsoft.com/en-us/azure/sentinel/overview>

# Appendix A

**High-Level Architecture Overview**

The solution architecture includes endpoint devices monitored by Microsoft Defender for Endpoint, with Data Loss Prevention (DLP) policies enforced through Microsoft Purview. All activity logs are forwarded to Microsoft Sentinel for centralized monitoring and analysis.

**Key Components:**

- Endpoint Devices (User Workstations)
- Microsoft Defender for Endpoint (Monitoring and Enforcement)
- Microsoft Purview (DLP and Data Classification)
- Microsoft Sentinel (SIEM and Logging)
- Generative AI Tools (e.g., Microsoft Copilot, browser-based AI platforms)

**Data Flow:**

User → Endpoint → DLP Policy Check → Allowed or Blocked Action → Logged in Microsoft Sentinel

# Appendix B

**Sample Data Loss Prevention (DLP) Policy**

**Example Policy: Prevent Sensitive Data Entry into AI Tools**

**Conditions:**

- Detect keywords such as "password," "configuration," and "internal"
- Detect structured data such as IP addresses and account identifiers

**Actions:**

- Block transmission of sensitive data
- Alert the security team
- Log the event in Microsoft Sentinel

**User Notification:**

"Sensitive data detected. This action is not permitted in AI tools."
