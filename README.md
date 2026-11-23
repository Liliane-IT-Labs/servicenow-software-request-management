
# ServiceNow IT Support Project: Software Installation Request Management

**Turning a blocked software installation into a documented, assigned, and trackable IT service request.**

**Project:** IT Service Management (ITSM)

**Platform:** ServiceNow

**Environment:** Windows 11 | ServiceNow Developer Instance

**Focus:** Service Catalog, Software Requests, Request Fulfillment, IT Security

---

## 1. Business Scenario

### The Problem

A new employee working on a Windows 11 computer named **Office1** needs Audacity, a digital audio editing application, to complete work-related tasks.

However, when the employee attempts to install the application, Windows requests administrator credentials.

Because the employee has a standard user account without local administrator privileges, the installation cannot continue.

The employee needs assistance from the IT Support team.

### The IT Solution

I use **ServiceNow** to manage the software installation request through a structured IT service management process.

Instead of bypassing Windows security controls, the employee submits a Service Catalog request.

The request is documented, tracked, and routed to an IT technician for review and authorized fulfillment.

### Why ServiceNow?

ServiceNow provides a centralized platform for managing employee IT requests, assigning responsibilities, tracking progress, and maintaining a history of support activities.

This helps organizations manage software requests consistently while maintaining security and accountability.

---

## 2. Project Objectives

The goal is to demonstrate how a software installation request moves through the ServiceNow request management process.

**Technical objectives:**

- Submit a software installation request through the Service Catalog.
- Document the employee's business need.
- Capture contact and device information.
- Create a trackable Request (REQ) and Requested Item (RITM).
- Route the request to the appropriate IT technician.
- Record the required priority and due date.
- Review and verify the submitted request.
- Understand the approval and fulfillment process.

## 3. Lab Environment

| Component           | Configuration         |
| ------------------- | --------------------- |
| ITSM Platform       | ServiceNow            |
| Request Type        | Software Installation |
| Application         | Audacity              |
| Computer            | Office1               |
| Device              | HP Laptop             |
| Operating System    | Windows 11            |
| User Access         | Standard User         |
| Assigned Technician | Joshua Anderson       |
| Requested Priority  | High                  |
| Category            | Software              |

---

## 4. Project Architecture

```
EMPLOYEE
   |
   | Needs Audacity installed
   v
WINDOWS 11 - OFFICE1
   |
   | Administrator access required
   v
SERVICENOW SERVICE CATALOG
   |
   | Submit software request
   v
REQUEST (REQ)
   |
   v
REQUESTED ITEM (RITM)
   |
   | Review and assignment
   v
IT SUPPORT / CATALOG TASK
   |
   | Joshua Anderson
   v

```

---

# 5. Implementation: Step-by-Step

## Phase 1: Employee Software Request

### Step 1 — Identify the Access Restriction

**Action**

1. Sign in to Windows 11 on Office1.
2. Attempt to install Audacity.
3. Observe the administrator credential prompt.
4. Identify that the employee does not have administrator privileges.
5. Do not attempt to bypass the security restriction.

**Goal:** Understand why the employee cannot independently install the software.

**Technical explanation:**

Windows User Account Control (UAC) protects the system by requiring appropriate authorization for administrative operations.

The employee must request assistance through the approved IT process.

**Expected result:** The employee identifies the installation blocker and requests IT assistance.

### Step 2 — Access ServiceNow

**Action**

1. Open the ServiceNow instance.
2. Sign in with an authorized account.
3. Open the **All** menu or the employee self-service portal.
4. Navigate to **Self-Service → Service Catalog**, if available.
5. Locate the software request category or search for a software installation request item.

**Goal:** Access the centralized platform used to manage software requests.

**Why this matters:**

The Service Catalog provides a structured way for employees to request IT services without contacting individual technicians directly.

**Screenshot 1: ServiceNow Service Catalog**
<img width="899" height="856" alt="image" src="https://github.com/user-attachments/assets/d5288bd6-e5c1-4d28-b89d-a7a9d01b9552" />

Capture the catalog page showing the software request option.

### Step 3 — Create the Software Installation Request

**Action**

1. Select an existing **Software Installation** or equivalent request item.
2. Open the request form.
3. Enter the information below in the available fields.

**Short Description / Request Summary**

`Need Audacity installed`

**Business Justification / Description**

> The employee requires Audacity for work-related audio editing on computer Office1. Windows requests administrator credentials during installation, and the employee does not have local administrative privileges. IT assistance is required to review, approve, and install the application according to company policy.

