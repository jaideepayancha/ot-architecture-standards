# How-To: Add a New Plant to the OT Infrastructure

This guide outlines the standard onboarding process for integrating a new facility into our enterprise OT network.

## Phase 1: Planning & Network Setup

1. **VLAN Request**: Submit a request for the standard OT VLAN structure:
    - `VLAN 10`: Process/Control (L1-L2)
    - `VLAN 20`: Operations (L3)
    - `VLAN 30`: Security/Mgmt
2. **IP Allocation**: Assign a reserved CIDR block from the enterprise OT IP plan.
3. **Firewall Rules**: Configure the industrial firewall to allow traffic between the new site and the Enterprise DMZ (MQTTS, RDP).

## Phase 2: Infrastructure Deployment

1. **Server Provisioning**: Deploy standardized VM templates for:
    - Primary/Backup Ignition Gateways
    - Local SQL Historian
    - Asset Management Node
2. **OS Hardening**: Apply enterprise OT GPOs and install approved security agents (Antivirus, Patch Mgmt).
3. **Active Directory**: Join servers to the local OT Domain.

## Phase 3: Ignition & SCADA Setup

1. **Installation**: Install Ignition (LTS version) with the required modules.
2. **Gateway Configuration**:
    - Configure Redundancy.
    - Setup Database and Historian connections.
    - Configure MQTT Engine and Transmission with enterprise broker credentials.
3. **Project Import**: Import the standard Enterprise Template and Project structure.

## Phase 4: Verification

1. **Data Flow Check**: Verify tags are publishing to the enterprise MQTT broker.
2. **Remote Access Check**: Test RDP access via the Jump Host.
3. **Security Scan**: Perform an initial vulnerability scan and remediate high-risk findings.
