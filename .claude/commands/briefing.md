# /briefing

Démarrer la journée avec une veille personnalisée en 30 secondes.

## Séquence

1. Charge silencieusement CLAUDE.md, CONTEXT.md, HISTORY.md (pas de résumé)
2. Lance la skill recherche-actualites-contextualisees avec : actualités IA + secteur d'activité
3. Si un connecteur calendrier est actif, récupère les événements du jour
4. Présente le tout :

```
Bonjour. Voici ton briefing du jour.

**Veille du jour**
[Résultat de la skill]

**Agenda** (si connecteur disponible)
[Événements]

**Focus suggéré**
[1 phrase basée sur veille + agenda + projets en cours]

Bonne journée. Je suis prêt.
```

## Règles

- Maximum 1 page. Si rien de pertinent, le dire plutôt que remplir avec du bruit
- Si quelque chose n'est pas disponible (pas de calendrier par ex.), passer sans mentionner
- Français, pas de tirets longs
