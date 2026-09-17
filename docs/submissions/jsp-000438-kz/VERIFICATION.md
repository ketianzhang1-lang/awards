# Verification receipt

These are contributor-run machine checks, including an independent checker
implementation. They are not organizer approval or independent human review.

## Pinned proof and successful execution

- [Proof commit 11a32e130fa669a4f23f0bbe7a320fd9675dbb7c](https://github.com/ketianzhang1-lang/jsp-000301-lean/tree/11a32e130fa669a4f23f0bbe7a320fd9675dbb7c/projects/jsp-000438).
- [Exact workflow](https://github.com/ketianzhang1-lang/jsp-000301-lean/blob/11a32e130fa669a4f23f0bbe7a320fd9675dbb7c/.github/workflows/jsp-000438.yml).
- [Successful run 35175029806](https://github.com/ketianzhang1-lang/jsp-000301-lean/actions/runs/35175029806).
- [Successful job 105054732657](https://github.com/ketianzhang1-lang/jsp-000301-lean/actions/runs/35175029806/job/105054732657).
- Checks completed 2026-09-17 UTC, with Lean 4.34.0 and Mathlib
  `5ed2965256430c3649e86755f9576b54eca72435`.

The 18 copied project files match the checked commit byte-for-byte; their
SHA-256 hashes are in [PROOF_SHA256SUMS](PROOF_SHA256SUMS).
The uploaded Git tree was compared with the locally prepared tree and matched.
The exact workflow is also copied as [PROOF_WORKFLOW.yml](PROOF_WORKFLOW.yml).

| Check | Observed result |
| --- | --- |
| Build with warnings treated as errors | Success; 3,132 build jobs |
| Bundled Lean checker replay | Success |
| Five named axiom closures | Only `propext`, `Classical.choice`, `Quot.sound` |
| Actual dependency Git revisions against lockfile | All matched |
| Invalid arithmetic negative control (`1 = 0`) | Rejected as required |
| NaNoda strict-allowlist check | 10,909 declarations checked with no errors |
| Archive source and upload evidence | Success |
| Ramsey definitions and full universal type | Verbatim match to pinned Formal Conjectures source |

The audited targets include the actual upstream `tree_free_edge_bound`, both
direct containment theorems, the asymmetric Ramsey bound, and the exact
`Erdos547.erdos_547` target. No project axiom, `sorryAx`, or native-evaluation
axiom is permitted. The scripts reject any axiom outside the stated allowlist.

The independent checker is NaNoda at
`4c544ed4099c8227f07d5de77ad1e69fb0740a27`, with lean4export at
`6cea97789dc088ea47fcea15692db85685aedac5`. All five declarations and their
dependency closures are exported. The run used an Ubuntu 24.04 hosted runner,
network access and dependency caches; no air-gapped full-library rebuild is
claimed.

Observed results are preserved in the [public log excerpt](evidence/log-excerpt.txt),
[job status](evidence/job-status.json), [run status](evidence/run-status.json),
and supplementary [local axiom output](evidence/local-axioms.log).

## External evidence artifact

[GitHub Actions artifact 10478133208](https://github.com/ketianzhang1-lang/jsp-000301-lean/actions/runs/35175029806/artifacts/10478133208)
contains the tested source archive, lockfile, build/checker/audit logs, negative
control output, compressed dependency export, checker configuration, printed
statements and internal checksums.

| Field | Recorded service value |
| --- | --- |
| Name | `jsp-000438-evidence` |
| ZIP bytes | `8112880` |
| ZIP SHA-256 | `fb1405c9051fba1bfb217242478d0c96e79ba155ea9b98a804533929263f17df` |
| Created | `2026-09-17T02:38:49Z` |
| Reported expiry | `2026-12-16T02:35:57Z` |

The API metadata and upload log agree on the artifact ID, byte count and digest
([metadata snapshot](evidence/artifact-metadata.json)). The complete ZIP was
subsequently materialized and its byte count and SHA-256 independently
recalculated locally; both match the service metadata. All internal source and
checker checksums match. Each of the 18 source files in the tested archive
matches this submission byte-for-byte, including all proof modules and the
lockfile. The actual archive records the same fixed proof commit.

See the [archive comparison receipt](evidence/archive-validation.json),
[archived axiom output](evidence/archive-axioms.log),
[NaNoda output](evidence/archive-nanoda.log),
[printed statements](evidence/archive-nanoda-statements.txt), and
[negative control](evidence/archive-negative-control.log).
The source and these compact receipts are preserved in Git.

The artifact has finite retention and is not a permanent archival deposit.
Reviewers can preserve it or reproduce the committed scripts before expiry.

## Official-repository preflight

Against official base `f4e7173d89dfe91022a185427d63452c8ffbf6ae`, record
validation, Markdown links, deterministic data generation, generated-data
consistency, history preservation and all 22 repository tests passed. The
change is confined to this submission directory. These checks verify repository
structure, not award eligibility or payment authorization.
