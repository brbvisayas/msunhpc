# 00 – HPC Access

Welcome to the MSU HPC Workshop!

This module is your starting point. Here, you'll learn how to access the MSU High-Performance Computing (HPC) cluster so that you can begin running computational chemistry calculations using ORCA in later modules.

> **Target Audience:** This guide is intended for **end users**, not system administrators. No prior HPC experience is required.

---

## What You'll Learn

By the end of this module, you will:

- Understand what an HPC cluster is and how it is organized
- Learn how to connect to the MSU HPC cluster using SSH
- Know where to store your files and how to navigate the file system
- Be able to verify your access and test basic cluster functionality

---

## Topics Covered

Each of the following files will walk you through a specific aspect of HPC access:

| File | Description |
|------|-------------|
| `01_cluster_overview.md` | Overview of the MSU HPC system layout |
| `02_ssh_access.md`       | How to connect to the cluster via SSH |
| `03_directory_structure.md` | Understanding the file systems: `/home`, `/shared`, and `/tmp` |
| `04_modules_environment.md` | Environment setup for using software like ORCA |
| `05_test_connection.sh` | A script to verify your cluster access and environment setup |
| `06_troubleshooting.md` *(optional)* | Common issues and how to resolve them |

---

## Prerequisites

- You should already have an MSU HPC user account.
- You should have been provided with your SSH login credentials and instructions.
- Software requriements:
    •	[Visual Studio Code](https://code.visualstudio.com/download)

	•	For Windows: [Git Bash](https://gitforwindows.org/)
    
    •	[Chemcraft](https://www.chemcraftprog.com/download.html)

---

## Next Steps

Once you complete this module and confirm your access, you’ll be ready to submit and run real ORCA jobs on the cluster, starting in module [`03_orca`](../03_orca/).