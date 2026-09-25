# Automated Network Request Management

A ServiceNow-based application that automates network access and configuration requests through catalog-driven request submission, dynamic form behavior, approval workflows, and network team task assignment.

## Project Overview

The Automated Network Request Management system streamlines the process of submitting and processing network-related requests in ServiceNow.

Users can submit requests for:

- Network Access
- Router/Switch Configuration
- VPN Access
- Firewall Changes
- IP or Port Requests

The system dynamically displays the required fields based on the selected request type.

## Key Features

- Service Catalog-based Network Request
- Dynamic field visibility using Catalog UI Policies
- Network Team approval workflow
- Approval and rejection handling
- Automatic Catalog Task creation for approved requests
- Network Team assignment
- Request status/stage updates
- Email notification for rejected requests
- Automated completion handling

## Request Flow

User submits Network Request
        ↓
Request sent for Network Team approval
        ↓
   ┌───────────────┐
   │               │
Approved        Rejected
   │               │
   ↓               ↓
Create Task    Cancel Request
   │               │
   ↓               ↓
Network Team    Email User
works on task
   │
   ↓
Task completed
   │
   ↓
Request marked Completed

## Technologies

- ServiceNow
- Service Catalog
- Flow Designer / Workflow Studio
- Catalog UI Policies
- Catalog Variables
- Update Sets
- GitHub

## Catalog Variables

The Network Request catalog item contains:

1. Requested For
2. Request Type
3. Access Level
4. Priority
5. Device Name
6. Business Justification
7. Required By
8. Source IP
9. Destination IP
10. Port Number
11. Protocol
12. VPN Duration

## Request Types

| Request Type | Relevant Fields |
|---|---|
| Network Access | Access Level |
| Router/Switch Configuration | Device Name, Business Justification |
| VPN Access | Access Level, VPN Duration |
| Firewall Change | Source IP, Destination IP, Port Number, Protocol |
| IP or Port Request | Device Name, Source IP, Destination IP, Port Number, Protocol |

## Workflow

The Network Request Approval Flow uses:

- Service Catalog trigger
- Ask For Approval on Requested Item
- Network Team approval
- Approved/rejected branching
- Catalog Task creation
- Network Team assignment
- Request completion
- Rejection email notification

## Repository Contents

The repository contains the exported ServiceNow Update Set XML containing the project configuration.

## Author

**Sruthi B**

B.Tech – Artificial Intelligence & Machine Learning  
Bannari Amman Institute of Technology
