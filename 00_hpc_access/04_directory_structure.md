# 04 – Understanding the Cluster File System

The MSU HPC cluster uses a **shared file system** that all nodes can access. Knowing where to store your files is crucial for performance, efficiency, and avoiding data loss.

---

## 📁 Key Directories

Here are the main locations you'll interact with:

| Path        | Description |
|-------------|-------------|
| `/home`     | Your personal user space. Good for small scripts, source files, and configuration. Backed up occasionally. |
| `/shared`   | High-capacity shared storage. Use this for large input/output files, ORCA jobs, and shared project data. Accessible by all users. |
| `/tmp`      | Temporary scratch space **local to each compute node**. Fast, but not shared between nodes and deleted after job completion. Ideal for ORCA runtime scratch. |

---

## 🧭 Where Should You Work?

- Keep scripts and Slurm job files in your `/home` directory.
- Run ORCA jobs from a **job-specific folder inside `/shared`**.
- Use `/tmp` inside your job script for scratch data (e.g., `TMPDIR=/tmp/$SLURM_JOBID`).

---

## 💡 Example Folder Layout

/home/training/yourname
├── orca_scripts/
│   ├── job1.slurm
│   └── job2.slurm
/shared/yourusername/
├── job1/
│   ├── input.inp
│   ├── output.out
│   └── scratch/  ← created by the job script using /tmp