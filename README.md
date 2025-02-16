# Ansible Playbook zur Installation von Pterodactyl Gameserver auf Ubuntu Server >= 24.02
Dieses Ansible-Playbook installiert den [Pterodactyl Gameserver](https://pterodactyl.io/) bestehend aus Panel und Wings. Die ausgeführten Tasks hangeln sich hierbei an der generellen [Installationsanleintung](https://pterodactyl.io/panel/1.0/getting_started.html) für _Panel_ und _Winge_ entlang.

Ich gehe davon aus, dass es auf einem frish installierten Ubuntu Server ausgeführt wird. Falls nicht, könnte es ggf. Seiteneffekte geben und möglicherweise gehen Dinge kaputt.

__WARNUNG__: Benutzung des Playbooks auf eigene Gefahr!

## Installation der notwenidgen Pakete
Zum Starten des Playbooks werden nur ein paar Pakete nachinstalliert, alles weitere geschieht in den jeweiligen TASKS.

```bash
apt update
apt upgrade -y
apt install -y python3 ansible git
```

## Ausführen des Playbooks
Die Folgenden Punkte beschreiben die Ausführung des Playbook. Wir gehen davon aus, dass Dein User __sudo__ verwenden darf. Du wirst nach dem Start des Playbooks aufgefürdert, dein Passwort einzugeben.

### Clonen des Repositories
    wget -qO- https://github.com/Ichnafi/pterodactyl-ansible-installer/releases/latest/download/pterodactyl-ansible-installer.tar.gz | tar xzf -

### Starten des Playbooks

1. Wechsle in das geclonte Verzeichnis
```bash
cd ptero-install
```

2. Starte das Playbook und beantworte die Fragen

```bash
ansible-playbook playbook_ptrerodactyl.yml
```

3. Daumen drücken
