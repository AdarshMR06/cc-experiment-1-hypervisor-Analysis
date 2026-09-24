CC-Experiment-01: Performance Analysis of Type-1 and Type-2 Hypervisors
1. Experiment Title
Performance Analysis of Type-1 and Type-2 Hypervisors

2. Aim
To create and configure identically resourced Ubuntu virtual machines on a Type-1 hypervisor (Proxmox VE) and a Type-2 hypervisor (VMware Workstation) and compare their CPU performance using the Sysbench CPU benchmark.

3. Objectives
The objectives of this experiment are:

To understand the concept of virtualization and the role of hypervisors.
To study the differences between Type-1 and Type-2 hypervisors.
To configure and run an Ubuntu virtual machine on Proxmox VE.
To configure and run an Ubuntu virtual machine on VMware Workstation.
To allocate identical CPU, memory, and other relevant resources to both virtual machines.
To perform CPU benchmarking using Sysbench.
To collect CPU performance metrics from both virtualization environments.
To compare execution time, total events, events per second, and average latency.
To analyze the effect of the virtualization layer on CPU performance.
To document the experimental procedure, observations, screenshots, and benchmark results.
4. Introduction
4.1 Virtualization
Virtualization is a technology that enables physical computing resources such as CPU, memory, storage, and network interfaces to be abstracted and allocated to multiple virtual machines.

A Virtual Machine (VM) is a software-based computer system that operates independently within a physical computer. It has its own virtual CPU, memory, storage, network interface, and operating system.

Virtualization allows multiple virtual machines to run simultaneously on the same physical hardware while maintaining a degree of isolation between them.
