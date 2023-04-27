---
title: "Bien débuter"
date: 2021-04-11T03:01:02+02:00
draft: true
weight: 100
toc: true
---

## Processus

### Synoptique

Le processus de Relevé de Décisions d'Architecture _(eng. Architectural Decision Record (ADR))_ vise à assurer la traçabilité des discussions, justifications et décisions associées relatives à un choix d'architure logiciel, matériel, ou organisationnel significatif pour le projet.
Par significatif on entend que l'on estime le choix relève un enjeu stratégique pour la viabilité économique du projet, qui affecte le style de développement du système ou la viabilité de son exploitation à long-terme.

### Entrées

Le processus de Relevé de Décision d'Architecture est amorcé lorsqu'une partie prenante du projet identifie un problème architectural qui requiert un arbitrage collectif des différents contributeurs du projet.
La demande peut provenir des canaux de communication suivants:

* L'enregistrement d'un nouveau scénario utilisateur ou d'une fonctionnalité logiciel supplémentaire
* L'enregistremnet d'un rapport de bug ou d'incident d'exploitation
* L'enregistement direct d'une demande d'ADR dans le gestionnaire de ticket
* Un sujet discuté en committé ayant été validé comme éligible au processus ADR

### Sortie

Le processus de Relevé de Décision d'Architecture débouche sur les résultat suivants:

* Arbitrage collégiale de la décision d'architecture
* Clôture de la demande
* Planification et mise en oeuvre du plan d'action de mise en conformité

### Ordonnancement

![ADR Process](/docs/adrs/diagrams/adr_process.drawio.svg)

### Séquencement du suivi

`#` | Etape | Outil | Etat | Decription
:-: | ----- | ----- | ---- | ----------
1   | Réception de la demande | Outil de gestion de tickets (Gihub, Gilab, Jira, etc.) | Nouveau | Création d'un ticket
2   | Enregistrement et validation | [Hugo](https://gohugo.io), Editeur de texte | Enregistré | Création du document dans le répertoire de dépôt des ADRs, Commit & Push du document mentionnant l'ID du ticket
3   | Catégorisation, priorisation & validation | Outil de gestion de tickets (Github, Gilab, Jira, etc.) | Référencé | Référencement:<url><li>Labellisation</li><li>Allocation des participants</li><li>Définition de la date butoire</li><li>Assignation à un jalon</li></ul>
4   | Revue & enrichissement collectif | Commentaires dans l'outil de gestion de tickets (Github, Gilab, Jira, etc.), committé, revue de paire-à-paire | En cours | Affinage du contexte, de l'argumentaire prospectif, et de l'évaluation d'impact. Mise à jour du document
5   | Arbitrage, publication du document et clôture de la demande | Outil de gestion de tickets (Github, Gilab, Jira, etc.), Editeur de texte | Clôturé | Modfification de la balise `draf: false` dans le document, Commit & Push mentionnant l'ID du ticket, et clôture du ticket

## Comment utiliser les ADRs à l'aide de Gitalb

> Ce mode opératoire est spécifique à la structure de la documentation technique du projet Connect Building qui s'appuie sur [Hugo](https://gohugo.io) et [Gitlab](https://gitlab.groupeonepoint.com) pour la publication sous forme de page web statique.

### Convention de nommage des fichiers

Il est crucial de respecter la convention de nommage décrite ci-dessous afin de satisfaire le besoin de traçabilité des ADRs.

`<prefix><3 digit>-<architecture layer>-<verb>-<summary>.<extension>`

* **Préfix**: ADR
* **Numéro**: 0001-9999
* **Verbe**: _choisir, adopter, supprimer, changer, etc._
* **Couche**: _frontend, backend, persistence, database_
* **Résumé**: choose_db_engine_version
* **Extention**: .md _(MarDown)_

#### Exemple

* ADR0042-backend-choose-api-runtime.md
* ADR1789-backup_restore-select-object-storage-provider.md

### Création du ticket dans Gitlab

Naviguer vers le gestionnaire de ticket intégré à Gitlab <https://gitlab.groupeonepoint.com/connect-building/documentation/-/issues>, puis cliquer sur le bouton **New Issue**.

Compléter le formulaire tels qu'indiquer ci-dessous:

* **Title**: [`<prefix><3 digit>`] `<architecture layer>: <verb>-<summary>.<extension>`
* **Type**: Issue
* **Description/Template**: adr_request
* **Assignee**: _Assign to me
* **Label**: _doc_, _backlog_

Cliquer sur le bouton **Submit issue**.

## Gestion du document

Les guides suivants sont à votre disposition pour accompagner dans la création de votre première ADR.

* [Edition en-ligne avec Gitlab](/public/adr/getting_started/online-gitlab): Hors développeurs
* [Edition hors-ligne avec Git](/public/adr/getting_started/vshode-hugo): Développeurs et mainteneurs du projet
* [Suggestion](/public/adr/getting_started/suggestions): Aide à la formulation des ADRs
