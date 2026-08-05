# /uninstall

Supprimer toutes les traces de l'IA du workspace. Ne conserve que les dossiers inputs/, outputs/ et documents/ (tes documents et les synthèses générées).

## Ce qui sera supprimé

Fichiers racine :
- CLAUDE.md, CONTEXT.md, HISTORY.md, README.md

Base de connaissances :
- wiki/ (tout le contenu)

Configuration Claude :
- .claude/ (commandes et skills, tout le dossier)

## Ce qui sera conservé

- inputs/ (tes documents déposés)
- outputs/ (les synthèses générées)
- documents/ (tes fichiers de travail actifs)

## Séquence

1. Affiche la liste complète de ce qui sera supprimé et ce qui sera conservé (ci-dessus)

2. Première confirmation :
```
ATTENTION : cette action est irréversible.

As-tu fait un backup complet de ce dossier ? (oui/non)
```
Si non → refuse de continuer. Dis de faire le backup d'abord.

3. Deuxième confirmation (case-sensitive) :
```
Pour confirmer la suppression, tape exactement cette phrase :

SUPPRIMER MON ASSISTANT

Toute autre réponse annulera l'opération.
```
La réponse doit être exactement "SUPPRIMER MON ASSISTANT" (majuscules, sans guillemets). Toute variation → annulation.

4. Une fois les deux confirmations validées, exécute la suppression :
   - Supprime les fichiers racine (CLAUDE.md, CONTEXT.md, HISTORY.md, README.md)
   - Supprime tout le contenu de wiki/
   - Supprime .claude/ entièrement

5. Confirmation finale :
```
Désinstallation terminée.

Fichiers conservés :
- inputs/ ([X] fichiers)
- outputs/ ([X] fichiers)
- documents/ ([X] fichiers)

Toutes les traces de l'assistant ont été supprimées.
```

## Règles

- JAMAIS de suppression sans les deux confirmations validées
- Si l'utilisateur hésite ou dit "attends", annule immédiatement
- Français, pas de tirets longs
