# C20 - Challenge final — Mini-projet Git & GitHub Ready

Objectif : prouver l'autonomie sur un workflow Git & GitHub complet.

## Actions réalisées

1. `git checkout master && git pull origin master`
2. `git checkout -b feature/C20`
3. Réécriture du `README.md` en version professionnelle (tableau des challenges, workflow, auteur)
4. Création du dossier `C20/` avec ce fichier de traçabilité
5. `git add README.md C20/tracabilite.md`
6. `git commit -m "C20: professional README + final challenge traceability"`
7. `git push origin feature/C20`
8. Ouverture d'une Pull Request sur GitHub :
   - Base : `master`
   - Compare : `feature/C20`
   - Titre : "C20: challenge final — repo professionnel"
   - Description : "Ajout d'un README professionnel et clôture du challenge final."
9. Merge de la PR sur GitHub

## Preuves du workflow complet

| Élément | Preuve |
|---------|--------|
| Branches | `feature/C18`, `feature/C20`, `feature/C15/A`, `feature/C15/B`... |
| PR + merge | C18 mergée via PR GitHub |
| Tags | `v1.0.0` annoté, visible sur GitHub |
| Historique lisible | Commits préfixés `CXX:` pour chaque challenge |
| README pro | Tableau complet + workflow documenté |

---
Validé : 11/06/2026
