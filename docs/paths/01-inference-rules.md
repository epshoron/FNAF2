# Inference Rules

## Core idea
- Input: (enemy, camera_id) from a single frame classifier
- Output: stage_index + risk_level + recommended response

## Stage index (example)
- 0 = spawn area
- 1..N = intermediate rooms
- N+1 = vent / hallway threshold
- N+2 = in-office attack window

## Risk heuristic (example)
- If camera_id in {CAM 05, CAM 06} => HIGH (vent threshold)
- If camera_id == CAM 07 => MED (hall pressure)
- If camera_id == CAM 11 and enemy == Puppet => HIGH (music box critical) :contentReference[oaicite:3]{index=3}

## Output template
- stage_index:
- likely_next_locations:
- must_do_now:
- confidence: OBSERVED / COMMUNITY / UNKNOWN
