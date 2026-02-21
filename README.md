# 📦 Ansible Roles

Collection of **Ansible roles** for automated server configuration management and application deployment.

## 📁 Project Structure

```
├── roles/                 # Ansible roles directory
│   ├── common/            # Base server configuration
│   ├── webserver/         # Web server setup (Nginx/Apache)
│   ├── database/          # Database installation & configuration
│   └── ...                # Additional roles
├── inventory              # Host inventory file
└── playbook.yml           # Main playbook
```

## 🛠️ Tech Stack

- **Configuration Management:** Ansible
- **OS:** RHEL, CentOS, Ubuntu
- **Patterns:** Roles, Handlers, Templates, Variables

## 🚀 Usage

```bash
# Run playbook against inventory
ansible-playbook -i inventory playbook.yml

# Run specific role with tags
ansible-playbook -i inventory playbook.yml --tags "webserver"

# Dry run (check mode)
ansible-playbook -i inventory playbook.yml --check
```

## 📋 Roles

| Role | Description |
|------|-------------|
| `common` | Base packages, users, SSH hardening, NTP |
| `webserver` | Nginx/Apache installation and vhost configuration |
| `database` | MySQL/MongoDB setup with secure defaults |

## ✅ Key Features

- Idempotent role-based architecture
- Environment-specific variable overrides
- Handler-driven service restarts
- Template-based configuration files
- Inventory-based multi-environment targeting
