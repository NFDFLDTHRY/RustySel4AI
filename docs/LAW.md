# Project law — C01/P01

## Authority and scope

The owner named `NFDFLDTHRY/RustySel4AI` as the canonical repository. The attached setup instruction authorizes **C01/P01 only**: establish a truthful current map and continuation entry, then plan P02-P06. Owner corrections govern over older project assumptions. Current scope is documentation and a tested external bootstrap gate; no system implementation is authorized by this cycle.

## Implementation boundary

1. Project implementation must be original first-party Rust using `#![no_std]`. No foreign implementation code may enter through dependencies, vendoring, copying, translation, generated copies, wrappers, object files, blobs, or linking.
2. References such as LLVM, seL4, Blender, FactTest, and laceArc can inform experiments. Their source and architecture are not automatically adopted.
3. External compilers, emulators, test runners, and operating systems are build or observation tools, not project implementation. Their versions and outputs must be recorded. Audit the provenance of generated and linked bytes before claiming a binary satisfies rule 1. The treatment of Rust `core`, compiler builtins, firmware services, startup objects, and hardware microcode remains `[GAP]` for a future implementation decision.
4. The first physical target is the owner's x86-64 laptop. C01 selects **freestanding x86-64 via a UEFI x64 PE32+ application entry and UEFI x64 C calling convention, followed by an explicitly designed private kernel handoff** as the candidate native path. [UEFI 2.11 overview](https://uefi.org/specs/UEFI/2.11/02_Overview.html) defines the x64 handoff and image type; [boot services](https://uefi.org/specs/UEFI/2.11/07_Services_Boot_Services.html) define the memory-map and ExitBootServices boundary. This is a design selection, not a claim that the laptop supports the path. Inventory and a boot experiment must validate it before promotion. A hosted `x86_64-unknown-linux-gnu` probe may check bounded algorithms but cannot prove kernel behavior. Wasm is optional and has no fixed width or browser requirement.
5. Make only evidence-backed claims: `[OBS]`, `[RUN]`, `[NEW]`, `[GAP]`, `[ERR]`, `[UNK]`. Record source, tool, machine, target, inputs, prediction, raw result, rights/resources, receipt, limits, and `STALE_IF`. Proposal, simulation, container run, and physical laptop observation remain distinct.

## Change law

```text
human intent -> AI-authored intended ASCII -> factory station -> isolated workpiece
             -> independent judge -> accepted repo revision -> execution/probe
             -> evidence -> observed ASCII -> human decision

forbidden: agent -------------------------------------------> canonical repo
```

Each station declares input/output, may-read and may-change surfaces, forbidden surfaces, preconditions, invariants, checks, and receipt. The judge checks the pinned base, scope, contracts, consumers, and evidence independently of candidate-controlled state. Test actual denied effects: worktree location and path lists alone are insufficient. A candidate cannot change accepted code, judge, rights, or prior evidence. Judge, kernel, and storage replacement require authority from the previous accepted system and a recovery plan. Test a repair immediately, integrate only verified work, then re-observe.

The C01 external bootstrap exists only to admit this initial documentary baseline while the in-repo factory is absent. It must check the pinned base, explicit path allowlist, old-file preservation, links, and denial tests and produce a receipt. It does not certify future executable system changes.

## System invariants

- Intended ASCII is the canonical design expression, with explicit IDs and revisions. Observed structure records evidence and can disagree with intent.
- Lace is a candidate for the filesystem and model/execution/learning substrate: one append-only history with logical I/O participation. Granularity, reuse, recovery, and access rules require experiments.
- Shared 3D, animation, and chat are planned views over shared IDs and revisions; views must rebuild and cannot acquire authority by presentation.
- Isolation uses owned protection domains and explicit rights; every replaceable part evolves under previous authority.
- The factory makes local conflicts visible for human judgment. It does not silently resolve missing premises.

## Explicit supersessions

| Earlier assumption carried from prior exploration | Current owner correction for RustySel4AI |
|---|---|
| A Chrome WebApp is the required output and `wasm64` is the only target. | x86-64 laptop first; Wasm is an optional target without width or browser mandate. |
| No external crates is sufficient, so an imported seL4 kernel or other foreign runtime may sit below the code. | Zero external **implementation code** across source, binary, linked, generated, and wrapped paths. |
| LLVM, seL4, or Blender architecture should be copied as the default design. | Use them as references; measure fit and invent project-specific mechanisms. |

These corrections define this new repository. They do not rewrite the history or law of FactTest or laceArc.
