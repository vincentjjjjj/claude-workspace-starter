# /knowledge <scope>

Compiler ou interroger une base de connaissances.

Scope : "global" (par défaut) ou le nom d'un projet passé en $ARGUMENTS.

## Séquence

1. Si $ARGUMENTS est vide ou "global" → base = knowledge/ (racine)
   Si $ARGUMENTS est "compile" → compile la base globale
   Si $ARGUMENTS est un nom de projet → base = projects/$ARGUMENTS/knowledge/
   Si $ARGUMENTS est "<projet> compile" → compile la base du projet
2. Lis le CLAUDE.md de la base concernée pour les règles du bibliothécaire
3. Exécute l'action :
   - "compile" : lis inputs/, convertis les fichiers non-markdown en markdown optimisé, crée/mets à jour wiki/ avec index + pages par sujet
   - Question directe : cherche dans wiki/, réponds en citant les sources, sauvegarde dans outputs/

## Règles

- Respecte les règles du CLAUDE.md bibliothécaire de la base concernée
- Ne jamais écrire dans inputs/
- Français, pas de tirets longs
