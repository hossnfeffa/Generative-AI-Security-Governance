# Securing Generative AI in a Managed Service Provider Environment

**John Brent Petty**

Western Governors University

D833 Cybersecurity Information and Assurance Capstone

John Jamison

April 20, 2026

Task 3: Technical Report

# Executive Summary

## Problem

Front Range Managed Services (FRMS), a mid-sized managed service provider (MSP), operated in a Microsoft-based environment where employees increasingly relied on generative artificial intelligence (AI) tools to support troubleshooting, documentation, and client service activities. However, the use of these tools was largely unmanaged, with no formal governance policies, Data Loss Prevention (DLP) controls, or monitoring mechanisms in place. This created a significant cybersecurity risk, as employees could unintentionally expose sensitive client data through AI interactions or rely on unverified AI-generated outputs.

## Objectives

The objective of this project was to implement a secure and controlled framework for generative AI usage within the organization. This included deploying Data Loss Prevention (DLP) policies using Microsoft Purview, implementing endpoint monitoring through Microsoft Defender for Endpoint, and enabling centralized logging and analysis using Microsoft Sentinel. Additionally, governance policies and employee training were introduced to define acceptable AI usage and improve awareness of risks such as data leakage and prompt injection.

## Outcomes

Following implementation, the solution improved visibility into employee interactions with generative AI tools and reduced the likelihood of sensitive data exposure. DLP controls successfully detected and prevented the transmission of confidential information, while centralized logging enabled monitoring, alerting, and investigation of potential policy violations. The solution maintained operational efficiency with only minor workflow adjustments, allowing employees to continue using AI tools in a more secure and controlled manner.

## Impact

The project resulted in measurable improvements to the organization's security posture, including enhanced data protection, improved monitoring capabilities, and stronger alignment with industry frameworks such as the NIST Cybersecurity Framework and CIS Critical Security Controls. Key lessons learned include the importance of balancing security controls with usability, the need for ongoing policy tuning, and the critical role of user training in mitigating human-related risks. The solution also provides a scalable foundation for managing future AI-related risks while enabling continued use of generative AI technologies.

## Cybersecurity Technical Control Solution

The implemented cybersecurity technical control solution establishes a secure framework for managing generative artificial intelligence (AI) usage within the Front Range Managed Services (FRMS) environment. The solution was designed to reduce the risk of sensitive data exposure, improve visibility into user interactions with AI tools, and enforce governance over how generative AI technologies are used during daily operations.

The solution leverages existing Microsoft security technologies to provide layered protection through Data Loss Prevention (DLP), endpoint monitoring, and centralized logging. Microsoft Purview was implemented to enforce DLP policies that detect and prevent the transmission of sensitive client data into generative AI platforms. These policies identify data types such as personally identifiable information (PII), system configurations, and client-specific technical details. When sensitive data is detected, actions such as blocking the request, generating alerts, or notifying the user are triggered to prevent unauthorized data exposure.

Microsoft Defender for Endpoint was configured to monitor endpoint-level activity and enforce access controls related to AI usage. This includes visibility into browser activity, application usage, and access to AI platforms. Controls were applied to restrict access to unapproved AI tools and identify potentially risky behavior associated with data handling and external communication.

Microsoft Sentinel was implemented as the centralized Security Information and Event Management (SIEM) solution to aggregate logs from Microsoft Purview and Defender for Endpoint. This enabled correlation of events across the environment, real-time alerting, and investigation of suspicious activity related to generative AI usage. The integration of these tools provides continuous monitoring and supports incident detection and response capabilities.

In addition to technical controls, governance policies were developed to define acceptable use of generative AI tools within the organization. These policies establish clear guidelines for handling sensitive data, interacting with AI systems, and verifying AI-generated outputs. Employee training was conducted to reinforce these policies and improve awareness of risks such as data leakage and prompt injection attacks.

Overall, this solution provides a layered and integrated approach to securing generative AI usage. By combining technical enforcement, monitoring, and governance, the organization is able to reduce cybersecurity risk while maintaining the operational benefits of AI technologies.

## Stakeholders

Several key stakeholders were involved in the implementation and ongoing success of the cybersecurity technical control solution within Front Range Managed Services (FRMS).

The IT and help desk teams were primary stakeholders, as they are the primary users of generative artificial intelligence (AI) tools within the organization. These individuals were responsible for adopting the implemented controls, adhering to acceptable use policies, and incorporating secure AI practices into their daily workflows. Their feedback was critical in ensuring that the solution maintained operational efficiency while enhancing security.

