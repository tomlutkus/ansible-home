# 💠 ansible-home

Ansible playbooks and roles for managing my personal infrastructure and development machines. Clean, modular, and minimal — built for reproducibility and sanity.

## 📁 Structure

```
ansible-home/
├── ansible.cfg            # Central config
├── inventory/             # Inventory files (YAML)
│   ├── group_vars/        # Host group variables
│   │   ├── all.yml
│   │   └── homelab.yml
│   └── inventory.yml      # Inventory definition
├── playbooks/             # Playbooks for various tasks
│   ├── site.yml
│   ├── add_new_admin.yml
│   ├── remove_key.yml
│   └── ...
├── roles/                 # Reusable Ansible roles
├── templates/             # Jinja2 templates
└── files/                 # Static files to deploy
```

## ▶️ Usage

Run a playbook:

```bash
ansible-playbook -i inventory/inventory.yml playbooks/site.yml
```

Add `--ask-become-pass` if needed for sudo.

## 🧰 Playbooks

| Playbook            | Description                  |
| ------------------- | ---------------------------- |
| `site.yml`          | Main entry point             |
| `add_new_admin.yml` | Add new admin user + SSH key |
| `remove_key.yml`    | Remove an SSH key            |
| `set_hostname.yml`  | Set system hostname          |
| `open_port_ufw.yml` | Open UFW port for a service  |

## 🔒 Secrets

Sensitive data (vault passwords, private inventories) are **not included** and should be stored securely elsewhere.

## ✅ Status

✔️ Works on Arch, Debian, Ubuntu
☁️ No cloud-specific hardcoding
🩼 Clean YAML, linted, human-readable

## 📜 License
