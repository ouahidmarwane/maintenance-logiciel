# C12 - Traçabilité du challenge Workflow entreprise

Objectif : appliquer un workflow entreprise réaliste avec deux features et ordre de merge.

## Branche principale
- master

## Branches de feature
- `feature/C12/a`
- `feature/C12/b`

## Actions réalisées
1. `git checkout master`
2. `git checkout -b feature/C12/a`
3. `echo "Feature A 1 - baseline" > C12/a1.txt`
4. `git add C12/a1.txt`
5. `git commit -m "C12: feature/a commit 1"`
6. `echo "Feature A 2 - added step" > C12/a2.txt`
7. `git add C12/a2.txt`
8. `git commit -m "C12: feature/a commit 2"`
9. `git checkout master`
10. `git checkout -b feature/C12/b`
11. `mkdir -Force C12` (si nécessaire)
12. `echo "Feature B 1 - baseline" > C12/b1.txt`
13. `git add C12/b1.txt`
14. `git commit -m "C12: feature/b commit 1"`
15. `echo "Feature B 2 - added step" > C12/b2.txt`
16. `git add C12/b2.txt`
17. `git commit -m "C12: feature/b commit 2"`
18. `git checkout master`
19. `git merge --no-ff feature/C12/a -m "C12: merge feature/a into master"`
20. `git merge --no-ff feature/C12/b -m "C12: merge feature/b into master"`

## Résultats
- `C12/a1.txt`, `C12/a2.txt`, `C12/b1.txt`, `C12/b2.txt` ajoutés à master via merges
- historique propre avec commits feature distincts puis merges

## Vérifications
- `git log --oneline --decorate --graph --all`
- `git status --short --branch`

---
Validé : 24/03/2026
