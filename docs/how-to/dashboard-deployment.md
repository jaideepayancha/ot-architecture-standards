# How-To: Standard Dashboard Deployment Process

To ensure high availability and prevent production downtime, all Ignition Perspective dashboards must follow the standard Dev -> Staging -> Prod lifecycle.

## 1. Development Environment (Site-Level)

- **Purpose**: Feature development, UI prototyping, and initial tag binding.
- **Rules**: Developers work on local "Dev" gateways or workstation designers.
- **Check**: Use the `Naming Conventions` document for all component and view names.

## 2. Staging / QA Environment (Site or Enterprise)

- **Purpose**: Verification against live data and user acceptance testing (UAT).
- **Process**:
    1. Export project/views from Dev.
    2. Import into Staging Gateway.
    3. Verify data bindings, security permissions, and responsive layout performance.
- **Approval**: Operations lead must sign off on the dashboard functionality.

## 3. Production Deployment

- **Process**:
    1. Use the **Ignition Enterprise Administration Module (EAM)** to push resources to production gateways.
    2. Alternatively, perform a manual import during a scheduled maintenance window.
- **Monitoring**: After deployment, monitor gateway logs for script errors or high tag-change rates.

## Version Control with Git

All Ignition projects should be backed up using the external project-sync feature to a Git repository.
- **Commit Messages**: Reference the Change Management ticket number.
- **Branching**: Use `feature/` branches and merge into `main` after UAT approval.
