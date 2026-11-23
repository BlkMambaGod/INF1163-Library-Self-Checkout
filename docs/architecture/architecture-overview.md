# Vue d'ensemble de la conception

Ce document décrit actuellement **la cohérence attendue entre les artefacts**. Il ne prétend pas définir une architecture logicielle finale déjà validée.

## Enchaînement des artefacts

```text
Exigences et règles métier
          ↓
Cas d'utilisation détaillé
          ↓
Diagramme de séquence système (DSS)
          ↓
Modèle du domaine
          ↓
Diagramme de classes de la couche affaires
          ↓
Implémentation Java et intégration SQLite
          ↓
Tests et validation
```

Ces activités peuvent se chevaucher. Le diagramme de séquence système représente les interactions externes avec le système; le modèle du domaine décrit les concepts métier; le diagramme de classes précise les responsabilités et relations des classes de conception.

Toute modification substantielle des exigences doit déclencher une vérification des documents, diagrammes, classes et tests concernés.

## Artefacts de référence

- `docs/requirements/use-cases/` : cas d'utilisation détaillés.
- `docs/requirements/business-rules.md` : règles métier.
- `docs/requirements/exception-scenarios.md` : exceptions.
- `docs/uml/system-sequence/` : DSS exportés.
- `docs/uml/domain-model/` : modèle du domaine exporté.
- `docs/uml/class-diagrams/` : diagrammes de classes exportés.
- `modelio/` : sources éditables des modèles.

## À compléter lors de la conception

Les choix d'architecture Java, les frontières entre couches, les dépendances, l'accès aux données et les décisions de conception devront être décrits ici lorsqu'ils auront été établis par l'équipe.
