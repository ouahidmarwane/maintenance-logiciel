# C13 - Traçabilité du challenge git stash

Objectif : sauvegarder temporairement un travail en cours, changer de branche puis réappliquer la sauvegarde et committer.

## Etat initial
- Branche : `master`
- Fichier : `C13.txt`

## Actions réalisées
1. `git checkout master`
2. `git pull origin master`
3. `echo "C13 initial file" > C13.txt`
4. `git add C13.txt`
5. `git commit -m "C13: create base file"`
6. Modification WIP : `echo "WIP change on C13" >> C13.txt`
7. `git status --short` montre `M C13.txt`
8. `git stash push -m "C13: WIP stash"`
9. `git checkout -b feature/C13/temp`
10. `echo "temp change branch" >> C13.txt`
11. `git add C13.txt`
12. `git commit -m "C13: temp branch commit"`
13. `git checkout master`
14. `git stash list` confirme stash présent
15. `git stash apply stash@{0}`
16. `git status --short` montre `M C13.txt`
17. `git add C13.txt`
18. `git commit -m "C13: apply stash and finalize"`

## Résultats
- branche `master` contient:
  - `d895b84` C13: create base file
  - `f0aa469` C13: apply stash and finalize
- fichier `C13.txt` contient `C13 initial file`, ligne WIP et lignes temp (fusion)

## Vérifications utiles
- `git log --oneline --decorate --graph -n 10`
- `git status --short --branch`
- `git stash list` (après `apply`, stash reste tant que `stash drop` non lancé)

---
Validé : 24/03/2026
