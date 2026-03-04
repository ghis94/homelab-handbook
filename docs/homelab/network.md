# Réseau homelab

## Contexte
- Réseau local principal avec services auto-hébergés (docs, domotique, apps métiers perso).
- Objectif: accès stable + segmentation raisonnable + maintenance simple.

## Configuration
- Services exposés localement sur LAN selon besoins (ex: docs MkDocs).
- Reverse proxy utilisé selon les apps (Nginx Proxy Manager dans certains usages).

## Problèmes connus
- Risque de confusion entre environnements local/dev/prod.
- Incohérences possibles si cache navigateur + images Docker non rebuild.

## Solutions
- Standardiser les procédures `git pull + rebuild + hard refresh`.
- Documenter chaque service avec URL/port/owner.

## Historique
- 2026-03-04: fiche initiale créée dans le handbook.
