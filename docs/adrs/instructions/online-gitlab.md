---
title: "Edition en-ligne Gitlab"
description: ""
date: 2021-04-17T17:31:05+02:00
draft: false
weight: 0
enableToc: true
tocLevels: ["h2", "h3", "h4"]
---

## Création du document à l'aide de Gitlab (Web IDE)

Une fois le ticket créé, selectionner **Repository** dans le panneau latéral gauche.
Cliquer sur le bouton **Web IDE**.

Dans le panneau de gauche, naviguer vers [docs/adrs/records/](/docs/adrs/records).

Faire une clique-droit sur le répertoire `records`, puis sélectionner **New file**.
Nommer le fichier selon la convention de nommage en vigueur.

```
# Exemple
content/fr/public/adr/records/ADR000-dites_bonjour_tous_le_monde.md
```

Dans le panneau de gauche, naviguer vers [docs/adrs/templates](/docs/adrs/templates).
Copier le contenu du modèle de document le plus adapté à votre problématique, puis le coller dans le nouveau document précédement créé.

A l'aide de l'éditeur de texte en ligne, modifier l'en-tête du fichier tels qu'indiqué ci-dessous.

```yaml
---
title: "ADR000 Dites bonjour tous le monde"
description: ""
date: 2021-04-13T01:27:48+02:00
draft: false
weight: 0
---
```

## Alimentation du document

Formuler l'ADR en suivant les préconisations du modèle.
Dans le panneau latéral gauche, selection le module **Source Contrôle (Ctrl+Maj+G)**.
Compléter le formulaire tels qu'indiqué ci dessous:

> **Remplacer** la balise `{{ numéro de ticket }}` la numéro du ticket créé à l'étape précédente (e.g. `#1`).

* **Commit Message**: #{{ numéro de ticket}} Ajout de l'ADR id: 0000

Cliquer sur le bouton **Commit & Push**.

A la question **Commit to a new branch ?**, Sélectionner **Yes** puis renseigner l'identifiant le champs **New branch name** avec le préfixe `adr/` suivi de l'identifiant de l'ADR.

* **exemple**: `adr/adr000`

Un notification sera envoyé aux membres du projet.

## Fusion des modifications

> **Attention**
> Les opération décrites ci-dessous requiert à minima le **rôle Developer**

Dans le formulaire **New Merge Request** ou **Create Merge Request**, compléter le formulaire tels qu'indiqué ci-dessous:

* **Assignee**: _Nom d'un membre du commité d'architecture_
* **Labels**: _doc_, _backlog_
* **Merge option**: Delete source branch when merge request is accepted.

Cliquer sur le bouton **Submit Merge Request**
