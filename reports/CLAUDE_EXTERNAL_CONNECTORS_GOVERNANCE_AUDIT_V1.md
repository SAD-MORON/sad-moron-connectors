# SAD-MORON-CONNECTORS — External Governance Audit V1

## Metadata

| Field | Value |
|---|---|
| Audit ID | CLAUDE_EXTERNAL_CONNECTORS_GOVERNANCE_AUDIT_V1 |
| Audit type | External documentation-only governance review |
| Audited repository | SAD-MORON/sad-moron-connectors |
| Governance source | SAD-MORON/sad-moron-framework |
| Audit date | 2026-05-27 |
| Auditor | Claude (claude-sonnet-4-6), acting as external governance reviewer |
| Scope | Connector governance consistency only |
| Exclusions | Runtime execution review, security pentest, implementation analysis |
| Artifact status | Append-only — do not modify this document; append new versions as V2, V3, etc. |

---

## Executive Summary

`SAD-MORON-CONNECTORS` is a documentation-first, pre-implementation connector specification repository for the SAD Moron institutional governance system.

The repository is correctly structured as a governed connector specification layer. Its boundary prohibitions are consistently stated, its framework dependency is explicit, and its connector packs correctly treat all connectors as pre-implementation. No runtime code, API, Apps Script, credentials, or scraping logic is present anywhere in the repository.

The primary governance issues are structural asymmetries between connector packs, a language risk in the root README that could invite premature runtime expansion, and the absence of a formal transition protocol to a future implementation repository such as `sad-moron-appscript`.

**Connector governance verdict: CONDITIONAL PASS.**

The repository passes as a governance-specification layer. Three items must be resolved before `sad-moron-appscript` can be safely created without governance leakage from this repository.

---

## 1. Framework Inheritance

### 1.1 Framework dependency declaration

The dependency on `sad-moron-framework` is declared at multiple layers:

- `README.md` explicitly names the framework URL and states that connector-layer documents may apply governance but cannot redefine governance, evidence semantics, normative scope, repository separation, or omission review meaning.
- `docs/framework-governance-reference.md` lists 8 specific governance domains that this repository depends on the framework for.
- `docs/connector-layer-boundary.md` Rule 2 states that connector-layer artifacts must inherit governance from `sad-moron-framework`.
- Both full connector packs (`sheets/compliance-rules.md` and `connectors/5650-900/compliance-rules.md`) open with an explicit governance inheritance statement.

**Finding: PASS.** The framework dependency is clearly declared, redundantly reinforced, and structurally embedded at the repository, document, and pack layers.

### 1.2 Connector rules subordinated to framework

All compliance-rules documents state explicitly that connector logic may apply framework rules but may not redefine:

- governance meaning
- evidence classes
- declared-source scope
- omission review boundaries
- normative document authority

The `docs/source-declaration-model.md` includes a `Connector Use Rule` that states "a connector must not create a broader source boundary than the declared source model allows" and "the connector layer consumes declared source meaning; it does not invent source authority."

**Finding: PASS.** Connector rules are correctly subordinated. The prohibition on governance redefinition is stated in at least four distinct documents.

### 1.3 Risk of accidental governance redefinition

No connector document contains language that widens, narrows, or reinterprets governance terms defined in the framework.

**Finding: PASS.** No accidental governance redefinition was detected. The consistent repetition of the same governance-inheritance header across all connector-level compliance documents reduces drift risk.

---

## 2. Repository Boundary

### 2.1 Documentation/specification-only character

Every document in the repository is specification or contract content. The file tree contains only `.md` files and a `.gitignore`. No source code files, scripts, configuration files for runtime services, or credential files are present.

**Finding: PASS.** The repository is documentation-only at time of audit.

### 2.2 Runtime, API, Apps Script, credential, and scraping exclusions

The following exclusions are stated at the repository root (`README.md` Prohibitions section):

- unrestricted scraping
- credential storage
- data extraction beyond declared boundary
- production execution
- runtime services
- API implementation
- Apps Script implementation

The `.gitignore` file explicitly blocks: `.env`, `credentials/`, `secrets/`, `tmp/`.

