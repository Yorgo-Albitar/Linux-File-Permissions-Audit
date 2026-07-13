# 🔐 Linux File Permissions Audit & Remediation

A hands-on security audit and permissions remediation project completed as part of the Google Cybersecurity Professional Certificate.

## 📖 Project Overview

Conducted a security audit of file and directory permissions within a Linux research team's projects directory. Identified permission misconfigurations that violated the Principle of Least Privilege and applied targeted remediations to align permissions with organizational authorization requirements.

## 🎯 Scenario

The research team's file permissions were misaligned with their intended authorization levels, creating a security risk. As the security analyst, my responsibilities were to:

- Audit existing permissions across files and directories
- Identify non-compliant access rights
- Apply corrective permissions
- Verify and document all changes

## 🛠️ Tools & Skills Used

- Linux CLI (Bash)
- ls -la command
- chmod command
- Permission string analysis
- Security auditing
- Principle of Least Privilege

## 📋 Step 1: Initial Permission Audit

Used ls -la to enumerate all files and directories, including hidden files.

![Initial audit](screenshot%201%20linux%20access%20commands.png)

The output revealed one directory (drafts), one hidden file (.project_x.txt), and five project files.

## 📋 Step 2: Removed Write Access on project_k.txt

The organization determined that "other" users should not have write access to any files.

Command used: `chmod o-w project_k.txt`

![Chmod project_k](screenshot%202%20linux%20access%20commands.png)

## 📋 Step 3: Modified Permissions on Hidden File

No one should have write access to this project, but the user and group should retain read access.

Command used: `chmod u-w,g-w,g+r .project_x.txt`

![Chmod hidden file](screenshot%203%20linux%20access%20commands.png)

## 📋 Step 4: Final Verification

Ran ls -la one final time to confirm all permissions matched the required state.

![Final verification](screenshot%204%20linux%20access.png)

## 💡 Key Concepts Applied

- Principle of Least Privilege
- Permission String Analysis
- Multi-Argument chmod syntax
- Verification Workflow

## 🎓 Lessons Learned

- Real-world security auditing begins with careful enumeration
- The chmod command's multi-argument syntax enables efficient remediation
- Verification after each change is essential for compliance
- Hidden files require the same security scrutiny as regular files

## 📚 Certificate Context

This project was completed as part of the Google Cybersecurity Professional Certificate on Coursera, demonstrating practical application of Linux security fundamentals in a simulated enterprise environment.

## 👤 Author

Yorgo Albitar
Cybersecurity Student | Aspiring SOC Analyst
Email: Yorgobitar59@gmail.com
GitHub: https://github.com/Yorgo-Albitar
