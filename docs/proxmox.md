# Proxmox

## Objectif

Documenter l’hôte de virtualisation Proxmox VE : accès, règles d’exploitation, sauvegardes, sécurité et dépannage.

## Accès

- URL (à compléter) : `https://<ip-ou-dns-proxmox>:8006`
- Port interface web : `8006`
- Protocole : HTTPS

## Utilisateur dédié

Un utilisateur dédié a été créé (info fournie par ghis).

À documenter ici (sans mot de passe) :
- identifiant utilisateur : `à compléter`
- realm : `pam` / `pve` / autre (`à compléter`)
- rôle(x) attribué(s) : `à compléter`
- périmètre des permissions (Datacenter, nœud, pool, VM/CT) : `à compléter`

> Ne jamais stocker de mot de passe, token secret, clé privée, ou backup key en clair dans ce dépôt.

## Standard d’exploitation

### VM / CT
- Convention de nommage : `service-env-numero` (ex: `ha-prod-01`)
- Éviter les changements hors fenêtre de maintenance
- Documenter toute création/suppression de VM/CT

### Réseau
- Documenter bridges (`vmbr*`) et VLAN utilisés
- Indiquer les plages IP réservées par type de service

### Stockage
- Lister les stockages (local-lvm, NFS, ZFS, etc.)
- Renseigner la stratégie de snapshots et rétention

## Sauvegardes

- Cible de backup : `à compléter`
- Politique recommandée :
  - quotidien incrémental
  - hebdomadaire complet
  - test de restauration mensuel

## Sécurité minimale

- Compte root réservé à l’admin seulement
- Utilisateur dédié avec privilèges minimaux nécessaires
- Mises à jour régulières de Proxmox VE
- MFA activée si possible
- Accès web limité au LAN/VPN

## Dépannage rapide

- Vérifier disponibilité de l’interface `:8006`
- Vérifier état des services Proxmox (`pveproxy`, `pvedaemon`, `pvestatd`)
- Vérifier espace disque (cause fréquente d’échecs backup/VM)
- Vérifier logs système + tâches Proxmox

## À compléter

- [ ] URL/IP réelle du serveur Proxmox
- [ ] Nom exact de l’utilisateur dédié créé
- [ ] Rôles/ACL exacts appliqués
- [ ] Politique de backup réellement en place
