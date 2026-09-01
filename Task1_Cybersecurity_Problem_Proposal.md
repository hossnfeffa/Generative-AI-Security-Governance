# Implementing Secure Governance and Technical Controls for Generative AI Usage in a Managed Service Provider Environment

**Brent Petty**

Cybersecurity and Information Assurance Capstone (D833)

Western Governors University

March 2026

Task 1: Cybersecurity Problem

# Cybersecurity Problem - Context

This project will be conducted within a mid-sized managed service provider (MSP) environment that supports multiple small-to-medium business clients across various industries. Employees within the MSP, including help desk technicians and support staff, typically have limited administrative access but routinely interact with client systems for troubleshooting, remote support, and issue resolution.

As part of daily operations, employees are increasingly using generative AI tools such as AI-assisted troubleshooting platforms and integrated assistants like Microsoft Copilot to improve efficiency and reduce resolution times. These tools may be used during screen-sharing sessions, documentation creation, or problem analysis, often involving real-time interaction with client environments.

While these tools provide operational benefits, their rapid adoption has outpaced the implementation of formal security controls, monitoring mechanisms, and usage policies within the MSP environment. This creates a gap between productivity gains and the organization's ability to manage emerging cybersecurity risks associated with generative AI usage.

# Cybersecurity Problem - Problem Statement

The unmanaged use of generative AI tools within the MSP environment introduces significant cybersecurity risks, including the potential exposure of proprietary and sensitive client information. Employees may unintentionally input confidential data—such as system configurations, logs, or client-specific details—into AI platforms without awareness of how that data is stored, processed, or reused.

Additionally, the lack of governance and technical controls surrounding AI usage increases the risk of prompt injection attacks, data leakage, and non-compliance with client security requirements or regulatory standards. Without a structured framework to control and monitor AI interactions, the organization is unable to effectively mitigate these risks.

This project will address the need for a secure and controlled approach to generative AI usage by identifying vulnerabilities, assessing associated risks, and proposing a combination of technical and governance-based controls to protect sensitive information within the MSP environment.

# Cybersecurity Technical Control Solution - Proposed Control

This project will implement a secure governance and technical control framework to manage the use of generative AI tools within a managed service provider (MSP) environment. The proposed solution will combine data loss prevention (DLP), access control, monitoring, and policy enforcement to reduce the risk of sensitive data exposure.

The technical implementation will leverage tools within the Microsoft security ecosystem, including Microsoft Purview for Data Loss Prevention (DLP) policy enforcement and data classification, Microsoft Defender for Endpoint for endpoint monitoring and control, and Microsoft Sentinel for centralized logging and security event analysis.

These tools will be used to detect and prevent the transmission of sensitive data into generative AI platforms, monitor user interactions with AI tools, and provide visibility into potential misuse. In addition to technical controls, the solution will include the development of acceptable use policies and user awareness guidance to ensure that employees understand how to securely interact with AI technologies.

# Scope

The scope of this project will include endpoint devices used by MSP employees, such as workstations and laptops, as well as the applications and services through which generative AI tools are accessed, including browser-based platforms and Microsoft Copilot.

The project will focus on systems used for client support activities, including help desk operations, remote troubleshooting sessions, and documentation workflows. Data within scope includes client-related information such as system configurations, logs, and other potentially sensitive data.

The implementation will be designed for a mid-sized MSP environment and will focus on securing internal processes rather than modifying client systems.

# Objectives

- Implement Data Loss Prevention (DLP) controls to prevent sensitive data exposure.
- Establish monitoring and logging for AI usage.
- Develop governance policies for AI usage.
- Reduce risks such as data leakage and prompt injection.
- Align with NIST and CIS frameworks.
- Improve employee awareness of secure AI practices.

# Project Stakeholders

The project will involve IT and help desk teams, the security team, MSP leadership, clients, compliance/legal stakeholders, and all employees. Each group plays a role in implementation, oversight, or adherence to policies, ensuring the solution balances security with operational efficiency.

# Implementation Plan

Phase 1: Assessment – Identify current AI usage and risks.

Phase 2: Design – Develop DLP policies, monitoring, and governance framework.

Phase 3: Implementation – Deploy controls using Microsoft tools.

Phase 4: Testing – Validate effectiveness and refine.

Phase 5: Deployment – Roll out organization-wide with training.

Phase 6: Monitoring – Continuously improve and adjust controls.

# Sources

National Institute of Standards and Technology. (2018). Framework for Improving Critical Infrastructure Cybersecurity.

National Institute of Standards and Technology. (2020). NIST SP 800-53 Rev. 5.

National Institute of Standards and Technology. (2023). AI Risk Management Framework.

Center for Internet Security. (2021). CIS Critical Security Controls v8.

Microsoft. (2023). Microsoft Purview Documentation.

Microsoft. (2023). Microsoft Defender for Endpoint Documentation.

Microsoft. (2023). Microsoft Sentinel Documentation.