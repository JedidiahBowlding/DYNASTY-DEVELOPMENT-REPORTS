# Milestone report

## Report metadata

Unreal graphics pilot setup and stage validation, 2026-11-26. PARTIAL. Dynasty source baseline 83c16b56d4b1faf951a2d8bd28f96d45065e85cb.

## Executive summary

Unreal Engine 5.8.4 launched the isolated pilot. The stock digital actor opened in the character editor. A chair stage and camera sequence were created. Epic sign-in succeeded. The stock rig and textures were recovered in a separate editor copy, but complete character assembly failed.

## Implemented features

Saved an editable stock character, imported eight reference meshes, and built a 24 fps chair test sequence and render preset.

## Testing and verification

A Blender comparison baseline exists. Unreal verified the imported chair dimensions and displayed the stock character in its editor preview. The preassembled stock MetaHuman rendered in the vendor cinematic. Visual inspection confirmed visible skin, eyes, hair and hands with the sample control graphics. A separate portrait stage produced front, three-quarter, and close-up renders of the stock sample character. The first close-up was overexposed and soft. Revised exposure, focus, and framing made the face and groom readable. The same stock actor rendered a four-second sit, hold, and rise in locked side and three-quarter views. Both 96-frame exports decoded completely at 24 fps. Visual sampling covered the full movement. The owner responded positively to the chair preview and requested the office pilot. The 12-second office benchmark uses two stock stand-ins, includes an entrance walk, a sit, a locally solved dialogue close-up, and a listener reaction. A private, editable character likeness candidate was saved and rendered in three controlled local preview views. Character likeness and formal production acceptance remain pending.

## Performance

The empty chair stage rendered one 960 by 540 frame through Movie Render Queue on the RTX 4070 Ti SUPER. Process wall time was 53.10 seconds including startup. Peak sampled GPU-wide memory was 3127 MiB. The frame was overexposed and qualifies only as a render-path check. The preassembled sample rendered one 960 by 540 frame in 66.84 seconds including startup, with 6562 MiB peak sampled GPU-wide memory. Each of the three portrait frames was rendered at 960 by 540. Startup-inclusive wall time ranged from 21.83 to 22.60 seconds and peak sampled GPU-wide memory reached 5694 MiB. The revised chair views rendered in 22.32 and 22.78 seconds, with peak sampled GPU-wide memory of 5112 and 5151 MiB, respectively. The final office pilot rendered all 288 frames at 960 by 540 and 24 fps in 32.24 seconds, with 14599 MiB peak sampled GPU-wide use. The video and audio streams decoded completely. The local facial solve took 1.48 seconds. Audio placement was measured separately from phoneme accuracy. The walk revision rerendered and fully decoded all 288 frames in a 12-second cut. Render wall time was 34.01 seconds and sampled peak GPU-wide memory was 7057 MiB for that run. The runs had different GPU load and are not a memory optimization comparison.

## Known problems

The initial character assembly failed during texture baking. A separate editor retry reopened the rigged stock asset with textures, but failed while compiling facial controls. The Optimized path reproduced the same facial control errors in a fresh output folder and saved no assembled assets. Fab sign-in completed and the preassembled sample downloaded. An isolated copy was inventoried successfully in Unreal 5.8.4, including the authored sequence and Control Rig assets. The original pilot portrait frames are invalid. The sample render establishes a separate working path for an assembled character. The chair test uses skeletal animation editable in Sequencer after direct Control Rig authoring failed. The hold looks stiff and weight transfer is limited. Shoe, seat, and wardrobe collision clearance remain unmeasured. The first office render exposed a head-to-body separation during speech. A revised render aligned the facial animation with the seated body and showed mouth, brow, and eyelid movement. The owner flagged the original walk as awkward. The revised entrance uses a shorter forward walk paced against sampled foot movement and cuts into the sit instead of showing the unsupported turn. The owner approved the revised walk and edit into the sit and reported that the turn and chair contact looked good. This records visual feedback on the pilot cut. The cut skips the continuous turn, and foot and chair contact have not been measured on the rendered character. Chair contact, listener acting, and phoneme-level timing need separate assessment. The early likeness candidate still differs in hair silhouette and color, skin appearance, and lip shape. The temporary wardrobe remains in use. The preview has not been approved for animation. The prior Dynasty chair-support and garment-fit blockers remain.

## Experimental integrations

Unreal Engine and a reference MetaHuman are under evaluation in an isolated project. Rendering quality and motion contact will be judged separately.

## Security and privacy

SANITIZATION PASS. Private character files and reference images remain private.

## Production readiness

NO-GO for a pipeline switch. Comparative evidence and owner review are pending.

## Next priorities

1. Review the office pilot as a graphics, body motion, and dialogue benchmark.
2. Compare a likeness candidate against the approved private references.
3. Measure shoe, seat, and garment clearance and compare the facial solve to independently labeled dialogue timing.

## Questions for ChatGPT

1. What comparison would isolate character quality from lighting?
2. What render settings make GPU timing comparable?
3. What evidence is needed to evaluate the seated transition?

## Developer declaration

I have separated verified results from assumptions, disclosed known failures, and excluded private source code and sensitive information.
