# JCNC V-22 Osprey — Carrier-Folding Articulation

Owner-directed JCNC asset project. Authored by **claude-design / GPT-6 / Crowd cg42**, 2026-10-27.

**Status: r0001 candidate (artist-authored mechanical preview; native UE5 validation pending).**

This repository tracks the source code, rig specification, provenance, QA and revision records of the JCNC Osprey. The inherited source mesh was recovered from the owner's private Google Drive, and the source license is **NOT VERIFIED**. Do **not** upload the inherited or derivative 36.8 MB binary to this public repo until distribution rights are confirmed.

**Variant distinction:** Source model is labeled MV-22; Navy CMV-22B target-specific exterior, avionics, markings and range extensions are **not yet validated**.

## Mechanical scope

- Correctly **no arresting hook**; vertical landing, not arrested carrier approach.
- One 90-degree shipboard wing-stow pivot, nacelle articulation for each side, six separately articulated rotor-blade hinge pivots, and two rotor rotation joints.
- Seven glTF animation clips: `JCNC_Flight_To_Hover`, `JCNC_Hover_To_Flight`, `JCNC_Deck_Fold_Stow`, `JCNC_Deck_Unfold_Ready`, `JCNC_Rotor_Spin_Training`, `JCNC_Gear_Retract_Illustrative`, `JCNC_Actuate_Everything_Preview`.
- Landing gear proxy joint movement is **illustrative**, not actual bay/door geometry. Cargo ramp, flaps/control surfaces, equipment and four damage-state art are not built.
- Delivered review GLB: **528 nodes, 513 meshes, 174,608 triangles, 44 embedded images, 7 clips**; ZIP and rigged GLB provided in the owning ChatGPT chat, not yet publicly mirrored.
- Sampled compact bounding envelope: ~19.24 m long, 5.81 m wide, 5.89 m high; not proven mechanically collision-free.

## Build and viewer

The owning ChatGPT delivery ZIP (`JCNC_Osprey_Carrier_Fold_r0001.zip`) includes:
`build_osprey_rig.py`, `audit_osprey.py`, `osprey-viewer.html`, `osprey-r0001-articulated.glb`, manifests, reference ledger, revision notes, rig and state description.

Run the rebuild script against **exactly** the original 2026-10-09 V-22 GLB, SHA-256
`266cfdc84c92ae36f811f359627c99f097673d77f0392a0e81d51370b4652c03`.
Python 3 + numpy + scipy required. No original mesh included here.

Open `osprey-viewer.html` locally and select the downloaded GLB. Viewer needs Three.js CDN; browser runtime is **NOT RUN** as of r0001. The global toolbar exposes **Actuate everything**, **Pause**, **Reverse**, **Reset**.

## Acceptance gates

**Static structure PASS**, 7 glTF animation clips, 528 nodes and 513 mesh nodes, 174,608 triangles preserved. **Sampled folded bounds only**, not continuous swept collision. Blender DCC, real browser interactions, Unreal Engine 5 import/cook/runtime, CMV-22B visual fidelity, damage bindings, true hinge locations, live Crowd schema and source licensing: **NOT VERIFIED/NOT RUN**.

## Evidence

- [NAVAIR CMV-22B](https://www.navair.navy.mil/product/CMV-22B-Osprey)
- [US Navy V-22 shipboard fold/FRCE maintenance](https://www.navy.mil/Press-Office/News-Stories/Article/3178207/frce-marks-maintenance-firsts-with-v-22-repairs/)
- [Marine Corps MV-22 guidebook PDF](https://www.mcipac.marines.mil/Portals/28/Documents/MV22Guidebook.pdf)

Preserve every old release and record assumptions and exact hashes before revision. Never claim operational mechanics or UE5 acceptance from animated preview clips alone.
