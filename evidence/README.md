# Validation evidence

This directory contains the compact records used for the report's tables and
figures. It does not include datasets or model checkpoints.

## GraphUniverse

- `graphuniverse/coordinate-free-results.json`: 72-run coordinate-free result
  record.
- `graphuniverse/structural-lappe-results.json`: 72-run structural-coordinate
  result record.

These are byte-for-byte copies of the committed challenge result files at
TopoBench revision `776dcf4972974d17df36869f84e8f84302ec2f2c`.

## QM9 physical integration

The `qm9/physical-integration/` directory contains the model and training
configuration plus epoch metrics for each reduced integration variant. The
`summary.json` file records the test metric and elapsed time used in the report.
Machine-local paths have been removed from the configuration records.

This study checks the public
`QM9 -> GraphTriangleInducedCC -> physical ETNN -> readout -> loss` path. It is
not a paper-comparable performance study.

## QM9 model-core comparison

- `qm9/topobench-core/model-parity.json`: adapter and model-core parity audit.
- `qm9/topobench-core/training-record.json`: protocol and final results for the
  TopoBench ETNN core parity harness.
- `qm9/topobench-core/epoch-metrics.csv`: its 1,000-epoch learning trajectory.
- `qm9/native-reference/run-record.json`: protocol and final results for the
  native NSAPH reproduction.
- `qm9/native-reference/epoch-metrics.jsonl`: its 1,000-epoch learning
  trajectory.

The public JSON records omit checkpoint paths and hardware identifiers. The
scientific protocol, results, checks, tensor shapes, and tensor hashes are
retained. In particular, the model-parity record preserves the one strict
optimizer-parameter check that did not pass.

## Integrity

`SHA256SUMS` lists every public evidence record. Verify it from the repository
root with:

```bash
shasum -a 256 -c evidence/SHA256SUMS
```
