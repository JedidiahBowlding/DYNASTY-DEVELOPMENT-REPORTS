# Milestone report

## Report metadata

Unreal graphics pilot setup and stage validation, 2026-11-26. PARTIAL. Dynasty source baseline 83c16b56d4b1faf951a2d8bd28f96d45065e85cb.

## Executive summary

Unreal Engine 5.8.4 launched the isolated pilot. The stock digital actor opened in the character editor. A chair stage and camera sequence were created. Epic sign-in succeeded. The stock rig and textures were recovered in a separate editor copy, but complete character assembly failed.

## Implemented features

Saved an editable stock character, imported eight reference meshes, and built a 24 fps chair test sequence and render preset.

## Testing and verification

A Blender comparison baseline exists. Unreal verified the imported chair dimensions and displayed the stock character in its editor preview. The preassembled stock MetaHuman rendered in the vendor cinematic. Visual inspection confirmed visible skin, eyes, hair and hands with the sample control graphics. Matched portrait and motion acceptance remain pending.

## Performance

The empty chair stage rendered one 960 by 540 frame through Movie Render Queue on the RTX 4070 Ti SUPER. Process wall time was 53.10 seconds including startup. Peak sampled GPU-wide memory was 3127 MiB. The frame was overexposed and qualifies only as a render-path check. The preassembled sample rendered one 960 by 540 frame in 66.84 seconds including startup, with 6562 MiB peak sampled GPU-wide memory. This is a single-frame measurement.

## Known problems

The initial character assembly failed during texture baking. A separate editor retry reopened the rigged stock asset with textures, but failed while compiling facial controls. The Optimized path reproduced the same facial control errors in a fresh output folder and saved no assembled assets. Fab sign-in completed and the preassembled sample downloaded. An isolated copy was inventoried successfully in Unreal 5.8.4, including the authored sequence and Control Rig assets. The original pilot portrait frames are invalid. The sample render establishes a separate working path for an assembled character. The prior Dynasty chair-support and garment-fit blockers remain.

## Experimental integrations

Unreal Engine and a reference MetaHuman are under evaluation in an isolated project. Rendering quality and motion contact will be judged separately.

## Security and privacy

SANITIZATION PASS. Private character files and reference images remain private.

## Production readiness

NO-GO for a pipeline switch. Comparative evidence and owner review are pending.

## Next priorities

1. Use an isolated copy of the preassembled character for a clean close-up and chair test.
2. Render a comparable close-up using a stock character.
3. Check a short seated transition separately for contact and visual quality.

## Questions for ChatGPT

1. What comparison would isolate character quality from lighting?
2. What render settings make GPU timing comparable?
3. What evidence is needed to evaluate the seated transition?

## Developer declaration

I have separated verified results from assumptions, disclosed known failures, and excluded private source code and sensitive information.
