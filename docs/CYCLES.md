# Cycle record — C01

Each pass runs the entire loop: direction and planning → ASCII diagram/documentation → machine evidence → analysis, mapping, interpretation → next decision. Evidence can redirect a later pass. Revisit every affected contract and consumer when an observation changes the map. The owner authorized **C01/P01 setup only**; P02–P06 below are plans, not executed work.

## P01 — anchor vision, repository, machine, and provenance

| Loop step | C01/P01 record |
| --- | --- |
| Direction and planning | Use `NFDFLDTHRY/RustySel4AI` `main` as canonical. Establish an AI-first OS baseline and truthful continuation. Pin remote `HEAD=f16e023beb0edf6ff4a023e51d1c2e274c3ccb7a` and `tree=b2bc0b658356c10caef2069904f715ad896b76df` before candidate changes. Preserve its README/LICENSE. Do not implement an OS in P01. |
| Intended ASCII | [SYSTEM](SYSTEM.md) gives the whole-system typed diagram and status. [CONTRACTS](CONTRACTS.md) names the blocks, authority, invariants, gaps, and change triggers. [LAW](LAW.md) records owner corrections and change rules; [PROVENANCE](PROVENANCE.md) separates reference material, tools, and project implementation. |
| Machine and source evidence | [O-001](EVIDENCE.md): remote tree has only README/LICENSE. [O-002](EVIDENCE.md): task container is x86-64 Linux, not the target laptop. [E-001](EVIDENCE.md): this container's Rust tool commands failed during rustup setup. [E-002](EVIDENCE.md) preserves the first denied gate; [R-001](EVIDENCE.md) records the repaired documentary gate, independent witness, and nine denial cases. Physical laptop inventory, Rust build, UEFI boot, kernel execution, and Lace tests are **NOT RUN**. |
| Analysis and mapping | The design includes a connected human/AI → ASCII → Rust → execution → Lace/evidence → human loop, but the remote baseline implements none of these blocks. Current code paths, target device facts, Lace granularity, judge rights, and recovery are `[GAP]`/`[UNK]`. Candidate native handoff is freestanding x86-64 PE/COFF via UEFI x64; laptop acceptance remains `[UNK]`. |
| Interpretation and decision | Stage a documentary baseline and an external bootstrap gate. The first check denied an incorrect baseline copy and missing status definition; repair and immediate retest produced a passing gate and independent witness. Publish only after the verified receipt; re-observe remote HEAD/tree in the task's publication record. Do not infer OS progress from documentation. |

### P01 disagreements and supersessions

The earlier browser/`wasm64` requirement and allowance for imported seL4 or other external implementation are superseded **for this new repository** by the owner's x86-64-first and zero-external-implementation constraints. LLVM, seL4, Blender, FactTest, and laceArc remain references, not imported architecture or code. [LAW](LAW.md) is the authoritative statement; no history in the referenced projects is rewritten.

### P01 acceptance check

The bootstrap receipt identifies the pinned base, complete candidate path list, checks and negative witnesses, judge identity/method, raw results, rights, and limits. The task's publication record adds the resulting commit/tree after an independent remote read. If the base moves or a check fails, keep the candidate out of the accepted repository and record the conflict. A successful gate for documentary files does not certify later executable code.

## Planned passes, not run

Each row names a direction, ASCII revision, falsifiable machine experiment, and interpretation step. Before executing any pass, confirm authority, experiment inputs, target environment, expected result, denied effects, and the contracts/consumers it can change.

| Pass | Direction and ASCII/documentation | Proposed machine evidence | Analysis, mapping, interpretation |
| --- | --- | --- | --- |
| P02 — Lace/filesystem | Define identities, logical I/O granularity, extents, append boundary, commit/recovery, access rights, and resource limits in B-60/K-60. Keep one history concept across storage and execution. | On an isolated first-party host model, compare candidate granularities with repeat writes, references, interrupted commits, corruption, and denied reads/writes. Record exact inputs, raw history, recovery, and reusable bytes/events. **NOT RUN.** | Distinguish growth from measured reuse; revise K-60, K-50 and consumers only on evidence. Decide a granularity or retain the gap. |
| P03 — ASCII/3D/time | Define shared ID/revision semantics, drill-down, time transitions, and lowering between accepted ASCII and views B-20/B-70. | Rebuild a tiny scene/chat/timeline from the same fixture after revision and replay; compare displayed meaning and provenance. Test proposal/simulation/observation labels. **NOT RUN.** | Reconcile differences with K-20, K-40, K-60, K-70; choose the minimum representation that preserves meaning. |
| P04 — replacement | Specify protection domains, prior authority, candidate confinement, judge/kernel/storage migration, and recovery before replacement. | Attempt an unauthorized patch to old evidence, accepted code, judge, and rights; inject a bad repair and interrupted migration. Verify denied effects and recovery. **NOT RUN.** | A containment result is not correctness. Update K-30–K-32, K-50, K-60 and affected consumers; require independent evidence. |
| P05 — inference/reuse | Define how Lace participates in model execution and learning, reference validity, resource accounting, and a useful baseline. | Compare a repeated task with and without permitted reuse, including stale/invalid references and rollback; measure correctness, work, memory, and time. **NOT RUN.** | Claim reuse only for measured valid references and gain; update K-60 and user-visible evidence, not just data volume. |
| P06 — integrate/attack/replay | Reconcile one system map, connected interfaces, provenance, and current law. | Replay a full accepted path and attack cross-boundary assumptions; inspect raw results and recovery. **NOT RUN.** | Record contradictions, revise affected blocks/consumers, and derive C02 from evidence and unresolved owner decisions. |

## Cycle control

No pass advances by assertion. Use `[OBS]` for inspected sources, `[RUN]` for executed checks with raw results, `[NEW]` for proposals, `[GAP]` for missing capability, `[ERR]` for failure/contradiction, and `[UNK]` for unknown facts. A container run is not a physical laptop observation, a hosted test is not kernel proof, and an old receipt is not a fresh run.
