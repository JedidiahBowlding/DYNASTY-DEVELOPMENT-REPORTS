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