The security team played a central role in the design, implementation, and monitoring of the solution. This included configuring Data Loss Prevention (DLP) policies within Microsoft Purview, managing endpoint monitoring through Microsoft Defender for Endpoint, and analyzing security events and alerts within Microsoft Sentinel. The security team is also responsible for ongoing policy tuning, threat detection, and incident response.

MSP leadership and management served as key stakeholders by providing strategic direction, approving resource allocation, and ensuring alignment with organizational goals. Their support was essential for enforcing governance policies and driving organization-wide adoption of secure AI practices.

Clients are indirect but critical stakeholders, as the MSP handles sensitive client data during support operations. Protecting client information was a primary objective of the solution, and maintaining client trust is essential to the organization's continued success and contractual obligations.

Compliance and legal stakeholders ensured that the implementation aligned with applicable regulatory requirements, industry standards, and contractual obligations. Their involvement helped reduce legal and compliance risks associated with generative AI usage.

Finally, all employees within the organization are stakeholders, as they are required to follow established policies and participate in training to ensure the secure and appropriate use of generative AI tools.

# Methodology

## Implementation Strategy

The implementation of the cybersecurity technical control solution was executed using a structured, phase-based approach to ensure controlled deployment, minimal disruption to operations, and effective integration within the existing Front Range Managed Services (FRMS) environment. The strategy focused on aligning technical controls with existing Microsoft infrastructure while gradually introducing governance and monitoring capabilities.

The first phase involved assessment and requirements analysis. During this phase, current usage of generative artificial intelligence (AI) tools across the organization was evaluated to identify how employees interacted with these platforms and what types of data were being shared. Stakeholder input from IT, security, and management teams was collected to define security requirements and prioritize risks related to data exposure and AI misuse.

The second phase focused on solution design. Data Loss Prevention (DLP) policies were developed within Microsoft Purview to identify and protect sensitive data types, including personally identifiable information (PII), system configurations, and client-specific technical data. Endpoint monitoring and access control strategies were designed using Microsoft Defender for Endpoint to provide visibility into user behavior and restrict access to unapproved AI platforms. Logging and monitoring requirements were defined for Microsoft Sentinel to ensure centralized visibility and correlation of security events.

The third phase consisted of implementation and configuration of the technical controls. Microsoft Purview DLP policies were deployed to monitor and control data interactions with generative AI tools, including blocking or alerting on sensitive data transmission. Microsoft Defender for Endpoint was configured across all relevant endpoint devices to monitor application usage and enforce security policies related to AI access. Microsoft Sentinel was integrated with both Purview and Defender for Endpoint to collect logs, enable alerting, and support incident investigation. Governance policies were also implemented to define acceptable use of generative AI tools, and access controls were enforced based on organizational requirements.

The fourth phase involved testing and validation. DLP policies were tested to ensure accurate detection of sensitive data and to minimize false positives. Endpoint monitoring and access restrictions were validated to confirm that unauthorized AI tools were appropriately controlled. Logging and alerting within Microsoft Sentinel were tested to ensure that events were correctly captured and correlated. Feedback from users was collected to identify usability issues and refine policy configurations.

The final phase included full deployment and user training. The solution was rolled out across the organization, and employees were trained on acceptable use policies, secure AI practices, and awareness of risks such as data leakage and prompt injection. Training ensured that users understood both the technical controls and their role in maintaining security. Following deployment, the solution transitioned into continuous monitoring and improvement, with ongoing adjustments made to policies and configurations based on observed user behavior and emerging threats.

This phased implementation strategy ensured that the solution was effectively integrated into the existing environment, provided strong security controls, and maintained operational efficiency while addressing the risks associated with generative AI usage.

## Implementation Challenges

During the implementation of the cybersecurity technical control solution, several challenges were encountered that required adjustments to ensure both security effectiveness and operational usability.

The first challenge involved the occurrence of false positives within Data Loss Prevention (DLP) policies implemented through Microsoft Purview. Initial policy configurations were overly restrictive, resulting in legitimate user activity being flagged or blocked when interacting with generative artificial intelligence (AI) tools. This created workflow disruptions for help desk staff and reduced user confidence in the solution.

To address this challenge, DLP policies were refined through iterative tuning. Sensitivity labels and rule conditions were adjusted to better align with actual data classification needs, and exception handling was implemented for approved use cases. Additionally, a phased rollout approach was used to monitor policy behavior and make incremental improvements, significantly reducing false positives while maintaining effective protection of sensitive data.

The second challenge involved user resistance to newly implemented controls and governance policies. Employees were accustomed to unrestricted use of AI tools and initially viewed the new restrictions and monitoring capabilities as barriers to productivity. This resistance created a risk of non-compliance and potential attempts to bypass controls.

