# Stack recommandée (pragmatique)

## Recommandation principale

**Obsidian + Git + OpenWebUI + LLM local**

## Rôle de chaque brique

- **Obsidian**: édition rapide Markdown, navigation et liens
- **Git**: historique, rollback, traçabilité
- **OpenWebUI**: interface IA locale pour interroger la base
- **LLM local**: réponses contextualisées sur tes docs

## Alternatives

### Option web collaborative
- **Wiki.js** (Docker)
- utile si plusieurs personnes modifient

### Option docs technique
- **Docusaurus**
- utile pour docs versionnées style projet open-source

## Cas d’usage IA ciblés

Exemples de requêtes utiles:

- "Pourquoi le thermostat salon oscille ?"
- "Quels réglages TPI actifs sur chauffage Frisquet ?"
- "Dernier incident Frigate + action prise ?"
- "Procédure de reprise Proxmox après reboot ?"

## Plan de déploiement minimal

1. Créer le repo `ghis-knowledge-base`
2. Initialiser dossiers (homelab/ha/ia/sncf/famille/incidents)
3. Ajouter templates de page
4. Commiter les docs existantes
5. Brancher OpenWebUI sur ce corpus

## Résultat attendu

- documentation centralisée
- mémoire technique durable
- aide IA fiable basée sur tes vraies données
