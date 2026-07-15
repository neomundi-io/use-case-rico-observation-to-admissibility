# NeoMundi–RiCo Minimal Field Mapping

**Version:** v0.1  
**Status:** Working draft  
**Scope:** Synthetic interoperability pilot  
**Purpose:** Define the minimum information required to connect a NeoMundi runtime observation with a RiCo admissibility assessment and governance receipt, while preserving clear responsibility boundaries.

---

## 1. Architectural Boundary

NeoMundi produces runtime observations and measurement signals.

RiCo evaluates whether execution remains admissible under the applicable authority, policy, evidence and context.

A NeoMundi signal does not directly impose an execution consequence. RiCo remains responsible for determining whether execution should continue, require review, be held, or be denied.

---

## 2. Minimal Field Mapping

| NeoMundi field | Meaning | RiCo use | Responsibility owner |
|---|---|---|---|
| `schema_version` | Version of the NeoMundi observation schema | Confirms how the observation record should be interpreted | NeoMundi |
| `observation_id` | Unique identifier of the observation | Primary reference from the RiCo governance receipt to the NeoMundi record | NeoMundi |
| `trace_id` | Identifier linking observations belonging to the same execution or trace | Correlates the runtime observation with the governed execution | Shared reference |
| `generated_at` | Time at which the observation record was generated | Supports temporal reconstruction of the governance sequence | NeoMundi |
| `prompt_family` | Functional or methodological category of the observed request | Provides context for applying the appropriate policy or admissibility rules | NeoMundi |
| `coverage_rate` | Proportion of the execution covered by the available measurement | Allows RiCo to distinguish a complete observation from partial measurement | NeoMundi |
| `stability_mean` | Aggregate behavioral stability observed during execution | Contextual evidence for admissibility assessment | NeoMundi |
| `semantic_variation_rate` | Observed rate of semantic variation or instability | May trigger review or additional verification under RiCo policy | NeoMundi |
| `factual_risk_mean` | Aggregate factual-risk signal, where applicable | Supports proportionate factual-verification requirements | NeoMundi |
| `coherence_score` | Aggregate coherence measurement, where available | Additional contextual evidence for admissibility assessment | NeoMundi |
| `regime` | Observed runtime behavioral regime | Helps RiCo identify whether the execution remains within expected operational conditions | NeoMundi |
| `observation_class` | Classification such as `within_bounds`, `flagged`, or `incomplete` | Initial evidence input for the RiCo admissibility evaluation | NeoMundi |
| `limitations` | Known methodological, coverage or interpretation limitations | Prevents RiCo from treating the measurement as conclusive or complete beyond its scope | NeoMundi |
| `payload_hash` | Cryptographic hash of the complete observation payload | Enables integrity verification and binding to the RiCo governance receipt | NeoMundi |
| `key_id` | Identifier of the signing or verification key, where used | Enables verification of the observation source | NeoMundi |
| `signature` | Cryptographic signature of the observation object, where implemented | Supports source authentication and integrity verification | NeoMundi |
| `authorization_status` | Observed authorization context, where available | Provides contextual input but does not determine admissibility | Source system / NeoMundi |
| `execution_permission_changed` | Indicates whether an external governance component changed execution permission | Allows reconstruction of whether an observation was followed by a governance consequence | RiCo or execution boundary |

---

## 3. RiCo Governance Fields

The following fields belong to the RiCo governance domain and should not be produced or decided by NeoMundi.