The `docs/connector-layer-boundary.md` Out of Scope section independently lists: executable connectors, runtime services, APIs, Apps Script, credential flows, scraping logic, synchronization behavior.

The `sheets/compliance-rules.md` Exclusions section independently names: authentication methods, API clients, Apps Script behavior, extraction mechanics, synchronization workflows.

**Finding: PASS.** Exclusions are stated redundantly and consistently.

### 2.3 Implementation boundary clarity

`docs/connector-layer-boundary.md` Rule 4 states: "Connector definitions remain pre-implementation until a later governed repository introduces bounded execution."

**Finding: PARTIAL.** The boundary is clear in its prohibition direction. However, the phrase "a later governed repository" does not name what that repository is. If `sad-moron-appscript` is the intended implementation repository, this repo does not formally declare the handoff protocol. See Ambiguity Risk A3 and Recommendation R5.

---

## 3. Connector Contracts

### 3.1 contracts/connector-contract.md

The document correctly defines:

- minimum contract elements (7 required fields)
- connector obligations including framework inheritance
- exclusion of executable interfaces
- a pre-implementation gate: "No connector should move into implementation until this governance contract is satisfied."

**Finding: PASS.** The contract is clear and well-scoped.

**Gap noted:** The document contains no cross-reference to which connectors have satisfied it, no status field, and no mechanism for tracking contract fulfillment. This is not a failure at the current stage, but will create ambiguity as the number of connector packs grows. See Recommendation R6.

### 3.2 contracts/source-contract.md

The document correctly defines:

- minimum source elements (7 required fields)
- source constraints including institutional intelligibility and temporal interpretability
- explicit exclusion of authentication, storage, and extraction mechanics

**Finding: PASS.** The source contract is clear and well-scoped.

**Gap noted:** This global-level document coexists with a pack-level `connectors/5650-900/source-contract.md`. There is no declared hierarchy between the two. See Inconsistency I3.

### 3.3 docs/source-declaration-model.md

The document correctly defines the connector use rule: a connector may exist only for a source already declared or intended to be declared under the governance framework. It explicitly excludes extraction logic, API fields, scraping selectors, and data transport formats.

**Finding: PASS.**

### 3.4 docs/connector-layer-boundary.md

The document defines four boundary rules cleanly: no execution, no governance redefinition, no unrestricted source access, no production posture.

**Finding: PASS.** This document is structurally sound and does not conflict with any other governance document reviewed.

---

## 4. Connector Packs

### 4.1 connectors/sheets/ — Completeness Assessment

| Required element | File present | Status |
|---|---|---|
| Source scope | `source-scope.md` | PRESENT |
| Declared events | `declared-events.md` | PRESENT |
| Temporal boundaries | `temporal-boundaries.md` | PRESENT |
| Compliance rules | `compliance-rules.md` | PRESENT |
| Known limitations | `known-limitations.md` | PRESENT |
| Open questions | — | ABSENT |
| Pack-level source contract | — | ABSENT |

**Finding: PARTIAL PASS.** The sheets pack is substantively complete for 5 of 7 elements. Two structural elements present in the `5650-900` pack are absent. See Inconsistency I1 and I2.

**Substantive quality assessment:**

- `source-scope.md` correctly defines institutional origin, allowed institutional use, excluded use (including "use of Sheets as an undefined general data lake"), and four boundary rules. Quality is high.
- `declared-events.md` defines 6 event families with governance use descriptions. All events are correctly framed as planning-level scaffolding with no implementation authority. The "Connector non-finality" rule (Rule 3) is explicit.
- `temporal-boundaries.md` addresses the mutable-source problem (overwrites, row reordering, tab restructuring, manual cleanup), defines the "no timeless omission rule," and correctly notes that snapshot expectation is a governance need without defining snapshot implementation.
- `compliance-rules.md` correctly inherits governance from the framework and explicitly excludes Apps Script behavior in its Exclusions section.
- `known-limitations.md` is substantively governance-aware, not merely technical. It lists schema drift, manual entry variability, historical incompleteness, and formatting ambiguity as governance-relevant constraints.

### 4.2 connectors/5650-900/ — Completeness Assessment