To mitigate this issue, targeted user training and awareness initiatives were introduced to explain the purpose of the controls and the risks associated with unsecured AI usage. Training emphasized real-world scenarios involving data leakage and prompt injection attacks to reinforce the importance of secure practices. In addition, leadership support and clear communication of acceptable use policies helped drive adoption and encourage compliance across the organization.

By addressing these challenges through policy refinement, user engagement, and phased implementation, the organization was able to balance security requirements with operational efficiency and ensure successful adoption of the solution.

## Physical Resources

The implementation of the cybersecurity technical control solution utilized a combination of existing infrastructure, security tools, and supporting technologies within the Front Range Managed Services (FRMS) environment. These resources were selected to integrate seamlessly with the organization's Microsoft-based ecosystem while providing effective protection and monitoring of generative artificial intelligence (AI) usage.

Endpoint devices, including employee workstations and laptops running Windows 10 and Windows 11, served as the primary platforms for user interaction with generative AI tools. These devices were critical to the implementation, as they are the point at which users access AI platforms and handle client-related data during daily operations.

Microsoft Purview was used as the primary tool for Data Loss Prevention (DLP) and data classification. It played a central role in identifying sensitive data, enforcing policies, and preventing the transmission of confidential information into generative AI platforms. This tool enabled real-time detection, blocking, and alerting based on predefined policy conditions.

Microsoft Defender for Endpoint was implemented to provide endpoint monitoring and enforcement capabilities. It enabled visibility into user activity, including access to AI tools through browsers and applications, and allowed for the restriction of unapproved or high-risk platforms. This tool also contributed telemetry used for detecting suspicious behavior and potential security incidents.

Microsoft Sentinel served as the centralized Security Information and Event Management (SIEM) platform. It aggregated logs and alerts from Microsoft Purview and Defender for Endpoint, allowing for correlation of events, real-time monitoring, and incident investigation. Sentinel also provided dashboards and reporting capabilities to support ongoing analysis and decision-making.

Additional supporting resources included Microsoft 365 and Azure Active Directory, which provided identity management, access control, and integration across the environment. Remote monitoring and management (RMM) tools and the organization's ticketing system were also leveraged to support operational workflows and incident tracking.

These physical and technical resources collectively enabled the implementation of a layered security approach, providing data protection, endpoint visibility, centralized monitoring, and governance over generative AI usage within the organization.

## Testing Protocols

Testing protocols and validation methods were implemented to ensure that the cybersecurity technical control solution functioned as intended and effectively mitigated the risks associated with generative artificial intelligence (AI) usage within the Front Range Managed Services (FRMS) environment. Testing followed a structured approach aligned with industry best practices, focusing on functionality, accuracy, and operational impact.

Data Loss Prevention (DLP) policies within Microsoft Purview were tested using controlled scenarios that simulated real-world user behavior. Test cases included attempts to input sensitive data such as personally identifiable information (PII), system configurations, and client-specific details into generative AI tools. These tests validated that DLP policies correctly detected sensitive data and triggered appropriate actions, including blocking, alerting, or user notification. Additional testing was conducted to evaluate false positives, allowing policies to be refined for accuracy and usability.

Endpoint monitoring and access controls implemented through Microsoft Defender for Endpoint were validated by simulating user access to both approved and unapproved AI platforms. Testing confirmed that access restrictions were enforced as configured and that endpoint telemetry accurately captured user activity. This ensured that unauthorized tools were effectively controlled and that relevant activity was visible for monitoring and analysis.

Centralized logging and alerting capabilities within Microsoft Sentinel were tested to verify that events from Microsoft Purview and Defender for Endpoint were successfully ingested, correlated, and displayed. Test scenarios included generating DLP alerts and simulated suspicious behavior to confirm that alerts were triggered, properly categorized, and available for investigation. Dashboards and reporting features were also reviewed to ensure visibility into system activity and policy enforcement.

User acceptance testing (UAT) was conducted to evaluate the impact of the solution on daily operations. Selected users performed typical tasks involving AI tools to identify any workflow disruptions or usability issues. Feedback from this testing phase was used to refine policy configurations and ensure that the solution balanced security with operational efficiency.

These testing protocols ensured that the implemented solution was validated across technical functionality, monitoring effectiveness, and user experience, providing confidence that the controls were operating as intended and effectively reducing cybersecurity risk.

## Data Collection and Analysis

Data collection and analysis were conducted to evaluate the effectiveness of the implemented cybersecurity technical control solution and to provide continuous visibility into generative artificial intelligence (AI) usage within the Front Range Managed Services (FRMS) environment. The approach focused on collecting relevant security telemetry, analyzing patterns of user behavior, and measuring the impact of the implemented controls.

