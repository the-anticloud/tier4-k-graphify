# L5 Narrow / L2 General Classification — K_GRAPHIFY
**Platform:** Anticloud | **Tier:** TIER_4_INFERENCE_AGENTS | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
K_GRAPHIFY specializes in extracting structured knowledge graphs from Anticloud documentation, AIOSS chain entries, benchmark results, and compliance reports. Narrow scope: Anticloud domain entity extraction only — not general NLP graph construction for arbitrary corpora.

## L2 General
L2 General: K_GRAPHIFY builds the shared knowledge graph that all tiers can query via SPARQL. TIER_7 biosignal entities and TIER_9 robotics entities coexist in the same graph with cross-domain relationship edges.

## PAX 27B Integration
PAX 27B performs entity extraction and relation classification: given a document, PAX identifies Anticloud named entities and their relationships for graph insertion. Each graph mutation (batch of entities + edges) is AIOSS-chained.

## AIOSS Audit Chain
Every graph mutation (document hash + extracted entities hash + new edges hash + graph state hash) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
ISO/IEC 42001 (knowledge representation for AI systems). NIST SP 800-188 (de-identification).
