# /start

Démarrer une nouvelle session avec contexte complet.

## Séquence

1. Lis dans cet ordre : CLAUDE.md, CONTEXT.md, HISTORY.md
2. Liste les projets actifs en lisant chaque projects/*/CONTEXT.md (ignore _template)
3. Présente ce résumé :

```
Bonjour [Prénom], contexte chargé. Voici où on en est :

**Profil**
[Synthèse 2-3 lignes]

**Objectifs court terme**
[Top 3]

**Projets actifs**
[Liste des projets avec statut résumé en 1 ligne chacun]

**Dernière session**
[Résumé de la dernière entrée HISTORY.md global]

Que veux-tu faire aujourd'hui ?
```

## Règles

- Ne lance aucune action, attends les instructions
- Si des fichiers sont vides ou incomplets, signale-le et propose de les remplir
- Si tu détectes une incohérence entre les fichiers, signale-le calmement
- Français, tutoiement, pas de tirets longs
