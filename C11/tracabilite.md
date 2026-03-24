# C11 - Traçabilité du challenge Merge Conflict

Objectif: créer et résoudre un conflit Git sur le même fichier dans deux branches, puis merger sur master.

## Contexte
- Fichier ciblé: `C07/undo.md`
- Branche de base: `master`
- branches de travail: `feature/c11-conflict` (A), `feature/c11-conflict-b` (B)

## Actions réalisées
1. `git checkout -b feature/c11-conflict` depuis `master`
2. Modification A sur `C07/undo.md` (ligne `## git reset`)
3. `git commit -m "C11: branch A update on git reset description"`
4. `git checkout master`
5. `git checkout -b feature/c11-conflict-b`
6. Modification B sur le même point de `C07/undo.md`
7. `git commit -m "C11: branch B update on git reset description"`
8. `git checkout feature/c11-conflict`
9. `git merge feature/c11-conflict-b` -> conflit de contenu sur `C07/undo.md`
10. Résolution manuelle combinée du conflit dans `C07/undo.md`
11. `git add C07/undo.md`
12. `git commit -m "C11: resolve merge conflict for undo.md"`
13. `git checkout master`
14. `git merge --no-ff feature/c11-conflict -m "C11: merge resolved conflict into master"`

## Historique de commits (fichier `C07/undo.md`)
- `3059af7` (feature/c11-conflict) C11: resolve merge conflict for undo.md
- `894ce85` (feature/c11-conflict-b) C11: branch B update on git reset description
- `b7d97e0` C11: branch A update on git reset description
- `bc2cd2e` docs: explain git restore vs git reset

## Contenu final de `C07/undo.md`
- `## git reset` enrichi avec les explications issues des deux branches
- section `### Difference` conservée

## Préparation pour validation
- Le repo est sur `master` avec le merge final effectué
- Ajout de ce fichier de traçabilité pour examen
- Commandes utiles pour revue du correctif:
  - `git status --short --branch`
  - `git log --oneline --decorate --all -- C07/undo.md`
  - `git diff origin/master..master`

---

Valide: 24 mars 2026
