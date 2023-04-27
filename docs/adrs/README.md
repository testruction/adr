---
title: "Quesqu'un relevé de décision d'architecture ?"
date: 2021-04-11T03:01:02+02:00
draft: true
weight: 1
toc: true
---

[![English (en)](https://img.shields.io/badge/lang-en-red.svg)](/docs/adrs/README.en.md)

## Quesqu'un relevé de décision d'architecture

Un relevé de décision d'architecture _Architectural Decision Record (ADR)_ est un document qui capture les décisions importantes relatives à l'architecture en les contextualisant et en mesurant les conséquences.

Une **décision d'architecture** _Architecture Decision (AD)_ est une choix de conception logiciel qui adresse un exigence significative.

Un **journal de décision d'architecture** _Architecture Decision Log (ADL)_ est une collection de tous les ARDs créés et maintenue pour un projet particulier, ou une organisation particulière.

Une **exigence significative d'architecture** _Architecturally-significant requirement (ASR)_ est une exigence qui détient un effet mesurable sur le système de l'architecture du logiciel.

Ces documents font partie du domaine de la **gestion de la connaissance de l'architecture** _Architecture Knowledge Management (AKM)_

L'objectif de ce document est de fournir une aperçu rapide des ADRS, comment les créer, et où consulter des informations complémentaires.

Abbréviation | Signification
------------ | -------------
**AD** | Décision d'architecture _(eng. Architecture decision)_
**ADL** | Journal de décision d'architecture _(eng. Architecture decision log)_
**ADR** | Rélévé de décision d'architecture _(eng. Architecture Descision Record)_
**AKM** | Gestion de la connaissance de l'architecture _(eng. Architecture Knowledge Management)_
**ASR** | Exigence significative d'architecture _(eng. Architecturally-significant requirement)_

## Comment commencer à utiliser les ADRs

### Identification de la décision

Pour correctement initier le processus ADR, ouvrez le dialogue avec vos équipiers en répondant le questionnaire:

* Est-il urgent et à quel point l'AD est importante ?
* Est-ce que l'AD doit être lancée maintenant, ou celà peut-il attendre pour de plus amples informations ?
* Est-ce que l'expérience personnelle et collective; ainsi que des méthodes et pratiques de conception; peuvent aider à déterminer la décision ?
* Faut-il maintenir une liste de décision à prendre _(eng. Decision Todo-list)_ en complément de la todo-list du produit _(eng. product todo-list)_?

### Prise de décision

Il existe un certain nombre de techniques de prise de décision, à la fois générales et spécifiques à l'architecture logicielle. (e.g. Cartographie du diaglogue _[Dialogue mapping](https://en.wikipedia.org/wiki/Issue-based_information_system)_)

> Le groupe des décisions est un sujet actif dans le domaine de la recherche.

### Adoption et application des décisions

Les ADs sont utilisées dans la conception de logiciels; par conséquent, elles doivent être communiquées et acceptées par les intervenants du système qui le financent, du dévelopement, et de l'exploitation.

Les tyles de codage architecturaux évidents et les révisions de code qui mettent l'accent sur les préoccupations architecturales et les décisions sont deux pratiques connexes.

Les AD doivent également être (re)prises en compte lors de la modernisation d'un système logiciel comme point départ de toutes évolution l'affectant.

### Partage des décisions (facultatif)

De nombreuses AD sont produites dans le cycle de vie des projets.
Par conséquent, l'expérience des décisions passées; qu'elle soit bonnes ou mauvaises; peut être des attouts réutilisables précieux lors de l'utilisation d'une stratégie explicite de gestion des connaissances.

> La prise de décision en groupe est un sujet actif dans le domaine de la recherche.

### Documentation de la décision

De nombreux modèles et outils de prise décision existent (e.g. Communautés agile, M. Nygard's ADRs)

Consultez les processus traditionnels d'ingénierie logicielle et de conception d'architecture, par exemple les modèles de tableaux suggérés par IBM UMF, ainsi que par Tyree And Akerman de CapitalOne.

### Orientation des décision

les étapes décrites ci-dessus se réferent de la page Wikipedia relative à la définion de la décision architecturale (ref. [Architectural Decision](https://en.wikipedia.org/wiki/Architectural_decision)).

### Suggestion de formulation

Caractéristiques d'une bonne ADR:

* **Horodaté**: Identifier quand l'ADR a été formulée
* **Rationnelle**: Expliquer la raison particulière de l'AD
* **Immuable**: Les décisions prises dans un ADR déjà publié (i.e. `draft: false`), ne doivent pas être modifiées
* **Spécifique**: Chaque ADR correspond à un AD unique, dans la mesure du possible

Charactéristiques d'une bonne mise en contexte dans un ADR:

* Expliquer la situation et les priorités opérationnelles de votre organistion ou projet
* Inclure les justifications et les considérations fondées sur les transformations de compétence et sociales de vos équipes

Caractérisque d'une bonne formulation des conséquences:

* **Bonne approche**: _"Nous devons commencer à faire X au lieur de Y"_
* **Mauvaise approche**: "Ne pas expliquer l'AD en terme les _"Pour & Contre"_ d'une AD particulière

Un nouvel ADR peut remplacer un ADR précédent:

Lorsque'une AD replace ou invalide un ADR précédent

### Modèles d'ADRs

* [ADR template by Michael Nygard](https://github.com/fjudith/architecture_decision_record/blob/master/adr_template_by_michael_nygard.md) (simple et populaire)
* [ADR template for Alexandrian pattern](https://github.com/fjudith/architecture_decision_record/blob/master/adr_template_by_jeff_tyree_and_art_akerman.md) (plus sophistiqué)
* [ADR template for business case](https://github.com/fjudith/architecture_decision_record/blob/master/adr_template_for_alexandrian_pattern.md) (simple et contextualisé)
* [ADR template for business case](https://github.com/fjudith/architecture_decision_record/blob/master/adr_template_for_business_case.md) (orienté MBA. comprend les notions de coût, SWOT, et plus d'opinions)
* [ADR template MADR](https://github.com/fjudith/architecture_decision_record/blob/master/adr_template_madr.md) (plus Markdown)
* [ADR template using Planguage](https://github.com/fjudith/architecture_decision_record/blob/master/adr_template_using_planguage.md) (plus orienté assurance qualité)

### Travail en équipe

Si vous envisagez d'utiliser les relevés de décision avec votre équipe, voici quelques conseils issues des leçons apprises sur des terrains plus ou moins larges.

Vous avez l'occasion de diriger vos coéquipiers, en parlant ensemble du "pourquoi", plutôt que d'imposer le "quoi".

Exemple:

* les relevés de décision sont un moyen pour les équipes de penser plus intelligemment et de mieux communiquer
* Les relevés de décision ne sont pas utiles s'ils ne son qu'une exigence de paperasserie **après les faits**.

Certaines équipes préfèrent de loin le nom "décisions" à l'abréviation "ADR". Lorsque certaines équipes utilisent le nom de répertoire "décisions", c'est comme si une ampoule s'allumait, et l'équipe commençait à mettre plus d'informations dans le répertoire, comme les décision des fournisseurs, les décisions de planification, les décisions d'ordonancement, etc.

Tous ces types d'information peuvent utiliser le même modèle.