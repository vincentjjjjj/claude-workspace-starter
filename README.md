# Claude Workspace Starter

Un workspace prêt à l'emploi pour transformer Claude (Code ou Cowork) en assistant personnel avec mémoire persistante et base de connaissances.

## Ce que ça fait

- **Contexte qui se construit tout seul** : pas d'interview obligatoire, Claude amorce le contexte à la volée dès la première session
- **Base de connaissances intelligente** : déposez n'importe quel fichier (Word, Excel, PDF, CSV...), Claude le convertit en markdown optimisé et l'organise automatiquement
- **Contexte évolutif** : Claude détecte les changements importants et propose de mettre à jour vos fichiers de contexte
- **Veille personnalisée** : briefing matinal filtré selon vos projets et objectifs

## Installation

### Prérequis

- [Claude Desktop](https://claude.ai/download) avec un abonnement Pro, Team ou Enterprise
- Ou [Claude Code](https://docs.claude.com/en/docs/claude-code) (CLI)

### Démarrage rapide

1. Clonez ce repo (remplacez `mon-assistant` par le nom de dossier que vous voulez) :
```bash
git clone https://github.com/vincentjjjjj/claude-workspace-starter.git mon-assistant
```

2. Ouvrez le dossier dans Claude Cowork (ou `cd mon-assistant` avec Claude Code)

3. Dites simplement `/start`. Claude charge CLAUDE.md et CONTEXT.md, et comme c'est la première fois, il vous posera 2-3 questions rapides sur ce workspace (sur quoi vous travaillez, quel est l'objectif). Pas d'interview formelle.

Votre profil, votre style de communication et vos préférences générales n'ont pas leur place ici : configurez-les une fois dans votre profil Claude (Réglages > Profil), ils s'appliqueront à toutes vos sessions et tous vos workspaces.

### Désinstallation

Pour supprimer toutes les traces de l'IA et ne garder que vos documents (inputs/ et outputs/) :
```
/uninstall
```
Une double confirmation vous sera demandée avant toute suppression.

## Structure

```
.
├── CLAUDE.md              # Fondation (chargé à chaque session)
├── CONTEXT.md             # Vos projets et objectifs pour ce workspace
├── HISTORY.md             # Journal des sessions
├── inputs/                # Déposez vos fichiers ici
├── wiki/                  # Base de connaissances organisée (markdown)
├── outputs/               # Synthèses générées
└── .claude/
    ├── commands/          # Slash commands
    └── skills/            # Skills personnalisées
```

## Commandes

| Commande | Description |
|----------|-------------|
| `/start` | Charger le contexte en début de session (amorce CONTEXT.md si vide) |
| `/update-context` | Mettre à jour le contexte après un changement |
| `/briefing` | Veille matinale personnalisée |
| `/input compile` | Compiler la base de connaissances |
| `/uninstall` | Supprimer toutes les traces de l'IA (garde inputs/ et outputs/) |

## Base de connaissances

Pour alimenter votre base :
1. Déposez vos fichiers dans `inputs/` (Word, Excel, PDF, CSV, markdown, texte...)
2. Dites `/input compile`
3. Claude lit tout, convertit en markdown optimisé, et organise dans `wiki/`

Les fichiers originaux restent intacts dans `inputs/`. Le `wiki/` est une version markdown pure, optimisée pour minimiser la consommation de tokens.

## Pourquoi ce starter ?

Claude est puissant, mais sans contexte persistant il repart de zéro à chaque session. Ce workspace résout ça, sans imposer de cérémonie d'installation :

- **Mémoire** : Claude sait sur quoi vous travaillez et où vous en êtes dans ce workspace
- **Zéro friction** : pas d'interview à rallonge, le contexte s'amorce dès que vous commencez à travailler
- **Séparation nette** : qui vous êtes reste dans votre profil Claude (une fois pour toutes) ; ce que vous faites ici reste dans ce workspace
- **Efficacité** : les documents sont convertis en markdown pour minimiser les tokens consommés

## Inspirations

Ce projet fusionne deux approches complémentaires :
- L'architecture base de connaissances (inputs/wiki/outputs) de [Décuplez votre Claude](https://www.youtube.com/@yassine-sdiri)
- Le système de contexte évolutif et commandes du [Jarvis Starter Kit](https://skool.com/intelligenceartificielle)

## Licence

MIT
