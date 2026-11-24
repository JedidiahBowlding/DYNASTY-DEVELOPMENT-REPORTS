# Milestone report

## Report metadata

Phase 20 captured motion, 2026-11-23. PARTIAL. Private source commit 665edcdf673d4246c6cd9d2700378b98d5944798, draft PR #6.

## Executive summary

Four captured actions and two transitions were evaluated on the intended actor. The correction reduced floor penetration on several clips. The walking contact proxy and seated contact still failed.

## Implemented features

| Area | Result |
|---|---|
| Body | Isolated captured motion and contact correction trials |
| Evidence | Matched raw and corrected renders and editable motion actions |
| Portrait and facial dialogue | Outside this body-only milestone |

## Testing and verification

167 backend tests and 24 frontend tests passed. Frontend production build passed. Real GPU renders, six editable action reopens and full decoding of ten comparison or transition videos completed. Human acceptance is pending.

### Visual evidence

Matched walk renders were retained privately. Floor clearance improved across the take. The candidate planted displacement estimate regressed. This milestone has no new portrait or facial comparison.

## Performance

RTX 4070 Ti SUPER. Bench footage 640 × 360. Benchmark previews were encoded at 30 fps from sampled poses. Peak sampled GPU-wide memory 2,232 MiB. Longest Blender trial 64.86 seconds.

## Known problems

Walking stance excursion regressed. Sitting intersects the chair. Turn pivot labels and contact-safe transitions remain unverified.

## Experimental integrations

Authorized captured motion was evaluated with offline deterministic Blender tools. No production integration.

## Security and privacy

SANITIZATION PASS for the reviewed snapshot. Raw motion, editable assets and videos remain private. Public visual previews require separate owner approval.

## Production readiness

NO-GO. The tested body candidate failed technical acceptance. No human approval was recorded. Earlier portrait and facial decisions were outside this phase.

## Next priorities

1. Validate stable heel and toe contact intervals against foot pivots.
2. Test a control rig with pelvis compensation and independent foot locks.
3. Validate chair contact and transitions against actual collision surfaces.

## Questions for ChatGPT

1. How should the benchmark distinguish normal foot roll from sliding?
2. Which rig constraints can maintain both foot and seat contact?
3. Which ground-truth motions would validate the transition diagnostics?

## Developer declaration

I have separated verified results from assumptions, disclosed known failures, and excluded private source code and sensitive information.
