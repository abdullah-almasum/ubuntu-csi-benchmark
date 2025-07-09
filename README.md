# Ubuntu CIS Benchmark Automation

This repository contains Ansible playbooks to **assess and remediate Ubuntu servers** according to the [CIS Benchmark](https://www.cisecurity.org/cis-benchmarks) guidelines using the **Red Hat Ansible Automation Platform (AAP)**.

---

## 📌 Project Objective

Automate CIS compliance checks and remediation for Ubuntu 24.10 servers to ensure a secure, consistent, and auditable baseline across all Linux systems.

---

## 📁 Repository Structure

---

## 🚀 Usage

### 🔧 Requirements

- Ansible 2.12+ (Recommended: 2.15+)
- Passwordless SSH access to Ubuntu targets
- Sudo privileges for automation user
- `ansible-lockdown.ubuntu24_cis` role (or customized role in `roles/`)

---

### 📝 Inventory Example (`inventory_ubuntu.yml`)

```yaml
all:
  children:
    linux:
      hosts:
        linux-server-01:
          ansible_host: Target Host IP
          ansible_user: Target UserName
          ansible_port: 22
          ansible_connection: ssh
