# Test history

The integration results were verified against local execution logs for b5555c44d5006c988782dc4318f2eab6af36cde3. The subsequent policy-only revision did not rerun those suites. Historical hardware evidence is separate.

| Check | Observed result | Scope |
|---|---|---|
| Backend | 135 passed | Integration code revision |
| Frontend | 24 passed, 0 failed | Integration code revision |
| Frontend production build | Passed | Integration code revision |
| Local GPU inference | Historical Audio2Face sandbox ran on an RTX 4070 Ti SUPER | Sandbox, separate from the integration branch |
| Local Blender render | Historical 15-second Eevee office render completed | Pre-release scene benchmark |
| Release end-to-end workflow | No run for this snapshot | Open |
| Human visual acceptance | Pending; previous candidates failed review | Open |

## Phase 16 execution

| Check | Result |
|---|---|
| Fresh baseline | 135 backend and 24 frontend tests passed; frontend production build passed |
| Final revision | 143 backend and 24 frontend tests passed; frontend production build passed |
| Local hardware | Blender office and separate Wan smoke completed |
| Recovery | Targeted cancellation, explicit retry and fault injection executed |
| Controlled export | 360 continuous frames and one audio stream; full decode passed |
| Human acceptance and clean installation | Open |

## Phase 17 execution

151 backend tests passed, including eight gate-specific regressions. 24 frontend tests and the frontend build passed. Actual GPU portrait, movement and facial comparison renders completed, with full video decode checks. The owner has yet to approve any gate.

## Phase 18 execution

156 backend tests and 24 frontend tests passed, and the frontend production build passed. Real Blender portrait, body and dialogue comparisons rendered. The editable actor reopened with both actions, and encoded video passed complete decoding. Human approval is pending.

## Phase 19 update

163 backend and 24 frontend tests passed. Frontend build passed. Four captured-motion comparisons and editable action reopening were verified.

## Phase 20

Private source commit 665edcdf673d4246c6cd9d2700378b98d5944798. 167 backend tests and 24 frontend tests passed. Frontend production build passed. Real GPU renders, six Blender asset reopens and ten full media decodes completed. Human review is pending and body technical acceptance failed.

## Phase 21

176 backend tests, 24 frontend tests, and production build passed at private source commit 66e1b7917e4a09f38d569b8e903690d6666b09b9. Native-rate GPU previews and editable actions verified. Visual approval pending.

## Phase 22

Nine focused solver tests passed. A static Blender asset reopened and matched side views rendered.
