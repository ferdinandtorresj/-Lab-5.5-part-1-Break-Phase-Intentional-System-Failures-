# -Lab-5.5-part-1-Break-Phase-Intentional-System-Failures-

This repository contains the break phase for Lab 5.5 part 1.   Three realistic Linux failures were intentionally introduced to simulate common issues in user management, permissions, and automation workflows.


No fixes are included in this phase.  
Fixes will be documented in **Lab 5.5 – Part 2 (Fix Phase)** after a delay to simulate real-world troubleshooting.

---

## 🔧 Break 1 – Directory Permission Issue
A team directory was modified so that valid users could no longer access it.  
Permissions and/or ownership were intentionally altered to create a realistic access failure.

**Symptoms captured:**
- User receives “permission denied”
- Directory ownership does not match expected values
- Group members cannot access their team folder


<img width="1909" height="980" alt="ticket 1 david cant edit emilys file" src="https://github.com/user-attachments/assets/2780ed3c-bdd4-49af-a8e8-0395d705a1b8" />



<img width="1919" height="915" alt="ticket 1 showing emily and daving are in the group along with emily creating a file" src="https://github.com/user-attachments/assets/b64749eb-6c7d-4914-b65a-bd7dca355fe8" />



---

## 🔧 Break 2 – Group Membership Desync
A user was removed from a group and re-added while still logged into an active session.  
This created a stale session where the system and the user’s shell disagreed on group membership.

**Symptoms captured:**
- `id` does not show the correct group
- `getent group` shows the user in the group
- User cannot access the team directory despite correct membership

<img width="1917" height="944" alt="ticket 2 liam is in dev group but cant access team dir" src="https://github.com/user-attachments/assets/8b1eab5c-66df-4749-b177-fddc5be2d7de" />



---

## 🔧 Break 3 – Automation Script Input File Corruption
The `adduser.sh` automation script was sabotaged by modifying its input text file.  
Malformed entries (extra spaces, formatting issues) were added to cause incorrect directory creation.

**Symptoms captured:**
- Script runs without errors but produces incorrect directory names
- Unexpected or malformed user directories appear
- Automation output is inconsistent with expected usernames


<img width="1920" height="915" alt="ticket 3 adduser script does not work" src="https://github.com/user-attachments/assets/d8515c54-4f5a-4885-8f18-e9aa6a083faf" />


---

## 📚 Notes
This phase focuses solely on creating realistic system failures.  
Fixes and root-cause analysis will be documented in **Lab 5.5 – Part 2 (Fix Phase)**.
