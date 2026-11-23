# Development roadmap

Windows integration is the last code milestone verified by the recorded automated execution. Blender, Audio2Face and ChatDev have separate historical local evidence as labeled below.

| Component | State | Evidence and known limitation | Next acceptance criterion | Readiness |
|---|---|---|---|---|
| Windows installer | Launcher and workstation detection implemented | Clean-machine installation unverified | Fresh Windows installation starts and runs a trial project | Open |
| Scene Generation | Scene preview and shot validation implemented | Prior motion candidates failed visual review | Complete a representative directed scene and approve playback | Open |
| Wan Video Engine | Wan 2.2 and shot diagnostics implemented | Historical local rendering, unstable acting and background drift | Approve repeatable motion and stable framing on target GPU | Open |
| Blender Integration | Local render path implemented; Blender 4.5.16 LTS historically exercised | A prior office render completed; no new run at this revision | Reproduce a clean GPU scene render and import | Open |
| Character Factory | Editable characters demonstrated in earlier work | Reusable production likeness and deformation unapproved | Approve an editable rig in close-up and motion | Open |
| Digital Humans | Sandbox and preview studies | Likeness, hair, facial anatomy and gait remain blockers | Human approval for portrait, movement and dialogue | Open |
| Audio2Face | Sandbox only | Local inference and editable facial animation; teeth and tongue artifacts; phoneme improvement unverified | Independently align phonemes and approve counterbalanced comparisons | Open |
| Timeline | Audio handling implemented and regression tested | Full editor playback and export still need release validation | Review dialogue round-trip and mixed export for duplication and sync | Open |
| Render Queue | Lifecycle and outcome selection implemented | Recovery after interrupted production jobs unverified | Interrupt a job, resume or retry, and validate output | Open |
| Asset Library | Import, update and deletion covered by integration changes | Clean-machine persistence unverified | Verify import, restart, version retention and safe deletion | Open |
| ChatDev | Sandbox only | Three roles and local Ollama ran; identical videos and incorrect reviewer assessment | Blind evaluations show a reproducible quality benefit | Hold |
| Publishing | Release flow remains gated | No release-grade publish verified for this snapshot | Validate approved master, metadata and destination in a controlled dry run | Open |
