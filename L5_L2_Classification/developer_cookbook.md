# Developer Cookbook — K_GRAPHIFY
**Stack:** Python 3.11, spaCy 3.7+, networkx 3.2+, RDFLib 7.0+, PAX 27B, AIOSS_FORMAT
**Domain:** Knowledge graph extraction: automatic graph construction from Anticloud project outputs

## Extract knowledge graph from project docs
```python
from k_graphify import GraphifyExtractor

extractor = GraphifyExtractor(
    pax_model="./pax-27b-q4.gguf",
    graph_path="./anticloud_graph.ttl",
    aioss_chain="./graphify.aioss"
)

extractor.extract_from_directory(
    "E:/fenta/Downloads/The Anticloud/TIER_7_BIOSIGNALS_NEURO/K_BRAINFLOW",
    domain="biosignals"
)
print(f"Nodes added: {extractor.last_result.nodes_added}")
print(f"Edges added: {extractor.last_result.edges_added}")
```

## SPARQL query
```python
from k_graphify import GraphQuery
gq = GraphQuery("./anticloud_graph.ttl")
# Find all TIER_7 projects with HIPAA compliance
rows = gq.sparql(
    "SELECT ?p ?r WHERE { ?p a :AnticloudProject . "
    "?p :hasRegulatory ?r . ?p :inTier :TIER_7 . }"
)
for row in rows:
    print(row.p, row.r)
```

## Export to PAX_KNOWLEDGE_GRAPH (T2)
```python
extractor.export_to_pax_kg("./pax_knowledge_graph/")
```

## Cross-tier relationship extraction
```python
extractor.extract_cross_tier_relationships(
    source_tier="TIER_7_BIOSIGNALS_NEURO",
    target_tier="TIER_4_INFERENCE_AGENTS",
    relationship_type="uses_model"
)
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
