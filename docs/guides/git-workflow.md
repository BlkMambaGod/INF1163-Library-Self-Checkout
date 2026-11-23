# Procédure Git

Voir [CONTRIBUTING.md](../../CONTRIBUTING.md) pour les règles de révision et [conventions.md](conventions.md) pour les noms de branches et de commits.

## Démarrer une tâche

```bash
git switch main
git pull origin main
git switch -c feat/user-authentication
```

Si la branche existe déjà localement :

```bash
git switch docs/use-case
```

Si elle existe seulement sur le dépôt distant :

```bash
git fetch origin
git switch --track origin/docs/use-case
```

## Vérifier, enregistrer et publier

```bash
git status
git diff
git add chemin/du/fichier
git commit -m "feat: implémenter la validation du NIP"
git push -u origin feat/user-authentication
```

Pour les publications suivantes, `git push` suffit lorsque la branche suit déjà une branche distante. Préférer l'ajout ciblé (`git add chemin/du/fichier`) afin d'éviter de committer des fichiers sans rapport.

## Soumettre et terminer

Ouvrir une Pull Request de la branche de travail vers `main`, renseigner le modèle et demander une révision. Après la fusion :

```bash
git switch main
git pull origin main
```

## Conflits

Éviter les modifications simultanées des mêmes fichiers et synchroniser régulièrement. En cas de conflit, inspecter les fichiers concernés, comparer les versions, résoudre les sections conflictuelles, vérifier le résultat, puis terminer l'opération Git en cours selon qu'il s'agit d'une fusion ou d'un rebase. Demander une révision si la résolution est incertaine.

## Dossiers vides et fichiers ignorés

Git ne suit pas les dossiers vides. Un fichier `.gitkeep` peut préserver un dossier dans le dépôt, puis être supprimé lorsque de vrais fichiers suivis y sont ajoutés.

Le fichier `.gitignore` exclut notamment les fichiers temporaires, journaux, compilations intermédiaires et données locales non destinées au dépôt. Ne pas exclure les configurations nécessaires à l'équipe sans concertation.
