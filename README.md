<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket Post Installation Setup

## Overview
This repository provides a structured approach to setting up osTicket on a Windows 10 Virtual Machine hosted in Microsoft Azure.

## Prerequisites
Ensure the following are available before installation:
- Azure Virtual Machine (Windows 10, 4 vCPUs)
- Remote Desktop Access
- Internet Information Services (IIS) with CGI enabled
- PHP 7.3.8, MySQL 5.5.62, and required modules
- osTicket v1.15.8 installation files

## Installation Steps

### Post-Installation Configuration
After installing osTicket, perform the following configurations:

1. **Admin/Analyst Login Page:**
   - [Admin Panel](http://localhost/osTicket/scp/login.php)
   - [End Users Portal](http://localhost/osTicket)

2. **Agent and User Management:**
   - **Configure Roles:**
     - Admin Panel → Agents → Roles → Create and assign roles (e.g., Supreme Admin)
   - **Configure Departments:**
     - Admin Panel → Agents → Departments (e.g., SysAdmins, Help Desk, Networking)
   - **Configure Teams:**
     - Admin Panel → Agents → Teams (e.g., Online Banking)
   - **Allow Ticket Creation:**
     - Admin Panel → Settings → User Settings (Uncheck: unregistered users can create tickets)
   - **Require Registration:**
     - Ensure only registered users can create tickets

3. **Configure Agents and Users:**
   - **Agents:**
     - Admin Panel → Agents → Add New
     - Example: Jane (SysAdmins), John (Support)
   - **Users:**
     - Agent Panel → Users → Add New
     - Example: Karen, Ken

4. **Service Level Agreement (SLA) Configuration:**
   - Admin Panel → Manage → SLA
     - **Sev-A:** 1-hour grace period, 24/7 schedule
     - **Sev-B:** 4-hour grace period, 24/7 schedule
     - **Sev-C:** 8-hour grace period, business hours
