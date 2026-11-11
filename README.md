# Ansible Start/Stop Lab

## Purpose

This repository is a clean-room learning and prototyping project for dependency-aware service Start/Stop automation using Ansible and Ansible Automation Platform.

The lab uses synthetic configuration and generic open-source technologies.

No BAY, Krungsri, Kyndryl proprietary source code, customer inventory, credentials, internal scripts, or internal configuration should be stored in this repository.

## Target workflow

Validate
→ Pre-check
→ Stop
→ Verify
→ Maintenance Gate
→ Start
→ Verify
→ Health Check
→ Evidence

## Synthetic dependency model

### Stop

APP → Middleware → Database

### Start

Database → Middleware → APP

## Initial technologies

- Linux
- systemd
- AWS EC2
- Ansible Automation Platform
- SSH

## Safety defaults

Service Start and Stop operations are disabled by default.

The initial supported operation is:

`validate_only`

Actual change operations must be explicitly enabled after connectivity and pre-check testing have succeeded.

## Development roadmap

1. Validate project inputs
2. Connect AAP to Git repository
3. Create AWS development inventory
4. Validate SSH connectivity
5. Run pre-check
6. Test one harmless systemd service
7. Add APP/MDW/DB dependency orchestration
8. Add health checks
9. Add evidence collection
10. Build AAP Workflow Template
