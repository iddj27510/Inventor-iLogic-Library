# Inventor iLogic Library

Production-grade iLogic automation tools for Autodesk Inventor.
Open source. MIT license.

---

## IL-03 — Flat Pattern DXF Batch Exporter

Batch exports flat pattern DXF files from any Inventor Assembly.
Tested on Autodesk Inventor 2027.

**Two versions:**
- `IL-03_FlatPatternDXFBatchExporter.iLogicVb` — Full version with report window and log file
- `IL-03_FlatPatternDXFBatchExporter - Minimal.iLogicVb` — Minimal version, single MsgBox on completion

**What it does:**
- Recursively scans the entire assembly tree
- Finds every sheet metal part
- Creates flat patterns where missing
- Exports DXF with Part Number + thickness + revision in the filename
- Skips Content Center, non-sheet-metal, and suppressed parts
- Handles duplicate parts, filename collisions, unsaved files, circular references
- Leaves every model exactly as it found it

**DXF layer structure:**

| Layer | Purpose |
|---|---|
| IV_OUTER | Cutting contour |
| IV_BEND_UP | Bend up direction |
| IV_BEND_DOWN | Bend down direction |
| IV_TANGENT | Excluded via InvisibleLayers |

**Test result:**
125-part assembly — 2 sheet metal DXFs exported — 0 errors

**How to use:**
1. Open an Assembly (.iam) in Autodesk Inventor
2. iLogic panel → Add/Edit Rule → paste the code
3. Edit the CONFIG section if needed
4. Run

---

## License

MIT — free to use with attribution.

## Author

Jugoslav Ilic
[LinkedIn](https://www.linkedin.com/in/jugoslav-ilic)
[GitHub](https://github.com/iddj27510)