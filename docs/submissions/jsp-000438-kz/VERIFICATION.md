# Verification evidence for JSP-000438

## English

This is a contributor-generated verification report, not an organizer decision
or an independent human mathematical review. The independent-checker entry
below refers to a separate checker implementation operated by the contributor.

## Checked source and environment

| Item | Value |
| --- | --- |
| Proof repository | `ketianzhang1-lang/jsp-000301-lean` |
| Proof commit | `11a32e130fa669a4f23f0bbe7a320fd9675dbb7c` |
| Project | `projects/jsp-000438` |
| Lean | `leanprover/lean4:v4.34.0` |
| Mathlib | `5ed2965256430c3649e86755f9576b54eca72435` |
| Dependency lock | [lake-manifest.json](source/lake-manifest.json) |
| Runner | GitHub-hosted `ubuntu-24.04` |
| Workflow run | [35175029806](https://github.com/ketianzhang1-lang/jsp-000301-lean/actions/runs/35175029806) |
| Verification job | `105054732657` |
| Result | Completed successfully on September 17, 2026 |

The workflow uses pinned checkout and artifact actions and read-only repository
permissions. Dependencies and checker tools are fetched from pinned revisions.
The run checks actual dependency Git revisions against the manifest. This is
reproducible contributor CI with network access, not a claim of the organizer's
isolated offline verification.

## Observed checks

| Check | Observed result |
| --- | --- |
| `lake build --wfail` | Success, 3,132 build jobs |
| Bundled `leanchecker JSP000438` | Exit success |
| Five declaration axiom closures | Only `propext`, `Classical.choice`, `Quot.sound` |
| Exact explicit target type | Checked in `Audit.lean` |
| False arithmetic negative control | `1 = 0` rejected by Lean |
| Pinned NaNoda independent implementation | 10,909 declarations checked, no errors |
| Downloaded artifact ZIP | SHA-256 verified against GitHub's artifact digest |
| Archived source | Every file compared byte-for-byte with the submitted source project |

The five audited declarations are `Erdos548.tree_free_edge_bound`,
`JSP000438.trees_monochromatic`, `JSP000438.tree_monochromatic`,
`JSP000438.graphRamsey_trees`, and `Erdos547.erdos_547`.
This includes the actual sharp upstream inequality used by the Ramsey proof.
The statement and standard axiom declarations are shown in
[nanoda-statements.txt](evidence/nanoda-statements.txt).

Checker pins:

- lean4export: `6cea97789dc088ea47fcea15692db85685aedac5`.
- NaNoda: `4c544ed4099c8227f07d5de77ad1e69fb0740a27`.
- The [configuration](evidence/nanoda-config.json) enables hard failure on any
  axiom outside the three-axiom allowlist and checks the actual exported closure.

## Artifact identity and retention

The full machine artifact is
[jsp-000438-evidence](https://github.com/ketianzhang1-lang/jsp-000301-lean/actions/runs/35175029806/artifacts/10478133208),
artifact ID `10478133208`, 8,112,880 bytes.

- ZIP SHA-256: `fb1405c9051fba1bfb217242478d0c96e79ba155ea9b98a804533929263f17df`.
- Source archive SHA-256: `861e9c8925534dcc5c8d40f33ff8196865abea24277aa2d5b594262b812d5018`.
- Compressed export SHA-256: `30865367e8d08b34caaba4cc8b43ca341f299ac51ee76b42250ff23910e8278f`.

The Actions artifact is scheduled to expire on December 16, 2026. It is not
represented as a permanent public archive. The proof, reproduction scripts,
manifest, small verification logs, and these hashes are included in this Git
submission so that verification can be repeated after that expiration. The
large export and source archive remain in the referenced artifact and are not
duplicated in this PR. A permanent public archive can be added by the designated
verifier if required for formal intake.

## Mathematical fidelity and contribution limits

The exact target matches the pinned Formal Conjectures statement described in
[STATEMENT.md](source/STATEMENT.md). The direct coloring theorem constructs a
member of the Ramsey defining set, preventing reliance on an empty-set natural
infimum. The proof uses Mathlib's tree, complement, and injective non-induced
containment definitions. It covers all orders at least two and uses the sharp
tree-free bound for both colors; odd-parity cases are not omitted.

The Erdős–Sós proof is reused with its Apache-2.0 license and attribution. The
new integration does not establish a new mathematical discovery or any award
priority. Organizer statement review, attribution review, formal intake,
recipient confirmation, and award adjudication are still required.
