# Claude Workspace Starter

Un workspace prêt à l'emploi pour transformer Claude (Code ou Cowork) en assistant personnel avec mémoire persistante et base de connaissances.

## Ce que ça fait

- **Un assistant qui vous connaît** : interview interactive qui configure Claude selon votre profil, vos objectifs et votre style de communication
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

3. Dites à Claude :
```
Installe mon assistant en suivant le fichier INSTALLER.md
```

4. Répondez aux 8 questions. Claude configure tout automatiquement.

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
├── CONTEXT.md             # Votre profil et objectifs
├── HISTORY.md             # Journal des sessions
├── INSTALLER.md           # Installation interactive
├── knowledge/             # Base de connaissances
│   ├── CLAUDE.md          # Règles du bibliothécaire
│   ├── inputs/            # Déposez vos fichiers ici
│   ├── wiki/              # Version organisée (markdown)
│   └── outputs/           # Synthèses générées
└── .claude/
    ├── commands/          # Slash commands
    └── skills/            # Skills personnalisées
```

## Commandes

| Commande | Description |
|----------|-------------|
| `/start` | Charger le contexte complet en début de session |
| `/update-context` | Mettre à jour le contexte après un changement |
| `/briefing` | Veille matinale personnalisée |
| `/knowledge compile` | Compiler la base de connaissances |
| `/uninstall` | Supprimer toutes les traces de l'IA (garde inputs/ et outputs/) |

## Base de connaissances

Pour alimenter votre base :
1. Déposez vos fichiers dans `knowledge/inputs/` (Word, Excel, PDF, CSV, markdown, texte...)
2. Dites `/knowledge compile`
3. Claude lit tout, convertit en markdown optimisé, et organise dans `wiki/`

Les fichiers originaux restent intacts dans `inputs/`. Le `wiki/` est une version markdown pure, optimisée pour minimiser la consommation de tokens.

## Pourquoi ce starter ?

Claude est puissant, mais sans contexte persistant il repart de zéro à chaque session. Ce workspace résout ça :

- **Mémoire** : Claude sait qui vous êtes, ce que vous faites, où vous en êtes
- **Évolutivité** : le contexte se met à jour au fil du temps, pas besoin de tout re-expliquer
- **Efficacité** : les documents sont convertis en markdown pour minimiser les tokens consommés

## Inspirations

Ce projet fusionne deux approches complémentaires :
- L'architecture base de connaissances (inputs/wiki/outputs) de [Décuplez votre Claude](https://www.youtube.com/@yassine-sdiri)
- Le système de contexte évolutif et commandes du [Jarvis Starter Kit](https://skool.com/intelligenceartificielle)

## Licence

MIT
