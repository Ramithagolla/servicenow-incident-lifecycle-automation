#  Incident Lifecycle Automation in ServiceNow

> A practical ServiceNow IT Service Management project demonstrating the complete lifecycle of an IT incident from creation to resolution, including classification, prioritization, escalation, knowledge management, emergency change coordination, child-incident tracking, and final validation.

---

##  Project Overview

**Incident Lifecycle Automation in ServiceNow** is a hands-on IT Service Management project implemented using a **ServiceNow Developer Instance**.

The project demonstrates how an IT incident can be systematically managed throughout its lifecycle using ServiceNow capabilities such as:

- Incident Management
- Service Configuration
- Service Offerings
- Incident Classification
- Priority Management
- Assignment Groups
- Level 2 Escalation
- Knowledge Management
- Change Management
- Parent and Child Incidents
- Work Notes and Investigation Tracking
- Incident Resolution
- Testing and Validation

The project follows a structured **14-phase implementation and documentation approach**, with each phase containing its own documentation and implementation evidence.

---

##  Project Objective

The primary objective of this project is to demonstrate a structured and traceable incident management workflow in ServiceNow.

The implementation focuses on an IT support scenario where a user is unable to connect to the company VPN.

The incident is progressed through the following lifecycle:

**Incident Creation → Classification → Priority Assessment → Assignment → Level 2 Escalation → Investigation → Knowledge Support → Emergency Change Activity → Child Incident Tracking → Resolution → Validation**

---

##  ServiceNow Environment

| Component | Details |
|---|---|
| Platform | ServiceNow |
| Environment | ServiceNow Developer Instance |
| Application Area | IT Service Management |
| Primary Process | Incident Management |
| Service | IT Incident Management Service |
| Service Offering | Standard IT Support |
| Assignment Group | Network |

---

##  Primary Incident

### Incident: INC0010014

**Issue:** Unable to connect to company VPN

| Field | Value |
|---|---|
| Incident Number | INC0010014 |
| Caller | Abel Tuter |
| Category | Network |
| Subcategory | VPN |
| Service | IT Incident Management Service |
| Service Offering | Standard IT Support |
| Channel | Self-service |
| Impact | 2 – Medium |
| Urgency | 2 – Medium |
| Priority | 3 – Moderate |
| Assignment Group | Network |
| Final State | Resolved |
| Resolution Code | Resolved by change |

The incident was classified as a **Network > VPN** issue and progressed through investigation, escalation, change coordination, and resolution.

---

##  Child Incident

A child incident was created to track the Level 2 investigation separately.

### Incident: INC0010016

| Field | Value |
|---|---|
| Child Incident | INC0010016 |
| Parent Incident | INC0010014 |
| Category | Network |
| Subcategory | VPN |
| Assignment Group | Network |
| Purpose | Level 2 investigation and troubleshooting |
| Final State | Resolved |

The parent-child relationship provides traceability between the primary incident and the detailed Level 2 investigation.

---

##  Knowledge Management

### Knowledge Article: KB0010001

**Title:** VPN Connection Troubleshooting

The approved knowledge article was integrated into the incident workflow to provide troubleshooting guidance for the VPN connectivity issue.

The existing approved knowledge article was reused rather than creating a duplicate article.

**Status:** Approved

---

##  Change Management

### Emergency Change: CHG0030002

An Emergency Change was manually created to support the restoration of VPN connectivity.

| Field | Value |
|---|---|
| Change Number | CHG0030002 |
| Model | Emergency |
| Type | Emergency |
| State | New |
| Category | Other |
| Service | IT Incident Management Service |
| Service Offering | Standard IT Support |
| Assignment Group | Network |
| Priority | 3 – Moderate |
| Impact | 2 – Medium |

The Emergency Change was documented in the incident work notes and its purpose was recorded in relation to **INC0010014**.

> **Note:** The ServiceNow instance used for this project did not expose a standard `rfc` field on the Incident form. Therefore, the incident-to-change traceability was maintained through the change description and incident work notes rather than claiming an RFC field relationship.

---

#  Project Lifecycle

The project was implemented and documented in **14 phases**.

| Phase | Description |
|---|---|
| **01** | Requirement Analysis |
| **02** | Service and Service Offering |
| **03** | Incident Record Creation |
| **04** | Incident Classification and Priority |
| **05** | Knowledge Integration |
| **06** | Reassignment and Level 2 Escalation |
| **07** | Level 2 Investigation Tracking |
| **08** | Emergency Change Request Creation |
| **09** | Child Incident Creation |
| **10** | Incident Resolution |
| **11** | Knowledge Creation and Reuse |
| **12** | Final Validation |
| **13** | Testing and Deployment Validation |
| **14** | Conclusion |

---

# 🛠️ Implementation Workflow

