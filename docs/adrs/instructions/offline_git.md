---
title: "Edition hors-ligne avec Git"
description: ""
date: 2021-04-17T17:29:12+02:00
draft: false
weight: 0
enableToc: true
tocLevels: ["h2", "h3", "h4"]
---

## Création du document

Exécuter la commande suivante pour créer le répertoire dédié rescenssement des ADRs.

```bash
mkdir -p docs/adrs/records
```

Créer l'ADR en copiant un des modèles de document disponible dans le répertoire `docs/adrs/template`.


```bash
cp docs/adrs/templates/intermediare.md docs/adrs/records/adr000_dire_bonjours_tous_le_monde.md
```

A l'aide d'un éditeur de texte. Modifier l'en-tête du fichier tels qu'indiqué ci-dessous.

```yaml
title: "ADR000 Dire bonjour tous le monde"
description: ""
date: 2021-04-13T01:27:48+02:00
draft: false
weight: 0
```

## Alimentation du document

Formuler l'ADR à l'aide du [modèle de document](/docs/adrs/templates) le plus adapté à votre problématique.

Enregister le fichier dans la file d'attent, puis dans l'historique du dépôt Git.

> **Remplacer** la balise `{{ numéro de ticket }}` la numéro du ticket créé à l'étape précédente (e.g. `#1`).

```bash
# Mise en file d'attente
git docs/adrs/records/adr000_dire_bonjours_tous_le_monde.md

# Enregistrement / Historisation
git commit -a -m "#{{ numéro de ticket}} Ajout de l'ADR id: 000"

# Publication des modification
git push
```
