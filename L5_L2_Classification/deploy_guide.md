# Deploy Guide — K_GRAPHIFY
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, spaCy 3.7+, networkx 3.2+, RDFLib 7.0+, PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, spaCy 3.7+ (en_core_web_trf, ~1.5GB), networkx 3.2+, rdflib 7.0+, PAX 27B.

## Environment
8GB RAM for 1M-node graph. GPU for PAX entity extraction. spaCy transformer model requires ~1.5GB VRAM.

## AIOSS Integration
```bash
aioss init --module K_GRAPHIFY --output ./k_graphify.aioss
aioss append --chain ./k_graphify.aioss --payload ./output.bin --module K_GRAPHIFY
aioss verify --chain ./k_graphify.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_GRAPHIFY",
    aioss_chain="./K_GRAPHIFY.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_GRAPHIFY.aioss --verbose
python -m K_GRAPHIFY.tests.smoke
```
