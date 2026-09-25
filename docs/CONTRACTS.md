# Contracts and gaps — C01/P01

These are intended block contracts, not claims that the blocks exist. The [system map](SYSTEM.md) gives their typed connections. [LAW](LAW.md) governs every contract; [PROVENANCE](PROVENANCE.md) governs implementation sources. Keep the IDs when a block changes and record the revision and reason in [CYCLES](CYCLES.md).

## IDs and observed floor

| ID | Statement | Status |
| --- | --- | --- |
| I-001 | One connected intent → ASCII → Rust → execution → evidence → human decision loop. | `[NEW]` intent |
| I-002 | Lace supplies one append-only history and participates in logical I/O, execution, and learning; measure reuse and choose granularity experimentally. | `[NEW]` intent |
| I-003 | Canonical ASCII and shared 3D, animation, and chat views use the same IDs/revisions; views rebuild and label proposals versus observations. | `[NEW]` intent |
| I-004 | Agent proposals enter an isolated candidate; an independent judge checks pinned base, scope, contracts, consumers, evidence, and rights. Prior authority controls replacement of judge, kernel, and storage. | `[NEW]` intent |
| I-005 | Original first-party Rust, `no_std`, zero external implementation code; audit tool and linked output provenance. x86-64 laptop first with measured boot/ABI/hardware; Wasm remains allowed. | `[NEW]` target and provenance constraint |
| O-001 | At the pinned remote `main` baseline, `HEAD=f16e023beb0edf6ff4a023e51d1c2e274c3ccb7a` and `tree=b2bc0b658356c10caef2069904f715ad896b76df`. Its tree has only `README.md` (`# RustySel4AI`) and `LICENSE` (Apache-2.0), with no first-party OS implementation or project law. | `[OBS]` remote inspection; see [EVIDENCE](EVIDENCE.md) |
| O-002 | The available machine audit is of the task container, not the owner's x86-64 laptop. | `[OBS]` bounded audit; see [EVIDENCE](EVIDENCE.md) |

## Block register

`I/O` means a contract boundary, not a currently functioning interface. All code paths remain `[GAP]` until an experiment and its authority are specified. “Owner” is a responsibility role; only the repository owner may assign operating maintainers.

| Contract / block / parent | Purpose and I/O | State | Authority and owner | Failure rule |
| --- | --- | --- | --- | --- |
| K-00 / B-00 / none | Preserve one coherent system. In: owner intent, pinned repo state, evidence. Out: accepted revisions, claims, next experiment. | `[NEW]` governance map | Repository owner decides direction; accepted law limits all operators. | Stop integration on ambiguous authority, provenance, base, or contradictory evidence; retain the conflict. |
| K-10 / B-10 / B-00 | Human explores/decides; AI drafts ASCII and candidate changes. In: intent, accepted map, observed evidence. Out: proposals and human decisions. | `[NEW]`; no product UI | Human owns judgment; AI has proposal and delegated workpiece rights only. | Label uncertainty; never send agent changes straight to accepted repo or present simulation as observation. |
| K-20 / B-20 / B-00 | Canonical ASCII and linked contracts carry system meaning. In: reviewed intent/evidence. Out: IDs, revisions, invariants for builders and views. | `[RUN]` documentary gate; accepted only if the published main ref matches its checked tree | Repository owner approves; judge verifies scope and trace before integration. | Reject unlinked edits, broken IDs, silent supersession, or a map that claims absent code. |
| K-30 / B-30 / B-00 | Factory creates and checks a candidate from a pinned base. In: accepted base, station limits, proposed change. Out: workpiece, checks, receipt, integration decision. | `[RUN]` bounded external C01 gate; `[GAP]` in-repo factory and executable isolation | Prior law grants narrow station rights; operating owner `[GAP]`. | A path/worktree rule alone is insufficient: test denied effects and stop if rights can be crossed. |
| K-31 / B-31 / B-30 | Candidate workpiece holds unaccepted code/docs. In: base plus proposal. Out: diff, artifacts, declared checks. | `[NEW]` staged bootstrap only | AI/operator may change only candidate scope; cannot change judge, accepted code, rights, or old evidence. | Discard or quarantine candidate on unauthorized effect; keep its evidence. |
| K-32 / B-32 / B-30 | Independent judge checks scope, consumers, contracts, provenance, tests, and pinned base. In: workpiece plus trusted baseline. Out: recorded verdict and limits. | `[RUN]` independent external C01 witness for docs only; `[GAP]` system judge | Judge authority derives from prior accepted state; judge owner `[GAP]`, separate from candidate. | Missing evidence is a failed gate, not a pass; judge replacement needs prior authority and recovery. |
| K-40 / B-40 / B-00 | First-party `no_std` Rust semantics and lowering implement accepted ASCII meaning. In: accepted contracts. Out: audited native/Wasm artifacts. | `[GAP]` implementation | Project owner approves interfaces; first-party builders work under bounded rights. | Reject foreign implementation or untraced generated/linked code; recheck consumers after changes. |
| K-50 / B-50 / B-00 | Execute on measured target and return observations. In: audited image, actual ABI/boot/hardware. Out: execution result, faults, resource and permission record. | `[GAP]`; UEFI x64 is a candidate only | Boot/execution authority and device ownership `[UNK]` until measured. | No laptop or kernel claim from container/hosted tests; fail closed on unknown hardware assumptions. |
| K-60 / B-60 / B-00 | Lace joins filesystem identity, append/recovery, execution, model/learning, and logical I/O. In: logical operations and execution evidence. Out: append-only history and reusable references. | `[GAP]` design and implementation | Prior accepted storage authority; owner `[GAP]`. | Preserve old evidence; test recovery and access denial; growth alone does not prove learning or reuse. |
| K-70 / B-70 / B-00 | 3D, animation, and chat project shared meaning for human inspection. In: accepted IDs/revisions/history. Out: rebuildable views and decisions. | `[GAP]` product view | Read/project according to accepted access rights; human owns interpretation. | Mark proposal/simulation/observation distinctly; rebuild or invalidate stale projections. |

