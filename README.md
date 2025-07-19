# 🚀 AWS EC2 using Ansible

This project creates an EC2 instance on AWS using Ansible, roles, variables, and Ansible Vault.

---

## 🔧 How to Run

```bash
ansible-playbook -i inventory.ini create-aws-ec2 --ask-vault-pass
```

Project Structure

    create-aws-ec2: Main playbook

    ec2/tasks/main.yml: EC2 creation logic

    group_vars/all.yml: Variables (vault-encrypted)

    vault.pass: Vault password (ignored in Git)

## 🔒 Secrets
Sensitive values like ec2_access_key and ec2_secret_key are stored securely using Ansible Vault.
 
## ✅ Example Output
After running the playbook, an EC2 instance will be created in your AWS account with the configured parameters.
