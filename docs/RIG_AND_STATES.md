# JCNC Osprey — Rig and state contract (r0001)

Author: claude-design / GPT-6 / Crowd cg42, 2026-10-27.

**Variant:** source is MV-22, carrier target CMV-22B NOT VERIFIED.
**Arresting hook:** NONE. V-22 uses vertical landings on ships, not arrested landings. Do not confuse a cargo sling hook for a tailhook.

## Exported hierarchy

Exported glTF axes: metres, +Y up, nose -Z, inherited source +X forward / +Z up and scale 0.01.

| Mechanism | glTF node ID |
|---|---:|
| Wing rotating stow | 523 |
| Nacelle +Y / -Y | 517 / 522 |
| Rotor +Y / -Y | 516 / 521 |
| Blades +Y | 513 / 514 / 515 |
| Blades -Y | 518 / 519 / 520 |
| Nose / +Y main / -Y main gear proxy | 524 / 525 / 526 |
| Root | 527 |

528 total nodes, 513 mesh nodes, 174,608 triangles, 44 inherited embedded images and 11 materials. All original donor triangle counts were preserved.

## Animation clips physically embedded

| Clip | Channels |
|---|---:|
| JCNC_Flight_To_Hover | 2 |
| JCNC_Hover_To_Flight | 2 |
| JCNC_Deck_Fold_Stow | 9 |
| JCNC_Deck_Unfold_Ready | 9 |
| JCNC_Rotor_Spin_Training | 2 |
| JCNC_Gear_Retract_Illustrative | 6 |
| JCNC_Actuate_Everything_Preview | 17 |

All timings and blade angles are visual authoring estimates, not certified real procedures.

Shipboard sequence: land and shut down; stop/index the rotors; raise nacelles; fold six rotor blades; position nacelles for clearance; unlock wing and stow 90°; reverse dependency order for deployment.

Never run continuous rotor spin simultaneously with indexed blade folding. Pause every active visual/rotor channel. Reverse through dependency-safe states. Reset to one canonical rest pose. The authored composite preview approximates this ordering but is NOT a real UE5 interlock implementation.

Sampled stow bounding envelope: 19.237 m long × 5.807 m wide × 5.886 m high. Full swept-triangle collisions and carrier hangar clearances NOT RUN. User-provided model rights NOT VERIFIED.

## Unreal handoff

Import original glTF node animations and verify real pivot frames and transforms in the target UE5 version. Scale and axes must be checked with an asymmetric datum (UE target centimeters, +X forward, +Z up). If necessary convert rigid nodes to tested bones in Blender; no such native project is delivered.

Still required: physical gear wells/conforming doors, rear cargo ramp and bounded cabin, animated control surfaces, CMV-22B-specific geometry/decals, cockpit equipment, engine/damage states, level 1 reusable crew/components, physics/LOD/UE5 cook/runtime and direct browser-viewer QA. Damage lives in central JCNC gameplay authority, not invented local health rules.

This revision is an articulated visual model, not a fully accepted CMV-22B UE5 asset. Source rebuild script and actual GLB are supplied in the owner's downloadable ZIP. Because source licensing is unknown, do not mirror the inherited or derived GLB in this public repo before legal review.
