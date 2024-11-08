---
title: 'NIST SP 800-53 & 800-53B'
subtitle: 'U.S. Federal Cybersecurity Compliance Part II: NIST SP 800-53 & 800-53B'
date: 2024-11-07 10:40:00
location: New York, NY
description: The Security and Privacy Controls for Information Systems and Organizations provides an entire catalog of security and privacy controls to protect organizations from many different threats.
featured_image: '/images/post/security_controls.png'
---

## U.S. Federal Cybersecurity Compliance Part II

You can find Part I of my U.S. Federal Cybersecurity Compliance blog, [here](/blog/usfederal-cybersecurity-compliance/).

## NIST 800-53: Security and Privacy Controls for Information Systems and Organizations

As a Cybersecurity professional, engineering lead, or an analyst, this is one of the documents to keep bookmarked (or better yet, saved on your desktop but make sure you’re checking for updates). When you think of the NIST SP 800-53, think “security controls.”

According to the document’s abstract, “This publication provides a catalog of security and privacy controls for information systems and organizations to protect organizational operations and assets, individuals, other organizations, and the Nation from a diverse set of threats and risks, including hostile attacks, human errors, natural disasters, structural failures, foreign intelligence entities, and privacy risks. The controls are flexible and customizable and implemented as part of an organization-wide process to manage risk.” [^1] 

### Meet the Security Control Families

There are 20 families of security controls, and each of those families will contain controls related to the topic referenced by the family. The families all have a two-character unique identifier. Please see the table below:

| ID | Familiy                                   |
|------------------------------------------------|
| AC | Access Control                            |
| AT | Awareness and Training                    |
| AU | Audit and Accountability                  |
| CA | Assessment, Authorization, and Monitoring |
| CM | Configuration Management                  |
| CP | Contingency Planning                      |
| IA | Identification and Authentication         |
| IR | Incident Response                         | 
| MA | Maintenance                               |
| MP | Media Protection                          |
| PE | Physical and Environmental Protection     |
| PL | Planning                                  |
| PM | Program Management                        |
| PS | Personnel Security                        |
| PT | PII Processing and Transparency           |
| RA | Risk Assessment                           |
| SA | System and Services Acquisition           |
| SC | System and Communications Protection      |
| SI | System and Information Integrity          |
| SR | Supply Chain Risk Management              |

In the cases where you’re looking to implement controls from the ground up, it is best to reference the [NIST SP 800-53B publication](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53B.pdf), called Control Baselines for Information Systems and Organizations. These are the “…minimum set of controls mandatory to protect federal information and information systems.” 

## NIST SP 800-53B: Control Baselines for Information Systems and Organizations
On the NIST SP 800-53B publication, you will find not only the security control baseline allocations per family, but also those security control baselines that are specific for low-impact, moderate-impact, and high-impact systems.

If you’re starting from the ground up with a low-impact system, below is a breakdown of the minimum set of security and privacy control baselines recommended by NIST 800-53B:

