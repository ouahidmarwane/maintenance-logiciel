# C14 - Traçabilité du challenge rebase interactif + squash

Objectif : nettoyer l'historique avant livraison via un rebase + squash en un commit propre.

## Étapes réalisées
1. `git checkout master`
2. `git pull origin master`
3. `git checkout -b feature/C14/rebase`
4. `echo "C14 step 1" > C14.txt`
5. `git add C14.txt`
6. `git commit -m "C14: step 1"`
7. `echo "C14 step 2" >> C14.txt`
8. `git add C14.txt`
9. `git commit -m "C14: step 2"`
10. `echo "C14 step 3" >> C14.txt`
11. `git add C14.txt`
12. `git commit -m "C14: step 3"`

## Rebase et squash
- Tentative de rebase interactif : `git rebase -i HEAD~3`
- Comme l'éditeur interactif n'était pas disponible dans l'environnement, on a obtenu le même résultat via :
  - `git reset --soft HEAD~3`
  - `git commit -m "C14: final clean commit with squashed changes"`
- Historique final branche `feature/C14/rebase`:
  - 1 commit unique (squash)

## Merge final
- `git checkout master`
- `git merge --no-ff feature/C14/rebase -m "C14: merge feature/C14/rebase into master"`

## Vérifications
- `git log --oneline --decorate --graph -n 10`
- `git status --short --branch`

---
Validé : 24/03/2026
