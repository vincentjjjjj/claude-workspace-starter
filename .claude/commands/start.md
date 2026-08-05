# /start

Démarrer une nouvelle session avec contexte complet.

## Séquence

1. Lis dans cet ordre : CLAUDE.md, CONTEXT.md, HISTORY.md
2. Si CONTEXT.md est vide ou quasi vide (première utilisation), pose 2-3 questions rapides à la volée pour amorcer le contexte :
   - Sur quoi tu comptes travailler dans ce workspace ?
   - C'est quoi l'objectif ?
   Remplis CONTEXT.md avec les réponses, ajoute une entrée dans HISTORY.md, puis enchaîne normalement. Pas d'interview formelle
3. Sinon, présente ce résumé :

```
Bonjour, contexte chargé. Voici où on en est :

**Projets / objectifs**
[Synthèse 2-3 lignes de CONTEXT.md]

**Dernière session**
[Résumé de la dernière entrée HISTORY.md]

Que veux-tu faire aujourd'hui ?
```

## Règles

- Ne lance aucune action, attends les instructions
- Ne redemande jamais l'identité ou le style de communication : c'est déjà dans le profil Claude
- Français, tutoiement, pas de tirets longs
