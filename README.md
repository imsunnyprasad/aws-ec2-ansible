# 🚀 AWS EC2 using Ansible

This project creates an EC2 instance on AWS using Ansible, roles, variables, and Ansible Vault.

---

## 🔧 How to Run

```bash
ansible-playbook -i inventory.ini create-aws-ec2 --ask-vault-pass
```

## 📁 Project Structure

aws-ec2/
├── create-aws-ec2         # Main playbook
├── ec2/                   # Role for EC2 instance
│   └── tasks/
│       └── main.yml       # Task to launch EC2 instance
├── group_vars/
│   └── all.yml            # Variables (Vault encrypted)
├── inventory.ini          # Inventory file (localhost)
├── vault.pass             # Vault password file (excluded via .gitignore)
└── .gitignore             # Git ignore rules

## 🔒 Secrets
Sensitive values like ec2_access_key and ec2_secret_key are stored securely using Ansible Vault.
 
## ✅ Example Output
After running the playbook, an EC2 instance will be created in your AWS account with the configured parameters.
