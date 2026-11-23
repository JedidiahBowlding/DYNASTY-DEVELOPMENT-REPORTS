# Milestone report

## Report metadata

- Report date: 2026-11-23
- Milestone name: Phase 16 end-to-end reliability and release validation
- Development status: PARTIAL
- Production status: NO-GO
- Private source branch: validation/phase16
- Source commit SHA: bd885fb2febd6d53240d7ff7439999e13a10764c
- Private draft pull request: #2
- Reporting commit SHA: available in published history after approval.

## Executive summary

Dynasty produced a 15-second local office scene and exported an assembled validation cut after reopening the saved project. Reliability corrections address duplicate renders, cancellation, output registration, interrupted deletion, Windows workflow compatibility, missing media and Timeline audio timing. Production gates remain open.

## Implemented features

| Component | Change | Status | Verification |
|---|---|---|---|
| Scene Generation | Four-shot office validation scene | Tested on one template | Walk, sit, dialogue and reaction rendered |
| Wan Video Engine | Preserved pinned workflow on Windows checkout | Smoke tested | Local GPU inference decoded |
| Blender Integration | Exercised real render interruption and retry | Tested | Intact frames reused, incomplete frame rebuilt |
| Character Factory | Exercised existing reusable identity records | Preview | Human likeness approval pending |
| Digital Humans | Walk, sit and facial reaction reviewed in frame samples | Preview | Facial and visual defects remain |
| Audio2Face | Prior sandbox retains experimental status | Sandbox only | Excluded from this scene |
| Timeline | Corrected audio processing latency and tail duration | Tested | Aggregate fixture tests and a real dialogue export |
| Render Queue | Safer cancellation, retry and duplicate handling | Tested in targeted scenarios | Full desktop crash recovery open |
| Asset Library | Improved missing-file and interrupted-deletion handling | Tested in targeted scenarios | Real assets reopened with matching content evidence |
| ChatDev | Existing sandbox unchanged | Sandbox only | Excluded from validation |
| Windows Installer | Development runtime verified | Blocked | Clean Windows installation unavailable |
| Publishing | Safety checks covered by automated tests | Blocked | Controlled release dry run pending |

## Testing and verification

Fresh baseline: 135 backend tests, 24 frontend tests and production build passed. Final revision: 143 backend tests, 24 frontend tests and production build passed. Local GPU inference, Blender render retry and Timeline export ran. FFprobe and full decoding validated the final media. Independent phoneme alignment, clean installation and human acceptance were not completed.

## Performance

RTX 4070 Ti SUPER. Blender rendered 640 × 360 at 24 fps for 15 seconds; sampled peak was 2,242 MiB. A forced interruption occurred at 121.37 seconds; explicit retry took 202.32 seconds and reused 125 valid frames. Timeline export took 1.74 seconds. A separate 320 × 192 Wan smoke generated 17 frames in 49.66 seconds with a sampled peak of 12,880 MiB. Memory peaks are whole-device samples. No per-process CPU or RAM benchmark was captured.

## Known problems

| Severity | Problem | Impact | Planned Correction |
|---|---|---|---|
| Release blocker | No clean Windows target | Installer readiness unknown | Run a disposable Windows installation and project smoke test |
| Release blocker | Eye appearance, shading and acting defects | Character quality unapproved | Conduct shot-specific review with independent speech alignment |
| Release blocker | Desktop crash recovery and full asset recovery unverified | Operational certification pending | Exercise crash and restart in a disposable Windows project |
| Release blocker | Commercial clearance and publish dry run pending | Release cannot proceed | Review exact release inputs and run a controlled publishing rehearsal |

## Experimental integrations

Audio2Face and ChatDev remain sandbox only. FreeMoCap and experimental character mesh generation remain research. Existing local ComfyUI served the verified Wan smoke. No experimental backend was enabled.

## Security and privacy

SANITIZATION PASS for the proposed public documentation after the local validation scan. Raw evidence remains private. Public publication requires owner approval.

## Production readiness

NO-GO. Supervised local validation can proceed. Technical evidence supports the tested template, GPU render and export. Clean installation, full recovery, commercial clearance and human visual review remain release gates. The four dialogue waveform checks demonstrate track placement, with independent face-to-phoneme verification pending.

## Next priorities

1. Complete a clean-machine install and reopen a generated project.
2. Interrupt the packaged application during a render and confirm predictable recovery with no duplicate output or leftover process.
3. Conduct human motion and appearance review and validate facial timing against independently labeled audio.

## Questions for ChatGPT

1. Which process-ownership behavior should gate restart certification for a local GPU job?
2. Which test scenarios best cover missing or partially imported media across restarts?
3. What independent labels should gate character contact and lip synchronization in the test cut?

## Developer declaration

I have separated verified results from assumptions, disclosed known failures, and excluded private source code and sensitive information.
