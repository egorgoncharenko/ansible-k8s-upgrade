# Ansible K8s Upgrade Playbook

Этот репозиторий содержит плейбуки для обновления Kubernetes-кластера с помощью Ansible.

## 📂 Структура проекта

```bash
ansible-k8s-upgrade/
├── inventories/       # инвентори (hosts, группы)
│   └── inventory.ini
│     
├── group_vars/        # переменные для групп хостов
│   └── all.yml
├
├── playbooks/         # плейбуки
│   └── upgrade.yml    # основной сценарий обновления
└── README.md
