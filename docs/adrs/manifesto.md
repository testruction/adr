# Relevé de Décision d'Architecture

[![English (en)](https://img.shields.io/badge/lang-en-red.svg)](/docs/adrs/manifesto.md)

en | fr
--- | ---
Décision d'Architecture (DA) | Architecture Decision (AD)
Exigence d'Architecture Significative (EAS) | Architecturally Significant Requirement (ASR)
Relevé de Décision d'Architecture (RDA) | Architecture Decision Record (ADR)
Gestion des Connaissances Architecturales (GCA) | Architectural Knowledge Management (AKM)

Une [Décision d'Architecture (DA)](https://en.wikipedia.org/wiki/Architectural_decision) est un choix de conception logiciel ou d'infrastructure qui adresse une éxigence fonctionnelle ou non-fonctionnelle significative architecturalement. Une [Exigence Significative Architecturalement (ESA)](https://en.wikipedia.org/wiki/Architecturally_significant_requirements) est une éxigence qui a un effet mesurable sur l'architecture et qualité d'un système logiciel ou réseau. Un _Relevé de Décision d'Architecture (RDA)_ capture une seule DA et ses relation; la collection des RDAs créés et maintenu dans un projet constitut son _journal de décision_. Tout cela relève du thème de la Gestion des Connaissances Architecturales (GCA), cependant l'usage de RDA peut être étendu à la conception et autres décisions ("toutes les relevés de décision").

La cible  de l'[organisation RDA sur GitHub](http://github.com/adr) est de:

1. Motiver le besoin et promouvoir le bénéfice de la capture des Décision d'Architecture (AD) et d'établir un vocabulaire commun
2. Renforcer l'outillage autour des RDAs, en support des pratique agile ainsi que les processus d'ingénierie logiciel incrémentaux et itératifs.
3. Fournir des pointeurs vers le contenu publique dans le contexte de la Gestion des Connaissances Architecturales (GCA) et des Relevés de Décision d'Architecture (RDAs)

# Les RDAs légères devrait être adoptées

[ThoughtWorks](https://www.thoughtworks.com/) liste les relevés de décision d'architecture à "adopter" dans leurs [technology radar vol. 18](https://assets.thoughtworks.com/assets/technology-radar-vol-18-en.pdf): <https://www.thoughtworks.com/en-us/radar/techniques/lightweight-architecture-decision-records>.

Une RDA "légère" consite en un [titre, statut, contexte, décision, et une conséquences](https://github.com/joelparkerhenderson/architecture-decision-record/blob/main/templates/decision-record-template-by-michael-nygard/index.md) (selon  [@mtnygard](https://github.com/mtnygard).

Nous pensons que les options considérés avec leurs avantages et inconvénient est cruciale pour comprendre la raison du choix d'une option. [MRDA](https://adr.github.io/madr/) --- Le Markdown de  Relevé de Décision de N'import quoi/d'Architecture (MADR: `[ˈmæɾɚ]`) dans cette organisation RDA inclut de telles informations d'analyse de compromis.

# La relation entre RDAs, MRDA, et autres

![RDA](diagrams/RDA.png)

# Décisions d'Architecture Durables

Nous basons notre travail sur les lignes directrices et principes de la publication [Décisions d'Architecture Durables](https://www.infoq.com/articles/sustainable-architectural-design-decisions) de  Zdun et al., par exemple le format d'instruction en Y suggéré dans cet article. Toutefois, nous sommes ouverts à d'autres format de RDAs tels que démontré dans le [dépôt de @joelparkerhenderson](https://github.com/joelparkerhenderson/architecture_decision_record).

En résumé l'instruction en Y se présente ainsi:

> Dans le contexte du `<cas d'usage/récit utilisateur u>`, faisant face à la `<préoccupation p>` nous avons décidés de retenir l'option `<option o>` pour achever `<qualité de système/conséquence désiré q>`, en acceptant `<incovénient/conséquences indésirés i>`

La forme longue; complété par une section "parce que" se présente ainsi:

> Dans le contexte du `<cas d'usage/récit utilisateur u>`,
> faisant face à la `<préoccupation p>`,
> nous avons décidés de retenir l'option `<option o>`,
> et de négliger `<autre options a>`,
> pour achever `<qualité de système/conséquence désiré q>`,
> en acceptant `<incovénient/conséquences indésirés i>`,
> parce que `<raisonnements additionnels>`.

Vous pouvez trouver plus d'explication et d'exemples sur Medium [Instruction en Y - Un modèle légé pour la Capture des Décisions d'Architecture](https://medium.com/@docsoc/y-statements-10eb07b5a177).

[Une Définition de Terminé pour la Prise de Décision d'Architecture](https://www.ozimmer.ch/practices/2020/05/22/ADDefinitionOfDone.html) propose cinque critères ainsi qu'une liste de contrôle (i.e. check-list) pour décider quand il est temps de définir le statut d'une décision à "terminé": preuves, critères et alternatives, accords, documentations, et plan de réalisation/revue. Ici, nous nous focalisons sur le 'D' dans pcaDPR.

## Modèles de documents éxistant

* Aperçu: [Architectural Decision Records](https://github.com/joelparkerhenderson/architecture_decision_record): Une collection de modèles de documents markdown converties en selon la syntaxe Markdown
* [MADR](https://adr.github.io/madr/): Le Markdown Architecture Decision Records (MADR: `[ˈmæɾɚ]`). Apprendre les RDAs pour rapidement documenter les décisions architecturales en code. - Slogan: Des décisions architecture qui comptes ([matter `[ˈmæɾɚ]`](https://en.wiktionary.org/wiki/matter#Pronunciation)).
* Comparaison de sept modèles de document: [Architectural Decision Guidance Across Projects - Problem Space Modeling, Decision Backlog Management and Cloud Computing Knowledge](http://www.ifs.hsr.ch/fileadmin/user_upload/customers/ifs.hsr.ch/Home/projekte/ADMentor-WICSA2015ubmissionv11nc.pdf). WICSA 2015: 85-94.
* Le contexte, l'historique et des exemples des bonnes et mauvaises justification peuvent être trouvés dans [cet article de blog](https://www.ozimmer.ch/practices/2020/04/27/ArchitectureDecisionMaking.html).
* [Capture de décision](https://schubmat.github.io/DecisionCapture/): Modèles de document pour les projets agile et des explications sur l'univers d'ADR avec un [exemple](https://github.com/schubmat/DecisionCapture/blob/master/samples/samples_simpleTemplate_secondSprint.md).
* cards42 a adopté le modèle d'instruction en Y dans sa [carte RDA](https://cards42.org#adr); La version Anglaise est similaire, mais ajoute l'information sur l'état.
* Le [modèle de document](http://www.iso-architecture.org/42010/templates/) pour [ISO/IEC/IEEE 42010:2011](https://en.wikipedia.org/wiki/ISO/IEC_42010), le standard International pour les descriptions d'architectures de systèmes et de logiciels, suggère neuf éléments d'information dans l'Appendice A pour RDAs. Il identifie notamment les domaines à considérer lorsque l'on identifie les décisions clés.

## Decision Capturing Tools

_Avertissement_:
La liste suivante est plutôt exhaustive.
Se renseigner sur l'état et la maturité des entrées de la liste en suivant les liens.
Nous sommes heureux d'inclure plus de candidats ici.

* [adr-manager](https://adr.github.io/adr-manager/#/): Créer directement dans le navigateur Web des modèles MADR 2.x.
* [adr-tools](https://github.com/npryce/adr-tools): scripts Bash pour gérer des ADRs dans le [format Nygard]((https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions.html)). [exemple]((https://github.com/npryce/adr-tools/blob/master/doc/adr/0002-implement-as-shell-scripts.md)).
* Script Ansible pour installer adr-tools : [ansible-adr-tools](https://github.com/escalate/ansible-adr-tools)
  * Réécriture en C# : [adr-cli](https://github.com/GingerTommy/adr-cli)
  * Réécriture en Go : [adr](https://github.com/marouni/adr)
  * Réécriture en Java : [adr-j](https://github.com/adoble/adr-j)
  * Portage ESM Node.js : [adr-tools](https://github.com/meza/adr-tools)
  * Réécriture en Node.js : [adr](https://github.com/phodal/adr)
  * Version PHP : [phpadr](https://github.com/globtec/phpadr)
  * Module Powershell : [adr-ps](https://github.com/rdagumampan/adr-ps)
  * Réécriture en Python : [adr-tools-python](https://pypi.org/project/adr-tools-python/)
  * Un autre module Powershell : [ArchitectureDecisionRecords](https://github.com/ajoberstar/ArchitectureDecisionRecords)
* [adr-viewer](https://github.com/mrwilson/adr-viewer) - application python pour générer un site web à partir d'un ensemble d'ADRs.
* [architectural-decision](https://github.com/cspray/architectural-decision): bibliothèque PHP pour créer des ADRs à l'aide d'attributs PHP8.
* [Embedded Architectural Decision Records](https://adr.github.io/e-adr/), qui montre comment un journal AD distribué peut être intégré dans le code Java via des annotations ADR.
* [Log4brains](https://github.com/thomvaill/log4brains): interface en ligne de commande et web pour enregistrer et publier vos ADRs en tant que site web statique
* [Loqbooq](https://loqbooq.app): application Web avec intégration Slack pour enregistrer des journaux de décision inspirés d'ADR.

### Outils associés à la gestion de l'architecture

* [ArchUnit](https://github.com/TNG/ArchUnit): Tests unitaires pour l'architecture
* [docToolchain](https://doctoolchain.github.io/docToolchain/): docToolchain est une implémentation de l'approche docs-as-code pour l'architecture logicielle, avec quelques automatisations supplémentaires.
* [Structurizr](https://www.structurizr.com/): Structurizr est une collection d'outils pour vous aider à visualiser, documenter et explorer votre architecture logicielle en utilisant le [modèle C4]((https://c4model.com/)).


### Outils intéressants, mais non maintenus

* [adr-log](https://github.com/adr/adr-log): Génère un journal des décisions architecturales à partir de MADRs.
* [ADMentor](https://github.com/IFS-HSR/ADMentor) : Extension de modélisation des décisions architecturales pour Sparx Enterprise Architect
* [eadlsync](https://adr.github.io/eadlsync/): synchronise les enregistrements intégrés de décisions architecturales avec un référentiel de décisions architecturales.
* [SE Repo](https://github.com/adr/serepo): Dépôt d'ingénierie Logiciel. Un référentiel pour la gestion de version des artefacts de génie logiciel, qui peuvent être des décisions architecturales, des modèles et autres.

## Plus d'informations

* [Architectural Decisions — The Making Of](https://www.ozimmer.ch/practices/2020/04/27/ArchitectureDecisionMaking.html): fournit un historique sur les enregistrements des décisions architecturales.
* [Architectural Decision Records (ADR): Open & Transparent Decision History](https://openpracticelibrary.com/practice/architectural-decision-records-adr/): Open & Transparent Decision History dans la Open Practice Library
* Des directives prescriptives d'AWS recommandent l'[utilisation d'enregistrements des décisions architecturales pour rationaliser la prise de décision technique pour un projet de développement de logiciel](https://docs.aws.amazon.com/prescriptive-guidance/latest/architectural-decision-records/welcome.html).
* [Architecture Knowledge Management (AKM) overview]((https://www.ost.ch/de/forschung-und-dienstleistungen/informatik/ifs-institut-fuer-software/labs/cloud-application-lab/architectural-knowledge-management-akm)) chez OST
* [Documenting Architecture Decisions](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions.html) par Michael Nygard
* [Architecture Decision Records in Action by Michael Keeling (IBM Watson Group) and Joe Runde (IBM)](https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=497744) par Michael Keeling (IBM Watson Group) et Joe Runde (IBM): présentation incluant des chiffres empiriques.
* [Documenting Architecture Decisions](https://www.fabian-keller.de/blog/documenting-architecture-decisions): Article de blog de Fabian Keller
* [From Architectural Decisions to Design Decisions](https://medium.com/olzzio/from-architectural-decisions-to-design-decisions-f05f6d57032b) et [ADR = Any Decision Record?](https://medium.com/olzzio/adr-any-decision-record-916d1b64b28d): Deux billets de blog d'Olaf Zimmermann proposant d'étendre la portée des ADR.
* Sélection et adaptation de méthodes dans DPR, le [Design Practice Repository (DPR)](https://socadk.github.io/design-practice-repository/) sur GitHub et le [Design Practice Reference](https://leanpub.com/dpr), un livre électronique correspondant sur LeanPub. La capture des décisions architecturales est présentée comme l'une des activités essentielles dans DPR.

<!-- - [Work by Daniel Popescu](https://scholar.google.com/citations?user=dASv28sAAAAJ) -->
<!-- - [French Translation by Florian JUDITH](https://github.com/fjudith) -->
