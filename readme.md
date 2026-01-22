# Ansible Project

Ce projet contient une collection de playbooks Ansible pour la gestion de l'infrastructure.

## Prérequis

Avant de commencer, assurez-vous que vous disposez des éléments suivants :

- **Git** - pour cloner le repository
- **Python 3.12.3** - pour exécuter Ansible
- **pip** - gestionnaire de paquets Python
- **virtualenv** - pour créer un environnement virtuel isolé

## Installation

### 1. Cloner le repository

```bash
git clone https://github.com/herkay/tp-ansible-ais-04.git
cd tp-ansible-ais-04
```

### 2. Créer et activer l'environnement virtuel

```bash
# Créer l'environnement virtuel
python3 -m venv venv

# Activer l'environnement virtuel
# Sur Linux/macOS :
source venv/bin/activate

# Sur Windows :
# venv\Scripts\activate
```

### 3. Installer Ansible

Une fois l'environnement virtuel activé, installez Ansible :

```bash
pip3 install ansible
```

## Exécution du Playbook

Une fois que l'environnement virtuel est activé, exécutez le playbook principal :

```bash
ansible-playbook -i inventory.yml ./playbooks/site.yml -k -K
```

### Explications des options

- `-i inventory.yml` - Spécifie le fichier d'inventaire
- `./playbooks/site.yml` - Chemin vers le playbook à exécuter
- `-k` - Demande le mot de passe SSH pour se connecter aux hosts
- `-K` - Demande le mot de passe sudo pour l'escalade de privilèges

### Étapes complètes pour démarrer

```bash
# 1. Cloner le repository
git clone https://github.com/herkay/tp-ansible-ais-04.git
cd tp-ansible-ais-04

# 2. Créer et activer l'environnement virtuel
python3 -m venv venv
source venv/bin/activate

# 3. Installer Ansible
pip install ansible

# 4. Exécuter le playbook
ansible-playbook -i inventory.yml ./playbooks/site.yml -k -K
```

## Structure du projet

```
tp-ansible-ais-04/
├── ansible.cfg           # Configuration Ansible
├── inventory.yml         # Inventaire des hosts
├── readme.md            # Ce fichier
├── group_vars/          # Variables de groupe
│   └── linux.yml        # Variables pour le groupe linux
└── playbooks/           # Playbooks Ansible
    ├── site.yml         # Playbook principal
    ├── packages.yml     # Gestion des paquets
    ├── security.yml     # Configuration de sécurité
    └── users.yml        # Gestion des utilisateurs
```

## Support

Pour plus d'informations sur Ansible, consultez la [documentation officielle](https://docs.ansible.com/).
