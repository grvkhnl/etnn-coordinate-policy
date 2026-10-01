# Rendering the report

The repository includes the rendered PDF. Rebuilding it requires:

- Quarto;
- a XeLaTeX distribution;
- the LaTeX packages used in the document header, including `mathdesign`,
  `booktabs`, `longtable`, `microtype`, and `xcolor`.

The required JetBrains Mono Nerd Font files are included under
`report/fonts/` with their SIL Open Font License.

From the repository root, run:

```bash
quarto render report/from-equations-to-code.qmd
```

The command writes `report/from-equations-to-code.pdf`. The report source is
prose-driven and does not rerun the computational studies. Figures are versioned
alongside the source so the document can be rendered without downloading
datasets, checkpoints, or private execution records.

## Immutable software context

The report describes the TopoBench fork at commit
`a0bd4113f431efce8eb1ca38dcfe4837ab995779` and the official NSAPH reference
implementation at commit `639e35e`. These revisions are intentionally pinned
because later changes to either repository may alter implementation details.

The public comparison notebook and validation artifacts are available in the
pinned TopoBench fork:

- [comparison notebook](https://github.com/grvkhnl/TopoBench/blob/a0bd4113f431efce8eb1ca38dcfe4837ab995779/2026_tdl_challenge/submissions/etnn_coordinate_policy_comparison.ipynb)
- [comparison figures and compact records](https://github.com/grvkhnl/TopoBench/tree/a0bd4113f431efce8eb1ca38dcfe4837ab995779/2026_tdl_challenge/submissions/assets/etnn_coordinate_policy)
- [GraphUniverse result records](https://github.com/grvkhnl/TopoBench/tree/a0bd4113f431efce8eb1ca38dcfe4837ab995779/2026_tdl_challenge/outputs)

Large datasets, model checkpoints, machine-specific scripts, and internal
execution logs are intentionally not redistributed in this portfolio
repository.