| Required element | File present | Status |
|---|---|---|
| Source scope | `source-scope.md` | PRESENT |
| Declared events | `declared-events.md` | PRESENT |
| Temporal boundaries | `temporal-boundaries.md` | PRESENT |
| Compliance rules | `compliance-rules.md` | PRESENT |
| Known limitations | `known-limitations.md` | PRESENT |
| Open questions | `open-questions.md` | PRESENT |
| Pack-level source contract | `source-contract.md` | PRESENT |

**Finding: PASS.** The `5650-900` pack is the most complete governance specification in the repository.

**Substantive quality assessment:**

- The treatment of `5650` and `900` as "declared source identifiers pending institutional confirmation" is correct and consistently maintained across all 8 files. No technical assumptions are made.
- `open-questions.md` lists 10 unresolved governance questions. All 10 are legitimately blocking. The framing "These questions are not optional refinement items. They are the minimum unresolved governance conditions for this connector boundary" is appropriately firm.
- The repeated "Implementation Block" section across all 8 pack files creates a multi-layer gate that prevents any document from being read as an implementation green-light in isolation.
- `declared-events.md` correctly restricts event planning to "identifying whether source-specific expected events may later need to be declared" — this is appropriately narrow for a source whose identity is not yet confirmed.

**Finding: PASS.** The 5650-900 connector is treated correctly as a pending declared source with all implementation gates in place.

### 4.3 Stub connectors (abc, administrative-acts, cobol, pofa)

All four stub connectors contain only a single README file with two or three sentences identifying the connector as a documentation-only placeholder. No implementation exists. All four correctly state "No implementation exists here."

**Finding: PASS for current state.** However, there is no formal protocol defining when a stub transitions to a full connector pack. See Over-Expansion Risk OE1.

---

## 5. Drift Risk

### 5.1 Pressure toward premature implementation

The repository does not contain language that creates urgency toward implementation. All connector packs are framed as pre-implementation or pending institutional confirmation.

**Finding: PASS.**

**Minor risk noted:** The `sheets/declared-events.md` defines 6 substantively detailed event families with named governance use patterns. While all events are correctly labeled "scaffold-level," the level of specificity (vacancy publication, POFA updates, assignment changes, manual correction records) could be read by a future implementer as a ready-to-implement specification. See Ambiguity Risk A2.

### 5.2 Apps Script isolation

Apps Script is named as a prohibited implementation method in:
- `README.md` Prohibitions
- `docs/connector-layer-boundary.md` Out of Scope
- `sheets/compliance-rules.md` Exclusions
- `sheets/README.md` Prohibitions

**Finding: PASS.** Apps Script is safely isolated as a prohibited category in the current repository. It is treated correctly as an out-of-scope implementation method, not as a pending reference.

**Gap noted:** There is no document in this repository that formally describes the relationship between `sad-moron-connectors` and a future `sad-moron-appscript` repository. When `sad-moron-appscript` is created, there will be no explicit governance handoff protocol from this repository. See Ambiguity Risk A3 and Recommendation R5.

### 5.3 5650/900 as pending declared sources

The treatment of `5650` and `900` across all 8 pack files is consistent and correct. Every document states "pending institutional confirmation" or "pending formal description in the declared sources catalog." No document treats them as active production connectors.

**Finding: PASS.**

---

## 6. Strengths

**S1. Multi-layer prohibition redundancy.**
The prohibitions against runtime code, APIs, Apps Script, credentials, and scraping are stated independently in at least 4 separate documents (root README, connector-layer-boundary.md, sheets/README.md, each compliance-rules.md). A single document being missed or misread cannot open an implementation door.

**S2. Consistent governance header across connector packs.**
Every governance-relevant file in both full connector packs opens with the same governance block listing the four governing protocols (framework, declared source, temporal boundary, evidence classification). This pattern makes governance inheritance verifiable at a glance.

**S3. Exemplary 5650-900 specification for a pending source.**
The `5650-900` pack is the correct model for how to treat an incompletely-understood institutional source. All 8 files are present. Implementation is blocked at every layer. Open questions are formally stated as blocking conditions.

**S4. Substantively correct temporal boundary discipline.**
The `sheets/temporal-boundaries.md` correctly addresses the mutable-source problem, defines the no-timeless-omission rule, and explicitly defers snapshot implementation without deferring snapshot governance awareness. This is governance-aware, not just documentation-complete.

