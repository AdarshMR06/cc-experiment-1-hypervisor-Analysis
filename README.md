# Hypervisor Performance Analysis

## Type-1 vs Type-2 Hypervisor Comparison

**Proxmox VE (Type-1) vs VMware Workstation (Type-2)**

## What is this experiment?

- We test two types of hypervisors.
- A hypervisor is software that runs virtual machines (VMs).
- **Type-1 hypervisor** — installs directly on a server. No host OS. Example: **Proxmox VE**.
- **Type-2 hypervisor** — installs on top of a normal OS, like an app. Example: **VMware Workstation**.
- We create the same Ubuntu VM on both.
- We run a CPU test called **Sysbench** on both.
- We compare the results.
- We check which hypervisor is faster.

## VM Settings (Same on Both Sides)

- **Guest OS:** Ubuntu 22.04 or later
- **CPU:** 2 vCPU
- **Memory:** 2 GB RAM
- **Disk:** 20 GB
- **Benchmark command:**

```bash
sysbench cpu --cpu-max-prime=20000 run

What is Inside This Folder?
CC-Experiment-01-Hypervisor-Analysis/
│
├── screenshots/
│   ├── type1-proxmox/
│   │   └── screenshots from Proxmox VE
│   │
│   ├── type2-vmware/
│   │   └── screenshots from VMware Workstation
│   │
│   └── comparison/
│       └── final comparison table screenshot
│
├── results/
│   └── performance-analysis.md
│
└── README.md
Steps We Followed
Logged in to Proxmox VE.
Created an Ubuntu VM with 2 vCPU, 2 GB RAM, and 20 GB disk.
Started the VM and installed Ubuntu.
Checked CPU and memory using lscpu and free -h.
Installed Sysbench.
Ran the CPU benchmark on the Proxmox VM.
Repeated the same steps in VMware Workstation.
Ran the CPU benchmark on the VMware VM.
Compared both results.
Saved screenshots as proof.
Before You Start (Prerequisites)
Proxmox VE server address
Proxmox VE port: 8006
Proxmox VE login details
VMware Workstation installed on your computer
Ubuntu ISO file
At least 20 GB free disk space
At least 4 GB free RAM
Git installed on your computer
GitHub account
Final Results
| Parameter            | Type-1: Proxmox VE | Type-2: VMware Workstation |
| -------------------- | -----------------: | -------------------------: |
| Total Execution Time |          10.0005 s |                  10.0006 s |
| Total Events         |             17,494 |                      7,077 |
| Events per Second    |           1,749.16 |                     707.43 |
| Average Latency      |            0.57 ms |                    1.41 ms |
Result Summary

Based on the recorded benchmark results, Proxmox VE produced higher events per second and lower average latency in this experiment.

Note: The result applies to this specific experimental setup and benchmark run.

Full details are available in:
results/performance-analysis.md
Screenshot File Names
Proxmox VE

Location:
screenshots/type1-proxmox/
Files:
01-proxmox-dashboard.png
02-proxmox-vm-configuration.png
03-proxmox-vm-running.png
04-proxmox-ubuntu-console.png
05-proxmox-system-configuration.png
06-proxmox-sysbench-result.png
07-proxmox-resource-monitoring.png
VMware Workstation
Location:
screenshots/type2-vmware/
Files:
01-vmware-vm-configuration.jpeg
02-vmware-vm-running.jpeg
03-vmware-system-configuration.jpeg
04-vmware-sysbench-result.jpeg
Comparison

Location:
screenshots/comparison/
File:
01-hypervisor-performance-comparison.jpeg
