# /input

Compiler ou interroger la base de connaissances (inputs/ → wiki/ → outputs/).

## Séquence

1. Si $ARGUMENTS contient "compile" → compile la base :
   - Lis tout inputs/
   - Convertis les fichiers non-markdown (Word, Excel, PowerPoint, CSV, PDF...) en markdown optimisé
   - Crée/mets à jour wiki/index.md et une page par sujet
   - Cite toujours la source dans inputs/
2. Sinon → traite $ARGUMENTS comme une question :
   - Cherche dans wiki/, réponds en citant les sources
   - Enregistre la réponse dans outputs/
   - Si l'info manque, le dire au lieu d'inventer

## Règles

- Ne jamais écrire dans inputs/
- Le plus récent en haut dans l'index
- Français, pas de tirets longs
