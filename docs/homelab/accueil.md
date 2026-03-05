# Homelab perso — Accueil

## Objectif
Cette section centralise uniquement le homelab perso (infra + domotique + exploitation), sans contenu SNCF/pro.

## Inventaire actuel (connu)
- Home Assistant: `http://192.168.1.219:8123`
- PC principal LAN: `192.168.1.201` (Arch), user `ghis`
- Caméras connues (skills): `jardin`, `sous-sol`
- Repo docs: `homelab-handbook`

## Procédures rapides

### Mettre à jour un service Docker
1. `git pull`
2. `docker compose down`
3. `docker compose build --no-cache`
4. `docker compose up -d`
5. Hard refresh navigateur (`Ctrl+F5`)

### Incident: “mes modifs ne s’affichent pas”
- Vérifier commit local (`git rev-parse --short HEAD`)
- Vérifier container up (`docker compose ps`)
- Vérifier logs (`docker compose logs --tail=100`)

## Liens internes
- [Proxmox](../proxmox.md)
- [Réseau](network.md)
- [Home Assistant](../home-assistant.md)
- [Chauffage Frisquet](../home-assistant/chauffage-frisquet.md)
- [Frigate](../ia/frigate.md)
- [Incidents](../incidents/incidents.md)
