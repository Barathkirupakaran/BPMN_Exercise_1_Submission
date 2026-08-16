BPMN Exercise 1 – Business Process Modeling
Overview

This repository contains the BPMN 2.0 process models developed for Exercise 1. The models demonstrate how business processes can be represented using basic BPMN building blocks such as Start Events, Tasks, Exclusive Gateways, End Events, and Sequence Flows.

The exercise includes three different business scenarios:

Employee Leave Approval
Online Purchase Order Processing
IT Service Request
Scenario 1: Employee Leave Approval
Description

This BPMN process represents how an employee's leave request is handled through an HR system.

The process begins when the employee submits a leave request. The HR system checks the employee's available leave balance. An Exclusive Gateway determines whether sufficient leave balance is available.

If the leave balance is insufficient, the system sends an insufficient-balance notification and the process ends.
If sufficient leave is available, the request is sent to the manager for approval.
If the manager approves the request, the system updates the employee's leave balance and sends an approval notification.
If the manager rejects the request, the system sends a rejection notification.
BPMN Elements Used
Start Event
Tasks
Exclusive Gateways
End Events
Sequence Flows
Process Flow

Start → Submit Leave Request → Check Leave Balance → Balance Available?

No → Send Insufficient-Balance Notification → End

Yes → Send Request to Manager → Manager Approves?

Yes → Update Leave Balance → Send Approval Notification → End

No → Send Rejection Notification → End

Scenario 2: Online Purchase Order Processing
Description

This BPMN process represents the processing of an online purchase order.

The process starts when a customer places an order. The system checks the availability of the requested product. An Exclusive Gateway determines whether the product is available.

If the product is unavailable, the customer is notified that the product is out of stock and the process ends.
If the product is available, the system processes the payment.
A second Exclusive Gateway checks whether the payment is successful.
If the payment fails, the customer receives a payment failure notification and the process ends.
If the payment succeeds, the system confirms the order, prepares the product for shipment, ships the order, and sends a shipping confirmation to the customer.
BPMN Elements Used
Start Event
Tasks
Exclusive Gateways
Multiple Process Paths
End Events
Sequence Flows
Process Flow

Start → Customer Places Order → Check Product Availability → Product Available?

No → Notify Customer: Product Out of Stock → End

Yes → Process Payment → Payment Successful?

No → Notify Customer: Payment Failure → End

Yes → Confirm Order → Prepare Product for Shipment → Ship Order → Shipping Confirmation → End

Scenario 3: IT Service Request
Description

This BPMN process represents how an employee's IT support request is handled.

The process begins when an employee submits an IT support request. The help desk registers the request and checks the severity of the problem. An Exclusive Gateway determines whether the problem has low or high severity.

A low-severity problem is assigned to a support technician.
A high-severity problem is assigned to a senior technician.
Both paths lead to the investigation of the problem.
After investigation, another Exclusive Gateway determines whether the problem can be resolved internally.
If it can be resolved internally, the technician fixes the problem.
If it cannot be resolved internally, the problem is escalated to an external service provider.
After resolution, the help desk updates the request status and sends a resolution notification to the employee.
The process then ends.
BPMN Elements Used
Start Event
Multiple Tasks
Exclusive Gateway
Alternative Process Paths
End Event
Sequence Flows
Process Flow

Start → Submit IT Support Request → Register Request → Check Problem Severity → Problem Severity?

Low → Assign to Support Technician

High → Assign to Senior Technician

Both Paths → Investigate Problem → Can Problem Be Resolved Internally?

Yes → Fix Problem

No → Escalate to External Service Provider

Both Paths → Update Request Status → Send Resolution Notification → End

BPMN Building Blocks Used

The three scenarios use the following basic BPMN elements:

BPMN Element	Purpose
Start Event	Indicates where the process begins
Task	Represents an activity performed during the process
Exclusive Gateway	Represents a decision where only one path is selected
Sequence Flow	Connects BPMN elements and shows the direction of the process
End Event	Indicates where a process path terminates
Repository Contents
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
Conclusion

These BPMN models demonstrate the use of fundamental BPMN 2.0 building blocks to represent different real-world business processes. Each model includes process activities, decision points, alternative paths, and appropriate start and end events.
