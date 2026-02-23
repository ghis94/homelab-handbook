# Home Assistant

## Objectif

Centraliser le pilotage de la maison (automations, présence, chauffage, alertes) et exposer une interface unique pour les usages quotidiens.

## Accès

- URL locale : `http://192.168.1.219:8123`
- Port : `8123`
- Type d’accès : interface web locale

> Sécurité : ne jamais stocker de token/API key en clair dans ce dépôt.

## Périmètre fonctionnel

- Gestion des équipements domotiques
- Scènes et automatisations
- Tableaux de bord par usage (maison, chauffage, énergie, présence)
- Notifications (mobile / bots / services internes)

## Structure recommandée

### Entités clés
- `sensor.*` : mesures (température, humidité, énergie, etc.)
- `switch.*` / `light.*` : actionneurs
- `climate.*` : chauffage / consignes
- `binary_sensor.*` : états booléens (présence, ouverture, mouvement)

### Automatisations (exemples)
- Chauffage selon plages horaires
- Alertes ouverture porte/fenêtre
- Rappels conditionnels (ex: météo, tâches récurrentes)

## Sauvegarde et maintenance

- Sauvegarde complète hebdomadaire
- Sauvegarde incrémentale quotidienne des changements de config
- Vérification après mise à jour :
  1. démarrage des intégrations critiques
  2. exécution d’une automatisation de test
  3. test des notifications

## Dépannage rapide

- Vérifier l’URL/port : `8123`
- Vérifier l’état des addons/intégrations critiques
- Contrôler les logs Home Assistant
- Vérifier la connectivité réseau locale

## À compléter

- [ ] Liste des intégrations actives
- [ ] Liste des automatisations en production
- [ ] Procédure de restauration détaillée
- [ ] Politique de rotation des sauvegardes
