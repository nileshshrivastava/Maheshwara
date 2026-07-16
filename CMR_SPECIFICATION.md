# CMR_SPECIFICATION.md

**Document ID:** SPEC-001
**Title:** Canonical Maheshwara Representation (CMR) Specification
**Version:** 1.0
**Status:** Draft Standard
**Date:** 16 July 2026
**Project:** Maheshwara

---

# Canonical Maheshwara Representation (CMR)

> **A faithful, canonical, minimal, and lossless computational representation of the Maheshwara Sutras.**

---

# 1. Purpose

This specification defines the Canonical Maheshwara Representation (CMR).

CMR is the foundational representation used throughout the Maheshwara Project.

Its purpose is to preserve the Maheshwara Sutras exactly as a computational object without introducing interpretation, grammatical theory, or derived knowledge.

Every implementation of the Maheshwara Project shall conform to this specification.

---

# 2. Scope

This specification defines:

* what CMR is,
* what information belongs in CMR,
* what information does not belong in CMR,
* the properties that every conforming implementation must preserve.

This specification does **not** define algorithms, grammatical analysis, phonetic interpretation, or application-specific behavior.

---

# 3. Source

The source of CMR is the traditional sequence of the fourteen Maheshwara Sutras.

CMR is derived directly from this sequence and from no other source.

No implementation may alter, reorder, omit, or insert symbols into the canonical sequence.

---

# 4. Definitions

For the purposes of this specification:

**Symbol**
A single written unit occurring within the Maheshwara Sutras.

**Marker**
A symbol traditionally functioning as an anubandha. Within CMR, markers are preserved exactly as they appear in the source and are not treated differently at the representation level.

**Sutra**
One ordered sequence of symbols within the fourteen Maheshwara Sutras.

**CMR**
The complete canonical representation formed directly from the sutras.

---

# 5. Design Objectives

CMR shall satisfy the following objectives:

1. Faithfulness
2. Completeness
3. Minimality
4. Canonicality
5. Losslessness
6. Reproducibility
7. Implementation Independence

These objectives take precedence over implementation convenience.

---

# 6. Fundamental Axioms

## Axiom 1 — Faithfulness

CMR shall preserve every symbol appearing in the source.

No symbol may be modified.

---

## Axiom 2 — Order Preservation

The order of symbols is part of the information.

No implementation may change that order.

---

## Axiom 3 — Completeness

No symbol may be omitted.

No symbol may be added.

---

## Axiom 4 — Losslessness

The original Maheshwara Sutras shall be reconstructable exactly from CMR.

---

## Axiom 5 — Minimality

CMR shall contain only information necessary to reconstruct the original source.

Any information that can be algorithmically derived shall not be permanently included within CMR.

---

## Axiom 6 — Canonicality

Given the same source, every conforming implementation shall produce an identical CMR.

There shall exist only one canonical representation.

---

## Axiom 7 — Immutability

CMR is immutable.

Algorithms may observe CMR.

Algorithms may derive information from CMR.

Algorithms shall never modify CMR.

---

# 7. Structure

CMR consists only of the canonical sequence of the fourteen Maheshwara Sutras.

Each sutra preserves:

* its position within the sequence,
* the order of its symbols,
* every symbol exactly as present in the source.

No additional metadata forms part of CMR.

---

# 8. Information Explicitly Excluded

The following shall **not** be stored within CMR:

* grammatical classes
* vowel classifications
* consonant classifications
* articulatory locations
* phonetic descriptions
* Unicode properties beyond the source text
* linguistic metadata
* parser annotations
* application-specific identifiers
* derived relationships

Such information may be derived by algorithms or introduced by higher-level models, but it is not part of CMR itself.

---

# 9. Derived Knowledge

Knowledge produced through computation is considered derived.

Examples include:

* phonetic grouping
* pratyāhāra expansion
* articulatory classification
* graph structures
* adjacency relationships
* search indices

Derived knowledge belongs to computational layers above CMR.

It shall never become part of the canonical representation.

---

# 10. Primitive Operations

CMR defines no grammatical operations.

It merely provides a canonical object upon which operations may act.

Primitive operations shall be specified independently.

Future specifications may define:

* traversal
* observation
* selection
* transformation
* validation

without altering CMR itself.

---

# 11. Validation Requirements

An implementation conforms to this specification if it satisfies the following conditions:

1. Every source symbol is preserved.
2. Symbol order is preserved.
3. Sutra order is preserved.
4. The original sutras can be reconstructed exactly.
5. No undocumented information is introduced.
6. No canonical information is lost.

---

# 12. Non-Goals

CMR is **not** intended to:

* explain Sanskrit grammar,
* replace grammatical theory,
* perform phonetic analysis,
* classify sounds,
* generate linguistic interpretations,
* optimize storage,
* serve as an NLP model.

These tasks belong to higher computational layers.

---

# 13. Implementation Independence

CMR is independent of programming language.

A conforming implementation may be written in:

* Python
* C
* Rust
* Java
* Haskell
* or any other language.

Correctness is determined by conformance to this specification, not by implementation details.

---

# 14. Layered Architecture

The Maheshwara Project is organized into distinct layers:

Layer 0 — Source
The Maheshwara Sutras.

↓

Layer 1 — CMR
Canonical representation defined by this specification.

↓

Layer 2 — Primitive Operations
Fundamental computational operations acting upon CMR.

↓

Layer 3 — Derived Structures
Graphs, indices, classifications, and other computed objects.

↓

Layer 4 — Applications
Grammar engines, search systems, visualization tools, educational software, research experiments, and future computational models.

Each layer depends only upon lower layers.

Lower layers never depend upon higher layers.

---

# 15. Compliance

An implementation claiming compliance with SPEC-001 shall document:

* the source used,
* the method of construction,
* validation procedures,
* specification version.

Any deviation from this specification shall be explicitly documented.

---

# 16. Future Evolution

Future versions of this specification may clarify definitions or improve precision.

However, backward compatibility should be preserved whenever possible.

Changes that alter the canonical representation require a new major version of the specification.

---

# Closing Statement

The Canonical Maheshwara Representation is not an interpretation of the Maheshwara Sutras.

It is a faithful computational foundation upon which interpretations may be explored.

By preserving only what is present in the source and requiring all additional knowledge to be explicitly derived, CMR provides a stable reference that remains independent of implementation, programming language, and evolving research.

Every future algorithm, experiment, and application within the Maheshwara Project begins here.

---

> **Nothing is assumed. Everything is derived.**

---

**This specification is a living standard of the Maheshwara Project and may evolve through documented research, community review, and reproducible evidence while preserving its commitment to canonical representation.**
