# Ansible K8s Upgrade Playbook

Этот репозиторий содержит плейбуки для обновления Kubernetes-кластера с помощью Ansible.

## 📂 Структура проекта

```bash
ansible-k8s-upgrade/
├── inventories/       # инвентори (hosts, группы)
│   └── prod/
│       └── inventory.ini
├── group_vars/        # переменные для групп хостов
│   └── all.yml
├── roles/             # роли (по сервисам / компонентам)
│   └── k8s_upgrade/
├── playbooks/         # плейбуки
│   └── upgrade.yml    # основной сценарий обновления
└── README.md
