# /project <nom>

Charger le contexte d'un projet spécifique pour travailler dessus.

## Séquence

1. Vérifie que projects/$ARGUMENTS/ existe
2. Lis projects/$ARGUMENTS/CONTEXT.md et projects/$ARGUMENTS/HISTORY.md
3. Présente ce résumé :

```
Projet [$ARGUMENTS] chargé.

**Objectif**
[Objectif du projet]

**État actuel**
[Statut, avancement]

**Dernière session**
[Dernière entrée HISTORY.md du projet]

**Base de connaissances**
[Nombre de fichiers dans inputs/, pages dans wiki/]

Prêt à travailler sur [$ARGUMENTS]. Que fait-on ?
```

## Règles

- À partir de là, cherche d'abord dans projects/$ARGUMENTS/knowledge/, puis dans knowledge/ global si nécessaire
- Si le projet n'existe pas, liste les projets disponibles et propose de le créer via /new-project
- Français, tutoiement, pas de tirets longs
