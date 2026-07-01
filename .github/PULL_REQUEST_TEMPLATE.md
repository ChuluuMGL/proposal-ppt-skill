## What this changes

<!-- One or two sentences on the proposal-ppt skill change. -->

## Why

<!-- Which proposal-production problem or QA gap does this address? -->

## Type

- [ ] New proposal route / page type
- [ ] Style-template family or Style DNA change
- [ ] QA gate / `scripts/audit_proposal_pptx.py` check
- [ ] Documentation (README / SKILL / references)
- [ ] Runtime compatibility
- [ ] Other

## Anti-fabrication / honesty checks

- [ ] No invented data, cases, pricing, awards, or permissions added.
- [ ] No claim that a PPTX was delivered when only markdown/HTML/PDF exists.
- [ ] AI-generated demo visuals are marked as conceptual, not real client proof.
- [ ] Author company info is not inserted into user-facing templates.

## Verification

- [ ] `python3 scripts/audit_proposal_pptx.py <deck.pptx> --script <script.md>` passes on a sample deck.
- [ ] README "Included Files" / directory tree updated if files were added or renamed.
