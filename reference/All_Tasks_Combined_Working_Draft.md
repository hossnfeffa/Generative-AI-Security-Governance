_Archived reference draft — a single working document combining drafted content for all three tasks, labeled with the WGU rubric section codes (A1, A2, B1, etc.). The Task 2 section here is more granular than any other draft and was likely the source material for the polished final Task 2 proposal. Kept as a reference in case any of this phrasing is useful; the individual final documents are the documents of record._

# Task 1

**Cybersecurity Problem – Context**

This project will be conducted within a mid-sized managed service provider (MSP) environment that supports multiple small-to-medium business clients across various industries. Employees within the MSP, including help desk technicians and support staff, typically have limited administrative access but routinely interact with client systems for troubleshooting, remote support, and issue resolution.

As part of daily operations, employees are increasingly using generative AI tools such as AI-assisted troubleshooting platforms and integrated assistants like Microsoft Copilot to improve efficiency and reduce resolution times. These tools may be used during screen-sharing sessions, documentation creation, or problem analysis, often involving real-time interaction with client environments.

While these tools provide operational benefits, their rapid adoption has outpaced the implementation of formal security controls, monitoring mechanisms, and usage policies within the MSP environment. This creates a gap between productivity gains and the organization's ability to manage emerging cybersecurity risks associated with generative AI usage.

**Cybersecurity Problem – Problem Statement**

The unmanaged use of generative AI tools within the MSP environment introduces significant cybersecurity risks, including the potential exposure of proprietary and sensitive client information. Employees may unintentionally input confidential data—such as system configurations, logs, or client-specific details—into AI platforms without awareness of how that data is stored, processed, or reused.

Additionally, the lack of governance and technical controls surrounding AI usage increases the risk of prompt injection attacks, data leakage, and non-compliance with client security requirements or regulatory standards. Without a structured framework to control and monitor AI interactions, the organization is unable to effectively mitigate these risks.

This project will address the need for a secure and controlled approach to generative AI usage by identifying vulnerabilities, assessing associated risks, and proposing a combination of technical and governance-based controls to protect sensitive information within the MSP environment.

**Proposed Control**

This project will implement a secure governance and technical control framework to manage the use of generative AI tools within a managed service provider (MSP) environment. The proposed solution will combine data loss prevention (DLP), access control, monitoring, and policy enforcement to reduce the risk of sensitive data exposure.

The technical implementation will leverage tools within the Microsoft security ecosystem, including Microsoft Purview for Data Loss Prevention (DLP) policy enforcement and data classification, Microsoft Defender for Endpoint for endpoint monitoring and control, and Microsoft Sentinel for centralized logging and security event analysis.

These tools will be used to detect and prevent the transmission of sensitive data into generative AI platforms, monitor user interactions with AI tools, and provide visibility into potential misuse. In addition to technical controls, the solution will include the development of acceptable use policies and user awareness guidance to ensure that employees understand how to securely interact with AI technologies.

This combined approach ensures that generative AI usage is both controlled and aligned with cybersecurity best practices while maintaining operational efficiency within the MSP environment.

**Scope**

The scope of this project will include endpoint devices used by MSP employees, such as workstations and laptops, as well as the applications and services through which generative AI tools are accessed. This includes browser-based AI platforms and integrated tools such as Microsoft Copilot.

The project will focus on systems used for client support activities, including help desk operations, remote troubleshooting sessions, and documentation workflows. Data within scope includes client-related information such as system configurations, logs, and any potentially sensitive or proprietary data handled during support interactions.

The implementation will be designed for a mid-sized MSP environment and will not include direct modification of client systems, but will instead focus on securing the MSP's internal processes and employee interactions with AI tools.

**Objectives**

- Implement Data Loss Prevention (DLP) controls to detect and prevent the transmission of sensitive data into generative AI tools.
- Establish monitoring and logging capabilities to provide visibility into employee interactions with AI platforms.
- Develop and enforce governance policies that define acceptable use of generative AI within the MSP environment.
- Reduce the risk of data leakage, prompt injection, and unauthorized data exposure associated with AI usage.
- Align the solution with established cybersecurity frameworks such as NIST and CIS Controls.
- Improve employee awareness of secure AI usage practices through guidance and policy integration.

**Project Stakeholders**

