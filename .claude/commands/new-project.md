# /new-project <nom>

Créer un nouveau projet à partir du template.

## Séquence

1. Copie le contenu de projects/_template/ dans projects/$ARGUMENTS/
2. Lance une mini-interview (5 questions max) :
   - C'est quoi ce projet en une phrase ?
   - Quel est l'objectif principal ?
   - Quelle est la stack/les outils utilisés ? (si pertinent)
   - Quel est l'état actuel ? (idée, en cours, maintenance)
   - Deadline ou horizon de temps ?
3. Remplis projects/$ARGUMENTS/CONTEXT.md avec les réponses
4. Ajoute la première entrée dans projects/$ARGUMENTS/HISTORY.md
5. Ajoute le projet dans la liste des projets actifs de CONTEXT.md (racine)
6. Confirme :

```
Projet [$ARGUMENTS] créé et configuré.
Lance "/project $ARGUMENTS" pour commencer à travailler dessus.
```

## Règles

- Ne crée jamais un projet sans au moins un nom et une description d'une ligne
- Français, pas de tirets longs
