# Chauffage Frisquet

## Contexte
- Chaudière Frisquet (projet de pilotage via Home Assistant/OpenFrisquet).
- Objectif: stabilité de température + réduction oscillations + supervision locale.

## Configuration
- Intégration Home Assistant avec réglages TPI (en cours d’itération terrain).
- Projet OpenFrisquet avec branche dédiée d’affichage OLED utile déjà implémentée.

## Problèmes connus
- Risque d’oscillation selon réglage TPI et inertie du logement.
- Réglages sensibles selon saison (demi-saison vs froid).

## Solutions / bonnes pratiques
- Modifier un seul paramètre à la fois (coeff/int/ext, fenêtre d’activation).
- Observer 24-48h avant nouvelle correction.
- Journaliser chaque changement avec date/effet.

## Historique
- 2026-02-23: affichage OLED utile intégré sur branche `feature/affichage-ecran` (`4fc363a`).
- 2026-03-04: fiche initiale créée dans le handbook.