**Goal:** Clearly explain what software is needed, why it is needed, and what is blocking installation.

**Why this matters:**

Clear documentation allows the IT team to understand the request without unnecessary back-and-forth communication.

**Screenshot 2: Software Request Form**
<img width="899" height="820" alt="image" src="https://github.com/user-attachments/assets/6ed3407f-de77-4e6a-890c-48a72585b910" />

Capture the request summary and business justification before submission.

### Step 4 — Document Employee and Device Information

**Action**

Enter the following information in the software request form where supported:

| Field               | Value           |
| ------------------- | --------------- |
| Contact Information | 435-555-1234    |
| Computer Name       | Office1         |
| Device Information  | HP Laptop/Win11 |
| Requested Software  | Audacity        |
| Category            | Software        |

If the catalog item does not provide dedicated contact or device fields, include this information in the request description or additional details field.

**Goal:** Give the IT technician enough information to identify the computer and contact the employee.

**Why this matters:**

Accurate device and contact information helps the technician prepare for the installation and reduces troubleshooting delays.
<img width="895" height="824" alt="image" src="https://github.com/user-attachments/assets/50dc57fd-b252-4f30-972c-d06c503487ad" />

### Step 5 — Submit the Software Request

**Action**

1. Review the request details.
2. Confirm the application name and business justification.
3. Verify the contact and device information.
4. Select **Submit** or **Order Now**, depending on the configured catalog.
5. Open the submitted request.
6. Record the generated request number.

**Goal:** Create an official IT service request that can be tracked.

**Expected result:**

ServiceNow records the software request and, in a standard catalog workflow, generates a Request (REQ) and a Requested Item (RITM).

**Screenshot 3: Submitted Request**

Capture the generated REQ/RITM number and request details.
<img width="905" height="549" alt="image" src="https://github.com/user-attachments/assets/55a2b09c-d741-4531-af10-53859c27a242" />

---

<img width="938" height="869" alt="image" src="https://github.com/user-attachments/assets/c73c6bb2-eec8-4cd4-9fe8-28f9511ebbd3" />


---

## Phase 2: IT Support Review and Assignment

### Step 6 — Locate the Requested Item (RITM)

**Action**

1. Open the ServiceNow application navigator.
2. Search for **Requested Items** or **My Work**, depending on the instance configuration.
3. Open the Requested Items list.
4. Locate the Audacity request using its RITM number or short description.
5. Open the record.

**Goal:** Review the submitted request from the IT Support perspective.

**Why this matters:**

A Requested Item represents the specific service or item being requested. It allows the IT team to track fulfillment separately from the overall request.

**Screenshot 4: Requested Item Details**
<img width="913" height="885" alt="image" src="https://github.com/user-attachments/assets/dc8b1641-e30f-4e33-942a-22424ec9f700" />

Capture the RITM record showing Audacity and the request information.

### Step 7 — Set Priority and Target Date

**Action**

Open the appropriate Requested Item or Catalog Task record.

Set the following values where the instance provides editable fields:

| Field            | Required Value  |
| ---------------- | --------------- |
| Priority         | High            |
| Due Date         | Tomorrow's date |
| Request Category | Software        |

For example, if performing the lab on November 22, 2026, the due date is **November 23, 2026**.

**Goal:** Establish the required priority and target date for the request.

**Why this matters:**

Priority and due dates help support teams organize work and manage expectations.

**ServiceNow note:** Not every instance exposes an editable Priority or Due Date field on a Requested Item. Some use Catalog Tasks, Flow Designer, or custom request variables to manage these values. Use the corresponding available field without changing unrelated system settings.

### Step 8 — Assign the Request to an IT Technician

**Action**

1. Open the fulfillment Catalog Task, if one is available.
2. Locate the **Assignment group** field.
3. Select the appropriate Software Support or Service Desk group, if configured.
4. Locate the **Assigned to** field.
5. Search for **Joshua Anderson**.
6. Select the technician.
7. Save the record.

**Goal:** Assign responsibility for handling the software installation request.

**Why this matters:**

Ticket assignment creates accountability by identifying who is responsible for progressing the work.

**Screenshot 5: Technician Assignment**
<img width="911" height="595" alt="image" src="https://github.com/user-attachments/assets/07815d82-6497-4155-9c33-3e5c785c329c" />

Capture the request or catalog task showing Joshua Anderson as the assignee.

### Step 9 — Verify the Request Details

**Action**

Review the submitted ServiceNow record and confirm:

