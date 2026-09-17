# JSP-001016: logarithmic-density wording correction note

## Scope

This note requests review of the wording of JSP-001016. It does **not** claim a new solution, a first solution, prize eligibility, or a change to any award or candidate record.

The current catalog describes the problem as asking whether, in every two-coloring of the positive integers, one color's finite subset sums have a uniformly positive **lower logarithmic density**. The cited Conlon–Fox–Pham paper, *The upper logarithmic density of monochromatic subset sums* (Mathematika 2022; arXiv:2105.15195), instead proves the corresponding sharp statement for **upper logarithmic density**: one color has upper logarithmic density at least `(2 + sqrt(3))/4`, and this is best possible.

Because upper and lower logarithmic density are different notions, the catalog wording should be checked against the original Erdős formulation and the cited solution before treating the present lower-density wording as equivalent to the published solved problem.

## Explicit counterexample to the literal lower-density wording

For completeness, the literal lower-density formulation currently displayed in the catalog has a simple block-coloring counterexample.

Let

```text
t_0 = 2,
t_{j+1} = 2^(t_j).
```

Color the integer blocks

```text
[t_j, t_{j+1})
```

alternately red and blue; color `1` arbitrarily. For a color class `A`, let `FS(A)` be the set of nonempty finite sums of distinct elements of `A`.

Fix a block `[t_j, t_{j+1})` having the opposite color from `A`, and put

```text
N_j = t_{j+1} - 1.
```

Any representation of an integer at most `N_j` as a finite sum of distinct elements of `A` can use no element from the current block, and can use no later element because every later element is greater than `N_j`. Hence every summand is less than `t_j`, so

```text
FS(A) ∩ [1, N_j] ⊆ [1, t_j(t_j - 1)/2].
```

Therefore

```text
sum_{n <= N_j, n in FS(A)} 1/n
  <= 1 + log(t_j(t_j - 1)/2)
  <= 1 + 2 log t_j.
```

On the other hand,

```text
log N_j = log(2^(t_j) - 1) >= (t_j - 1) log 2.
```

Thus along these infinitely many opposite-color blocks,

```text
(1/log N_j) * sum_{n <= N_j, n in FS(A)} 1/n
  <= (1 + 2 log t_j) / ((t_j - 1) log 2)
  -> 0.
```

The same argument applies to both colors, since each color has infinitely many opposite-color blocks. Consequently both monochromatic finite-subset-sum sets have lower logarithmic density zero.

This does **not** contradict the Conlon–Fox–Pham theorem: a set may have lower logarithmic density zero while having large upper logarithmic density.

## Requested review

Please check the original Erdős source and update the catalog wording if appropriate. In particular, if the intended solved statement is the one established by Conlon–Fox–Pham, the phrase `lower logarithmic density` should not be used in place of `upper logarithmic density`.

No changes to `Current status`, `Lean proof`, `Eligible to claim`, candidate records, recipient records, or award records are requested by this note.

## References

- D. Conlon, J. Fox, H. T. Pham, *The upper logarithmic density of monochromatic subset sums*, Mathematika 68 (2022), 1292–1301. arXiv:2105.15195.
- JSP-001016 in this repository, which currently cites that paper as the solution source.
