# Claude Workspace Starter

Un workspace prêt à l'emploi pour transformer Claude (Code ou Cowork) en assistant personnel multiprojets avec mémoire persistante.

## Ce que ça fait

- **Un assistant qui vous connaît** : interview interactive qui configure Claude selon votre profil, vos objectifs et votre style de communication
- **Architecture multiprojets** : chaque projet a son propre contexte, historique et base de connaissances isolée
- **Base de connaissances intelligente** : déposez n'importe quel fichier (Word, Excel, PDF, CSV...), Claude le convertit en markdown optimisé et l'organise automatiquement
- **Contexte évolutif** : Claude détecte les changements importants et propose de mettre à jour vos fichiers de contexte
- **Veille personnalisée** : briefing matinal filtré selon vos projets et objectifs

## Installation

### Prérequis

- [Claude Desktop](https://claude.ai/download) avec un abonnement Pro, Team ou Enterprise
- Ou [Claude Code](https://docs.claude.com/en/docs/claude-code) (CLI)

### Démarrage rapide

1. Clonez ce repo :
```bash
git clone https://github.com/VOTRE-USERNAME/claude-workspace-starter.git
```

2. Ouvrez le dossier dans Claude Cowork (ou `cd` dedans avec Claude Code)

3. Dites à Claude :
```
Installe mon assistant en suivant le fichier INSTALLER.md
```

4. Répondez aux 8 questions. Claude configure tout automatiquement.

## Structure

```
.
├── CLAUDE.md              # Fondation (chargé à chaque session)
├── CONTEXT.md             # Votre profil global
├── HISTORY.md             # Journal transversal
├── INSTALLER.md           # Installation interactive
├── knowledge/             # Base de connaissances globale
│   ├── CLAUDE.md          # Règles du bibliothécaire
│   ├── raw/               # Déposez vos fichiers ici
│   ├── wiki/              # Version organisée (markdown)
│   └── outputs/           # Synthèses générées
├── projects/
│   ├── _template/         # Modèle pour nouveaux projets
│   └── [vos-projets]/     # Un dossier par projet
└── .claude/
    └── skills/            # Skills personnalisées
```

## Commandes

| Commande | Description |
|----------|-------------|
| `start` | Charger le contexte complet en début de session |
| `project <nom>` | Basculer sur un projet spécifique |
| `new-project <nom>` | Créer un nouveau projet (interview + structure auto) |
| `update-context` | Mettre à jour le contexte après un changement |
| `briefing` | Veille matinale personnalisée |
| `knowledge compile` | Compiler la base de connaissances (global ou projet) |

## Base de connaissances

Le système fonctionne à deux niveaux :

**Global** (`knowledge/`) : savoirs transversaux (fiscalité, veille techno, notes générales...)

**Par projet** (`projects/<nom>/knowledge/`) : connaissances spécifiques au projet

Pour alimenter une base :
1. Déposez vos fichiers dans `raw/` (Word, Excel, PDF, CSV, markdown, texte...)
2. Dites `knowledge compile` (ou `knowledge compile <nom-projet>`)
3. Claude lit tout, convertit en markdown optimisé, et organise dans `wiki/`

Les fichiers originaux restent intacts dans `raw/`. Le `wiki/` est une version markdown pure, optimisée pour minimiser la consommation de tokens.

## Pourquoi ce starter ?

Claude est puissant, mais sans contexte persistant il repart de zéro à chaque session. Ce workspace résout ça :

- **Mémoire** : Claude sait qui vous êtes, ce que vous faites, où vous en êtes
- **Organisation** : chaque projet est isolé avec son propre contexte et sa base de connaissances
- **Évolutivité** : le contexte se met à jour au fil du temps, pas besoin de tout re-expliquer
- **Efficacité** : les documents sont convertis en markdown pour minimiser les tokens consommés

## Inspirations

Ce projet fusionne deux approches complémentaires :
- L'architecture base de connaissances (raw/wiki/outputs) de [Décuplez votre Claude](https://www.youtube.com/@yassine-sdiri)
- Le système de contexte évolutif et commandes du [Jarvis Starter Kit](https://skool.com/intelligenceartificielle)

## Licence

MIT
