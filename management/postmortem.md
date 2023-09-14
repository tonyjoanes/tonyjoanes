# Postmortem

After an incident happens, make sure it doesn't happen again. Put in processes, code changes etc to see what can be introduced to prevent its reocurrence.

## Example Format

# Incident Postmortem Report

### General Information
- **Incident Title:** 
- **Date of Incident:** 
- **Date of Postmortem:**
- **Incident Leader:**
- **Postmortem Facilitator:**
- **Team Members Involved:**

### Summary
- **Incident Duration:**
- **User Impact:**
- **Affected Services:**
  * (e.g., API Gateway, User Service, Payment Service)
  
### Timeline
- **Incident Discovery:**
  * How was the incident identified?
- **Initial Triage:**
  * What immediate actions were taken?
- **Resolution:**
  * Steps to mitigate/resolve the incident
- **Post-Incident:**
  * Follow-up actions

### Root Cause Analysis
- **Root Cause(s):**
  * (e.g., Code bug, server failure, incorrect configuration)
- **Contributing Factors:**
  * (e.g., Lack of monitoring, insufficient testing)
  
### Lessons Learned
- **What Went Well:**
- **What Could Have Been Done Better:**
- **What Was Surprising:**

### Action Items
| Action Item | Owner | Due Date | Status |
|-------------|-------|----------|--------|
| Example: Implement circuit breaker for User Service | John D. | MM/DD/YYYY | In Progress |

### Appendices
- **Incident Metrics:**
  * (e.g., Error rates, latency)
- **Screenshots/Logs:**
- **Related Tickets/Documentation:**
