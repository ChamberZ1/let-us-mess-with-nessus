# Ubuntu Desktop Vulnerability Assessment

## Overview
This assessment evaluates the security posture of a local Ubuntu host. The objective was to identify vulnerabilities, determine root causes, apply remediation, and validate the effectiveness of those fixes.

---

## Environment
- **Operating System:** Ubuntu 24.04  
- **Target:** Localhost (127.0.0.1)

---

## Methodology
1. Conduct initial vulnerability assessment  
2. Analyze and prioritize findings by severity  
3. Identify root causes  
4. Apply remediation measures  
5. Re-assess to validate remediation 

---

## Results

### Before Remediation
- **Critical:** 1 
- **High:** 7
- **Medium:** 3

![Initial Scan](../assets/wtf-my-sys-is-vuln.png)

---

### After Remediation
- **Critical:** 0 
- **High:** 0 
- **Medium:** 1 

![After Patch](../assets/after-patch.png)

---

## Key Findings

- **Outdated System Packages**  
  The majority of identified vulnerabilities were due to outdated packages. These were remediated through Extended Security Maintenance (ESM) updates.

- **Self-Signed SSL Certificate**  
  A self-signed certificate was detected on a local service. This is expected behavior and presents minimal risk as the service is not externally exposed.

---

## Analysis

### Initial Findings
The assessment identified multiple medium to critical vulnerabilities. Review of individual findings showed that most issues were associated with outdated packages.

![Critical Vulnerabilities](../assets/critical-vulns.png)

---

### Root Cause
Some vulnerabilities were present because their fixes are distributed through Ubuntu’s ESM repositories, which were not enabled on the system.

---

### Remediation
Remediation actions included:

- Enabling ESM access via Ubuntu Pro
- Applying all available security patches
- Rebooting the system to ensure updates were applied 

---

### Outcome
Following remediation:

- All critical and high-severity vulnerabilities were resolved
- 1 medium-severity vulnerability remains and is considered low risk due to limited exposure (local service)
- Remaining findings are informational only

---

## Key Takeaways
- Effective patch management significantly reduces vulnerability exposure  
- Severity ratings require contextual interpretation based on system exposure  
- Validation through re-assessment is essential to confirm remediation effectiveness  
