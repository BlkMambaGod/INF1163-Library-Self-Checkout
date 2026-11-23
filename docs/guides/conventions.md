# Conventions du dépôt

## Langues

| Élément | Langue |
|---|---|
| README, documentation, Issues, Pull Requests, commits | Français |
| Noms de branches et dossiers techniques | Anglais |
| Classes, méthodes et variables Java | Anglais |
| Commentaires Java | Français |
| Concepts métier UML | Français |
| Identifiants UML correspondant au code | Anglais |

## Fichiers et dossiers

Choisir des noms descriptifs, sans espaces ni accents dans les chemins. Utiliser `kebab-case` pour les dossiers et les noms descriptifs, en conservant les acronymes établis.

Exemples : `docs/requirements/use-cases/`, `UC-01-emprunter-documents.md`, `DSS-emprunter-documents.pdf`, `modele-domaine.pdf`.

## Java

| Élément | Convention | Exemple |
|---|---|---|
| Classe ou interface | `PascalCase` | `LibraryUser`, `LoanRepository` |
| Méthode ou variable | `camelCase` | `validateUser()`, `bookCopy` |
| Constante | `UPPER_SNAKE_CASE` | `MAX_LOGIN_ATTEMPTS` |
| Package | Minuscules | `library.checkout` |

## Branches

| Préfixe | Utilisation | Exemple |
|---|---|---|
| `docs/` | Documentation et UML | `docs/use-case` |
| `feat/` | Fonctionnalité Java | `feat/user-authentication` |
| `fix/` | Correction | `fix/invalid-rfid` |
| `data/` | SQLite et données | `data/library-schema` |
| `test/` | Tests | `test/checkout-validation` |
| `chore/` | Maintenance | `chore/eclipse-setup` |
| `release/` | Livraison | `release/v1.0` |

Les branches de la première phase sont consignées dans [contributions.md](../reports/contributions.md).

## Commits

Convention adaptée de **Conventional Commits** : `type(portee): description`. La portée est facultative; la description est en français, concise et commence de préférence par un verbe à l'infinitif.

Types : `docs`, `feat`, `fix`, `data`, `test`, `chore`, `refactor`, `build`, `ci`, `style`.

```text
docs: définir les scénarios d'exception du prêt
docs(uml): ajouter le diagramme de séquence système
feat: implémenter l'authentification des usagers
fix: gérer les identifiants RFID invalides
data: créer le schéma SQLite de la bibliothèque
test: ajouter les tests de validation des emprunts
chore(git): configurer les fichiers ignorés
```

Un commit doit correspondre à une modification logique. Éviter les descriptions vagues et les fichiers générés inutiles.
