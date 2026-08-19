# Ansible K8s Upgrade Playbook

Этот репозиторий содержит плейбуки для обновления Kubernetes-кластера с помощью Ansible.

## 📂 Структура проекта

```bash
ansible-k8s-upgrade/
├── ansible.cfg
├── inventories/
│   ├── inventory.ini
│   └── group_vars/
│       └── all.yml
├── playbooks/
│   ├── upgrade_containerd.yml
│   └── k8s-upgrade-1.36.yml
└── README.md
```

## Предварительные условия

- Сделан и проверен backup etcd.
- На control-plane нодах доступен рабочий `kubectl` и kubeconfig.
- CNI, CSI и другие addons совместимы с целевой версией Kubernetes.
- Все ноды используют cgroup v2 и containerd 2.x, если эти проверки включены.
- В `pkgs.k8s.io` доступна версия `k8s_package_version`.

`kubectl drain` удаляет данные `emptyDir`. PodDisruptionBudget соблюдается по
умолчанию; `drain_disable_eviction=true` допустим только как осознанное аварийное исключение.
