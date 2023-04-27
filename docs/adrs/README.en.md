---
title: "What is an architecture decision record ?"
date: 2021-04-11T03:01:02+02:00
draft: true
weight: 1
toc: true
---

[![Français (fr)](https://img.shields.io/badge/lang-fr-blue.svg)](/docs/adrs/README.md)

## What is an architecture decision record ?

An **architecture decision record** (ADR) is a document that captures an important architectural decision made along with its context and consequences.

An **architecture decision** (AD) is a software design choice that addresses a significant requirement.

An **architecture decision log** (ADL) is the collection of all ADRs created and maintained for a particular project (or organization).

An **architecturally-significant requirement** (ASR) is a requirement that has a measurable effect on a software system’s architecture.

All these are within the topic of **architecture knowledge management** (AKM).

The goal of this document is to provide a fast overview of ADRs, how to create them, and where to look for more information.

Abbréviation | Signification
------------ | -------------
**AD** | Architecture decision
**ADL** | Architecture decision log
**ADR** | Architecture Descision Record
**AKM** | Architecture Knowledge Management
**ASR** | Architecturally-significant requirement

## How to start using ADRs

To start using ADRs, talk with your teammates about these areas.

### Decision identification:

* How urgent and how important is the AD?
* Does it have to be made now, or can it wait until more is known?
* Both personal and collective experience, as well as recognized design methods and practices, can assist with decision identification.
* Ideally maintain a decision todo list that complements the product todo list.

### Decision making:

A number of decision making techniques exists, both general ones and software architecture specific ones, for instance, dialogue mapping.

> Group decision making is an active research topic.

### Decision enactment and enforcement:

ADs are used in software design; hence they have to be communicated to, and accepted by, the stakeholders of the system that fund, develop, and operate it.

Architecturally evident coding styles and code reviews that focus on architectural concerns and decisions are two related practices.

ADs also have to be (re-)considered when modernizing a software system in software evolution.

### Decision sharing (optional):

* Many ADs recur across projects.
* Hence, experiences with past decisions, both good and bad, can be valuable reusable assets when employing an explicit knowledge management strategy.
* Group decision making is an active research topic.

### Decision documentation:

* Many templates and tools for decision capturing exist.
* See agile communities, e.g. M. Nygard's ADRs.
* See traditional software engineering and architecture design processes, e.g. table layouts suggested by IBM UMF and by Tyree and Akerman from CapitalOne.

### Decision guidance:

* The steps above are adopted from the Wikipedia entry on [Architectural Decision](https://en.wikipedia.org/wiki/Architectural_decision)
* A number of decision making techniques exists, both general ones and software architecture specific ones, for instance, dialogue mapping.

## Suggestions for writing good ADRs

Characteristics of a good ADR:

* **Rationale**: Explain the reasons for doing the particular AD. This can include the context (see below), pros and cons of various potential choices, feature comparions, cost/benefit discussions, and more.
* **Specific**: Each ADR should be about one AD, not multiple ADs.
* **Timestamps**: Identify when each item in the ADR is written. This is especially important for aspects that may change over time, such as costs, schedules, scaling, and the like.
* **Immutable**: Don't alter existing information in an ADR. Instead, amend the ADR by adding new information, or supersede the ADR by creating a new ADR.

Characteristics of a good "Context" section in an ADR:

* Explain your organization's situation and business priorities.
* Include rationale and considerations based on social and skills makeups of your teams.
* Include pros and cons that are relevant, and describe them in terms that align with your needs and goals.

Characteristics of good "Consequences" section in an ADR:

* Explain what follows from making the decision. This can include the effects, outcomes, outputs, follow ups, and more.
* Include information about any subsequent ADRs. It's relatively common for one ADR to trigger the need for more ADRs, such as when one ADR makes a big overarching choice, which in turn creates needs for more smaller decisions.
* Include any after-action review processes. It's typical for teams to review each ADR one month later, to compare the ADR information with what's happened in actual practice, in order to learn and grow.

A new ADR may take the place of a previous ADR:

* When an AD is made that replaces or invalidates a previous ADR, then a new ADR should be created

## ADR example templates

ADR example templates that we have collected on the net:

* [ADR template by Michael Nygard](templates/decision-record-template-by-michael-nygard/index.md) (simple and popular)
* [ADR template by Jeff Tyree and Art Akerman](templates/decision-record-template-by-jeff-tyree-and-art-akerman/index.md) (more sophisticated)
* [ADR template for Alexandrian pattern](templates/decision-record-template-for-alexandrian-pattern/index.md) (simple with context specifics)
* [ADR template for business case](templates/decision-record-template-for-business-case/index.md) (more MBA-oriented, with costs, SWOT, and more opinions)
* [ADR template Markdown Any Decision Records (MADR)](templates/decision-record-template-madr/index.md) (both simple and elaborate version; the latter emphasizes options and their pros and cons)
* [ADR template using Planguage](templates/decision-record-template-using-planguage/index.md) (more quality assurance oriented)

## Teamwork advice

If you're considering using decision records with your team, then here's some advice that we've learned by working with many teams.

You have an opportunity to lead your teammates, by talking together about the "why", rather than mandating the "what". For example, decision records are a way for teams to think smarter and communicate better; decision records are not valuable if they're just an after-the-fact forced paperwork requirement.

Some teams much prefer the name "decisions" over the abbreviation "ADRs". When some teams use the directory name "decisions", then it's as if a light bulb turns on, and the team starts putting more information into the directory, such as vendor decisions, planning decisions, scheduling decisions, etc. All of these kinds of information can use the same template. We hypothesize that people learn faster with words ("decisions") over abbreviations ("ADRs"), and people are more motivated to write work-in-progress docs when the word "record" is removed, and also some developers and some managers dislike the word "architecture".

In theory, immutability is ideal. In practice, mutability has worked better for our teams. We insert the new info the existing ADR, with a date stamp, and a note that the info arrived after the decision. This kind of approach leads to a "living document" that we all can update. Typical updates are when we get information thanks to new teammates, or new offerings, or real-world results of our usages, or after-the-fact third-party changes such as vendor capabilties, pricing plans, license agreements, etc.
