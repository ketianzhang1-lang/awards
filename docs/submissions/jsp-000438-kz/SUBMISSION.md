# Prepared pull request description

## Change

Please review this **full-statement Lean integration for JSP-000438 / Erdős 547**
for statement fidelity, attribution, overlap, and formalization-contribution
eligibility. It proves, for every `n ≥ 2` and every tree `T` on `Fin n`,
`SimpleGraph.diagonalGraphRamsey T ≤ 2*n-2`.

The mathematical input is the existing, credited Erdős–Sós proof from
`tadamcz/erdos548` at `82ffb751f3d37768927df9239ed08439bbe0dd09`, already
referenced by JSP-000439. This contribution ports that complete proof to Lean
4.34.0 and supplies the all-order Ramsey deduction and exact target interface.
The terminal theorem does not assume Erdős–Sós and is not restricted to
sufficiently large trees. A stronger asymmetric consequence is also proved.

The standard implication is credited to prior work (the consulted Erdős 547
source attributes the observation to Burr and Erdős). **No authorship of the
upstream Erdős–Sós proof, discovery of that implication, or first-formalization
priority is claimed.** Upstream attribution to GPT-6 Astra, the FrontierMath
Erdős benchmark, Tom Adamczewski / Epoch AI and Thomas F. Bloom is retained.
The original source, copyright, NOTICE, Apache-2.0 license and complete port
patch are included. OpenAI Codex assisted the new work.

## Evidence

- [Immutable source](https://github.com/ketianzhang1-lang/jsp-000301-lean/tree/11a32e130fa669a4f23f0bbe7a320fd9675dbb7c/projects/jsp-000438).
- [Verification run](https://github.com/ketianzhang1-lang/jsp-000301-lean/actions/runs/35175029806).
- [Statement comparison](STATEMENT.md), [verification receipt](VERIFICATION.md),
  [dependency attribution and port](UPSTREAM_PORT.md), and [source hashes](PROOF_SHA256SUMS).
- Lean 4.34.0, Mathlib `5ed2965256430c3649e86755f9576b54eca72435`, and a complete lockfile.
- The copied Ramsey definitions and full target type were compared verbatim
  with Formal Conjectures commit `40e7c98697de6f66b8cbdbf641749ab39ed9c152`.

Verification results and artifact metadata are recorded in `VERIFICATION.md`.
The checks are contributor-run, including an independent checker implementation;
they are not independent human certification or an organizer decision.

## Record or policy impact

Only `docs/submissions/jsp-000438-kz/` is added. Please review whether the catalog
entry should be updated in light of this full-statement evidence; this intake
package does not itself change catalog, candidate, recipient, award or payment
records. The currently checked catalog flags remain Open / Lean proof No /
Eligible to claim No until an authorized review changes them.

Proposed formalization-contribution recipient: `RECIPIENT-JSP-000438-KZ-A`,
confirmation pending. This is a self-submission with a direct interest in the
review outcome. No solver nomination is made for the credited upstream result.
The extent of any recognizable new contribution is specifically left to review.

## Checks

- [x] Submitted materials are in English; no award is announced.
- [x] The proposed recipient uses a placeholder; no private contacts, payment
  details, internal assessment material or credentials are included.
- [x] The exact proof source and dependency revisions are publicly pinned.
- [x] Prior published statements and decisions are preserved.
- [x] Lean build, checker replay, five axiom audits and negative control passed.
- [x] Pinned NaNoda checked **10,909 declarations with no errors**.
- [x] External artifact `10478133208`: 8,112,880 bytes; locally verified ZIP SHA-256
  `fb1405c9051fba1bfb217242478d0c96e79ba155ea9b98a804533929263f17df`.
  It expires on 2026-12-16; all 18 archived source files match the submission.
  Finite retention and human-review limits are stated in the receipt.
- [x] Record validation, local links, data generation, consistency and history
  checks passed; all 22 repository tests passed.

## Reviewer decision

Pending organizer review. A correct formal proof alone does not establish
award eligibility or entitlement. Please redirect the intake package if a
different submission location is required.
