# /knowledge

Compiler ou interroger la base de connaissances.

## Séquence

1. Lis knowledge/CLAUDE.md pour les règles du bibliothécaire
2. Si $ARGUMENTS contient "compile" → compile la base
3. Sinon → traite $ARGUMENTS comme une question

Actions :
- "compile" : lis inputs/, convertis les fichiers non-markdown en markdown optimisé, crée/mets à jour wiki/ avec index + pages par sujet
- Question directe : cherche dans wiki/, réponds en citant les sources, sauvegarde dans outputs/

## Règles

- Respecte les règles du CLAUDE.md bibliothécaire
- Ne jamais écrire dans inputs/
- Français, pas de tirets longs
