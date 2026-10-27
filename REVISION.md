# Osprey r0001 — Revision and acceptance record
Date: 2026-10-27
Author: claude-design / GPT-6 / JSLC Crowd cg42

## Changes
Recovered owner's MV-22 GLB from Google Drive, SHA-256 266cfdc84c92ae36f811f359627c99f097673d77f0392a0e81d51370b4652c03, 36,800,760 bytes. Source mesh reportedly comes from a Sketchfab downloader; redistribution rights NOT VERIFIED.

Retained 174,608 triangles, 44 embedded images and 11 materials; introduced 17 animation pivots and a 528-node/513-mesh exported GLB with 7 clips. Split portions of two static primitives that should move with wing. Used glTF rigid node transformations, no native UE5 files.

Output: osprey-r0001-articulated.glb, 36,850,192 bytes, SHA-256 1b83ea25ec6d4c80e0d103a37ad271f23da3d82b2c11ceb3406df86905086ae9.
User ZIP: JCNC_Osprey_Carrier_Fold_r0001.zip, 28,035,852 bytes, SHA-256 6632f0942c07d0cc8c5601539e375c7412600d4cc8808660e9215a781423dbb9.

## Assumptions
- User asked for carrier-folding Osprey; starting mesh MV-22, CMV-22B target but conversion incomplete.
- Wing pivot, blade hinge angular travel and fold timings are visually inferred, not verified to operational engineering manual.
- Fold wing 90 degrees after rotor indexing and fold, with nacelle staging. No arresting hook.
- Source extents scale 0.01; +Y up/-Z nose after orientation conversion.
- Landing gear animation is demonstrative; well openings and doors absent.

## Static evidence
GLB v2 parses, exact scenes accessible, legal quaternion animations, 174,608 source triangles retained, 528 nodes, 513 meshes, 7 embedded clips. Orthogonal/sampled fold AABB 19.237m length × 5.807m width × 5.886m height. No inference of continuous sweep clearance from endpoints.

## Remaining blockers/gates
Source license/public binary distribution NOT VERIFIED.
Original model not photoreal accepted; variant conversion not done.
Gear bay/door, cargo ramp/opening, control surfaces, functional systems and shared four-tier damage art NOT IMPLEMENTED.
Continuous geometry collision NOT RUN.
Browser viewer execution NOT RUN.
Native Blender, UE5 import/rig/materials, physics/cook/runtime NOT RUN.
Crowd binary model ingestion not verified; package >20MB direct upload limit.
GitHub source-only artifacts are not proof of model binary backup.

## Next executable action
Check source license, reference-match actual wing/blade mechanisms and complete unbuilt physical apertures. Run actual Blender/UE5 import and continuous collision inspection before claiming carrier-compatible accepted CMV-22B.
