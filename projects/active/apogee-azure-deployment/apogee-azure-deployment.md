# Apogee Azure Deployment Project

**Status**: Active
**Start Date**: 2025-01-09
**Priority**: High
**Project Type**: Cloud infrastructure deployment, data pipeline

## Project Overview

Deploy containerized Apogee data pipeline to Azure with proper documentation, roles, permissions, and demo. Complete E2E testing with 1/8 data batch and prepare for production data processing starting with 1/22 batch.

## Critical Deadlines

- **Friday 1/10 5pm**: Slot for demo/review with team
- **Thursday 1/16**: Katie sends new data
- **Friday 1/17** (ideally): Complete data processing and return to Katie
- **Monday 1/20** (latest): Return processed data to Katie (start of business)
- **1/22**: Next Apogee data dump
- **1/23** (ideally): Process 1/22 data and return to Kate
- **1/26** (latest): Return 1/22 processed data to Kate
- **1/23**: Update project timelines
- **Two weeks from 1/9**: Beck gets update (week of 1/20)

## 1/9 Meeting Notes Summary

**Key Decisions:**
- Mike prefers NOT using Terraform; think about alternatives (multisoft or bash script)
- Need to provide specific roles and access requirements for pipeline
- Need documentation and demo walkthrough
- Beck will get update away for two weeks (returns ~1/20)

**Data Processing Timeline:**
- Katie will send new data Thursday 1/16
- Turn around by start of business Monday 1/20 (ideally by Friday 1/17)
- Run the 1/8 batch as validation
- Next batch will be 1/22 (turn around by 1/23 ideally, 1/26 latest)

**Deliverables Requested:**
- Pipeline definition
- Roles and permissions documentation
- Update on timelines
- Demo walkthrough
- Documentation for setup

**Roles Needed:**
- Role for the app itself
- Role for WNA any users
- Role for admins

## Weekend Work Tasks (From Notes)

### Phase 1: E2E Data Processing & Validation
- [ ] **Run 1/8 data using E2E local script**
  - [ ] Get it running successfully
  - [ ] Also run old data to validate
  - [ ] Make sure results are the same (old vs new)
  - [ ] Share results with Katie by Sunday EOP

