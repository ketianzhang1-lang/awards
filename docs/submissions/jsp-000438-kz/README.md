# JSP-000438: full tree Ramsey upper bound

## English

This is a contributor-prepared submission for review of the complete formal
statement associated with JSP-000438 / Erdős 547. For every integer `n >= 2`
and every tree `T` with `n` vertices, the Lean development proves

\[
R(T,T)\le 2n-2.
\]

The stronger asymmetric statement `R(T,S) <= |T|+|S|-2` is also proved when
both trees have at least two vertices. The main statement is
`Erdos547.erdos_547` in [JSP000438.lean](source/JSP000438.lean).
All orders in the corrected original statement are covered. This is an upper
bound, not an exact formula for each individual tree's Ramsey number.

The proof is a short consequence of the **previously published** Erdős–Sós
formalization by GPT-6 Astra in the FrontierMath Erdős benchmark, released by
Tom Adamczewski / Epoch AI. The complete credited dependency is included;
Erdős–Sós is not left as a hypothesis. The submitter contributes the Lean
4.34 port, all-order Ramsey integration, statement alignment, and reproducible
verification. No new-mathematics or first-formalization claim is made.

## Materials and reproduction

- [Complete source project](source/README.md), with pinned toolchain and dependencies.
- [Statement alignment](source/STATEMENT.md), including non-vacuity of the Ramsey definition.
- [Upstream source and exact port changes](source/UPSTREAM_PORT.md).
- [Verification report](VERIFICATION.md) and checked theorem statements in
  [NaNoda's output](evidence/nanoda-statements.txt).
- [File hashes](SHA256SUMS).

The exact proof commit is
[`11a32e130fa669a4f23f0bbe7a320fd9675dbb7c`](https://github.com/ketianzhang1-lang/jsp-000301-lean/tree/11a32e130fa669a4f23f0bbe7a320fd9675dbb7c/projects/jsp-000438).
The successful
[verification run](https://github.com/ketianzhang1-lang/jsp-000301-lean/actions/runs/35175029806)
checked the source included here byte-for-byte. From `source/`, run:

```sh
lake exe cache get
bash scripts/verify.sh
bash scripts/verify_nanoda.sh
```

## Attribution and requested review

Recipient placeholder: `RECIPIENT-JSP-000438-KZ-A`; confirmation is pending.
This is a self-submission prepared with OpenAI ChatGPT / Codex assistance.
Please review the evidenced formalization contribution, statement fidelity,
overlap, priority, and eligibility under the published rules. The upstream
mathematical proof and its contributors retain their credit; see the included
[NOTICE](source/NOTICE) and [license](source/LICENSE-APACHE-2.0).

The existing `plby/lean-proofs` treatment of Erdős 547 covers sufficiently
large orders; this package explicitly covers every `n >= 2` using the
credited all-order extremal theorem. Official issue and PR searches for
`JSP-000438` returned no match at the preparation check on September 17, 2026.
These searches do not establish global priority or exclude every possible
overlap.

No candidate status, catalog eligibility flag, announced award, recipient
confirmation, payment entitlement, or monetary allocation is asserted or
changed by this evidence package. Machine verification reported here was
performed on the contributor's workflow; organizer verification and award
adjudication remain pending.
