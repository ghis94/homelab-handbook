# Knowledge Base — méthode recommandée

## Objectif

Construire une base de connaissance **structurée, recherchable, exploitable par IA et auto-hébergée**.

## Les 4 critères à respecter

- 📂 **Structurée**
- 🔎 **Recherchable rapidement**
- 🤖 **Exploitable par IA**
- 💾 **Hébergée chez toi**

## Méthode principale: Markdown + Git

La base est stockée en Markdown, versionnée dans Git.

### Arborescence conseillée

```text
ghis-knowledge-base/
│
├── homelab/
│   ├── proxmox.md
│   ├── network.md
│   └── storage.md
│
├── home-assistant/
│   ├── chauffage-frisquet.md
│   ├── thermostats-tpi.md
│   └── automatisations.md
│
├── ia/
│   ├── frigate.md
│   ├── coral.md
│   └── llm.md
│
├── sncf/
│   ├── notices.md
│   ├── estimation.md
│   └── planning.md
│
├── famille/
│   ├── maison.md
│   └── mariage.md
│
└── incidents/
    └── incidents.md
```

## Format standard d’une fiche

Chaque page doit contenir:

1. **Contexte**
2. **Configuration**
3. **Problèmes connus**
4. **Solutions**
5. **Historique**

### Template rapide

```markdown
# <Sujet>

## Contexte

## Configuration

## Problèmes connus

## Solutions

## Historique
- YYYY-MM-DD: ...
```

## Exemple — chauffage Frisquet

```markdown
# Chauffage Frisquet

## Contexte
Chaudière: Frisquet Prestige Condensation 32

## Configuration
Loi d'eau: 1.2
Départ min: 35°C

## Problèmes connus
- Sous-chauffe possible de 0.2°C selon météo

## Solutions
- Ajuster coeff_ext de 0.040 à 0.042 en période froide

## Historique
- 2026-02-16: sous-chauffe observée
```

## Intégration dans ton homelab

Option simple:

- Dossier partagé sur NAS: `/knowledge-base`
- Édition locale + sync Git

Option dédiée:

- VM documentation (Docker)
- Wiki.js / outils docs + Git

## Pourquoi c’est efficace

- lisible par humain
- diff/versioning clair
- audit des décisions
- base parfaite pour un agent IA/RAG
