# BPMN Process Models

## Overview

This repository contains three BPMN process models created using Camunda 8 Modeler. The models demonstrate the use of basic BPMN building blocks such as Start Events, Tasks, Exclusive Gateways, Sequence Flows, and End Events.

## Scenario 1 – Employee Leave Approval

### Process Description

The process begins when an employee submits a leave request. The HR system checks the employee's available leave balance.

If sufficient leave balance is available, the request is sent to the manager for approval. If the manager approves the request, the system updates the employee's leave balance and sends an approval notification. If the manager rejects the request, a rejection notification is sent.

If insufficient leave balance is available, the system sends an insufficient-balance notification and the process ends.

### BPMN Elements Used

- Start Event
- Tasks
- Exclusive Gateways
- Sequence Flows
- End Events

### Process Paths

- Sufficient balance → Manager approval → Approved → Update balance → Approval notification
- Sufficient balance → Manager approval → Rejected → Rejection notification
- Insufficient balance → Insufficient-balance notification

## Scenario 2 – Online Purchase Order Processing

### Process Description

The process starts when a customer places an order. The system checks product availability.

If the product is unavailable, the customer receives an out-of-stock notification and the process ends.

If the product is available, payment is processed. If payment fails, the customer receives a payment-failure notification and the process ends.

If payment is successful, the order is confirmed, the product is prepared, shipped, and a shipping confirmation is sent to the customer.

### BPMN Elements Used

- Start Event
- Tasks
- Exclusive Gateways
- Sequence Flows
- End Events

### Process Paths

- Product unavailable → Out-of-stock notification → End
- Product available → Payment failure → Payment-failure notification → End
- Product available → Successful payment → Confirm order → Prepare product → Ship order → Shipping confirmation → End

## Scenario 3 – IT Service Request

### Process Description

The process begins when an employee submits an IT support request. The help desk registers the request and checks the severity of the problem.

For low-severity problems, the request is assigned to a support technician. For high-severity problems, it is assigned to a senior technician.

The technician investigates the problem. If it can be resolved internally, the technician fixes it. Otherwise, the problem is escalated to an external service provider.

After the problem is resolved, the help desk updates the request status and sends a resolution notification to the employee.

### BPMN Elements Used

- Start Event
- Tasks
- Exclusive Gateways
- Sequence Flows
- End Event

### Process Paths

- Low severity → Support technician → Investigation
- High severity → Senior technician → Investigation
- Problem resolved → Fix problem → Update status → Resolution notification
- Problem cannot be resolved internally → External service provider → Update status → Resolution notification

## Tool Used

**Camunda 8 Modeler**

## Conclusion

The three BPMN models demonstrate the modelling of sequential activities, decision points, alternative process paths, and process termination using basic BPMN 2.0 elements.