**S5. Source declaration model correctly limits connector authority.**
The `docs/source-declaration-model.md` contains a critical governance principle: "the connector layer consumes declared source meaning; it does not invent source authority." This principle, if respected in future development, prevents connectors from becoming de facto governance actors.

**S6. .gitignore correctly excludes sensitive file types.**
The `.gitignore` explicitly blocks `credentials/`, `secrets/`, and `.env`. This is a structural barrier, not merely a documented prohibition.

**S7. Stub connectors are minimal and correctly scoped.**
The four stub connectors (abc, administrative-acts, cobol, pofa) correctly use only a README placeholder with no specification content. This avoids creating premature governance scaffolding for sources not yet ready for connector planning.

**S8. Commit history follows consistent governance naming.**
All three commits use the `SAD-MORON:` prefix and describe governance actions at the correct layer of abstraction.

---

## 7. Inconsistencies

**I1. sheets/ pack missing open-questions.md (asymmetry with 5650-900).**

The `5650-900` connector pack includes an `open-questions.md` that formally states 10 blocking governance questions. The `sheets/` pack has no equivalent document. This is asymmetric treatment. Google Sheets sources, while more technically accessible, have non-trivial open governance questions: which specific sheet families are declared, who is the institutional owner, what access method is authorized, and what audit expectations apply. The absence of this document does not create a governance failure at the current scaffold stage, but it creates asymmetry and reduces the formalism of the sheets connector's pre-implementation gate.

**I2. sheets/ pack missing pack-level source-contract.md (asymmetry with 5650-900).**

The `5650-900` connector pack includes a `source-contract.md` at the pack level that states the contract requirements the source must satisfy before implementation. The `sheets/` pack has no equivalent document. The global `contracts/source-contract.md` applies, but the absence of a pack-level contract means the sheets connector's implementation gate is less explicitly stated than the 5650-900 gate.

**I3. Two-tier source-contract documentation without declared hierarchy.**

`contracts/source-contract.md` (global) and `connectors/5650-900/source-contract.md` (pack-level) both exist but serve different levels of abstraction. There is no document that declares which is authoritative, whether the pack-level contract supplements or overrides the global contract, or how conflicts between them would be resolved. At the current stage this creates no practical conflict, but as pack-level contracts accumulate, the lack of hierarchy will become a governance ambiguity.

**I4. No connector status registry.**

Neither the root README nor any governance document contains a table or registry showing which connectors have satisfied the global `contracts/connector-contract.md`. At 2 full connector packs and 4 stubs, the governance state is inferrable from reading all files. At 10+ connectors, this will become unmanageable. There is currently no mechanism for an auditor to determine at a glance which connectors are stub, scaffold, pending-source-declaration, or implementation-blocked.

---

## 8. Ambiguity Risks

**A1. "This is not a runtime repository yet" creates implied future expansion within this repo.**

The root README concludes: "This is not a runtime repository yet." The word "yet" implies that this repository may eventually become a runtime repository. This is likely unintentional — the correct governance architecture would place runtime behavior in a separate governed repository. However, the current language does not make that explicit. A future maintainer reading this phrase could interpret it as authorization to eventually add runtime content to this repository when it is "time."

**A2. Sheets event families are substantively detailed enough to be misread as implementation-ready.**

The `sheets/declared-events.md` defines 6 event families (vacancy publication, administrative updates, POFA updates, assignment changes, status changes, manual correction records) with named governance use descriptions per family. All families are correctly labeled "scaffold-level" at the document level, but the status note appears once at the top. A reader who begins reading event definitions without the status header will encounter what appears to be a production event specification. The per-family governance use descriptions say "possible governance use: identifying whether..." which is correctly hedged, but "possible" could be read as "probable."

**A3. No formal governance handoff protocol to a future implementation repository.**

`docs/connector-layer-boundary.md` Rule 4 states that "connector definitions remain pre-implementation until a later governed repository introduces bounded execution." It does not name what that repository is, what governance conditions must be met before it can be created, or what artifacts this repository should produce before the handoff. If `sad-moron-appscript` is created without a formal reference in this repository, it may be unclear which connector packs are considered ready for implementation, which governance documents apply to the appscript layer, and what the change-control relationship between the two repositories is.

