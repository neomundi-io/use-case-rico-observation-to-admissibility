# ManChine RiCo × NeoMundi

**Runtime observation, admissibility determination and consequential execution — architectural interoperability use case.**

[🇫🇷 Lire en français](#version-française)

---

# English

## What happened here?

NeoMundi and ManChine AI Technologies explored how runtime measurement can support governance immediately before consequential AI execution.

NeoMundi provides **runtime observational evidence**.

Runtime Integrity Control (**RiCo**) evaluates that evidence together with **Authority, Evidence, Context and Policy** in order to perform **Admissibility Determination**.

The Runtime Execution Boundary (**REB**) is the architectural point at which the resulting governance consequence can be enforced before consequential execution.

**In simple terms:**

> **NeoMundi observes. RiCo determines admissibility. The REB governs the transition to consequential execution.**

The purpose of this use case is to preserve those responsibilities as separate architectural functions rather than merging measurement, governance determination and execution authority.

---

## What this shows

This architectural use case documents that:

- runtime observation can be provided as evidence to an independent governance layer;
- measurement does not need to become decision authority;
- RiCo can evaluate NeoMundi observations alongside Authority, Evidence, Context and Policy;
- Admissibility Determination remains a RiCo governance function;
- enforcement remains associated with the Runtime Execution Boundary;
- observational evidence and Governance Receipts can remain distinct;
- the resulting chain can be designed for later reconstruction and Constitutional Replay.

This is currently an **architectural interoperability use case**.

It is not yet evidence of a completed machine-to-machine interoperability run.

---

## Use case context

- **Runtime governance architecture:** Runtime Integrity Control (RiCo) · ManChine AI Technologies
- **Runtime observation and measurement:** NeoMundi
- **Governance determination:** RiCo
- **Execution boundary:** Runtime Execution Boundary (REB)
- **Primary governance operation:** Admissibility Determination
- **Downstream governance artifact:** Governance Receipt
- **Reconstruction concept:** Constitutional Replay
- **Current interoperability status:** architectural articulation documented
- **Next validation step:** NeoMundi Runtime Interoperability JSON Contract

---

## Core question

> **Can runtime observational evidence support an independent admissibility determination immediately before consequential execution without turning the measurement layer itself into governance authority?**

The architecture explored here addresses this question by keeping observation, governance determination and execution enforcement explicitly separated.

---

## Architecture

```text
Runtime Observation
        │
        ▼
Observation Receipt
NeoMundi
        │
        ▼
Authority
Evidence
Context
Policy
        │
        ▼
Admissibility Determination
RiCo
        │
        ▼
Runtime Execution Boundary
REB
        │
        ▼
Consequential Execution
        │
        ▼
Governance Receipt
        │
        ▼
Constitutional Replay
```

---

## Separation of responsibilities

### NeoMundi

NeoMundi observes runtime behavior and produces or preserves observational evidence.

Its role in this use case is measurement and observation.

NeoMundi does **not** independently:

- determine admissibility;
- authorize execution;
- deny execution;
- replace the applicable governance authority;
- enforce consequential execution.

### Runtime Integrity Control — RiCo

Runtime Integrity Control evaluates the applicable:

- **Authority**
- **Evidence**
- **Context**
- **Policy**

and performs **Admissibility Determination** immediately before consequential execution.

RiCo therefore remains responsible for the governance interpretation of the available evidence.

### Runtime Execution Boundary — REB

The Runtime Execution Boundary is the architectural boundary immediately preceding consequential execution.

Within the RiCo architecture, it is where the governance consequence associated with Admissibility Determination can be enforced.

### Governance Receipt

A Governance Receipt preserves the resulting governance event and supports later reconstruction of how the execution determination was reached.

### Constitutional Replay

Constitutional Replay refers to the ability to reconstruct and independently inspect the governance path using the preserved evidence, applicable authority, context and policy.

---

## Why this separation matters

A runtime measurement may indicate:

- stability or instability;
- variation;
- drift;
- factual-risk signals;
- incomplete measurement;
- other observable runtime conditions.

But an observational signal does not, by itself, answer:

> **Should this execution be allowed to proceed?**

That determination depends on the governance context in which the observation is interpreted.

This use case therefore preserves a fundamental separation:

> **Measurement produces evidence. Governance determines consequence.**

---

## Observation-to-Admissibility relationship

The intended relationship is:

```text
NeoMundi observation
        │
        │ observational evidence
        ▼
RiCo governance context
        │
        ├── Authority
        ├── Evidence
        ├── Context
        └── Policy
        │
        ▼
Admissibility Determination
        │
        ▼
Runtime Execution Boundary
        │
        ▼
Consequential Execution
```

The NeoMundi signal remains an input to governance rather than becoming governance authority itself.

---

## What this use case establishes

At its current stage, this repository establishes a documented architectural articulation for:

- independent runtime observation;
- preservation of observational evidence;
- integration of measurement signals into a broader governance context;
- separation between observation and Admissibility Determination;
- separation between determination and execution enforcement;
- preservation of governance outcomes;
- reconstructable governance through Governance Receipts and Constitutional Replay.

---

## What this use case does not establish

This repository does **not**, by itself, establish:

- a production deployment;
- certification of either architecture;
- legal admissibility;
- regulatory compliance;
- universal AI reliability;
- autonomous execution authority for NeoMundi;
- that a NeoMundi measurement signal constitutes a governance decision;
- a completed machine-to-machine interoperability implementation;
- empirical performance of RiCo across AI models or environments.

Further technical execution is required before broader claims can be made.

---

## Current technical boundary

The current repository documents the **architectural articulation** between NeoMundi runtime observation and RiCo Admissibility Determination.

The next planned step is to test this relationship using the **NeoMundi Runtime Interoperability JSON Contract**.

The intended validation path is:

```text
NeoMundi runtime observation
        │
        ▼
Runtime Interoperability JSON
        │
        ▼
RiCo consumption
        │
        ▼
Admissibility Determination
        │
        ▼
Governance artifact / receipt
```

Once this exchange has been executed and preserved, the repository can evolve from an architectural interoperability use case into a **documented interoperability pilot**.

---

## Repository purpose

This repository preserves an inspectable reference case for:

- runtime AI observation;
- governance-layer interoperability;
- admissibility determination;
- Runtime Execution Boundary architecture;
- separation of measurement and governance authority;
- Governance Receipts;
- reconstructable governance;
- future machine-readable interoperability.

The objective is not to merge NeoMundi and RiCo into one authority.

The value of the architecture is precisely that the layers remain independent.

**NeoMundi provides runtime observation and measurement.**

**RiCo provides Admissibility Determination and runtime governance architecture.**

---

## Status

**Architectural interoperability use case documented.**

Currently documented:

- NeoMundi observational role;
- RiCo governance role;
- Admissibility Determination;
- Runtime Execution Boundary;
- separation of measurement and governance authority;
- Governance Receipt concept;
- Constitutional Replay concept;
- observation-to-admissibility architecture.

### Next validation step

- NeoMundi Runtime Interoperability JSON Contract;
- machine-readable observation exchange;
- RiCo consumption of the observation;
- preservation of the resulting governance artifact;
- documented end-to-end interoperability run.

---

## Resources

### Richard Colmon / ManChine AI Technologies

**Richard Colmon**

Runtime Integrity Control (RiCo) · AI runtime governance architecture

- [LinkedIn](https://www.linkedin.com/in/richard-colimon-481645391/)
- [ManChine AI Technologies](https://manchine.ai/) — runtime governance architecture for AI integrity, continuity and consequential governance.
- [RGEP-01 — Runtime Governance Editorial & Publication Policy v1.0](https://manchine.ai/assets/whitepapers/RGEP-01_Runtime_Governance_Editorial_Publication_Policy.pdf)

### NeoMundi

- [NeoMundi Research](https://neomundi.org/)
- [ControlTower](https://controltower.neomundi.io/welcome)
- [Runtime Interoperability Contract](https://github.com/neomundi-io/runtime-interoperability-contract)
- [NeoMundi AI Observatory](https://github.com/neomundi-io/neomundi-ai-observatory)

---

## Attribution

The **Runtime Integrity Control (RiCo)** architecture and the concepts represented here as **Runtime Execution Boundary (REB)**, **Admissibility Determination**, **Governance Receipt** and **Constitutional Replay** are attributed in this repository to:

**Richard Colmon — ManChine AI Technologies**

NeoMundi contributes the runtime observational and measurement layer within the documented articulation.

The repository intentionally preserves the distinction between:

- runtime observation and measurement;
- governance interpretation;
- admissibility determination;
- execution enforcement.

Authorship and attribution must be preserved where explicitly identified.

---

# Version française

[🇬🇧 Back to English](#english)

## Qu’est-ce qui a été fait ici ?

NeoMundi et ManChine AI Technologies ont exploré comment une mesure runtime peut alimenter une gouvernance intervenant immédiatement avant l’exécution conséquente d’un système IA.

NeoMundi fournit des **preuves observationnelles runtime**.

Runtime Integrity Control (**RiCo**) évalue ces éléments conjointement avec l’**Autorité, les Preuves, le Contexte et la Politique** afin de réaliser une **Détermination d’Admissibilité**.

La **Runtime Execution Boundary (REB)** constitue le point architectural auquel la conséquence de gouvernance peut être appliquée avant l’exécution conséquente.

**En termes simples :**

> **NeoMundi observe. RiCo détermine l’admissibilité. La REB gouverne le passage vers l’exécution conséquente.**

L’objectif de ce use case est de conserver ces responsabilités comme des fonctions architecturales distinctes, sans fusionner mesure, détermination de gouvernance et autorité d’exécution.

---

## Ce que cela montre

Ce use case architectural documente que :

- l’observation runtime peut être fournie comme preuve à une couche de gouvernance indépendante ;
- la mesure n’a pas besoin de devenir une autorité de décision ;
- RiCo peut évaluer les observations NeoMundi avec l’Autorité, les Preuves, le Contexte et la Politique ;
- la Détermination d’Admissibilité reste une fonction de gouvernance RiCo ;
- l’enforcement reste associé à la Runtime Execution Boundary ;
- les preuves observationnelles et les Governance Receipts peuvent rester distincts ;
- la chaîne résultante peut être conçue pour permettre une reconstruction ultérieure et un Constitutional Replay.

Il s’agit actuellement d’un **use case architectural d’interopérabilité**.

Il ne constitue pas encore la preuve d’une exécution d’interopérabilité machine-to-machine complète.

---

## Contexte du use case

- **Architecture de gouvernance runtime :** Runtime Integrity Control (RiCo) · ManChine AI Technologies
- **Observation et mesure runtime :** NeoMundi
- **Détermination de gouvernance :** RiCo
- **Frontière d’exécution :** Runtime Execution Boundary (REB)
- **Opération de gouvernance principale :** Admissibility Determination
- **Artefact de gouvernance aval :** Governance Receipt
- **Concept de reconstruction :** Constitutional Replay
- **Statut actuel de l’interopérabilité :** articulation architecturale documentée
- **Prochaine étape de validation :** NeoMundi Runtime Interoperability JSON Contract

---

## Question centrale

> **Une preuve observationnelle runtime peut-elle soutenir une détermination indépendante d’admissibilité immédiatement avant une exécution conséquente sans transformer la couche de mesure elle-même en autorité de gouvernance ?**

L’architecture explorée ici répond à cette question en maintenant explicitement séparées l’observation, la détermination de gouvernance et l’enforcement de l’exécution.

---

## Architecture

```text
Observation runtime
        │
        ▼
Observation Receipt
NeoMundi
        │
        ▼
Autorité
Preuves
Contexte
Politique
        │
        ▼
Détermination d’Admissibilité
RiCo
        │
        ▼
Runtime Execution Boundary
REB
        │
        ▼
Exécution conséquente
        │
        ▼
Governance Receipt
        │
        ▼
Constitutional Replay
```

---

## Séparation des responsabilités

### NeoMundi

NeoMundi observe le comportement runtime et produit ou préserve les preuves observationnelles.

Son rôle dans ce use case est celui de la mesure et de l’observation.

NeoMundi ne :

- détermine pas indépendamment l’admissibilité ;
- n’autorise pas l’exécution ;
- ne refuse pas l’exécution ;
- ne remplace pas l’autorité de gouvernance applicable ;
- n’impose pas l’exécution conséquente.

### Runtime Integrity Control — RiCo

Runtime Integrity Control évalue :

- l’**Autorité** ;
- les **Preuves** ;
- le **Contexte** ;
- la **Politique** ;

et réalise une **Détermination d’Admissibilité** immédiatement avant l’exécution conséquente.

RiCo reste ainsi responsable de l’interprétation de gouvernance des preuves disponibles.

### Runtime Execution Boundary — REB

La Runtime Execution Boundary est la frontière architecturale située immédiatement avant l’exécution conséquente.

Dans l’architecture RiCo, c’est à ce niveau que la conséquence de gouvernance associée à la Détermination d’Admissibilité peut être appliquée.

### Governance Receipt

Un Governance Receipt préserve l’événement de gouvernance résultant et permet de reconstruire ultérieurement la manière dont la détermination d’exécution a été obtenue.

### Constitutional Replay

Le Constitutional Replay désigne la capacité à reconstruire et inspecter indépendamment le chemin de gouvernance à partir des preuves préservées ainsi que de l’autorité, du contexte et de la politique applicables.

---

## Pourquoi cette séparation est importante

Une mesure runtime peut indiquer :

- stabilité ou instabilité ;
- variation ;
- dérive ;
- signaux de risque factuel ;
- mesure incomplète ;
- autres conditions runtime observables.

Mais un signal observationnel ne répond pas, à lui seul, à la question :

> **Cette exécution doit-elle être autorisée à se poursuivre ?**

Cette détermination dépend du contexte de gouvernance dans lequel l’observation est interprétée.

Ce use case préserve donc une séparation fondamentale :

> **La mesure produit de la preuve. La gouvernance détermine la conséquence.**

---

## Relation Observation-to-Admissibility

La relation envisagée est :

```text
Observation NeoMundi
        │
        │ preuve observationnelle
        ▼
Contexte de gouvernance RiCo
        │
        ├── Autorité
        ├── Preuves
        ├── Contexte
        └── Politique
        │
        ▼
Détermination d’Admissibilité
        │
        ▼
Runtime Execution Boundary
        │
        ▼
Exécution conséquente
```

Le signal NeoMundi reste une entrée de la gouvernance plutôt que de devenir lui-même une autorité de gouvernance.

---

## Ce que ce use case établit

À son stade actuel, ce dépôt établit une articulation architecturale documentée pour :

- l’observation runtime indépendante ;
- la préservation des preuves observationnelles ;
- l’intégration de signaux de mesure dans un contexte plus large de gouvernance ;
- la séparation entre observation et Détermination d’Admissibilité ;
- la séparation entre détermination et enforcement de l’exécution ;
- la préservation des résultats de gouvernance ;
- une gouvernance reconstructible via Governance Receipts et Constitutional Replay.

---

## Ce que ce use case n’établit pas

Ce dépôt n’établit **pas**, à lui seul :

- un déploiement en production ;
- une certification de l’une ou l’autre architecture ;
- une admissibilité juridique ;
- une conformité réglementaire ;
- une fiabilité universelle des systèmes IA ;
- une autorité d’exécution autonome pour NeoMundi ;
- qu’un signal de mesure NeoMundi constitue une décision de gouvernance ;
- une implémentation machine-to-machine complète ;
- des performances empiriques de RiCo sur différents modèles ou environnements IA.

Une exécution technique supplémentaire est nécessaire avant toute généralisation plus large.

---

## Frontière technique actuelle

Le dépôt documente actuellement **l’articulation architecturale** entre l’observation runtime NeoMundi et la Détermination d’Admissibilité RiCo.

La prochaine étape prévue consiste à tester cette relation au moyen du **NeoMundi Runtime Interoperability JSON Contract**.

Le chemin de validation prévu est :

```text
Observation runtime NeoMundi
        │
        ▼
JSON d’interopérabilité
        │
        ▼
Consommation par RiCo
        │
        ▼
Détermination d’Admissibilité
        │
        ▼
Artefact / reçu de gouvernance
```

Lorsque cet échange aura été effectivement exécuté et préservé, le dépôt pourra évoluer d’un use case architectural d’interopérabilité vers un **pilote d’interopérabilité documenté**.

---

## Objet du dépôt

Ce dépôt conserve un cas de référence inspectable pour :

- l’observation runtime des systèmes IA ;
- l’interopérabilité avec une couche de gouvernance ;
- la détermination d’admissibilité ;
- l’architecture Runtime Execution Boundary ;
- la séparation entre mesure et autorité de gouvernance ;
- les Governance Receipts ;
- la gouvernance reconstructible ;
- une future interopérabilité machine-readable.

L’objectif n’est pas de fusionner NeoMundi et RiCo en une seule autorité.

La valeur de l’architecture vient précisément du maintien de l’indépendance des couches.

**NeoMundi fournit l’observation et la mesure runtime.**

**RiCo fournit la Détermination d’Admissibilité et l’architecture de gouvernance runtime.**

---

## Statut

**Use case architectural d’interopérabilité documenté.**

Actuellement documentés :

- rôle observationnel de NeoMundi ;
- rôle de gouvernance de RiCo ;
- Admissibility Determination ;
- Runtime Execution Boundary ;
- séparation entre mesure et autorité de gouvernance ;
- concept de Governance Receipt ;
- concept de Constitutional Replay ;
- architecture observation-to-admissibility.

### Prochaine étape de validation

- NeoMundi Runtime Interoperability JSON Contract ;
- échange machine-readable de l’observation ;
- consommation de l’observation par RiCo ;
- préservation de l’artefact de gouvernance résultant ;
- run d’interopérabilité end-to-end documenté.

---

## Ressources

### Richard Colmon / ManChine AI Technologies

**Richard Colmon**

Runtime Integrity Control (RiCo) · Architecture de gouvernance runtime des systèmes IA

- [LinkedIn](https://www.linkedin.com/in/richard-colimon-481645391/)
- [ManChine AI Technologies](https://manchine.ai/) — architecture de gouvernance runtime dédiée à l’intégrité, la continuité et la gouvernance conséquente des systèmes IA.
- [RGEP-01 — Runtime Governance Editorial & Publication Policy v1.0](https://manchine.ai/assets/whitepapers/RGEP-01_Runtime_Governance_Editorial_Publication_Policy.pdf)

### NeoMundi

- [NeoMundi Research](https://neomundi.org/)
- [ControlTower](https://controltower.neomundi.io/welcome)
- [Runtime Interoperability Contract](https://github.com/neomundi-io/runtime-interoperability-contract)
- [NeoMundi AI Observatory](https://github.com/neomundi-io/neomundi-ai-observatory)

---

## Attribution

Les concepts **Runtime Integrity Control (RiCo)**, **Runtime Execution Boundary (REB)**, **Admissibility Determination**, **Governance Receipt** et **Constitutional Replay** représentés dans ce dépôt sont attribués à :

**Richard Colmon — ManChine AI Technologies**

NeoMundi apporte la couche d’observation et de mesure runtime dans l’articulation documentée.

Le dépôt maintient intentionnellement la distinction entre :

- observation et mesure runtime ;
- interprétation de gouvernance ;
- détermination d’admissibilité ;
- enforcement de l’exécution.

Les mentions d’auteur et d’attribution doivent être conservées lorsqu’elles sont explicitement indiquées.