## 1. Requirement Analysis

The incident lifecycle requirements were analyzed and the overall workflow was planned before implementation.

The project was designed around an IT VPN connectivity incident requiring classification, escalation, investigation, knowledge support, change coordination, and resolution.

---

## 2. Service and Service Offering

A dedicated ServiceNow service was configured:

**IT Incident Management Service**

A corresponding service offering was created:

**Standard IT Support**

This establishes the service context for the incident management process.

---

## 3. Incident Creation

Incident **INC0010014** was created to represent the VPN connectivity issue.

The incident contains the required caller, description, service, category, and other incident information.

---

## 4. Incident Classification and Priority

The incident was classified as:

**Category:** Network  
**Subcategory:** VPN

The incident was assessed using:

**Impact:** 2 – Medium  
**Urgency:** 2 – Medium  
**Priority:** 3 – Moderate

This provides a structured basis for determining incident priority.

---

## 5. Knowledge Integration

The approved knowledge article:

**KB0010001 – VPN Connection Troubleshooting**

was associated with the incident to support investigation and troubleshooting.

---

## 6. Level 2 Escalation

The incident was reassigned to the:

**Network** assignment group

A work note was added documenting the escalation to the Level 2 support team.

---

## 7. Level 2 Investigation

The investigation progress was tracked using ServiceNow work notes.

The incident remained in progress while the Network team investigated the VPN connectivity problem.

---

## 8. Emergency Change

Emergency Change **CHG0030002** was created to support the restoration of VPN connectivity.

The change activity was documented in the incident work notes.

---

## 9. Child Incident

Child Incident **INC0010016** was created under parent Incident **INC0010014**.

The child incident was used to track Level 2 investigation and troubleshooting activities.

---

## 10. Incident Resolution

After the investigation and change activity, the VPN connectivity issue was considered resolved.

The parent incident was resolved with:

**Resolution Code:** Resolved by change

The child incident was also resolved as part of the completed incident lifecycle.

---

## 11. Knowledge Creation and Reuse

The approved VPN troubleshooting knowledge article was reused as part of the incident resolution process.

This demonstrates how knowledge management can support faster and more consistent incident resolution.

---

## 12. Final Validation

The final implementation was validated by checking:

- Parent incident state
- Child incident state
- Knowledge article status
- Assignment group
- Incident classification
- Priority
- Resolution information
- Emergency Change documentation
- Parent-child relationship

All major implementation components were successfully validated.

---

## 13. Testing and Deployment Validation

Functional validation was performed against the implemented workflow.

The following areas were tested:

- Incident creation
- Incident classification
- Priority assessment
- Assignment
- Level 2 escalation
- Knowledge integration
- Emergency Change
- Child incident creation
- Investigation tracking
- Incident resolution
- Parent-child resolution

The implementation successfully passed the defined validation checks.

---

## 14. Conclusion

The project successfully demonstrates a complete incident lifecycle using ServiceNow IT Service Management capabilities.

It provides practical experience in managing incidents from initial creation through classification, prioritization, escalation, investigation, knowledge support, change coordination, child-incident tracking, and final resolution.

---

#  Skills Demonstrated

This project demonstrates practical knowledge of:

### ServiceNow

- Incident Management
- Service Configuration
- Service Offerings
- Incident Classification
- Impact and Urgency
- Priority Management
- Assignment Groups
- Incident Escalation
- Work Notes
- Knowledge Management
- Change Management
- Parent and Child Incidents
- Incident Resolution
- Testing and Validation

### ITSM Concepts

- Incident lifecycle management
- Incident prioritization
- Support group escalation
- Knowledge-based troubleshooting
- Change coordination
- Incident traceability
- Parent-child incident management
- Resolution and closure
- Functional validation

### Documentation & Version Control

- GitHub repository management
- Phase-based project documentation
- Technical documentation
- Implementation evidence
- Structured project organization
- Version-controlled project history

---

#  Repository Structure

The repository is organized according to the 14 implementation phases.

```text
servicenow-incident-lifecycle-automation/
│
├── Phase-01-Requirement-Analysis/
├── Phase-02-Service-and-Service-Offering/
├── Phase-03-Incident-Record-Creation/
├── Phase-04-Incident-Classification-and-Priority/
├── Phase-05-Knowledge-Integration/
├── Phase-06-Reassignment-and-Level-2-Escalation/
├── Phase-07-Level-2-Investigation-Tracking/
├── Phase-08-Emergency-Change-Request-Creation/
├── Phase-09-Child-Incident-Creation/
├── Phase-10-Incident-Resolution/
├── Phase-11-Knowledge-Creation-and-Reuse/
├── Phase-12-Final-Validation/
├── Phase-13-Testing-and-Deployment-Validation/
├── Phase-14-Conclusion/
│
└── README.md
