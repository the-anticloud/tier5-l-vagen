# Deploy Guide — L_VAGEN
**Tier:** TIER_5_WORLD_NEURO_EMBODIED | **Stack:** Python 3.11, PyTorch 2.10+, torchvision, PAX 27B vision head, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PyTorch 2.10+, torchvision 0.17+, T4 GPU (vision processing + PAX inference).

## Environment
T4 GPU. Vision preprocessing: ~1GB VRAM. PAX 27B Q4: ~8GB VRAM. Total: ~9GB.

## AIOSS Integration
```bash
aioss init --module L_VAGEN --output ./l_vagen.aioss
aioss append --chain ./l_vagen.aioss --payload ./output.bin --module L_VAGEN
aioss verify --chain ./l_vagen.aioss
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
    module="L_VAGEN",
    aioss_chain="./L_VAGEN.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./L_VAGEN.aioss --verbose
python -m L_VAGEN.tests.smoke
```
