# Developer Cookbook — L_VAGEN
**Stack:** Python 3.11, PyTorch 2.10+, torchvision, PAX 27B vision head, AIOSS_FORMAT
**Domain:** VAgent: vision-action agent for multi-modal PAX 27B with camera and sensor inputs

## Vision-grounded action
```python
from l_vagen import VAgentPipeline

pipeline = VAgentPipeline(
    pax_model="./pax-27b-q4.gguf",
    vision_encoder="./vision_encoder.pt",
    aioss_chain="./vagen.aioss"
)

# Robot camera + language command
result = pipeline.act(
    image=robot_camera_frame,  # numpy HxWx3
    command="Pick up the red cylinder on the left shelf",
    return_action_type="joint_delta"
)
print(f"Action: {result.joint_delta}")
print(f"Object detected: {result.detected_object}")
print(f"Confidence: {result.confidence:.2f}")
```

## Medical image analysis
```python
report = pipeline.analyze_image(
    image=mri_slice,
    query="Identify any lesions visible in this MRI slice",
    domain="clinical"
)
print(report.findings)
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