| **ID**                | **Family**               | **Privacy**           | **Low**                      |
| --------------------- | ------------------------ | --------------------- | ---------------------------- |
| **AC**                | Access Control           | AC-1, AC-3(14)        | AC-1, AC-2, AC-3, AC-7, AC-8, AC-14, AC-17, AC-18, AC-19, AC-20, AC-22                                                                                              |
| **AT**                | Awareness and Training   | AT-1, AT-2, AT-3, AT-3(5), AT-4  | AT-1, AT-2, AT-2(2), AT-3, AT-4                                                                                                      |
| **AU**                | Audit and Accountability | AU-1, AU-2, AU-3(3), AU-11  | AU-1, AU-2, AU-3, AU-4, AU-5, AU-6, AU-8, AU-9, AU-11, AU-12                                                                                              |
| **CA**                | Assessment, Authorization, and Monitoring | CA-1, CA-2, CA-5, CA-6, CA-7, CA-7(4)  | CA-1, CA-2, CA-3, CA-5, CA-6, CA-7, CA-7(4), CA-9                                                                                 |
| **CM**                | Configuration Management | CM-1, CM-4            | CM-1, CM-2, CM-4, CM-5, CM-6, CM-7, CM-8, CM-10, CM-11                                                                                                     |
| **CP**                | Contingency Planning     |               | CP-1, CP-2, CP-3, CP-4, CP-9, CP-10  |
| **IA**                | Identification and Authentication |      | IA-1, IA-2, IA-2(1), IA-2(2), IA-2(8), IA-2(12), IA-4, IA-5, IA-5(1), IA-6, IA-7, IA-8, IA-8(a), IA-8(2), IA-8(4), IA-11                                                   |
| **IR**                | Incident Response        | IR-1, IR-2, IR-2(3), IR-3, IR-4, IR-5, IR-6, IR-7, IR-8, IR-8(1) | IR-1, IR-2, IR-4, IR-5, IR-6, IR-7, IR-8                                                                              |
| **MA**                | Maintenance              |                        | MA-1, MA-2, MA-4, MA-5      |
| **MP**                | Media Protection         | MP-1, MP-6             | MP-1, MP-2, MP-6, MP-7      |
| **PE**                | Physical and Environmental Protection | PE-8(3)   | PE-1, PE-2, PE-3, PE-6, PE-8, PE-12, PE-12, PE-14, PE-15, PE-16                                                                                              |
| **PL**                | Planning                 | PL-1, PL-2, PL-4, PL-4(1), PL-8, PL-9                | PL-1, PL-2, PL-4, PL-4(1), PL-10, PL-11                                                                                              |
| **PM**                | Program Management       | PM-3, PM-4, PM-5(1), PM-6, PM-7, PM-8, PM-9, PM-10, PM-11, PM-13, PM-14, PM-17, PM-18, PM-19, PM-20, PM-20(1), PM-21, PM-22, PM-24, PM-25, PM-26, PM-27, PM-28, PM-31 | As per NIST’s documentation: _“Deployed organization-wide. Supports information security program. Independent of any system impact level.”_       |
| **PS**                | Personnel Security       | PS-6                    | PS-1, PS-2, PS-3, PS-4, PS-5, PS-6, PS-7, PS-8, PS-9                                                                                                      |
| **PT**                | PII Processing and Transparency | PT-1, PT-2, PT-3, PT-4, PT-5, PT-5(2), PT-6, PT-6(1), PT-6(2), PT-7, PT-7(1), PT-7(2), PT-8      | As per NIST’s documentation: _“Personally Identifiable Information Processing and Transparency controls are not allocated to the security baselines. Privacy baseline controls are selected based on the selection criteria defined in Section 2.2.”_                                                                                                      |
| **RA**                | Risk Assessment          | RA-1, RA-3, RA-7, RA-8   | RA-1, RA-2, RA-3, RA-3(1), RA-5, RA-5(2), RA-5(11), RA-7                                                                                                      |
| **SA**                | System and Services Acquisition | SA-1, SA-2, SA-3, SA-4, SA-8(33), SA-9, SA-11 | SA-1, SA-2, SA-3, SA-4, SA-4(10), SA-5, SA-8, SA-9, SA-22                                                                         |
| **SC**                | System and Communications Protection | SC-7(24)                                 | SC-1, SC-5, SC-7, SC-12, SC-13, SC-15, SC-20, SC-21, SC-22, SC-39                                                                                                     |
| **SI**                | System and Information Integrity | SI-1, SI-12, SI-12(1), SI-12(2), SI-12(3), SI-18, SI-18(4), SI-19 | SI-1, SI-2, SI-3, SI-4, SI-5, SI-12                                                                             |
| **SR**                | Supply Chain Risk Management     |                                              | SR-1, SR-2, SR-2(1), SR-3, SR-5, SR-8, SR-10, SR-11, SR-11(1), SR-11(2), SR-12                                                       |
|                       |                                  |                                              |                           |
| **Totals per baseline (privacy and low):** ||              **96**         | **149**                     |

That is a total of 96 privacy controls and 149 low-impact security controls that would need to be implemented. This can help you develop a roadmap and have a better understanding on security controls to prioritize for your organization.

### Real-World Example: Protecting Personally Identifiable Information (PII)
Let’s bring this into the real world with an example that’s familiar to many: protecting Personally Identifiable Information (PII). We can take security control **SI-12(2)** as our reference, which talks about minimizing personally identifiable information particularly in testing, training, and research. 

Here is how you can implement it practically:
1.	Create a Policy: Have a clear policy to enforce minimal PII use (**SI-1**).
2.	Use “Fake” Data: Whenever possible, substitute PII with mock data, especially in non-production environments.
3.	Be Mindful in Research: Sometimes, using real data is necessary, like in research. Make sure this aligns with your organization’s policy and is well-justified.

By following these steps, you help minimize data exposure risks, aligning with **SI-12(2)** and other privacy-focused controls.



[^1]: Taken from the Abstract section of the NIST SP 800-53, rev5: [https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r5.pdf](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r5.pdf)