| Required Information | Expected Value          |
| -------------------- | ----------------------- |
| Summary              | Need Audacity installed |
| Software             | Audacity                |
| Computer             | Office1                 |
| Device               | HP Laptop/Win11         |
| Contact              | 435-555-1234            |
| Category             | Software                |
| Priority             | High                    |
| Assigned to          | Joshua Anderson         |
| Due Date             | Tomorrow                |
| Request Record       | REQ/RITM created        |

**Goal:** Verify that the information has been recorded accurately and that the request is ready for IT processing.

**Why this matters:**

Verification prevents misrouted tickets, missing information, and unnecessary delays.

**Screenshot 6: Final Request Verification**
<img width="942" height="845" alt="image" src="https://github.com/user-attachments/assets/49e324c5-dee1-4f31-8785-3f6d2ff499f4" />

Capture the final ServiceNow record showing the request details, assignment, and current status.

---

# 6. Complete ITSM Request Lifecycle

The full software request lifecycle can be represented as follows.

| Stage              | IT Activity                             | Purpose                          |
| ------------------ | --------------------------------------- | -------------------------------- |
| 1. Request         | Employee submits Audacity request       | Document the business need       |
| 2. Record Creation | ServiceNow generates REQ/RITM           | Establish tracking               |
| 3. Review          | IT reviews the request                  | Check requirements               |
| 4. Approval        | Authorized approver reviews if required | Control software installation    |
| 5. Assignment      | Task routed to Joshua Anderson          | Establish ownership              |
| 6. Fulfillment     | Technician installs approved software   | Deliver requested service        |
| 7. Verification    | Technician confirms functionality       | Validate successful installation |
| 8. Closure         | Request/task closed with documentation  | Complete the service record      |

**Scope clarification:** Steps 1–5 represent the requested submission and routing workflow. Steps 6–8 are optional extensions and are not claimed as completed in this project.

---

# 7. Project Validation Checklist

- Accessed the ServiceNow Service Catalog.
- Located the software installation request item.
- Entered the Audacity installation summary.
- Documented the business justification.
- Recorded contact information.
- Documented the affected Windows 11 computer.
- Submitted the request successfully.
- Located the generated REQ/RITM.
- Verified the Software category.
- Configured or documented the required High priority.
- Set or documented the required due date.
- Assigned or routed the fulfillment task to Joshua Anderson.
- Verified the final request information.
- Captured relevant screenshots.

---

# 8. Business Value

### Security and Compliance

Administrative permissions help protect corporate computers from unauthorized software installations.

Using ServiceNow allows IT teams to manage the request without requiring employees to bypass security controls.

### Operational Efficiency

Centralized request documentation makes it easier for technicians to understand employee needs and determine the next action.

### Accountability

Ticket assignment identifies who is responsible for progressing the request.

### Visibility and Traceability

REQ and RITM records provide a way to track requests and review their status throughout the service management process.

---

# 9. Technical Skills Demonstrated

| Skill                | Application                                  |
| -------------------- | -------------------------------------------- |
| ServiceNow ITSM      | Managing employee IT requests                |
| Service Catalog      | Submitting software installation requests    |
| Request Management   | Tracking REQ and RITM records                |
| Ticket Documentation | Recording business and device details        |
| Task Assignment      | Routing work to an IT technician             |
| Windows Security     | Respecting administrator restrictions        |
| IT Service Delivery  | Following structured support processes       |
| Quality Assurance    | Reviewing and validating request information |

---

# 10. Key Takeaways

A software installation request may appear simple, but it involves several important IT support responsibilities.

**The employee needs software.**

**Windows requires administrative permission.**

**ServiceNow connects the employee's request with the authorized IT support process.**

Through this project, I demonstrate how to document an IT request, track it in ServiceNow, verify the necessary information, and route it for technician review.

---

# 11. Project Outcome

**Expected outcome:** A documented ServiceNow software installation request for Audacity, including the employee's business justification, device information, requested priority, target date, and technician assignment.

This project demonstrates practical IT Service Management skills involving ServiceNow request handling, technical documentation, access control awareness, and IT support coordination.

**Professional takeaway:** Reliable IT support is not only about installing software. It is about delivering services through a secure, documented, and accountable process.

---

**Technology:** ServiceNow | Windows 11 | ITSM

**Project Type:** IT Service Request Management

**Author:** Liliane Konissi


**Important ServiceNow distinction:** An Incident is generally used to restore a disrupted service. A Service Catalog Request is appropriate for obtaining software. Also, assignment, priority, and due-date fields depend on the instance configuration; they might belong to the RITM or a Catalog Task.&#x20;


