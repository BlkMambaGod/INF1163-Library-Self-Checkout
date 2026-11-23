# Structure du dépôt

Cette arborescence est **cible** : les fichiers et dossiers seront créés progressivement, et leur présence n'est pas garantie à ce stade.

```text
INF1163-Library-Self-Checkout/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── pull_request_template.md
├── data/
│   ├── schema/
│   ├── seed/
│   └── samples/
├── dist/
├── docs/
│   ├── requirements/
│   │   ├── use-cases/
│   │   │   └── UC-01-emprunter-documents.md
│   │   ├── business-rules.md
│   │   └── exception-scenarios.md
│   ├── uml/
│   │   ├── system-sequence/
│   │   │   └── DSS-emprunter-documents.pdf
│   │   ├── domain-model/
│   │   │   └── modele-domaine.pdf
│   │   └── class-diagrams/
│   │       └── diagramme-classes-affaires.pdf
│   ├── architecture/
│   │   └── architecture-overview.md
│   ├── guides/
│   │   ├── conventions.md
│   │   ├── git-workflow.md
│   │   ├── repository-structure.md
│   │   └── release-checklist.md
│   ├── reports/
│   │   ├── contributions.md
│   │   └── rapport-final.pdf
│   └── assets/
│       └── images/
├── modelio/
├── scripts/
├── src/
│   ├── main/java/
│   └── test/java/
├── .gitignore
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

## Rôle des dossiers

| Chemin | Usage |
|---|---|
| `.github/` | Templates GitHub et configuration de collaboration |
| `data/schema/` | Schéma SQLite |
| `data/seed/` | Données initiales |
| `data/samples/` | Jeux de données d'exemple |
| `dist/` | Livrables de distribution, dont le JAR final |
| `docs/requirements/` | Cas d'utilisation, règles métier et exceptions |
| `docs/uml/` | Exports des diagrammes UML |
| `docs/architecture/` | Architecture et décisions de conception |
| `docs/guides/` | Procédures et conventions du dépôt |
| `docs/reports/` | Contributions et rapports académiques |
| `docs/assets/images/` | Illustrations de la documentation |
| `modelio/` | Sources modifiables des diagrammes UML |
| `scripts/` | Automatisation et utilitaires |
| `src/main/java/` | Sources de l'application |
| `src/test/java/` | Tests automatisés |

Pour chaque diagramme, conserver les sources éditables dans `modelio/` et exporter le PDF correspondant dans `docs/uml/`. Mettre à jour les exports après modification. Ne pas versionner les compilations intermédiaires; réserver `dist/` aux livrables identifiables et validés.