Data was primarily collected through Microsoft Purview, Microsoft Defender for Endpoint, and Microsoft Sentinel. Microsoft Purview generated logs related to Data Loss Prevention (DLP) policy enforcement, including detected sensitive data, blocked actions, user notifications, and policy violations. These logs provided insight into how frequently sensitive data was being identified and prevented from being transmitted to generative AI tools.

Microsoft Defender for Endpoint contributed endpoint telemetry, including application usage, browser activity, and access attempts to AI platforms. This data was used to monitor how employees interacted with AI tools and to identify any attempts to access unapproved or high-risk platforms.

Microsoft Sentinel served as the centralized platform for aggregating and analyzing collected data. Logs from Purview and Defender for Endpoint were ingested into Sentinel, where they were correlated to identify patterns, trends, and potential security incidents. Sentinel dashboards and queries were used to monitor key metrics, such as the number of DLP alerts, frequency of blocked actions, and user activity related to AI tool usage.

Data analysis focused on evaluating the effectiveness of the solution by measuring reductions in risky behavior and improvements in visibility. Key effectiveness measures included the decrease in attempted transmission of sensitive data, the accuracy of DLP detections, and the organization's ability to detect and respond to suspicious activity. Trends in user behavior were also analyzed to assess the impact of training and policy enforcement over time.

The results of this analysis were used to refine DLP policies, adjust monitoring thresholds, and improve overall system performance. Continuous data collection and analysis enabled the organization to maintain an adaptive security posture, ensuring that controls remained effective against evolving threats associated with generative AI usage.

# Results

## Effectiveness

The implemented cybersecurity technical control solution was effective in mitigating the risks associated with unmanaged generative artificial intelligence (AI) usage within the Front Range Managed Services (FRMS) environment. Prior to implementation, the organization lacked visibility into how employees interacted with AI tools and had no controls in place to prevent the exposure of sensitive client data. Following implementation, the introduction of Data Loss Prevention (DLP), endpoint monitoring, and centralized logging significantly improved both risk reduction and operational awareness.

Microsoft Purview DLP policies successfully detected and prevented the transmission of sensitive data into generative AI platforms. Testing and operational data demonstrated that attempts to input confidential information—such as system configurations and client-related details—were consistently identified and blocked or flagged. This directly reduced the likelihood of data leakage, addressing one of the primary risks identified in the project.

Microsoft Defender for Endpoint improved visibility into user activity by monitoring access to AI tools and identifying potentially risky behavior. The organization gained the ability to detect access to unapproved platforms and enforce restrictions, reducing the attack surface associated with external AI services.

Microsoft Sentinel enhanced the organization's ability to monitor and respond to security events by providing centralized logging and correlation of data from multiple sources. Security teams were able to identify trends, investigate alerts, and respond more efficiently to potential policy violations. This increased the organization's overall detection and response capabilities.

Key performance indicators (KPIs) used to evaluate effectiveness included the number of DLP alerts generated, the reduction in successful attempts to transmit sensitive data, and improved visibility into AI-related user activity. Over time, analysis showed a decrease in high-risk behaviors, indicating that both technical controls and user training contributed to improved security practices.

Overall, the solution effectively mitigated the identified cybersecurity risks by reducing the likelihood of data exposure, improving monitoring capabilities, and enabling more proactive detection and response. The organization transitioned from a reactive posture with limited visibility to a more controlled and monitored environment for generative AI usage.

## Performance Impact

The implementation of the cybersecurity technical control solution had a moderate but manageable impact on system performance and user experience within the Front Range Managed Services (FRMS) environment. Overall, the solution was designed to integrate with existing Microsoft infrastructure, minimizing disruption while enhancing security controls around generative artificial intelligence (AI) usage.

From a system performance perspective, the impact was minimal. Data Loss Prevention (DLP) processing through Microsoft Purview and endpoint monitoring via Microsoft Defender for Endpoint operated efficiently in the background with no significant degradation in endpoint performance or system responsiveness. Log ingestion and analysis within Microsoft Sentinel introduced a slight increase in resource utilization and network traffic; however, this did not negatively affect core business operations or system availability.

From a user experience standpoint, some initial friction was observed following implementation. Users experienced occasional interruptions when DLP policies blocked or flagged attempts to input sensitive data into AI tools. These interactions required users to adjust their workflows and become more aware of how they handled client information during AI-assisted tasks.

Over time, the impact on user experience decreased as policies were refined and users became more familiar with acceptable use guidelines. Training and awareness efforts helped users understand the purpose of the controls, leading to increased compliance and smoother integration into daily workflows. The phased rollout approach also allowed for incremental adjustments, reducing disruption and improving usability.