## Trace and change triggers

The path column names the current documentary contract. `[GAP] code path` means no implementation location has been selected. Evidence pointers are in [EVIDENCE](EVIDENCE.md); unrun checks remain **NOT RUN**.

| Contract | Intent / observed | Path and invariant | Test / evidence | `STALE_IF` |
| --- | --- | --- | --- | --- |
| K-00 | I-001–I-005, O-001–O-002 | `README.md`, `AGENTS.md`, `docs/LAW.md`, `docs/SYSTEM.md`; one current map and preserved history | P01 repository/container audit; no OS test | Remote base, law, or owner decision changes |
| K-10 | I-001, I-004; no UI observation | `docs/SYSTEM.md`; AI proposes under human judgment | UI interaction test **NOT RUN** | Decision roles or view requirements change |
| K-20 | I-001, I-003, O-001 | `docs/SYSTEM.md`, `docs/CONTRACTS.md`; IDs and typed arrows remain traceable | Link/map review in P01; semantic machine test **NOT RUN** | Accepted architecture or linked consumer changes |
| K-30 / K-31 / K-32 | I-004, O-001 | `docs/LAW.md`, `docs/PROVENANCE.md`; candidate cannot change accepted code, judge, rights, or evidence | External C01 scope/denial witnesses `[RUN]` for docs; executable factory bad-patch tests **NOT RUN** | Station rights, base, judge, or recovery plan changes |
| K-40 | I-001, I-005, O-001 | `[GAP] code path`; implementation must match accepted ASCII and provenance | Build/lowering/kernel tests **NOT RUN** | Compiler, ABI, target, contract, or linked inputs change |
| K-50 | I-005, O-002 | `[GAP] code path`; native claim requires measured laptop boot/execution | Laptop boot test **NOT RUN**; container is not proof | Laptop firmware/hardware, boot choice, or image changes |
| K-60 | I-002, I-004, O-001 | `[GAP] code path`; one append-only history with recovery/access limits | Commit/recovery/reuse tests **NOT RUN** | Granularity, rights, storage model, or recovery changes |
| K-70 | I-001, I-003, O-001 | `[GAP] code path`; projections share accepted IDs/revisions | Rebuild/view tests **NOT RUN** | IDs, timeline, history, or presentation semantics change |

## Open decisions before implementation

1. Measure the owner's laptop firmware, x86-64 feature set, storage and display route, and chosen UEFI/other handoff before selecting an ABI or boot artifact.
2. Specify the bootstrap station's actual I/O, write scope, denied effects, invariant checks, independent verifier, and receipt. Test the gate before accepting generated code.
3. Specify Lace identity, logical I/O granularity, append boundary, recovery, and access model with a falsifiable reuse measure before choosing modules or crates.
4. Name the operating owners and replacement authorities for judge, kernel, and storage; define recovery before replacement.