| RiCo field | Meaning | NeoMundi relationship | Responsibility owner |
|---|---|---|---|
| `governance_receipt_id` | Unique identifier of the governance receipt | References the related NeoMundi `observation_id` | RiCo |
| `execution_id` | Identifier of the governed execution | May correspond to the shared `trace_id` | Shared reference / RiCo |
| `observation_reference` | Reference to the NeoMundi observation record | Contains `observation_id` and `payload_hash` | RiCo |
| `applicable_authority` | Authority under which the execution is evaluated | Not determined by NeoMundi | RiCo |
| `applicable_policy` | Policy or rule set applied to the execution | May use NeoMundi observations as evidence | RiCo |
| `policy_version` | Version of the policy used | Supports reconstructability and auditability | RiCo |
| `admissibility_state_before` | State before evaluation | Independent from the NeoMundi observation class | RiCo |
| `admissibility_state_after` | Resulting admissibility state | Determined by RiCo policy and authority | RiCo |
| `transition` | Governance transition applied | Examples: `continue`, `review_required`, `hold`, `deny`, `resume` | RiCo |
| `transition_reason` | Reconstructable reason for the transition | May reference one or more NeoMundi signals | RiCo |
| `execution_permission` | Whether execution is permitted after evaluation | Consequence-bearing decision | RiCo |
| `exit_conditions` | Conditions required to leave `review_required` or `hold` | Must be explicit and reconstructable | RiCo |
| `evaluated_at` | Time of the admissibility evaluation | Supports sequencing against `generated_at` | RiCo |
| `receipt_hash` | Hash of the governance receipt | Enables integrity verification | RiCo |
| `signature` | Signature of the governance receipt, where implemented | Independent from the NeoMundi signature | RiCo |

---

## 4. Proposed Admissibility States

The initial pilot may use the following limited state set:

| State | Meaning |
|---|---|
| `admissible` | Execution may continue under the applicable policy and authority |
| `review_required` | Human or additional automated review is required, without automatically suspending execution |
| `hold` | Execution is temporarily suspended under an explicit policy rule |
| `denied` | Execution is not authorized to proceed |
| `indeterminate` | Available evidence is insufficient to determine admissibility |

`review_required` must not be treated as equivalent to `hold` or `denied`.

---

## 5. Proposed Execution-Boundary Transitions

| From | To | Minimum requirement |
|---|---|---|
| `admissible` | `review_required` | A policy-defined condition requiring additional review |
| `admissible` | `hold` | Explicit policy and authority supporting temporary suspension |
| `admissible` | `denied` | Explicit policy and authority supporting denial |
| `review_required` | `admissible` | Completion of the stated review or exit conditions |
| `review_required` | `hold` | New evidence or policy condition justifying suspension |
| `hold` | `admissible` | Explicitly satisfied exit conditions and renewed authorization |
| `hold` | `denied` | Confirmed policy or authority basis for denial |
| `indeterminate` | Any state | Acquisition of sufficient evidence and application of an explicit policy rule |

---

## 6. Minimal Governance Receipt Example

```json
{
  "schema_version": "0.1",
  "governance_receipt_id": "rico-receipt-001",
  "execution_id": "synthetic-execution-001",
  "synthetic": true,
  "observation_reference": {
    "provider": "NeoMundi",
    "observation_id": "nm-observation-001",
    "trace_id": "synthetic-execution-001",
    "payload_hash": "sha256:..."
  },
  "applicable_authority": {
    "authority_id": "synthetic-authority-001",
    "authority_type": "delegated_execution_authority"
  },
  "applicable_policy": {
    "policy_id": "synthetic-policy-001",
    "policy_version": "0.1"
  },
  "admissibility_state_before": "admissible",
  "admissibility_state_after": "review_required",
  "transition": "review_required",
  "transition_reason": {
    "rule_id": "POLICY-RULE-01",
    "evidence_references": [
      "nm-observation-001"
    ],
    "summary": "Additional verification required under the applicable policy."
  },
  "execution_permission": {
    "status": "unchanged",
    "authorized": true
  },
  "exit_conditions": [
    "Complete the required factual verification",
    "Record the verification result",
    "Re-evaluate admissibility under policy version 0.1"
  ],
  "evaluated_at": "2026-07-15T00:00:00Z",
  "receipt_hash": "sha256:...",
  "signature": null
}
