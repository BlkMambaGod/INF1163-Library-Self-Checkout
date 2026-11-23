# INF1163 — Library Self-Checkout

**Simulation d'une borne de prêt en libre-service pour une bibliothèque.**

Projet du cours **INF1163 — Modélisation et conception orientée objet**, Université du Québec en Outaouais (UQO).

## Présentation

Le projet porte sur l'analyse, la modélisation UML, la conception et le développement d'un système de prêt en libre-service. Les fonctionnalités prévues comprennent l'authentification des usagers, la validation des emprunts, l'identification d'exemplaires par RFID simulée, l'enregistrement des transactions, le traitement des exceptions et la gestion des reçus.

## Technologies et outils

Java · SQLite · Modelio · Eclipse · Git et GitHub · Markdown

## Organisation du dépôt

| Répertoire | Contenu |
|---|---|
| [`docs/`](docs/) | Exigences, diagrammes UML, architecture, guides et rapports |
| `modelio/` | Sources modifiables des modèles UML |
| `src/` | Code Java et tests |
| `data/` | Schémas et jeux de données SQLite |
| `scripts/` | Scripts utilitaires |
| `dist/` | Livrables de distribution |
| `.github/` | Modèles d'Issues et de Pull Requests |

Consulter [la structure détaillée](docs/guides/repository-structure.md) pour l'arborescence cible et les règles de rangement.

## Documentation

- [Contribuer au projet](CONTRIBUTING.md)
- [Conventions de nommage et de commits](docs/guides/conventions.md)
- [Procédure Git](docs/guides/git-workflow.md)
- [Architecture et cohérence des artefacts](docs/architecture/architecture-overview.md)
- [Contributions de l'équipe](docs/reports/contributions.md)
- [Vérifications avant livraison](docs/guides/release-checklist.md)

Les spécifications fonctionnelles se trouvent dans `docs/requirements/` et les diagrammes exportés dans `docs/uml/`, au fur et à mesure de leur production.

## Équipe

William Youkna · Marieme Mbacke · Wilsan Waberi · Aziz Lam

Les responsabilités et réalisations de chaque membre sont consignées dans le [suivi des contributions](docs/reports/contributions.md).

## Licence

Projet distribué sous licence MIT. Voir [LICENSE](LICENSE).

> **État du projet :** certains répertoires, documents et livrables décrits dans les guides constituent la structure cible et seront ajoutés progressivement. Les instructions d'installation et d'exécution seront précisées lorsque la configuration de construction sera stabilisée.
