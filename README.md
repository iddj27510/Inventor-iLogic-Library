# Inventor iLogic Library

Production-grade iLogic rules for Autodesk Inventor.

Built for reliability and readability: every rule is self-contained,
documented with a standard header, uses Check-Before-Set for all write
operations, and handles edge cases (empty assemblies, missing
iProperties, locked files) without crashing the batch.

---

## Available Rules

### IL-03 — Flat Pattern DXF Batch Exporter

Recursively scans an assembly for sheet metal parts and exports each
flat pattern as a DXF file named after the part number and revision.

- Skips non-sheet-metal parts with a log entry
- Creates flat pattern if missing
- One file error does not stop the batch
- ShowReport summary at the end

**Compatibility:** Inventor 2018 – 2027

Files:
- `IL-03_FlatPatternDXFBatchExporter.iLogicVb` — full rule
- `IL-03_FlatPatternDXFBatchExporter - Minimal.iLogicVb` — minimal variant

---

## Roadmap

The library is expanding. Planned rules cover: iProperties validation,
drawing title block auto-population, BOM completeness checking,
revision auto-incrementing, and ERP data export.

Status and planned dates are tracked in the Batch PDF Publisher
project's internal roadmap. Public announcements will be made as
each rule is released.

---

## Related Projects

- [Batch PDF Publisher](https://github.com/iddj27510/BatchPDFPublisher) —
  VBA add-in for bulk IDW to PDF export. 52 components, 49 unit tests,
  CycloneDX SBOM, GitHub Actions CI, MIT licensed.

---

## License

MIT — free to use with attribution.

## Author

**Jugoslav Ilić**
Email: engilic@gmail.com
GitHub: [@iddj27510](https://github.com/iddj27510)