Overall, while the solution introduced minor workflow changes and brief initial resistance, it successfully balanced security and usability. The organization maintained operational efficiency while significantly improving its ability to protect sensitive data and monitor AI-related activity.

## Compliance Achievements

The implementation of the cybersecurity technical control solution resulted in improved alignment with industry-recognized cybersecurity frameworks and best practices within the Front Range Managed Services (FRMS) environment. By integrating Data Loss Prevention (DLP), endpoint monitoring, and centralized logging, the organization strengthened its ability to meet security and compliance expectations related to data protection and system monitoring.

The solution aligns with the National Institute of Standards and Technology Cybersecurity Framework (CSF), particularly within the Identify, Protect, Detect, and Respond functions. The implementation of DLP policies supports the Protect function by safeguarding sensitive data from unauthorized exposure. Endpoint monitoring and access controls contribute to the Detect function by identifying potentially risky behavior and unauthorized use of generative artificial intelligence (AI) tools. Centralized logging and alerting through Microsoft Sentinel enhance the Respond function by enabling timely investigation and response to security events (NIST, 2018).

Additionally, the solution supports control objectives outlined in Center for Internet Security Critical Security Controls (Version 8). Specifically, the implementation aligns with controls related to data protection, access control, and continuous monitoring. The use of DLP policies ensures that sensitive information is properly classified and protected, while endpoint monitoring and SIEM capabilities provide ongoing visibility into system activity and potential threats (CIS, 2021).

The solution also aligns with guidance from the NIST Artificial Intelligence Risk Management Framework (AI RMF), which emphasizes the importance of governance, risk management, and monitoring in AI-related systems. By implementing governance policies, monitoring user interactions, and reducing the risk of unintended data disclosure, the organization improved its ability to manage emerging risks associated with generative AI technologies (NIST, 2023).

Overall, the implementation enhanced the organization's compliance posture by establishing enforceable technical controls, improving audit visibility, and aligning operations with established cybersecurity standards. These achievements support both internal security objectives and external expectations related to client data protection and regulatory compliance.

## Residual Risks

**Residual Risk #1**

**Risk Description:** Despite the implementation of Data Loss Prevention (DLP) controls and monitoring mechanisms, there remains a risk that users may attempt to bypass controls by modifying or obfuscating sensitive data before submitting it to generative artificial intelligence (AI) tools.

**Threat Source:** Internal users (employees), whether through negligence or intentional behavior, who may attempt to work around implemented controls to complete tasks more quickly or avoid restrictions.

**Remaining Vulnerability:** DLP policies rely on pattern recognition and predefined rules, which may not detect all variations of sensitive data if it is altered or partially masked. Additionally, human behavior remains unpredictable, and users may unintentionally or deliberately circumvent established policies.

**Potential Impact:** If sensitive data is successfully transmitted to external AI platforms, it could result in data leakage, loss of confidentiality, and potential regulatory or contractual consequences. This may also lead to reputational damage and loss of client trust.

**Likelihood Assessment:** Medium — While DLP controls significantly reduce the likelihood of data exposure, the possibility of users attempting to bypass controls remains, particularly in high-pressure operational environments.

**Severity Assessment:** Medium — The impact of a successful bypass could be significant, but the presence of monitoring, logging, and user training reduces the overall severity compared to the pre-implementation environment.

**Residual Risk #2**

**Risk Description:** Generative AI tools may still produce inaccurate, misleading, or manipulated outputs due to prompt injection or adversarial input, which could lead employees to take incorrect actions.

**Threat Source:** External malicious actors or untrusted data sources that introduce adversarial input into AI systems, as well as inherent limitations in AI model reliability.

**Remaining Vulnerability:** The solution focuses primarily on controlling data input and monitoring usage but cannot fully validate the accuracy or integrity of AI-generated outputs. Users may still rely on AI responses without sufficient verification.

**Potential Impact:** Employees acting on incorrect or manipulated AI-generated information could result in system misconfigurations, service disruptions, or improper handling of client environments. This could impact system integrity and availability and lead to operational downtime.

**Likelihood Assessment:** Low to Medium — While user training reduces reliance on unverified outputs, the increasing use of AI tools means exposure to unreliable or manipulated responses remains possible.

**Severity Assessment:** High — Incorrect actions based on AI-generated output could have significant operational and security consequences, particularly in an MSP environment managing multiple client systems.

# Monitoring and Maintenance Plan

## Monitoring Plan