**A4. No formal activation criteria for stub connectors.**

Four stub connectors (abc, administrative-acts, cobol, pofa) exist as placeholders. There is no document defining what governance conditions must be satisfied for a stub to be promoted to a full connector pack. Without this protocol, the transition from stub to scaffold could happen informally and without adequate governance review.

---

## 9. Over-Expansion Risks

**OE1. Stub connectors have no governance-gated activation protocol.**

The stub connectors create named slots for future connector packs. Without a declared activation protocol, the transition from stub to scaffold could happen at any time, for any reason, without a formal review gate. As the system evolves, a stub could gradually accumulate specification content without triggering a formal governance review, effectively becoming a full connector pack through incremental drift rather than intentional promotion.

**OE2. The level of detail in sheets event families creates implementation pressure.**

The `sheets/declared-events.md` is substantively richer than would be needed for a pure governance placeholder. Six event families, each with a named governance use pattern, represent a planning artifact that is close to a functional specification. While no implementation pressure exists at the current stage, this document would be the most likely entry point for a future implementer to begin treating the connector as ready for development without completing the governance prerequisites (open-questions.md, pack-level source-contract.md).

**OE3. Compliance rules are repeated identically across packs with no shared inheritance mechanism.**

Both full connector packs contain a `compliance-rules.md` with 5 identical rules. As additional connector packs are created, the compliance rule set will be duplicated per pack. Without a shared inheritance mechanism, a future pack could silently alter or omit one of the 5 rules without it being detected as a governance deviation. The current duplication is harmless at 2 packs but represents a governance maintenance risk at scale.

---

## 10. Protocol Conflicts

**PC1. Global connector-contract.md has no per-connector fulfillment tracking.**

The global `contracts/connector-contract.md` defines what every connector must satisfy before implementation. However, there is no mechanism for confirming that a given connector has or has not satisfied this contract. The `sheets/` connector pack and `5650-900/` connector pack both address the required elements in their individual documents, but no document formally states "connector X has satisfied the global connector contract as of date Y." This creates a gap between the stated requirement and any auditable fulfillment record.

**PC2. The two-tier source-contract structure creates an unresolved precedence question.**

If the global `contracts/source-contract.md` and a pack-level `source-contract.md` ever diverge (e.g., the pack-level contract adds a requirement not in the global contract, or relaxes a requirement), there is no declared rule for which takes precedence. At the current stage the pack-level contract for `5650-900` is stricter than the global contract (it adds field-level requirements), which is safe. But this precedence question should be formally resolved before additional pack-level contracts are written.

**PC3. No formal integration between docs/framework-governance-reference.md and pack-level governance headers.**

The `docs/framework-governance-reference.md` is the authoritative statement of this repository's framework dependency. However, the per-pack compliance-rules.md files each independently declare their own governance inheritance list. If the framework dependency list in `framework-governance-reference.md` were updated, the per-pack lists would not automatically update. This creates a potential for silent divergence between the authoritative reference document and the per-pack governance claims.

---

## 11. Connector Governance Verdict

**CONDITIONAL PASS.**

### What passes

- The repository is correctly structured as a documentation-only, pre-implementation connector specification layer.
- Framework inheritance is clearly and redundantly declared.
- Connector rules are correctly subordinated to the framework.
- No connector can accidentally redefine governance under the current document structure.
- No runtime code, API, Apps Script, credentials, or scraping logic is present.
- All connector packs correctly treat their sources as pre-implementation.
- The 5650-900 connector is exemplary for a pending declared source.
- The sheets connector is substantively sound across all 5 present elements.
- Implementation boundaries are clear within this repository.

### What must be resolved before creating sad-moron-appscript

1. The language "This is not a runtime repository yet" must be corrected to explicitly redirect runtime behavior to a separate governed implementation repository. Without this, the handoff boundary is implied but not formally declared from this repository's side.
2. An explicit governance handoff protocol must be created that names `sad-moron-appscript` (or equivalent) as the implementation repository and defines what governance conditions must be satisfied in this repository before a connector is considered ready for implementation.
3. The sheets connector pack must be brought to structural parity with `5650-900` (open-questions.md and pack-level source-contract.md) before the sheets connector is treated as implementation-ready by any party.

