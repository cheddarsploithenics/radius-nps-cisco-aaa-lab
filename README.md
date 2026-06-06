Cisco AAA Authentication with Windows NPS (RADIUS)
Project Overview

Designed and implemented centralized network device authentication using Microsoft Network Policy Server (NPS) integrated with Active Directory.

The solution provides role-based administrative access to Cisco network devices through RADIUS authentication and authorization.

Technologies Used
Windows Server 2022
Active Directory
Network Policy Server (NPS)
Cisco IOS
RADIUS
PowerShell
TFTP
Objectives
Centralize switch authentication
Eliminate local-only administrative accounts
Implement role-based access controls
Assign privilege levels based on AD group membership
Back up network configurations using TFTP

Architecture

(Diagram)

AD Users
↓
AD Groups
↓
NPS Policies
↓
Cisco AAA
↓
Privilege Levels

Access Control Model
AD Group	                    Cisco Privilege
Network Engineers	            15
Network Technicians	          1

Cisco Configuration
aaa new-model
aaa authentication login default group radius local
aaa authorization exec default group radius if-authenticated

Results
Successful RADIUS authentication
AD group-based authorization
Dynamic privilege assignment
Centralized administration
Successful configuration backup and restore testing
