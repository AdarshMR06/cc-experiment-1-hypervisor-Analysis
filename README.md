Hypervisor Performance Analysis
Type-1 vs Type-2 Hypervisor Comparison Proxmox VE (Type-1) vs VMware Workstation (Type-2)

What is this experiment?
We test two types of hypervisors.
A hypervisor is software that runs virtual machines (VMs).
Type-1 hypervisor — installs directly on a server. No host OS. Example: Proxmox VE.
Type-2 hypervisor — installs on top of a normal OS, like an app. Example: VMware Workstation.
We create the same Ubuntu VM on both.
We run a CPU test called Sysbench on both.
We compare the results.
We check which hypervisor is faster.
VM settings (same on both sides)
Guest OS: Ubuntu 22.04 or later
CPU: 2 vCPU
Memory: 2 GB RAM
Disk: 20 GB
Benchmark command: sysbench cpu --cpu-max-prime=20000 run
What is inside this folder
CC-Experiment-01-Hypervisor-Analysis/
│
├── screenshots/
│   ├── type1-proxmox/      → screenshots from Proxmox VE
│   ├── type2-vmware/       → screenshots from VMware Workstation
│   └── comparison/         → final comparison table screenshot
│
├── results/
│   └── performance-analysis.md   → benchmark numbers and conclusion
│
└── README.md               → this file
Steps we followed
Logged in to Proxmox VE.
Created an Ubuntu VM (2 vCPU, 2 GB RAM, 20 GB disk).
Started the VM and installed Ubuntu.
Checked CPU and memory using lscpu and free -h.
Installed Sysbench.
Ran the CPU benchmark on Proxmox VM.
Repeated the same steps in VMware Workstation.
Ran the CPU benchmark on VMware VM.
Compared both results.
Saved screenshots as proof.
Before you start (prerequisites)
Proxmox VE server address, port 8006, and login details.
VMware Workstation installed on your computer.
An Ubuntu ISO file.
At least 20 GB free disk space.
At least 4 GB free RAM.
Git installed on your computer.
A GitHub account.
Final results
Parameter	Type-1: Proxmox VE	Type-2: VMware Workstation
Total Execution Time	10.0005 s	10.0006 s
Total Events	17,494	7,077
Events per Second	1,749.16	707.43
Average Latency	0.57 ms	1.41 ms
Winner: Proxmox VE (Type-1) — about 2.5 times faster.

Full details are in results/performance-analysis.md.

Screenshot file names
Proxmox VE (screenshots/type1-proxmox/)

01-proxmox-dashboard.png
02-proxmox-vm-configuration.png
03-proxmox-vm-running.png
04-proxmox-ubuntu-console.png
05-proxmox-system-configuration.png
06-proxmox-sysbench-result.png
07-proxmox-resource-monitoring.png
VMware Workstation (screenshots/type2-vmware/)

01-vmware-vm-configuration.jpeg
02-vmware-vm-running.jpeg
03-vmware-system-configuration.jpeg
04-vmware-sysbench-result.jpeg
Comparison (screenshots/comparison/)

01-hypervisor-performance-comparison.jpeg
How to upload to GitHub
Go to your GitHub repository.
Click Add file → Upload files.
Drag in the folders and files.
Click Commit changes.
Or using Git commands:

cd CC-Experiment-01-Hypervisor-Analysis
git init
git add .
git commit -m "Add hypervisor performance analysis experiment"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo-name>.git
git push -u origin main