---

## 12. Recommendations Before Creating sad-moron-appscript

**R1. Add open-questions.md to connectors/sheets/.**

Create `connectors/sheets/open-questions.md` following the `5650-900` model. Minimum questions should include: which specific sheet families are declared under institutional governance, who is the institutional owner of each declared sheet, what access method is authorized, what audit expectations apply per sheet family, and whether any sheets are already in scope for a known SAD Moron process.

**R2. Add source-contract.md to connectors/sheets/ at the pack level.**

Create `connectors/sheets/source-contract.md` following the `5650-900` model. This should state the specific source contract requirements that the Sheets connector must satisfy before implementation and include an explicit implementation-block statement.

**R3. Change "yet" language in README.md.**

Replace:

> This is not a runtime repository yet.

With:

> This is a pre-implementation specification repository. Runtime and execution behavior belongs exclusively in a separate governed implementation repository subordinate to `sad-moron-framework`.

This eliminates the implied future runtime expansion path within this repository.

**R4. Add a connector status table to README.md.**

Add a table listing each connector directory, its current governance status (stub / scaffold / pending-source-declaration / implementation-blocked / ready-for-handoff), and any known blocking conditions. This gives auditors and future maintainers a single entry point for governance state at the connector layer.

**R5. Create docs/implementation-handoff-protocol.md.**

Create a document that:
- names the expected future implementation repository (e.g., `sad-moron-appscript`)
- defines what governance conditions a connector must satisfy in this repository before it can be referenced for implementation
- defines what artifacts this repository should export or reference when the handoff occurs
- states that the handoff is governed and requires framework change-control discipline

This document should be referenced from `connector-layer-boundary.md` Rule 4.

**R6. Add a compliance checklist to contracts/connector-contract.md.**

Add a per-connector checklist section or a cross-reference table that allows a future maintainer to confirm which connectors have satisfied the global contract. This prevents the global contract from becoming a theoretical requirement with no auditable fulfillment path.

**R7. Clarify precedence between global and pack-level source contracts.**

Add a single paragraph to `contracts/source-contract.md` stating that pack-level source contracts may extend but not relax the global source contract requirements, and that in any conflict the more restrictive requirement applies.

---

## 13. Major Findings Summary

| # | Category | Severity | Finding |
|---|---|---|---|
| F1 | Inconsistency | Minor | sheets/ connector pack lacks open-questions.md (asymmetry with 5650-900) |
| F2 | Inconsistency | Minor | sheets/ connector pack lacks pack-level source-contract.md (asymmetry with 5650-900) |
| F3 | Ambiguity Risk | Moderate | README "yet" language implies future runtime expansion within this repository |
| F4 | Ambiguity Risk | Moderate | No formal governance handoff protocol to a future implementation repository |
| F5 | Inconsistency | Minor | Two-tier source-contract structure has no declared precedence rule |
| F6 | Over-Expansion | Low | Stub connectors have no governance-gated activation criteria |
| F7 | Protocol Conflict | Low | Compliance rules duplicated per pack with no shared inheritance mechanism |
| F8 | Inconsistency | Low | No connector status registry at repository level |

---

## 14. Whether Connector Boundaries Remain Preserved

**Yes, with qualification.**

All connector boundaries are structurally preserved at the time of this audit. No file in the repository violates the declared boundaries. No implementation, runtime code, API, Apps Script, credential, or scraping content exists.

The qualification is that two of the identified risks (A1 and A3 — the "yet" language and the absent handoff protocol) represent boundary ambiguities rather than boundary violations. The boundaries are preserved, but they are not fully formalized at the transition point to a future implementation repository. This means the boundary is enforced by prohibition today, but not by structural declaration. Creating `sad-moron-appscript` without resolving A1 and A3 first would leave the governance handoff zone under-specified.

---

*Audit V1 complete. This document is append-only. Do not modify. Append new audit versions as CLAUDE_EXTERNAL_CONNECTORS_GOVERNANCE_AUDIT_V2.md or by appending a dated section below.*
