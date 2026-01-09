# Apogee Azure Deployment

Containerized deployment of Apogee data processing pipeline to Azure with documentation, roles, permissions, and demo.

## Quick Links

- [Full Project Details](apogee-azure-deployment.md)

## Project Status

**Start Date**: 2025-01-09
**Status**: Active - Week 1 Development & Documentation
**Priority**: High

## Critical Deadlines

- **Friday 1/10 5pm**: Demo slot with team
- **Friday 1/17** (ideal) / **Monday 1/20** (latest): Return 1/16 processed data to Katie
- **Thursday 1/23** (ideal) / **Sunday 1/26** (latest): Return 1/22 processed data to Kate
- **Thursday 1/23**: Update project timelines

## Key Deliverables

1. ✅ E2E validation with 1/8 data (share with Katie by Sunday EOP)
2. 🔄 Containerized deployment (no Terraform - use bash/PowerShell script)
3. 🔄 Documentation: Roles & permissions
4. 🔄 Documentation: Pipeline definition
5. 🔄 Demo walkthrough
6. ⏳ Process 1/16 data batch
7. ⏳ Process 1/22 data batch
8. ⏳ Update timelines by 1/23

## This Week Focus (1/6-1/10)

**Mon-Wed:** Build deployment script, run E2E tests, create documentation
**Thu:** Finalize demo preparation
**Fri 5pm:** Present demo to team

## Key Technical Decisions (from 1/9 meeting)

- **No Terraform**: Mike prefers bash/PowerShell script approach
- **Three Role Types**: App service principal, WNA users, Admins
- **Documentation Required**: Pipeline definition, roles/permissions, timelines

## Immediate Next Steps

1. Run E2E script with 1/8 data
2. Validate against old data (ensure same results)
3. Build deployment script (replace Terraform)
4. Document roles and permissions
5. Create demo environment
6. Present Friday 5pm
