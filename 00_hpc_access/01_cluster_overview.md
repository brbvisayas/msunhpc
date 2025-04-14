# 01 – Cluster Overview

Before diving into calculations, it's important to understand what the HPC cluster is and how it works — at least at a basic level. This will help you navigate it with confidence and avoid common pitfalls.

---

## What Is an HPC Cluster?

An **HPC (High-Performance Computing) cluster** is a group of connected computers (called **nodes**) that work together to perform large-scale computations faster than a single desktop computer.

At MSUN, the HPC system is designed to support research in chemistry, physics, data science, machine learning, and related disciplines — including **ORCA-based quantum chemistry calculations**.

---

## The Cluster Architecture

The MSUN HPC consists of:

| Node       | Description |
|------------|-------------|
| `aghimuan` | The **head node** or **login/controller node**. This is where you log in, prepare jobs, submit them to the scheduler, and check on progress. |
| `nanogpu`  | The **compute node**, equipped with both CPUs and GPUs. This is where your ORCA jobs will actually run. |

You don’t log into the compute node directly. Instead, jobs are submitted through the **Slurm job scheduler**, which handles where and when your jobs run.

---

## Shared File System

All nodes in the cluster share access to a unified file system. Here are the main directories:

| Path        | Purpose |
|-------------|---------|
| `/home`     | Your personal space. Good for scripts and small files. |
| `/shared`   | A large shared storage area. Use this for input/output files and results. |
| `/tmp`      | Temporary space local to each compute node. Ideal for job scratch files. Files here may be deleted automatically after jobs finish. |

---

## Software Environment

Software like ORCA and NBO is **not globally installed**, but provided in shared directories and activated using environment variables or module scripts. You’ll learn how to do this in the `04_modules_environment.md` section.

---

## Your First Interaction

Once you're connected (see the next file), try running:

```
hostname      # Shows which node you're on
df -h         # Check available disk space
sinfo         # Show available Slurm partitions (if accessible)
```