# homelab-handbook

Documentation centralisée du homelab (infrastructure, services, procédures et exploitation quotidienne).

## Description du projet

Ce dépôt sert de handbook technique pour garder une source unique, claire et versionnée de l’environnement homelab.

Contenu visé :
- architecture (machines, réseau, VM/containers)
- services principaux (ex: Proxmox, Home Assistant, chaudière, etc.)
- procédures d’installation, maintenance, sauvegarde et dépannage

## Accès à la documentation

Le site de documentation est généré avec **MkDocs**.

### En local

```bash
mkdocs serve
```

Par défaut, la documentation est accessible sur :
- `http://127.0.0.1:8000`
- **Port : `8000`**

### Build statique

```bash
mkdocs build
```

Les fichiers générés sont placés dans le dossier `site/`.