The IT and help desk teams, the security team, MSP leadership and management, clients, compliance and legal stakeholders, and all MSP employees are stakeholders in this project, each with distinct roles and priorities in implementing, overseeing, or adhering to the proposed controls.

**Implementation Plan (Phase-Based)**

Phase 1: Assessment and Requirements Analysis — assess current AI usage, identify data exposure points, gather stakeholder input.

Phase 2: Solution Design — define DLP policies (Microsoft Purview), endpoint controls (Defender for Endpoint), logging requirements (Sentinel), and acceptable use policies.

Phase 3: Implementation and Configuration — deploy DLP policies, endpoint monitoring, logging pipelines, and formally introduce policies to employees.

Phase 4: Testing and Validation — simulate user interactions, validate DLP detection, evaluate monitoring systems, collect feedback.

Phase 5: Deployment and User Training — full deployment with employee training on secure AI usage.

Phase 6: Monitoring and Continuous Improvement — ongoing monitoring via Sentinel, regular review and refinement of controls.

**Sources**

National Institute of Standards and Technology. (2018). _Framework for improving critical infrastructure cybersecurity (Version 1.1)._

National Institute of Standards and Technology. (2020). _Security and privacy controls for information systems and organizations (NIST SP 800-53 Rev. 5)._

National Institute of Standards and Technology. (2023). _Artificial Intelligence Risk Management Framework (AI RMF 1.0)._

Center for Internet Security. (2021). _CIS Critical Security Controls (Version 8)._

Microsoft. (2023). _Microsoft Purview / Defender for Endpoint / Sentinel documentation._

# Task 2

**A1: Background draft**

The proposed project will take place within a mid-sized managed service provider (MSP) environment that supports multiple small-to-medium business clients across diverse industries. In this environment, help desk technicians, support staff, and security personnel regularly access client systems to perform troubleshooting, remote assistance, documentation, and service coordination. Because MSPs operate across multiple customer environments, they handle a large volume of sensitive operational and client-related information, including system configurations, support logs, device details, and internal business communications. This broad access to varied client data increases the importance of maintaining strong technical safeguards and consistent governance controls.

The organization's current security environment includes standard endpoint protection, limited-access support workflows, and existing operational controls designed to reduce unauthorized administrative activity. However, the increasing use of generative AI tools such as Microsoft Copilot and browser-based AI assistants has introduced a new layer of risk into routine support operations. Employees may use these tools to summarize issues, assist with troubleshooting, improve documentation, or streamline communication. While these capabilities can improve efficiency, they also create new exposure points when sensitive or proprietary information is entered into AI systems without sufficient technical restrictions or formal guidance.

This background is significant because the rapid adoption of generative AI in workplace environments has outpaced many organizations' ability to implement governance, monitoring, and data protection measures. NIST's Artificial Intelligence Risk Management Framework emphasizes that AI technologies introduce risks related to governance, privacy, reliability, and misuse that organizations must actively manage through structured controls and oversight (NIST, 2023). In addition, the NIST Cybersecurity Framework stresses the importance of identifying organizational risks, protecting sensitive assets, and detecting inappropriate activity as part of a mature cybersecurity program (NIST, 2018).

**A2: Problem**

The cybersecurity problem addressed in this proposal is the unmanaged use of generative AI tools within the MSP environment, which creates a risk of exposing proprietary and sensitive client information. Employees may unintentionally enter confidential data such as system logs, device configurations, troubleshooting notes, or client-specific operational details into AI platforms while seeking faster issue resolution or more efficient documentation support. Because these tools rely on external processing, retained prompts, or integrated cloud-based services, improper use can result in data leakage, misuse of sensitive information, and weakened client trust.

The significance of this problem is amplified by the MSP's business model. Unlike a single-organization environment, the MSP handles information across multiple clients, which means a single breakdown in AI governance can affect more than one business relationship and create wider contractual, operational, and reputational consequences. NIST's AI Risk Management Framework states that organizations should establish processes to govern AI usage and reduce adverse impacts associated with AI systems (NIST, 2023). Likewise, CIS Critical Security Controls emphasize data protection, security awareness, and audit log management as key practices for reducing organizational exposure to misuse and unauthorized disclosure (CIS, 2021).

**A3: Scope**

The scope of the cybersecurity problem includes the systems, networks, and data involved in daily MSP operations where generative AI tools are used. This primarily encompasses employee endpoint devices such as workstations and laptops, as well as the applications and platforms used to access generative AI tools, including browser-based interfaces and integrated solutions such as Microsoft Copilot.

