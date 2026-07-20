---
name: recherche-actualites-contextualisees
description: Skill pour effectuer une veille personnalisée des actualités. Quand l'utilisateur demande "fais-moi un point sur les actualités", "donne-moi les news du jour", "qu'est-ce que je dois savoir aujourd'hui", "fais-moi une veille", ou utilise la commande /morning, cette skill prend le relais pour effectuer une recherche d'actualités, les filtrer selon le contexte personnel de l'utilisateur (CONTEXT.md), et ne garder que celles qui sont pertinentes pour ses objectifs et projets actifs.
---

# Skill : Recherche d'Actualités Contextualisées

## Mission

Veille intelligente des actualités, filtrée selon le contexte personnel. L'objectif n'est pas de tout dire, mais de ne garder que ce qui concerne vraiment l'utilisateur.

---

## Phase 1 : Charger le contexte

Avant toute recherche, lire :

1. CONTEXT.md (racine) : profil, objectifs, projets
2. HISTORY.md (racine) : sessions récentes pour les sujets actifs
3. Les CONTEXT.md des projets actifs (projects/*/CONTEXT.md, ignorer _template)

Identifier le filtre de pertinence :
- Profil dominant et activité principale
- Objectifs court terme
- Projets en cours (tous)
- Domaine d'aide prioritaire

---

## Phase 2 : Périmètre de la veille

Si l'utilisateur n'a pas précisé le sujet :

```
Sur quel domaine ta veille du jour ?

1. Actualités IA et nouvelles technologies (par défaut)
2. Actualités de ton secteur d'activité
3. Actualités économiques et business
4. Un sujet spécifique (à préciser)
```

Si lancé via /morning, utiliser directement IA + secteur d'activité par défaut.

---

## Phase 3 : Recherche

3 à 5 recherches web ciblées maximum. Privilégier :
- Sources récentes (moins de 48h)
- 3 angles : annonces majeures, tendances émergentes, signaux faibles
- Sources francophones en priorité, internationales si nécessaire

Adapter les requêtes selon le contexte chargé (profil, secteur, projets actifs).

---

## Phase 4 : Filtrage contextuel

Pour chaque actualité, 3 questions :

1. Est-ce que ça concerne directement les objectifs de l'utilisateur ?
2. Est-ce que ça impacte un de ses projets en cours ?
3. Est-ce que ça change quelque chose dans son secteur ou son domaine prioritaire ?

Non aux 3 → écarter. Oui à au moins 1 → garder.

3 actualités pertinentes > 10 actualités génériques.

---

## Phase 5 : Présentation

```
Veille du [date]

Filtrée selon ton contexte : [résumé 1 ligne du profil et focus actuel]

---

Ce que tu dois savoir

[Actualité 1]
- Pourquoi c'est important pour toi : [explication personnalisée]
- Source : [lien]

[Actualité 2]
- Pourquoi c'est important pour toi : [explication personnalisée]
- Source : [lien]

---

Bon à savoir aussi

[Actualité 3 ou 4, bullet points courts]

---

Action recommandée

[1 action concrète que tu peux prendre aujourd'hui]
```

---

## Si rien de pertinent

```
Veille du [date]

J'ai cherché sur [domaines couverts] mais rien de majeur qui impacte directement tes objectifs ou projets aujourd'hui.

Pas de bruit. Tu veux que j'élargisse la recherche ?
```

---

## Règles

- Toujours expliquer pourquoi c'est pertinent pour CET utilisateur
- Maximum 3-4 actualités
- Action recommandée à la fin
- Ne jamais inventer d'actualité ou de source
- Français, pas de tirets longs
