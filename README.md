# 🐧 Linux File Permissions & Authorization – Security Investigation

## 📌 Project Description
In this project, I worked as a security analyst to configure authorization in a Linux environment by examining and modifying file and directory permissions. The objective was to ensure that only authorized users and groups could access sensitive files and directories.

Using Linux commands such as `ls` and `chmod`, I reviewed permission settings, identified misconfigurations, and removed unauthorized access. This project demonstrates how Linux file permissions support system security and access control.

---

## 🎯 Skills Demonstrated
- Linux file and directory permission management  
- Understanding permission strings (`rwx`)  
- Access control and authorization  
- Securing hidden and sensitive files  
- Command-line security analysis  
- Security best practices in Linux environments  

---

## 🛠 Tools Used
- Linux (Bash shell)
- chmod
- ls
- GitHub

---

## 🔍 Investigation Tasks & Commands

### 1️⃣ Check File and Directory Permissions
**Objective:** Review permissions, ownership, and group access for all files in the projects directory, including hidden files.

```bash
cd projects
ls -l
ls -la
```

![Check file and directory permissions](screenshots/step%201.png)

**Explanation:**

- Lists all files and directories with permission details.

- Identifies file owners and group ownership.

- Confirms the group research_team owns the files.

- Reveals the hidden file .project_x.txt.

### 2️⃣ Remove Unauthorized Write Access from Files

**Objective:** Ensure that other users do not have write permissions on any files.

```bash
chmod o-w project_k.txt
```

![Remove unauthorized write access](screenshots/step%202.png)

**Explanation:**

- Removes write permissions for other users.

- Prevents unauthorized modification of files.

- Strengthens access control.

### 3️⃣ Secure a Restricted File

**Objective:** Ensure that a sensitive file is accessible only to the file owner.

```bash
chmod g-r project_m.txt
```

![Secure restricted file](screenshots/step%203.png)

**Explanation:**

- Removes read access for the group.

- Ensures only the owner can access the file.

- Protects sensitive project data.

### 4️⃣ Change Permissions on a Hidden File

**Objective:** Secure an archived hidden file so it cannot be modified.

```bash

chmod ug-w .project_x.txt
```

![Hidden file permissions](screenshots/step%204.png)

**Explanation:**

- Removes write access for both user and group.

- Maintains read-only access.

- Preserves file integrity.

### 5️⃣ Restrict Directory Access

**Objective:** Ensure that only the file owner can access a sensitive directory.

```bash
chmod g-x drafts
```
![Directory permission changes](screenshots/step%205.png)

**Explanation:**

- Removes execute permissions for the group.

- Prevents unauthorized directory access.

- Ensures only the owner can access the directory contents.

## 📊 Summary:
This project demonstrates my ability to apply Linux authorization and access control principles to secure files and directories. I identified permission misconfigurations, removed unauthorized write and execute access, secured hidden and restricted files, and enforced least-privilege access.

