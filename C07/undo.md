# Git Restore vs Reset

## git restore
git restore allows you to discard changes in the working directory.
It restores a file to the last committed version without changing the commit history.

## git reset
git reset moves the HEAD pointer. Use --soft/--mixed/--hard to control staging and working tree. Branch A: use --soft/--mixed/--hard to control staged and working tree. Branch B: use --hard to reset working tree when necessary.

### Difference
- git restore: undo file changes safely
- git reset: modify staging or commit history