From a network perspective, the scope includes the MSP's internal network infrastructure and any secure connections used to access client environments. The data within scope includes client-related information handled by MSP employees during support activities: system configurations, troubleshooting logs, user account details, network information, and other proprietary or sensitive data encountered during service delivery.

Overall, the scope is focused on securing the MSP's internal processes, user behaviors, and technology interactions with generative AI tools, rather than altering client-side infrastructure.

**A4: Stakeholders**

The IT and help desk teams, the security team, MSP leadership and management, clients, compliance and legal stakeholders, and MSP employees as a whole are each essential to implementing, supporting, and sustaining the proposed cybersecurity solution within the MSP environment.

**A5: Risk Assessment**

Risk #1: Unauthorized exposure of sensitive client data through generative AI prompts. Threat Source/Event: Human error and misuse of AI tools, as well as external AI platforms that store or process user inputs. Vulnerability: Lack of Data Loss Prevention (DLP) controls, insufficient monitoring of AI usage, and absence of formal governance policies. Potential Impact: Loss of client trust, contractual violations, regulatory penalties, reputational damage. Likelihood: High. Severity: High.

Risk #2: Prompt injection or manipulation of AI-generated outputs leading to inaccurate or malicious guidance. Threat Source/Event: Malicious input crafted within AI prompts or external data sources. Vulnerability: Lack of validation and oversight of AI-generated outputs, employee reliance on AI-generated recommendations without verification. Potential Impact: Misconfigurations, service disruptions, or security vulnerabilities within client environments. Likelihood: Medium. Severity: High.

Literature Support: NIST SP 800-30 provides guidance on conducting risk assessments by identifying threats, vulnerabilities, likelihood, and impact (NIST, 2012). The NIST AI Risk Management Framework highlights risks associated with AI misuse, including data exposure and manipulation (NIST, 2023).

**A6: Objectives**

- Implement Data Loss Prevention (DLP) controls to detect and prevent the transmission of sensitive data into generative AI tools
- Establish monitoring and logging capabilities to provide visibility into employee interactions with AI platforms
- Develop and enforce governance policies that define acceptable use of generative AI
- Reduce risks related to data leakage, prompt injection, and unauthorized data exposure
- Align the solution with established cybersecurity frameworks such as NIST and CIS Controls
- Improve employee awareness and secure usage practices for AI technologies

**B1: Technical Solution**

The proposed cybersecurity solution is the implementation of a secure governance and technical control framework to manage the use of generative AI tools within the MSP environment, combining Data Loss Prevention (DLP), endpoint security controls, centralized logging, and policy enforcement. The core of the solution leverages Microsoft Purview for DLP and data classification, Microsoft Defender for Endpoint for endpoint monitoring and control, and Microsoft Sentinel for centralized logging and security analytics, together with governance measures such as acceptable use policies, employee guidance, and awareness training.

**B2: Standards & Compliance**

The proposed solution aligns with the NIST Cybersecurity Framework (identify, protect, detect, respond, recover), NIST SP 800-53 (access control, audit logging, data protection), the NIST AI Risk Management Framework (data misuse, governance, reliability), and the CIS Critical Security Controls Version 8 (data protection, security awareness, audit log management).

**B3: Integration**

Microsoft Purview DLP is configured to monitor and control data interactions at the endpoint and application level. Microsoft Defender for Endpoint provides visibility into user activity and enforces security policies across managed devices. Microsoft Sentinel acts as the centralized logging and analysis platform, collecting security events related to AI usage, endpoint activity, and policy enforcement, enabling real-time monitoring, alerting, and incident investigation.

**B4: Audit Trail / Reporting**

Microsoft Sentinel collects logs from endpoint devices, DLP policy enforcement actions, and user interactions with AI tools. Microsoft Purview DLP provides reporting on sensitive data detection and policy enforcement. Microsoft Defender for Endpoint contributes additional telemetry related to user behavior and system activity. Together these create a comprehensive audit trail supporting compliance, incident response, and ongoing security improvements.

**B5: Justification (comparison)**