The monitoring plan for the implemented cybersecurity technical control solution focuses on continuous oversight of generative artificial intelligence (AI) usage, data protection activities, and endpoint behavior within the Front Range Managed Services (FRMS) environment. The objective of this plan is to ensure that security controls remain effective, policy violations are detected in a timely manner, and potential threats are identified and addressed proactively.

Microsoft Sentinel serves as the primary monitoring platform, providing centralized visibility into security events and user activity. Logs from Microsoft Purview and Microsoft Defender for Endpoint are continuously ingested into Sentinel, enabling correlation of events across multiple systems. Security analysts utilize dashboards, queries, and alerting mechanisms within Sentinel to monitor key indicators, including Data Loss Prevention (DLP) alerts, blocked data transmission attempts, and access to generative AI platforms.

Microsoft Purview contributes to monitoring by generating real-time alerts related to DLP policy enforcement. These alerts notify the security team when sensitive data is detected or when policy violations occur. Monitoring of these events allows for immediate investigation and response to potential data exposure risks.

Microsoft Defender for Endpoint provides endpoint-level monitoring, capturing telemetry related to application usage, browser activity, and access to AI tools. This enables the organization to identify unusual or unauthorized behavior, such as attempts to access unapproved AI platforms or abnormal patterns of activity.

The monitoring plan includes regular review of alerts and logs by the security team to identify trends, assess policy effectiveness, and detect emerging threats. Automated alerts are configured for high-risk events to ensure rapid response, while periodic analysis of collected data supports continuous improvement of security controls.

By combining real-time alerting, centralized logging, and ongoing analysis, the monitoring plan ensures that the organization maintains visibility into AI-related activity and can respond effectively to potential security incidents.

## Maintenance Plan

The maintenance plan for the cybersecurity technical control solution ensures that implemented controls remain effective, up to date, and aligned with evolving threats and organizational needs within the Front Range Managed Services (FRMS) environment. Ongoing maintenance activities focus on policy refinement, system updates, performance optimization, and continuous support.

Data Loss Prevention (DLP) policies within Microsoft Purview require regular review and tuning to maintain accuracy and effectiveness. As user behavior evolves and new data patterns emerge, policies are adjusted to reduce false positives and ensure appropriate detection of sensitive information. Sensitivity labels, rule conditions, and exception handling are periodically updated based on observed activity and feedback from users.

Microsoft Defender for Endpoint is maintained through regular updates to ensure that endpoint monitoring and threat detection capabilities remain current. This includes applying security updates, updating detection signatures, and reviewing endpoint configurations to ensure consistent policy enforcement across all devices.

Microsoft Sentinel maintenance includes managing data ingestion, retention settings, and alert configurations. Queries, dashboards, and alert rules are periodically reviewed and optimized to improve detection accuracy and reduce noise. Log retention policies are adjusted as needed to balance visibility, compliance requirements, and cost considerations.

System updates and patch management are performed regularly across all endpoint devices and supporting infrastructure to address vulnerabilities and maintain system integrity. This ensures that the environment remains protected against known threats and exploits.

Ongoing support activities include reviewing system performance, addressing user-reported issues, and providing technical assistance related to the implemented controls. The security team conducts periodic evaluations of the solution to identify opportunities for improvement and ensure alignment with organizational security objectives.

Through continuous policy tuning, system updates, and proactive support, the maintenance plan ensures that the cybersecurity solution remains effective, adaptable, and capable of addressing emerging risks associated with generative artificial intelligence usage.

## Incident Response

The incident response plan for the implemented cybersecurity technical control solution outlines the procedures for detecting, responding to, and recovering from security events related to generative artificial intelligence (AI) usage within the Front Range Managed Services (FRMS) environment. The plan is designed to ensure timely identification of incidents, effective containment, and restoration of normal operations while minimizing potential impact.

Detection of potential incidents is primarily achieved through Microsoft Sentinel, which aggregates and correlates logs from Microsoft Purview and Microsoft Defender for Endpoint. Alerts generated from Data Loss Prevention (DLP) policy violations, unusual endpoint activity, or suspicious access to AI tools are monitored in real time by the security team. Automated alerting mechanisms prioritize high-risk events, enabling rapid identification of potential security incidents.

Once an incident is detected, the security team initiates an investigation to determine the scope and severity of the event. This includes analyzing logs, reviewing user activity, and identifying affected systems or data. Microsoft Sentinel provides the necessary visibility and tools to support this investigation, allowing analysts to trace events and understand the sequence of actions leading to the incident.

Containment actions are implemented to prevent further impact. This may include blocking user access to specific AI platforms, isolating affected endpoint devices using Microsoft Defender for Endpoint, or enforcing stricter DLP policies to prevent additional data exposure. These actions are taken based on the nature and severity of the incident.

