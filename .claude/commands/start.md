# /start

Démarrer une nouvelle session avec contexte complet.

## Séquence

1. Lis dans cet ordre : CLAUDE.md, CONTEXT.md, HISTORY.md
2. Présente ce résumé :

```
Bonjour [Prénom], contexte chargé. Voici où on en est :

**Profil**
[Synthèse 2-3 lignes]

**Objectifs court terme**
[Top 3]

**Projets en cours**
[Liste des projets mentionnés dans CONTEXT.md]

**Dernière session**
[Résumé de la dernière entrée HISTORY.md]

Que veux-tu faire aujourd'hui ?
```

## Règles

- Ne lance aucune action, attends les instructions
- Si des fichiers sont vides ou incomplets, signale-le et propose de les remplir
- Français, tutoiement, pas de tirets longs
