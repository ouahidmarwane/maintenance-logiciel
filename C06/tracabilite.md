# C06 - Traçabilité (git log + git show)

## Objectif du challenge
- Faire 3 commits.
- Utiliser `git log` pour retrouver le hash du 1er commit.
- Utiliser `git show <hash>` sur ce commit et fournir preuve (capture ou note).

## Status actuel
- success 1ère partie (validation verte): 3 commits réalisés sur `feature/C06/log-show`.
- 2ème partie manquante: `git show` sur le hash du 1er commit n'avait pas été fourni dans le challenge initial.

## Correction appliquée (C06 désormais terminé)
1. `git log --oneline -- C06.txt` show:
   - `a72decc C06: first commit` (1er commit du challenge)
   - `5698911 C06: second commit`
   - `63f8e19 C06: third commit`
2. `git show --stat --pretty=fuller a72decc` (preuve enregistrée dans `C06/show-first-commit-explicit.txt`).
3. `git show --name-only a72decc` (preuve enregistrée dans `C06/show-first-commit-files-explicit.txt`).

## Fichiers de preuve générés
- `C06/show-first-commit.txt` (démarrage avant reset)
- `C06/show-first-commit-files.txt` (démarrage avant reset)
- `C06/show-first-commit-explicit.txt` (commit explicite) ✅
- `C06/show-first-commit-files-explicit.txt` (commit explicite) ✅

## Merges et publication
- Branche: `feature/C06/log-show` puis `master` avec merge.
- Commit final sur master: `a4bb27f C06: add git show proof`.
- Push to remote déjà fait.

---
Validé : 24/03/2026