Following containment, remediation efforts are conducted to address the root cause of the incident. This may involve updating policies, correcting system configurations, or providing additional user guidance to prevent recurrence. If necessary, affected systems are restored to a secure state, and any compromised data or processes are addressed in accordance with organizational policies.

After the incident is resolved, a post-incident review is conducted to evaluate the effectiveness of the response and identify opportunities for improvement. Lessons learned are used to refine monitoring rules, update response procedures, and enhance user training.

This incident response plan ensures that the organization is prepared to effectively manage security events related to generative AI usage, reducing response time and minimizing the impact of potential incidents.

# Recommendations

## Improvements

To further enhance the effectiveness of the cybersecurity technical control solution and address evolving risks associated with generative artificial intelligence (AI), several improvements are recommended for the Front Range Managed Services (FRMS) environment.

The first recommended improvement is the integration of advanced AI-specific threat detection capabilities. While the current solution provides strong visibility and control over data input into AI tools, it does not fully address emerging threats such as prompt injection and adversarial manipulation. Implementing enhanced detection mechanisms—such as behavioral analytics or AI-driven threat detection within Microsoft Sentinel—would improve the organization's ability to identify suspicious patterns and anomalous AI interactions.

The second improvement involves the implementation of automated response capabilities through Security Orchestration, Automation, and Response (SOAR) functionality within Microsoft Sentinel. Automating responses to high-risk events, such as repeated DLP violations or attempts to access unapproved AI platforms, would reduce response time and improve consistency in incident handling. This would allow the security team to respond more efficiently to potential threats while reducing manual workload.

The third improvement is the enhancement of user behavior analytics (UBA) to provide deeper insight into how employees interact with generative AI tools. By establishing behavioral baselines and monitoring deviations, the organization can more effectively detect insider threats, policy violations, or abnormal usage patterns. This capability would strengthen the organization's ability to proactively identify risks that may not be detected through traditional rule-based controls.

These improvements build upon the existing solution by enhancing detection capabilities, increasing automation, and improving visibility into user behavior. Implementing these enhancements would further strengthen the organization's ability to manage emerging AI-related threats while maintaining operational efficiency.

## Mitigation Strategies

To further reduce the residual risks identified after implementation, additional mitigation strategies are recommended to strengthen the organization's security posture and address remaining vulnerabilities associated with generative artificial intelligence (AI) usage.

**Mitigation Strategy for Residual Risk #1 (Bypassing DLP Controls)**

The primary mitigation approach for this risk is the enhancement of Data Loss Prevention (DLP) capabilities through improved data classification, pattern recognition, and contextual analysis. This includes refining DLP policies within Microsoft Purview to detect variations of sensitive data, such as partially masked information or non-standard formatting. Additionally, implementing stricter access controls and limiting the use of generative AI tools to approved platforms can further reduce opportunities for bypass.

This strategy is appropriate and feasible because it builds upon existing tools already deployed within the environment, requiring configuration improvements rather than new infrastructure. Implementation considerations include the need for ongoing policy tuning, increased monitoring of user activity, and potential adjustments to sensitivity labels and detection rules.

The expected effectiveness of this approach is a reduction in the likelihood of successful bypass attempts by improving the accuracy and coverage of DLP detection mechanisms. While it may not eliminate the risk entirely, it significantly strengthens the organization's ability to identify and prevent unauthorized data transmission.

**Mitigation Strategy for Residual Risk #2 (Unreliable or Manipulated AI Outputs)**

To mitigate the risk of employees acting on inaccurate or manipulated AI-generated outputs, the recommended approach is to implement validation and verification procedures for AI-assisted decision-making. This includes requiring users to verify AI-generated recommendations against trusted sources before taking action, particularly for critical system changes or client-related activities. Additionally, integrating warning prompts or guidance within workflows can reinforce the need for validation.

This strategy is appropriate because it directly addresses the human factor associated with AI usage, which cannot be fully controlled through technical measures alone. It is also feasible within the organizational context, as it can be implemented through policy enforcement, training, and minor workflow adjustments without requiring significant technical changes.

Implementation considerations include updating governance policies, incorporating validation steps into standard operating procedures, and reinforcing expectations through ongoing training and awareness programs. Management support is essential to ensure adherence to these practices.

The expected effectiveness of this strategy is a reduction in the impact of incorrect or manipulated AI outputs by ensuring that decisions are verified before execution. This lowers the likelihood of operational errors and helps maintain system integrity and reliability.

## Training

Employee training and awareness are critical components of the cybersecurity technical control solution, ensuring that users understand both the risks associated with generative artificial intelligence (AI) usage and their role in maintaining security within the Front Range Managed Services (FRMS) environment.

