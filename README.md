# Network Automation Toolkit with Python and Ansible

## **Overview**
This project documents the automation of two manual network tasks: **configuration backups** with **Python and Netmiko**, and **VLAN changes** with an **Ansible** playbook. The time saved is measured against doing the same work by hand.

## **Lab Setup**
- **Network Devices:** the switches and routers from the earlier labs, reachable over SSH
- **Control Machine:** Linux or WSL with Python 3 and Ansible
- **Source Control:** Git

## **Project Objectives**
- Back up running configs from many devices with a **Python** script
- Keep credentials in environment variables, never in code
- Audit saved configs against the hardening checklist
- Create VLANs and assign access ports with an **Ansible** playbook
- Run changes in check mode before applying them
- Measure the time saved against manual work

---

## **1. Environment Setup**
1. **Set up a Python virtual environment**
2. **Install Netmiko, PyYAML and Ansible**
3. **Store the SSH credentials in environment variables**
4. **Test SSH access to each lab device**

## Environment Setup - Visual Guide

<!-- screenshots -->


## **2. Config Backup Script**
1. **Create a YAML inventory of devices**
2. **Connect to each device and read the running config**
3. **Save each config to a folder named after the device and the date**
4. **Log failures and carry on with the next device**
5. **Commit the backups to Git**

## Config Backup Script - Visual Guide

<!-- screenshots -->


## **3. Config Audit Script**
1. **Define the checks from the hardening checklist**
2. **Read the saved configs**
3. **Report each device that fails a check**

## Config Audit Script - Visual Guide

<!-- screenshots -->


## **4. Ansible Playbook for VLANs**
1. **Create the inventory and a variables file of VLANs**
2. **Write the playbook with the cisco.ios modules**
3. **Run it in check mode**
4. **Run it for real and confirm the VLANs on the switches**

## Ansible Playbook for VLANs - Visual Guide

<!-- screenshots -->


## **5. Time Comparison**
1. **Time a manual backup of all devices**
2. **Time the script**
3. **Time a manual VLAN change on every switch**
4. **Time the playbook**

## Time Comparison - Visual Guide

<!-- screenshots -->


## **Project Outcomes & Key Results**
- **Automated Backups** – Configs saved from every device with one command
- **Compliance Check** – Saved configs checked against the checklist
- **Repeatable VLAN Changes** – VLANs created from a single YAML file
- **Time Saved** – Manual and automated timings compared

## **Potential Next Steps**
- **Add a scheduled backup**
- **Collect device facts with NAPALM**
- **Query an IOS-XE device with RESTCONF**

---

This project is part of my **Networking and Infrastructure portfolio**. For any inquiries, reach out via **[LinkedIn](https://www.linkedin.com/in/kimutai-fredrick/)**.

**_Built and documented by Fredrick Kimutai._**
