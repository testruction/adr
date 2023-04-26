# Relevé de Décision d'Architecture

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

![RDA](RDA.png)

# Décisions d'Architecture Durables

Nous basons notre travail sur les lignes directrices et principes de la publication [Décisions d'Architecture Durables](https://www.infoq.com/articles/sustainable-architectural-design-decisions) de  Zdun et al., par exemple le format d'instruction en Y suggéré dans cet article. Toutefois, nous sommes ouverts à d'autres format de RDAs tels que démontré dans le [dépôt de @joelparkerhenderson](https://github.com/joelparkerhenderson/architecture_decision_record).

En résumé l'instruction en Y se présente ainsi:

> Dans le contexte du `<cas d'usage/récit utilisateur u>`, faisant face à la `<préoccupation p>` nous avons décidés de retenir l'option `<option o>` pour achever `<qualité de système/conséquence désiré q>`, en acceptant `<incovénient/conséquences indésirés i>`

La forme longue; complété par une section "parce que" se présente ainsi:

> Dans le contexte du `<cas d'usage/récit utilisateur u>`, faisant face à la `<préoccupation p>` nous avons décidés de retenir l'option `<option o>` et de négliger `<autre options a>`, pour achever `<qualité de système/conséquence désiré q>`, en acceptant `<incovénient/conséquences indésirés i>`, parce que `<raisonnements additionnels>`.

Vous pouvez trouver plus d'explication et d'exemples sur Medium [Instruction en Y - Un modèle légé pour la Capture des Décisions d'Architecture](https://medium.com/@docsoc/y-statements-10eb07b5a177).

[Une Définition de Terminé pour la Prise de Décision d'Architecture](https://www.ozimmer.ch/practices/2020/05/22/ADDefinitionOfDone.html) propose cinque critères ainsi qu'une liste de contrôle (i.e. check-list) pour décider quand il est temps de définir le statut d'une décision à "terminé": preuves, critères et alternatives, accords, documentations, et plan de réalisation/revue. Ici, nous nous focalisons sur le 'D' dans pcaDPR.
