# System map — C01/P01

This is the live whole-system map for RustySel4AI. It describes intended behavior, not an implemented OS. Read [LAW](LAW.md) for constraints, [CONTRACTS](CONTRACTS.md) for block responsibilities, [CYCLES](CYCLES.md) for the current pass, and [EVIDENCE](EVIDENCE.md) for what was actually inspected or run. The only observed repository content at the pinned baseline is a one-line README and Apache-2.0 license.

## Status and notation

`[OBS]` inspected, `[RUN]` executed, `[NEW]` proposed, `[GAP]` required but missing, `[ERR]` contradiction or failure, `[UNK]` unknown. A proposal or simulation never becomes an observation by being drawn here. Block IDs stay stable across views and revisions. `D` means data, `O` order, `P` permission, `C` containment, and `H` append-only history. Arrow labels name the payload or control condition.

```text
 [B-10 Human + AI interaction] [NEW]
     Human --D:intent/decision--> AI author
     Human <--D:3D/animation/chat/evidence-- AI author
                     |
                     D:authored intended ASCII revision
                     v
 [B-20:r+1 Intended ASCII draft] [NEW, unaccepted]
                     |
                     D:proposed contract/meaning change
                     v
 [B-30 Factory] [GAP: in-repo station; RUN: bounded C01 external gate]
     C: [B-31 Candidate workpiece] [NEW]
           --D:patch + claimed checks--> [B-32 Independent judge] [RUN: C01 docs only]
     B-32 --P:verified scope/authority--> integration decision
     B-32 --H:receipt + failures---------> [B-60 Lace history] [NEW]
     Human --P:missing judgment----------> integration decision
                     |
                     O:integrate only verified work
                     v
 [B-20:r+1 Accepted canonical ASCII + contracts] [C01 documentary baseline]
     | D:meaning/revisions         | D:constraints and trace IDs
     v                             v
 [B-40 First-party Rust semantics and lowering] [GAP]
     | D:machine image             ^ D:observed corrections
     v                             |
 [B-50 Native execution] [GAP] --D:observations/failures--+
     | H:logical I/O and execution participation
     v
 [B-60 Lace filesystem + model/execution/learning substrate] [GAP]
     | H:one append-only history, shared IDs and revisions
     +--D:rebuildable projection--> [B-70 Shared 3D/animation/chat views] [GAP]
     +--D:evidence/limits---------> B-10, B-20, B-32

 B-20:r accepted --D:current contracts--> B-30; B-30 --C:workpiece--> B-31.
 B-20:r accepted --P:prior authority--> B-32; B-32 is outside B-31's rights.
 No AI-to-accepted-repository edge exists; the factory and judge mediate changes.
```

## Boundary decisions for this baseline

- **Implementation provenance:** original first-party Rust with `no_std`; zero external implementation code. LLVM, seL4, and Blender may inform design but contribute no copied, translated, wrapped, vendored, or linked implementation. External build tools are a separate, audited category. See [PROVENANCE](PROVENANCE.md).
- **Native target:** x86-64 laptop first. The selected candidate is a freestanding x86-64 PE/COFF application using the UEFI x64 calling convention, then an explicitly designed private kernel handoff. Whether the owner's laptop supports and accepts that path, and its CPU features, devices, and boot configuration, are `[UNK]` until measured. Wasm is another allowed target; no browser or Wasm-width mandate applies.
- **Shared meaning:** ASCII, Rust semantics, execution, Lace, and visual/chat projections refer to the same IDs and revisions. Views rebuild from accepted history. Proposal and simulation must remain distinguishable from observed execution.
- **Protection:** each evolving part has an owner and authority inherited from the prior accepted state. Candidate code cannot revise accepted code, its judge, rights, or old evidence. A replacement of the judge, kernel, or storage requires prior authority and a recovery plan.
- **Current implementation:** no runtime, boot path, Lace store, views, or in-repo factory is claimed present. The external C01 gate checks only this documentary bootstrap; it does not certify executable changes.

## Trace entry

Start at [README](../README.md) → [LAW](LAW.md) → this map → [CONTRACTS](CONTRACTS.md) → [CYCLES](CYCLES.md) and [HANDOFF](HANDOFF.md). Follow each contract's path, invariant, test/evidence, and `STALE_IF` before editing it. Preserve disagreement and superseded assumptions in the cycle and evidence records instead of silently replacing history.
