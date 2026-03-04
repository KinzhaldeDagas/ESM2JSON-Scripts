This repo fixes the .pas xedit script and optimizes record traversal, slightly faster and hopefully exports more info into JSONs.

Split Pascal script variants (mirroring the existing JS split):
- `esm2json-exporter-part1.pas`: exports everything except CELL/WRLD records.
- `esm2json-exporter-part2.pas`: exports CELL records only.
- `esm2json-exporter-part3.pas`: exports WRLD records only.


Each split Pascal script now does a one-time pre-scan of matching records in the plugin and prints progress as `Progress: N/Total` while processing.
