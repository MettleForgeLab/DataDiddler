# DataDiddler

DataDiddler is a **deterministic meaning compiler** for inspecting, structuring, and reasoning about data.

It takes large, messy collections of documents and mechanically narrows them into structured, inspectable meaning — without using machine learning or probabilistic inference at runtime.

At its core, DataDiddler answers a single question:

> Under what conditions is a piece of data worth keeping?

---

## What DataDiddler Is

DataDiddler operates by applying explicit, inspectable rules (“hooks”) that detect moments of significance, attach traceable evidence, and organize results into overlapping semantic buckets.

The result is not a guess about meaning, but a grounded structure that shows:
- what was detected
- where it came from
- and why it was captured

DataDiddler favors constraint over inference, inspection over automation, and traceability over scale.

---

## Conceptual Model

DataDiddler is built from four primary concepts.

### Hooks
A **hook** is a detection rule paired with a capture instruction.

Hooks evaluate constrained conditions over normalized fragments of data. When a condition is met, a hook emits a signal — such as a claim, entity, or event — along with:
- an anchor (where it was found)
- the excerpt that triggered it
- the reason it was captured

Hooks are declarative in intent and imperative in execution. They do not infer or guess; they trigger when explicitly defined conditions are satisfied.

Think of hooks as *semantic tripwires*.

---

### Buckets
Buckets are organizational containers for signals emitted by hooks.

They are:
- overlapping
- non-exclusive
- extensible

A single detected element can land in multiple buckets simultaneously. Buckets behave more like **views** than folders, allowing the same underlying evidence to be examined from multiple semantic angles.

---

### Tags
Tagging in DataDiddler is **additive**, never destructive.

Original input data is always preserved. Tags are layered on top as metadata and can be:
- hierarchical
- compositional
- confidence-weighted

Nothing is removed from the source. Meaning is accumulated, not collapsed.

---

### Lenses
A lens is not software.

It is a **methodology for reading structured meaning** — a discipline for deciding what matters, what to trust, and what to question once data has been diddled.

Mettle Forge Lab develops lenses that guide:
- which hooks are written
- how buckets are interpreted
- how salience is evaluated

Lenses operate before and after DataDiddler runs, not during execution.

---

## How DataDiddler Works (Conceptually)

DataDiddler operates as a strictly ordered, multi-pass pipeline. Each stage reduces ambiguity and narrows the search space through constraint, not inference.

1. **Ingest and Normalize**  
   Input documents are normalized to remove irrelevant variation such as encoding inconsistencies, layout artifacts, and formatting noise.

2. **Rake (Artifact Creation)**  
   Documents are broken into bounded artifacts — small, enumerable text surfaces. Hooks never operate on entire documents.

3. **Separation**  
   Artifacts are classified by context (narrative text, tables, headers, metadata-like regions).

4. **Hook Evaluation**  
   Hooks scan progressively transformed input and emit fully traceable signals when conditions are satisfied.

5. **Triage**  
   Signals are evaluated for salience. Ambiguous and edge cases are preserved as first-class outputs.

6. **Tagging**  
   Signals are enriched with additive tags that add structure without deleting information.

7. **Weaving**  
   Detected elements are connected via explicit, rule-based relationships.

8. **Packaging**  
   Each run produces immutable artifacts: structured datasets, indexes, evidence reports, and execution logs.

Every run is deterministic. Intelligence does not persist between runs.

---

## Provenance and Construction

DataDiddler is a distinctly unusual artifact.

The system was designed and implemented **entirely through collaboration with an artificial intelligence system (Aria)**. Human involvement consisted of:
- directing intent
- articulating constraints
- selecting and assembling outputs
- and performing manual copy-and-paste integration

No human-authored source code was written from first principles. All operational logic, structure, and implementation detail originated from the AI system under guided iteration.

This provenance matters because it explains several properties of DataDiddler:
- the rule-dense architecture
- the emphasis on explicit constraints
- the absence of implicit assumptions
- and the system’s strong separation between design-time intelligence and runtime mechanics

---

## Built With AI, Not Powered by AI

Artificial intelligence was used extensively at **design time** to explore architecture, generate code, and iterate on structure.

At runtime, however, DataDiddler uses:
- no machine learning models
- no probabilistic inference
- no embeddings
- no LLM calls

All runtime behavior is deterministic, rule-based, and auditable.

Any sense of “intelligence” comes from the accumulation and ordering of explicit constraints — not from learned behavior.

In other words: AI helped build the tool, but the tool itself runs on mechanics.

---

## What DataDiddler Is Not

- It does not attempt to “understand” documents
- It does not guess intent
- It does not replace analysis or judgment
- It does not automate decisions

DataDiddler is the **entry point**: a front-end meaning compiler that turns documents into inspectable, structured material suitable for careful human or downstream machine interpretation.

---

## Releases

The initial release of DataDiddler publishes the system’s conceptual and ethical foundations.

Executable artifacts will be distributed via GitHub Releases as they become available.
