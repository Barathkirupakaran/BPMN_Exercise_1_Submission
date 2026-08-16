# 🔷 BPMN Exercise 1 – Business Process Modeling

> **BPMN 2.0 Process Modeling using Basic BPMN Building Blocks**

This repository contains the BPMN 2.0 models created for **Exercise 1**. The objective is to represent real-world business processes using fundamental BPMN elements such as **Start Events, Tasks, Exclusive Gateways, Sequence Flows, and End Events**.

---

## 📌 Scenarios Covered

| No. | Scenario                            | Description                                                                                    |
| --- | ----------------------------------- | ---------------------------------------------------------------------------------------------- |
| 01  | 👨‍💼 Employee Leave Approval       | Process for submitting, reviewing, approving, or rejecting employee leave requests             |
| 02  | 🛒 Online Purchase Order Processing | Process for checking product availability, processing payment, and completing an online order  |
| 03  | 🖥️ IT Service Request              | Process for handling IT support requests based on problem severity and resolution requirements |

---

# 01. 👨‍💼 Employee Leave Approval

### 📖 Description

The process begins when an employee submits a leave request. The system checks the employee's available leave balance before forwarding the request to the manager.

An **Exclusive Gateway** is used to determine whether sufficient leave balance is available. If there is insufficient balance, the employee receives a notification and the process ends.

When sufficient leave is available, the request is sent to the manager for approval. The manager's decision determines whether the leave balance is updated and an approval notification is sent, or a rejection notification is provided.

### 🧩 BPMN Elements Used

* **Start Event** – Begins the leave approval process
* **Tasks** – Represent leave submission, balance checking, manager processing, balance updating, and notifications
* **Exclusive Gateways** – Represent leave balance availability and manager approval decisions
* **Sequence Flows** – Connect the activities and decision paths
* **End Events** – Represent the completion of each outcome

---

# 02. 🛒 Online Purchase Order Processing

### 📖 Description

The process begins when a customer places an online order. The system checks whether the requested product is available.

An **Exclusive Gateway** determines whether the product can be purchased. If the product is unavailable, the customer is notified and the process ends.

When the product is available, payment is processed. A second **Exclusive Gateway** determines whether the payment is successful. A failed payment results in a notification to the customer, while a successful payment allows the order to proceed through confirmation, product preparation, shipping, and shipping confirmation.

### 🧩 BPMN Elements Used

* **Start Event** – Begins the order processing
* **Tasks** – Represent ordering, availability checking, payment, confirmation, preparation, shipping, and notifications
* **Exclusive Gateways** – Represent product availability and payment success decisions
* **Sequence Flows** – Connect the different process activities and alternative paths
* **End Events** – Represent successful completion or unsuccessful outcomes

---

# 03. 🖥️ IT Service Request

### 📖 Description

The process begins when an employee submits an IT support request. The help desk registers the request and checks the severity of the reported problem.

An **Exclusive Gateway** determines whether the problem has low or high severity. Low-severity problems are assigned to a support technician, while high-severity problems are assigned to a senior technician.

After investigation, another **Exclusive Gateway** determines whether the problem can be resolved internally. If it can, the technician fixes the problem. Otherwise, the issue is escalated to an external service provider.

Once the issue is handled, the request status is updated and a resolution notification is sent to the employee.

### 🧩 BPMN Elements Used

* **Start Event** – Begins the IT support process
* **Tasks** – Represent request submission, registration, assignment, investigation, resolution, escalation, and notification activities
* **Exclusive Gateways** – Represent severity and internal-resolution decisions
* **Sequence Flows** – Connect activities and alternative paths
* **End Event** – Indicates completion of the support request

---

# 🧱 BPMN Building Blocks

| BPMN Element          | Purpose                                                |
| --------------------- | ------------------------------------------------------ |
| **Start Event**       | Indicates where the process begins                     |
| **Task**              | Represents an activity or action                       |
| **Exclusive Gateway** | Represents a decision where one path is selected       |
| **Sequence Flow**     | Connects BPMN elements and indicates process direction |
| **End Event**         | Indicates where a process path ends                    |

> **Note:** Only the BPMN elements required for the scenarios are used. The models focus on basic tasks, events, exclusive decisions, and sequence flows.

---

# 📂 Repository Structure

```text
BPMN-Exercise-1/
│
├── Scenario-1/
│   └── Employee_Leave_Approval.bpmn
│
├── Scenario-2/
│   └── Online_Purchase_Order_Processing.bpmn
│
├── Scenario-3/
│   └── IT_Service_Request.bpmn
│
├── BPMN_Exercise_1.pdf
└── README.md
```

---

# 🎯 Learning Outcome

This exercise demonstrates how **BPMN 2.0** can be used to model and visualize business processes. The three scenarios show the practical use of **tasks, start and end events, exclusive gateways, and sequence flows** to represent different workflows and decision-based process paths.

---

## 📚 Exercise Details

**Exercise:** BPMN Exercise 1
**Standard:** BPMN 2.0
**Focus:** Business Process Modeling
**Core Elements:** Start Events, Tasks, Exclusive Gateways, Sequence Flows, and End Events
