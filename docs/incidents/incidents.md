# Incidents & leçons

## Objectif
Centraliser les incidents techniques pour éviter les récidives.

## Entrées récentes

### 2026-03 — Wedding Planner: différence de version affichée
- Symptôme: modifs non visibles après update.
- Cause probable: image/conteneur pas rebuild + cache navigateur.
- Résolution:
  1. `git pull`
  2. `docker compose down`
  3. `docker compose build --no-cache`
  4. `docker compose up -d`
  5. Hard refresh navigateur (`Ctrl+F5`)
- Prévention: inclure cette séquence dans la doc d’exploitation.

### 2026-03 — UX admin ambiguë (clic invité)
- Symptôme: clic invité retirait de la table au lieu d’ouvrir la fiche.
- Résolution: clic nom => fiche; action destructive isolée sur bouton/croix.
- Prévention: éviter les actions destructives implicites au clic global.
