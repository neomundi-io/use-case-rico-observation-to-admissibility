# NeoMundi × ManChine — Observation to governed execution

**Independent measurement. Explicit admissibility. Governed execution. Runtime continuity.**

**Status: architectural interoperability documented. Machine-to-machine validation remains pending.**

NeoMundi, RGE-01, REB-01 and RiCo-01 form four complementary responsibilities. None silently inherits another's authority.

[Français](#version-française)

## Explore NeoMundi

[![Station](https://img.shields.io/badge/Station-Observe_%26_experiment-7c3aed?style=flat-square)](https://github.com/neomundi-io/neomundi-station-public)
[![Runtime Measurement](https://img.shields.io/badge/Runtime_Measurement-Measure_%26_integrate-2563eb?style=flat-square)](https://github.com/neomundi-io/neomundi-runtime-measurement)
[![Use Cases](https://img.shields.io/badge/Use_Cases-Pilots_%26_evidence-059669?style=flat-square)](https://github.com/neomundi-io/neomundi-use-cases)
[![Create an Account](https://img.shields.io/badge/Create_an_Account-ControlTower-ea580c?style=flat-square)](https://controltower.neomundi.io/welcome)

# English

## Use case in plain terms

Can an independent runtime observation inform governance before and during consequential execution without turning the measurement layer into decision or execution authority?

The documented architecture answers by separating four functions:

```text
NeoMundi observation
        ↓ evidence
RGE-01 — Admissibility Determination before activation
        ↓ applicable governance state
REB-01 — governs crossing the consequential execution boundary
        ↓ activated execution
RiCo-01 — examines governance continuity after activation
```

## Responsibility map

| Component | Current functional allocation | Does not do |
| --- | --- | --- |
| **NeoMundi — Observation / Measurement** | Produces measurement signals and observational evidence. | Does not decide admissibility, apply policy or authorize execution. |
| **RGE-01 — Admissibility Determination** | Evaluates Authority, Evidence, Context and Policy at the applicable decision point before activation. | Does not inherit measurement authority or perform execution. |
| **REB-01 — Runtime Execution Boundary** | Governs whether consequential execution may cross the boundary and applies the applicable governance state. | Does not create the measurement or replace RGE-01. |
| **RiCo-01 — Runtime Governance Continuity** | After activation, examines continuity of the governance correspondence and any effect on portability of prior governance. | Does not itself produce the Admissibility Determination. |

## Intended interfaces and flow

A future validation run is expected to preserve:

1. a NeoMundi observation under the applicable interoperability contract;
2. explicit ingestion as observational evidence;
3. an RGE-01 Admissibility Determination at the relevant pre-activation decision point;
4. REB-01 application of the governance state at the execution boundary;
5. RiCo-01 continuity examination after activation;
6. separate, reconstructable artifacts for each responsibility.

A missing, null, unavailable or insufficiently covered measurement must not be converted into affirmative governance evidence.

## What is documented

- the four-responsibility architecture;
- sample NeoMundi observation payloads and historical RiCo assessments;
- working field-mapping and observation-to-execution documents;
- the requirement that measurement never becomes execution authority;
- forward-looking alignment with RGC v0.2 as an intended interface.

Examples, mappings and payloads are architectural artifacts. They are not evidence of a live integration.

## Historical formulation

Earlier documents in this repository used a historical formulation in which RiCo was described as producing the Admissibility Determination. Those documents remain preserved and traceable as working drafts.

The current ManChine allocation distinguishes:

- **RGE-01:** pre-activation Admissibility Determination;
- **REB-01:** execution-boundary governance;
- **RiCo-01:** post-activation Runtime Governance Continuity.

This README clarifies the current allocation; it does not rewrite historical artifacts as if they had always expressed it.

## What remains unverified

This repository does not demonstrate a complete machine-to-machine exchange, production deployment, regulatory certification, empirical performance across models, a live RGC v0.2 integration, or execution authorization by NeoMundi. Payload examples do not prove operational behavior.

## Next validation step

Run and preserve one bounded end-to-end exchange that keeps the NeoMundi observation, RGE-01 determination, REB-01 boundary application and RiCo-01 continuity examination technically distinct and independently reviewable.

## Resources and attribution

- [Current Use Cases index](https://github.com/neomundi-io/neomundi-use-cases)
- [NeoMundi Runtime Measurement](https://github.com/neomundi-io/neomundi-runtime-measurement)
- [Historical observation-to-execution draft](./docs/rico_observation_to_execution_chain_v0.1.md)
- [Historical minimal field mapping](./NEOMUNDI_RICO_MINIMAL_FIELD_MAPPING_v0.1.md)
- [Sample payloads](./payloads/)
- [ManChine AI Technology LLC](https://manchine.ai/)
- [RGEP-01 publication policy](https://manchine.ai/assets/whitepapers/RGEP-01_Runtime_Governance_Editorial_Publication_Policy.pdf)

RGE-01, REB-01, RiCo-01, Runtime Governance Continuity, Admissibility Determination, Governance Receipt and related ManChine concepts are attributed to **Richard Colimon / ManChine AI Technology LLC**. NeoMundi contributes only the independent observation and measurement layer described here.

---

# Version française

## Le cas d'usage simplement

Une observation runtime indépendante peut-elle informer la gouvernance avant et pendant une exécution conséquente sans transformer la mesure en autorité de décision ou d'exécution ?

```text
Observation NeoMundi
        ↓ preuve
RGE-01 — Admissibility Determination avant activation
        ↓ état de gouvernance applicable
REB-01 — gouverne le franchissement de la frontière d'exécution
        ↓ exécution activée
RiCo-01 — examine la continuité de gouvernance après activation
```

## Carte des responsabilités

| Composant | Allocation fonctionnelle actuelle | Ne fait pas |
| --- | --- | --- |
| **NeoMundi — Observation / Measurement** | Produit les signaux de mesure et les preuves observationnelles. | Ne décide pas de l'admissibilité, n'applique pas de politique et n'autorise pas l'exécution. |
| **RGE-01 — Admissibility Determination** | Évalue Autorité, Preuve, Contexte et Politique au point de décision applicable avant activation. | N'hérite pas de l'autorité de mesure et n'exécute pas. |
| **REB-01 — Runtime Execution Boundary** | Gouverne le franchissement de la frontière d'exécution conséquente et applique l'état de gouvernance applicable. | Ne produit pas la mesure et ne remplace pas RGE-01. |
| **RiCo-01 — Runtime Governance Continuity** | Après activation, examine la continuité de la correspondance de gouvernance et ses effets éventuels sur la portabilité de la gouvernance antérieure. | Ne produit pas lui-même l'Admissibility Determination. |

## Interfaces et flux envisagés

Une future validation doit préserver séparément : l'observation NeoMundi, son ingestion comme preuve, la détermination RGE-01 avant activation, l'application REB-01 à la frontière, l'examen de continuité RiCo-01 après activation et les artefacts reconstructibles associés.

Une mesure absente, nulle, indisponible ou insuffisamment couverte ne doit pas devenir une preuve de gouvernance affirmative.

## Ce qui est documenté

L'architecture des quatre responsabilités, des payloads d'exemple, les documents historiques de mapping et de chaîne, la séparation mesure/autorité et un alignement prospectif avec RGC v0.2. Ces exemples ne prouvent pas une intégration live.

## Formulation historique

Les documents antérieurs attribuaient historiquement l'Admissibility Determination à RiCo. Ils restent conservés comme working drafts traçables.

L'allocation ManChine actuelle distingue **RGE-01** pour la détermination avant activation, **REB-01** pour la frontière d'exécution et **RiCo-01** pour la continuité après activation. Ce README clarifie l'allocation actuelle sans réécrire rétroactivement les archives.

## Ce qui reste non vérifié

Aucun échange machine-à-machine complet, déploiement de production, certification réglementaire, performance empirique multi-modèles, intégration live RGC v0.2 ou autorisation d'exécution par NeoMundi n'est démontré. Les payloads ne constituent pas une preuve de fonctionnement opérationnel.

## Prochaine étape

Exécuter et préserver un échange end-to-end borné gardant techniquement distincts l'observation NeoMundi, la détermination RGE-01, l'application REB-01 et l'examen de continuité RiCo-01.

## Ressources et attribution

- [Index Use Cases](https://github.com/neomundi-io/neomundi-use-cases)
- [Runtime Measurement](https://github.com/neomundi-io/neomundi-runtime-measurement)
- [Draft historique de la chaîne](./docs/rico_observation_to_execution_chain_v0.1.md)
- [Mapping historique](./NEOMUNDI_RICO_MINIMAL_FIELD_MAPPING_v0.1.md)
- [Payloads d'exemple](./payloads/)
- [ManChine AI Technology LLC](https://manchine.ai/)
- [Politique RGEP-01](https://manchine.ai/assets/whitepapers/RGEP-01_Runtime_Governance_Editorial_Publication_Policy.pdf)

RGE-01, REB-01, RiCo-01, Runtime Governance Continuity, Admissibility Determination, Governance Receipt et les concepts ManChine associés sont attribués à **Richard Colimon / ManChine AI Technology LLC**. NeoMundi apporte uniquement la couche indépendante d'observation et de mesure décrite ici.
