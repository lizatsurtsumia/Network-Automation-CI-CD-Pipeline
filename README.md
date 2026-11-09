# NetDevOps – Network Automation CI/CD Pipeline

## Project Overview

This project demonstrates the implementation of a Network DevOps (NetDevOps) workflow using automation, version control, and Continuous Integration/Continuous Deployment (CI/CD).

The goal is to automate network configuration management, reduce manual CLI operations, improve configuration consistency, and introduce automated network validation.

The lab simulates an enterprise network environment where network configurations are managed through GitHub and deployed to Cisco network devices using Ansible and GitHub Actions.

## Objectives

- Automate Cisco network device configurations.
- Implement Infrastructure as Code (IaC) principles.
- Manage network configurations using Git and GitHub.
- Build automated CI/CD pipelines with GitHub Actions.
- Deploy configurations using Ansible.
- Perform pre-change and post-change network validation.
- Maintain configuration backups.
- Integrate NetBox as a centralized Network Source of Truth.

## Technology Stack

| Technology | Purpose |
|---|---|
| Linux Ubuntu | Automation server |
| Python | Network automation and validation |
| Ansible | Configuration management |
| Git | Version control |
| GitHub | Repository and collaboration |
| GitHub Actions | CI/CD automation |
| Cisco IOS | Network infrastructure |
| SSH | Secure device connectivity |
| NetBox | Network Source of Truth |

## Lab Architecture

The environment consists of an Ubuntu automation server connected to three Cisco IOS routers through a virtual network lab.

**Components:**

- Ubuntu Server – Ansible control node and automation environment.
- R1 – Cisco IOS router.
- R2 – Cisco IOS router.
- R3 – Cisco IOS router.
- GitHub – Central repository for network configurations and automation code.
- GitHub Actions – CI/CD execution environment.

## Project Workflow

The automation pipeline follows these stages:

1. **Configuration Development:** Network configurations and Ansible playbooks are maintained in GitHub.
2. **Version Control:** Changes are committed and pushed to the repository.
3. **CI Pipeline:** GitHub Actions automatically triggers workflow execution.
4. **Pre-Deployment Validation:** Configuration syntax and automation playbooks are checked.
5. **Configuration Deployment:** Ansible connects to Cisco devices through SSH and applies the intended configurations.
6. **Post-Deployment Validation:** Automated scripts verify device status, routing protocols, and network connectivity.
7. **Reporting:** Validation results are collected to identify successful deployments or configuration failures.

## Implementation Roadmap

### Phase 1 – Lab Infrastructure
- Deploy Cisco IOS routers.
- Install and configure Ubuntu automation server.
- Configure management connectivity.
- Enable SSH access.

### Phase 2 – Ansible Configuration
- Install Ansible.
- Configure device inventory.
- Establish SSH connectivity.
- Execute remote commands.
- Collect device information.

### Phase 3 – Network Automation
- Automate interface configuration.
- Deploy OSPF configurations.
- Automate routing configuration.
- Implement configuration backups.

### Phase 4 – Git Integration
- Initialize Git repository.
- Store network configurations.
- Track configuration changes.
- Maintain version history.

### Phase 5 – CI/CD Pipeline
- Implement GitHub Actions workflows.
- Trigger automation after Git pushes.
- Perform syntax and configuration checks.
- Execute Ansible deployment playbooks.

### Phase 6 – Network Validation
- Verify interface status.
- Check OSPF neighbor relationships.
- Validate routing tables.
- Perform end-to-end connectivity tests.
- Generate deployment validation reports.

### Phase 7 – NetBox Integration
- Deploy NetBox.
- Register network devices and IP addresses.
- Maintain centralized network inventory.
- Integrate NetBox with Ansible.

## Security Considerations

- Use SSH for secure device management.
- Store sensitive credentials using GitHub Secrets.
- Avoid committing passwords, private keys, or API tokens.
- Use dedicated automation accounts.
- Validate configuration changes before deployment.

## Learning Outcomes

This project provides practical experience with:

- Network Automation and Programmability.
- Infrastructure as Code (IaC).
- Ansible Network Automation.
- Python-based network validation.
- Git and GitHub workflows.
- CI/CD pipeline development.
- Linux administration.
- Enterprise network configuration management.
- Network monitoring and troubleshooting.

**Disclaimer:** This project is developed in a virtual lab environment for educational and professional portfolio purposes. No production network infrastructure is used.
