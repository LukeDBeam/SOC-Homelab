# Cybersecurity HomeLab -- Kali Linux & Windows 10
  This lab was created using Oracle Virtual Box, featuring Kali Linux as the 
  main workstation which is used to target the Windows 10 virtualbox 
  for Penatration testing

  The beginning of this focuses on configuring the virtual machines, while 
  establishing a foundation for security monitoring and incident response
  through security logging and network monitoring. 
  ### Project Scope: 
  This repository documents the lab infrastructure and initial 
  configuration, then going on to malware simulations and incident investigations that 
  will be documented in a separate project.
## Project Summary
  Provides two key architectures for Security:
    1.  *Blue Hat* The Windows machine for the Security Operations Center (SOC) Where
    events are generated, logged, and monitored. This is also the endpoint for Kali.
    2.  *Red Hat* The Kali machine which is our starting point for a pen test, which 
    provides ethical hacking tools to practice on this isolated virtual environment.
# Lab Framework
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/fb2734e3-53ae-4048-ae07-f69b7c922ff3" />

** Diagram of Architecture layout of the SOC home lab. **

# Objectives
  - Create a virtual Kali Linux security lab
  - Create a virtual Windows Victim Machine
  - Configure Windows machine as a monitored endpoint
  - Configure Linux as a Penatration test analysis machine
  - Verify communication between target and victim
  - Create foundation for future security exercises
# The Write up

## Creating The virtual machines

Orcale VirtualBox was used to host both the Windows 10 machine & the Kali machine. 
I used .iso files to give to Oracle for each of the machines and manually set up each 
with proper passwords and storage.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/22aa569c-6ab9-4cd1-a40f-6ab76df8b597" />

 **Image 1 - Windows and Kali virtual machines running with Oracle VirtualBox.**



## Settings page of Kali Linux Virtual Box

Kali Linux was set up as the primary machine for security testing and analysis. 
It includes a variety of cybersecurity tools that can be used to perform network scanning, 
reconnaissance, vulnerability assessments, and other security-related activities within the isolated lab environment.

<img width="1376" height="704" alt="image" src="https://github.com/user-attachments/assets/e49dc07b-f8e2-41d6-a455-417810aa7300" />

**Image 2 - Kali Settings in Oracle. **

# Settings page of Windows 10 Virtual Box

The Windows virtual machine serves as the target endpoint for security testing and monitoring within the lab. 
Its CPU, RAM, storage, and network settings were configured based on the host machine's available resources to ensure stable performance.

<img width="1376" height="711" alt="image" src="https://github.com/user-attachments/assets/6a4107eb-d386-4c00-a536-06347e180e4a" />

**Image 3 - Windows 10 settings in Oracle. **


# Installing System Monitor

Using PowerShell I was able to locate the System Monitor (sysmon) file on my computer 
and then install the file into the Windows machine.



<img width="1089" height="816" alt="image" src="https://github.com/user-attachments/assets/8620e687-53ec-4f98-86ed-867d9381851d" />

**Image 4 - Used powershell to install sysmon for Event Viewer. **

#Scanned local net in Kali to find Windows IP (Shown as IPv4: 10.0.2.15)
<img width="717" height="558" alt="image" src="https://github.com/user-attachments/assets/d98a7831-604c-4ee1-94ee-f90781dff4c1" />
<img width="884" height="666" alt="image" src="https://github.com/user-attachments/assets/b6e35dfb-7797-464b-a008-4d29e4706cca" />

# Windows Even viewer

Route- Applcations and Service Logs- Mirosoft- Windows- sysmon
<img width="949" height="838" alt="image" src="https://github.com/user-attachments/assets/1b84d069-8e17-4ed6-8d35-4a30317b4ba8" />