Training initiatives were implemented to educate employees on acceptable use policies for generative AI tools, with a focus on preventing the exposure of sensitive client data. Users were instructed on how Data Loss Prevention (DLP) policies function, including how and why certain actions may be blocked or flagged when interacting with AI platforms. This helped reduce confusion and improve compliance with security controls.

Additional training emphasized the risks associated with prompt injection, unreliable AI-generated outputs, and improper data handling. Employees were encouraged to validate AI-generated responses before acting on them, particularly when performing system changes or handling client-related information. Real-world examples and scenarios were used to reinforce these concepts and improve user understanding.

Ongoing awareness efforts include periodic refresher training, updates to policies as new risks emerge, and communication of lessons learned from security incidents. Training is integrated into onboarding processes for new employees and reinforced through regular security communications.

By establishing a strong training and awareness program, the organization reduces the likelihood of human error, improves adherence to security policies, and strengthens the overall effectiveness of the implemented solution.

# Conclusion

This project addressed the growing cybersecurity risks associated with unmanaged generative artificial intelligence (AI) usage within the Front Range Managed Services (FRMS) environment. The primary objective was to design and implement a secure framework that protects sensitive client data while allowing employees to continue leveraging AI tools for operational efficiency.

The implemented solution combined Data Loss Prevention (DLP) policies, endpoint monitoring, centralized logging, and governance controls to create a layered approach to security. Microsoft Purview, Microsoft Defender for Endpoint, and Microsoft Sentinel were successfully integrated to provide data protection, visibility into user activity, and improved detection and response capabilities. These controls effectively reduced the likelihood of data leakage, improved monitoring of AI usage, and strengthened the organization's overall security posture.

The solution was successful in balancing security and usability, allowing employees to continue using generative AI tools within a controlled and monitored environment. Measurable improvements included increased visibility into AI-related activity, reduced high-risk behavior, and stronger alignment with industry frameworks such as the NIST Cybersecurity Framework and CIS Critical Security Controls.

Two critical follow-up actions are recommended to further enhance the solution. First, the implementation of automated response capabilities through Security Orchestration, Automation, and Response (SOAR) would improve response times and reduce manual workload for the security team. Second, the expansion of user behavior analytics would provide deeper insight into user activity and enable more proactive identification of potential risks.

In conclusion, this project demonstrates that generative AI technologies can be securely integrated into an MSP environment when supported by appropriate technical controls, governance policies, and user training. The solution provides a scalable foundation for managing future AI-related risks while maintaining the organization's commitment to protecting client data and ensuring operational effectiveness.

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

The implemented cybersecurity technical control solution for securing generative artificial intelligence (AI) usage within the Front Range Managed Services (FRMS) environment is based on a layered architecture that integrates endpoint monitoring, Data Loss Prevention (DLP), and centralized logging.

**Architecture Description**

The solution architecture consists of endpoint devices used by employees, which serve as the primary interaction point for generative AI tools. These endpoints are monitored and controlled using Microsoft Defender for Endpoint, providing visibility into user activity and enforcing security policies.

Microsoft Purview is integrated to apply Data Loss Prevention (DLP) policies that inspect user interactions with generative AI platforms. These policies identify sensitive data, such as personally identifiable information (PII), system configurations, and client-specific details, and enforce actions such as blocking, alerting, or user notification when policy violations occur.

All activity generated from DLP enforcement and endpoint monitoring is forwarded to Microsoft Sentinel, which acts as the centralized Security Information and Event Management (SIEM) platform. Sentinel aggregates logs, correlates events, and enables real-time monitoring, alerting, and incident investigation.

Generative AI tools, including Microsoft Copilot and browser-based AI platforms, are accessed through endpoint devices and are subject to DLP inspection and monitoring controls. This ensures that all AI-related interactions are governed by security policies and are visible to the organization.

**Key Components**

- **Endpoint Devices (User Workstations)** — Primary interface for employee interaction with generative AI tools and client systems.
- **Microsoft Defender for Endpoint (Monitoring and Enforcement)** — Provides endpoint visibility, detects suspicious behavior, and enforces access controls related to AI usage.
- **Microsoft Purview (Data Loss Prevention and Data Classification)** — Identifies and protects sensitive data by enforcing DLP policies during AI interactions.
- **Microsoft Sentinel (SIEM and Centralized Logging)** — Aggregates logs, correlates events, enables alerting, and supports incident response.
- **Generative AI Tools (e.g., Microsoft Copilot, Browser-Based Platforms)** — Tools used by employees for troubleshooting, documentation, and analysis, operating within controlled and monitored environments.