# Guide de contribution

Ce guide décrit les règles de collaboration du projet INF1163. Les conventions de nommage figurent dans [conventions.md](docs/guides/conventions.md) et les commandes dans [git-workflow.md](docs/guides/git-workflow.md).

## Principes

- Utiliser le français pour les Issues, les Pull Requests et la documentation.
- Associer chaque tâche importante à une Issue avec un responsable, des objectifs, des livrables, des critères d'acceptation et les dépendances pertinentes.
- Effectuer le travail dans une branche dédiée, créée à partir de `main` à jour.
- Ne pas effectuer de développement directement sur `main`.
- Soumettre une Pull Request (PR) pour intégrer les changements et demander la révision d'au moins un autre membre.
- Vérifier les modifications et mettre à jour les documents concernés avant la fusion.
- Préférer **Squash and merge** lorsque plusieurs petits commits forment une seule modification logique; supprimer la branche de travail après fusion si elle n'est plus utile.

## Suivi des Issues

Labels utilisés : `documentation`, `uml`, `feature`, `bug`, `database`, `testing`, `priority:high`, `blocked`.

Statuts recommandés : **Todo**, **In Progress**, **In Review**, **Done**.

Mettre à jour les cases à cocher au fur et à mesure du travail. Mentionner les dépendances avec `#numéro`. Une PR qui termine une Issue peut contenir `Closes #12` (en remplaçant 12 par son vrai numéro).

## Pull Requests

Une PR doit décrire les changements, les fichiers touchés, les vérifications réalisées, les limites connues et l'Issue liée. Utiliser le modèle `.github/pull_request_template.md` lorsqu'il est présent.

### Vérification avant fusion

- [ ] Objectifs et critères d'acceptation de l'Issue satisfaits
- [ ] Fichiers placés aux bons emplacements et nommés correctement
- [ ] Documentation et diagrammes dépendants mis à jour
- [ ] Tests ou vérifications pertinents effectués
- [ ] Aucun fichier temporaire ou secret ajouté
- [ ] Au moins une révision par un autre membre

## Collaboration

Signaler rapidement les blocages et décisions qui affectent plusieurs membres. Éviter les modifications concurrentes d'un même fichier sans coordination. Ne pas écraser le travail d'autrui pour résoudre un conflit. Documenter les changements de conception importants et conserver `main` dans un état cohérent.

## Contributions

Les responsabilités ne se limitent pas aux premières tâches attribuées. Toute contribution nouvelle ou partagée doit être ajoutée au [registre des contributions](docs/reports/contributions.md), avec les références GitHub disponibles.