Compared to policy-only controls (which don't prevent accidental exposure) or third-party DLP/monitoring tools (added cost, integration effort), the proposed solution leverages existing Microsoft security tools already common in MSP environments, reducing implementation complexity while providing both preventative and detective controls in a layered approach that scales as AI usage evolves.

**B6: Cost Table**

| **Category** | **Item**                           | **Estimated Cost**          | **Notes**                                                         |
| ------------ | ---------------------------------- | --------------------------- | ----------------------------------------------------------------- |
| Hardware     | Existing infrastructure            | \$0                         | Assumes current endpoints and cloud infrastructure are sufficient |
| Software     | Microsoft Purview (DLP)            | \$5–\$10 per user/month     | Included in Microsoft 365 E5 or add-on licensing                  |
| Software     | Microsoft Defender for Endpoint    | \$3–\$6 per user/month      | Endpoint security licensing                                       |
| Software     | Microsoft Sentinel                 | \$2–\$5 per GB ingested/day | Pay-as-you-go SIEM pricing model                                  |
| Licensing    | Microsoft 365 E5 (if applicable)   | \$57 per user/month         | Bundled security + compliance tools                               |
| Personnel    | Security Engineer (implementation) | \$50–\$75/hour              | Estimated 40–80 hours for deployment                              |
| Personnel    | IT/Admin support                   | \$30–\$50/hour              | Policy configuration and rollout support                          |
| Maintenance  | Ongoing monitoring and tuning      | \$500–\$1,500/month         | Includes log monitoring and policy updates                        |
| Training     | Employee training sessions         | \$1,000–\$3,000             | Development and delivery of training materials                    |

Estimated Total (Initial Implementation): \$5,000 – \$15,000

Estimated Monthly Operational Cost: \$2,000 – \$6,000

**C1: Timeline**

Phase 1: Assessment and Requirements (Weeks 1–2). Phase 2: Solution Design (Weeks 3–4). Phase 3: Implementation and Configuration (Weeks 5–7). Phase 4: Testing and Validation (Weeks 8–9). Phase 5: Deployment and Training (Week 10). Phase 6: Ongoing Monitoring (Post-Implementation).

**C2: Resources**

Personnel: security engineer, IT administrators, management/compliance oversight. Technology: Microsoft Purview, Defender for Endpoint, Microsoft Sentinel, endpoint devices, secure network access. Stakeholder-specific: time for employee training, management support, compliance oversight.

**C3: Dependencies**

Appropriate Microsoft licensing (e.g., Microsoft 365 E5 or equivalent add-ons); proper endpoint configuration and enrollment in Defender for Endpoint; employee cooperation and stakeholder alignment; sustained network connectivity and system availability.

**C4: Risk Mitigation (per phase)**

Assessment: incomplete visibility → stakeholder interviews and log review. Design: misconfigured policies → stakeholder validation and controlled testing. Implementation: workflow disruption → incremental rollout and advance communication. Testing: missed edge cases → diverse test scenarios. Deployment: user resistance → training, documentation, support. Monitoring: alert fatigue → continuous tuning of rules and thresholds.

**D1: Security Benefits**

DLP controls reduce the likelihood of sensitive data exposure; centralized logging and monitoring (Sentinel) enable proactive detection and response; governance policies and awareness initiatives reduce human error. Together these create a layered security approach combining prevention, detection, and governance.

**D2: Operational Impact**

Cloud-based tools operate with minimal performance impact. Employees continue to use generative AI tools productively while safeguards reduce risk; minor initial adjustments give way to clearer guidelines and improved confidence over time.

**D3: Business Impact**

Strengthens client trust and reputation; reduces financial and legal risk from data leakage or noncompliance; supports scalable and secure adoption of emerging technologies, keeping the MSP competitive and adaptive.

**Section E: Conclusion**

The unmanaged use of generative AI tools within the MSP environment presents a significant cybersecurity risk, particularly regarding exposure of sensitive client data. The proposed solution — combining DLP, endpoint monitoring, centralized logging, and governance policies via Microsoft Purview, Defender for Endpoint, and Sentinel — directly mitigates the risk of data leakage, enhances visibility and control over AI usage, and supports long-term secure adoption of emerging technologies.

# Task 3

_(Identical content to the archived "Task3_Detailed_Draft.docx" — Sections A through G covering Executive Summary, Introduction, Methodology, Results, Monitoring and Maintenance Plan, Recommendations, and Conclusion for the completed implementation. See that file for the full text.)_