### Phase 2: Containerized Deployment
- [ ] **Complete containerized deployment**
  - [ ] Test deployment thoroughly
  - [ ] Use script in place of Terraform (per Mike's preference)
  - [ ] Clean up code
  - [ ] Ensure deployment is repeatable

### Phase 3: Documentation
- [ ] **Write up documentation for containerized deployment**
  - [ ] Roles and permissions required
  - [ ] Pipeline definition
  - [ ] Setup instructions
  - [ ] Deployment steps
  - [ ] Troubleshooting guide

### Phase 4: Demo & Presentation
- [ ] **Create demo if possible**
  - [ ] Prepare demo environment
  - [ ] Create walkthrough script
  - [ ] Test demo flow

### Phase 5: Team Sharing
- [ ] **Share with Apogee team early next week**
  - [ ] Schedule meeting/demo
  - [ ] Present documentation
  - [ ] Walk through deployment
  - [ ] Discuss roles and permissions

### Phase 6: Timeline & Planning
- [ ] **Update timelines by 1/23**
  - [ ] Account for 1/22 data dump
  - [ ] Plan for regular data processing cadence
  - [ ] Document expectations and SLAs

## Detailed Task Breakdown

### Task 1: E2E Local Script Testing
**Priority**: IMMEDIATE
**Deadline**: Share with Katie by Sunday EOP

**Steps:**
1. [ ] Set up E2E local script environment
2. [ ] Run 1/8 data batch through pipeline
3. [ ] Run old/previous data batch through pipeline
4. [ ] Compare results between 1/8 and old data
5. [ ] Validate that results are identical
6. [ ] Document any discrepancies
7. [ ] Share results with Katie by Sunday evening

**Success Criteria:**
- Script runs successfully on 1/8 data
- Old data produces same results as before
- Results are validated and documented
- Katie receives update by Sunday EOP

---

### Task 2: Containerized Deployment
**Priority**: HIGH
**Deadline**: Complete by Friday 1/10 for demo

**Steps:**
1. [ ] Review current containerized deployment approach
2. [ ] Replace Terraform with script-based deployment (bash or PowerShell)
3. [ ] Test deployment script end-to-end
4. [ ] Clean up code and remove unused/deprecated components
5. [ ] Ensure all configuration is parameterized
6. [ ] Test deployment in clean Azure environment
7. [ ] Validate pipeline runs after deployment
8. [ ] Document deployment script usage

**Terraform Replacement Options:**
- Bash script with Azure CLI commands
- PowerShell script with Az modules
- Python script with Azure SDK
- Combination approach (Mike's "multisoft" comment)

**Success Criteria:**
- Deployment script works without Terraform
- Clean, maintainable code
- Tested in fresh environment
- All resources properly configured

---

### Task 3: Documentation - Roles & Permissions
**Priority**: HIGH
**Deadline**: Complete by Friday 1/10 for demo

**Required Documentation:**

**Role 1: Pipeline Application Service Principal**
- Purpose: Run the pipeline itself
- Required permissions:
  - Azure Data Factory (or equivalent) execution rights
  - Storage account read/write access
  - Key Vault access for secrets
  - Resource group contributor (limited scope)
- Creation steps
- Assignment instructions

**Role 2: WNA End Users**
- Purpose: Users who need to access processed data
- Required permissions:
  - Storage account read access
  - Dashboard/reporting access (if applicable)
  - Data Lake read access
- Creation steps
- Assignment instructions

**Role 3: Administrators**
- Purpose: Team members who manage the pipeline
- Required permissions:
  - Full pipeline management access
  - Resource group contributor/owner
  - Ability to modify configurations
  - Troubleshooting and monitoring access
- Creation steps
- Assignment instructions

**Document Format:**
- Clear role definitions
- Step-by-step permission assignments
- Azure CLI commands for role creation
- PowerShell alternatives
- Principle of least privilege applied

---

### Task 4: Documentation - Pipeline Definition
**Priority**: HIGH
**Deadline**: Complete by Friday 1/10 for demo

**Pipeline Documentation Must Include:**

**Architecture Overview:**
- High-level architecture diagram
- Component descriptions
- Data flow diagram
- Azure resources used

**Pipeline Stages:**
1. Data Ingestion
   - Source: Where data comes from
   - Format: Expected data format
   - Validation: Initial data checks

2. Data Processing
   - Transformation steps
   - Business logic applied
   - Error handling

3. Data Output
   - Output format
   - Destination storage
   - Notification/completion triggers

**Configuration:**
- Environment variables
- Configuration files
- Secrets management (Key Vault)
- Parameter customization

**Monitoring & Logging:**
- Log locations
- Monitoring dashboards
- Alert configurations
- Troubleshooting logs

**Deployment:**
- Prerequisites
- Deployment steps
- Verification steps
- Rollback procedures

---

### Task 5: Create Demo
**Priority**: MEDIUM
**Deadline**: Ready by Friday 1/10 5pm

**Demo Components:**
1. [ ] Environment Setup
   - Clean Azure subscription or resource group
   - Demo data prepared
   - All scripts ready

2. [ ] Demo Script/Walkthrough
   - Introduction (2 min)
   - Architecture overview (3 min)
   - Deployment demonstration (5-7 min)
   - Pipeline execution (5 min)
   - Results review (3 min)
   - Q&A (flexible)

3. [ ] Demo Materials
   - Slide deck (optional, or just live demo)
   - Code walkthrough
   - Documentation references
   - Roles & permissions explanation

4. [ ] Backup Plan
   - Pre-recorded demo if live fails
   - Screenshots of successful run
   - Documentation as fallback

**Demo Flow:**
1. Show current state (no resources)
2. Run deployment script
3. Show resources created
4. Explain roles and permissions
5. Trigger pipeline with sample data
6. Show processing in action
7. Review output/results
8. Discuss next steps

---

### Task 6: Data Processing - 1/16 Batch
**Priority**: HIGH
**Deadline**: Friday 1/17 (ideally), Monday 1/20 latest

**Timeline:**
- Thursday 1/16: Receive data from Katie
- Friday 1/17: Process and return (ideal)
- Monday 1/20 AM: Return data (latest acceptable)

**Steps:**
1. [ ] Monitor for data arrival Thursday 1/16
2. [ ] Validate data received (format, completeness)
3. [ ] Run through E2E pipeline
4. [ ] Validate output
5. [ ] Return to Katie with summary
6. [ ] Document processing time and any issues

---

### Task 7: Data Processing - 1/22 Batch
**Priority**: HIGH
**Deadline**: Thursday 1/23 (ideally), Sunday 1/26 latest

**Timeline:**
- Wednesday 1/22: Data dump occurs
- Thursday 1/23: Process and return (ideal)
- Sunday 1/26: Return data (latest acceptable)

**Steps:**
1. [ ] Receive 1/22 data dump
2. [ ] Process through production pipeline
3. [ ] Validate output quality
4. [ ] Return to Kate by 1/23 (ideal) or 1/26 (latest)
5. [ ] Document processing time
6. [ ] Note any improvements or issues

---

### Task 8: Update Timelines
**Priority**: MEDIUM
**Deadline**: Thursday 1/23

**Timeline Document Should Include:**
- Regular data dump schedule
- Expected processing time per batch
- SLA for data turnaround
- Resource availability
- Maintenance windows
- Escalation procedures
- Future improvements roadmap

**Update Items:**
- Current state of deployment
- Remaining work
- Known issues or risks
- Resource requirements
- Support model
- Training needs

---

## Technical Considerations

### Deployment Approach (No Terraform)

**Option 1: Azure CLI Bash Script**
```bash
# Create resource group
az group create --name apogee-rg --location eastus

# Create storage account
az storage account create --name apogeestorage --resource-group apogee-rg

# Deploy container instances
az container create --resource-group apogee-rg --name apogee-pipeline --image apogee:latest

# Assign roles
az role assignment create --assignee <sp-id> --role Contributor --scope <resource-id>
```

**Option 2: PowerShell with Az Modules**
```powershell
# Similar to above but PowerShell syntax
New-AzResourceGroup -Name apogee-rg -Location eastus
New-AzStorageAccount -ResourceGroupName apogee-rg -Name apogeestorage
```

**Option 3: Python with Azure SDK**
```python
from azure.mgmt.resource import ResourceManagementClient
# Programmatic deployment
```

**Recommendation:** Start with Azure CLI bash script (most straightforward, well-documented)

---

### Roles & Permissions Structure

**Service Principal for Pipeline:**
```bash
# Create SP
az ad sp create-for-rbac --name apogee-pipeline-sp

# Assign Storage Blob Data Contributor
az role assignment create \
  --assignee <sp-id> \
  --role "Storage Blob Data Contributor" \
  --scope <storage-account-id>
```

**WNA User Group:**
```bash
# Create or reference existing AD group
az ad group create --display-name apogee-wna-users

# Assign read-only access
az role assignment create \
  --assignee <group-id> \
  --role "Storage Blob Data Reader" \
  --scope <container-scope>
```

**Admin Group:**
```bash
# Create or reference admin group
az ad group create --display-name apogee-admins

# Assign contributor access
az role assignment create \
  --assignee <group-id> \
  --role "Contributor" \
  --scope <resource-group-id>
```

---

## Weekly Schedule

### Week of 1/6 (Current Week)
**Focus:** Complete deployment, documentation, and demo prep

**Monday 1/6:**
- [ ] Review meeting notes
- [ ] Create project plan
- [ ] Set up work environment

**Tuesday 1/7:**
- [ ] Run E2E testing with 1/8 data
- [ ] Validate old data comparison
- [ ] Begin deployment script (replace Terraform)

**Wednesday 1/8:**
- [ ] Complete deployment script
- [ ] Test in clean environment
- [ ] Begin documentation (roles & permissions)

**Thursday 1/9:**
- [ ] Complete roles & permissions documentation
- [ ] Complete pipeline definition documentation
- [ ] Begin demo preparation

**Friday 1/10:**
- [ ] Finalize demo
- [ ] **5pm: Demo slot with team**
- [ ] Gather feedback
- [ ] Update based on feedback

**Weekend:**
- [ ] Address any feedback from Friday demo
- [ ] Prepare for Monday data processing

---

### Week of 1/13
**Focus:** Process 1/16 data, refine deployment

**Monday 1/13 - Wednesday 1/15:**
- [ ] Refine deployment based on feedback
- [ ] Update documentation
- [ ] Prepare for data processing

**Thursday 1/16:**
- [ ] **Receive new data from Katie**
- [ ] Begin processing immediately
- [ ] Monitor pipeline

**Friday 1/17:**
- [ ] **Complete processing (ideal deadline)**
- [ ] Return data to Katie
- [ ] Document processing time

---

### Week of 1/20
**Focus:** Beck update, prepare for 1/22 batch

**Monday 1/20:**
- [ ] Return 1/16 data if not done Friday
- [ ] **Beck returns from away - provide update**
- [ ] Review progress with team

**Tuesday 1/21:**
- [ ] Prepare for 1/22 data dump
- [ ] Ensure pipeline ready
- [ ] Pre-validate environment

**Wednesday 1/22:**
- [ ] **1/22 data dump occurs**
- [ ] Begin processing immediately

**Thursday 1/23:**
- [ ] **Complete processing (ideal deadline)**
- [ ] Return to Kate
- [ ] **Update timelines document**

---

## Success Criteria

### Deployment Success
- [ ] Deployment works without Terraform
- [ ] Script is repeatable and reliable
- [ ] All resources properly configured
- [ ] Roles and permissions correctly assigned
- [ ] Pipeline executes successfully

### Documentation Success
- [ ] Clear roles and permissions guide
- [ ] Complete pipeline definition
- [ ] Step-by-step deployment instructions
- [ ] Troubleshooting guide included
- [ ] Team can deploy without assistance

### Demo Success
- [ ] Live demo executes smoothly
- [ ] Team understands architecture
- [ ] Questions answered satisfactorily
- [ ] Feedback gathered and addressed
- [ ] Approval to proceed

### Data Processing Success
- [ ] 1/8 data validates correctly
- [ ] 1/16 data returned by deadline
- [ ] 1/22 data returned by deadline
- [ ] Processing time meets SLA
- [ ] Quality maintained

### Timeline Success
- [ ] Updated timeline document created
- [ ] Team aligned on schedule
- [ ] SLAs defined and agreed
- [ ] Resource plan established

---

## Risks & Mitigation

### Risk 1: Deployment Script Complexity
**Risk:** Replacing Terraform with scripts may be more complex than expected
**Mitigation:**
- Start with simple bash/Azure CLI approach
- Keep scripts modular
- Document thoroughly
- Test in multiple environments

### Risk 2: Role/Permission Issues
**Risk:** Incorrect permissions could block pipeline execution
**Mitigation:**
- Test with least-privilege approach first
- Document required permissions clearly
- Have admin access available for troubleshooting
- Test with actual service principal, not admin account

### Risk 3: Data Processing Delays
**Risk:** Data processing may take longer than expected, missing deadlines
**Mitigation:**
- Start processing immediately upon data receipt
- Monitor processing actively
- Have escalation plan
- Communicate early if delays anticipated

### Risk 4: Demo Technical Issues
**Risk:** Live demo could fail due to technical issues
**Mitigation:**
- Test demo thoroughly beforehand
- Have backup recorded demo
- Prepare screenshots of successful run
- Have documentation as fallback

### Risk 5: Timeline Slippage
**Risk:** Multiple deadlines in short timeframe could cause conflicts
**Mitigation:**
- Prioritize critical path items
- Front-load work where possible
- Communicate early about conflicts
- Get help if needed

---

## Communication Plan

### Daily Updates
- Quick Slack/email update on progress
- Flag any blockers immediately
- Share wins/completions

### Katie Updates
- Sunday EOP: 1/8 data results
- Monday 1/20 AM (or Fri 1/17): 1/16 processed data
- Thursday 1/23 (or Sun 1/26): 1/22 processed data

### Beck Update
- Week of 1/20 when he returns
- Summary of progress
- Current state and next steps

### Team Demo
- Friday 1/10 5pm
- Present deployment, docs, and demo
- Gather feedback
- Discuss next steps

---

## Next Actions (Immediate)

### Today/Tomorrow:
1. [ ] Set up E2E local script environment
2. [ ] Run 1/8 data validation
3. [ ] Start deployment script development
4. [ ] Outline roles & permissions document

### By Wednesday:
1. [ ] Complete E2E testing and validation
2. [ ] Complete deployment script
3. [ ] Draft roles & permissions doc

### By Thursday:
1. [ ] Complete all documentation
2. [ ] Prepare demo environment
3. [ ] Test demo flow

### By Friday 5pm:
1. [ ] **Deliver demo to team**
2. [ ] Present documentation
3. [ ] Discuss next steps

---

## Status: Active - Week 1 of 3

### Current Phase: Development & Documentation
**This Week (1/6-1/10):** Build, document, and demo
**Next Week (1/13-1/17):** Process 1/16 data, refine
**Week 3 (1/20-1/26):** Process 1/22 data, update timelines

**Critical Path:** E2E validation → Deployment script → Documentation → Demo → Data processing

---

*Project created: 2025-01-09*
*Based on: Weekend work notes + 1/9 meeting notes*
*Next update: After Friday 1/10 demo*
