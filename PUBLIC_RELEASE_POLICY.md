# Public Release Policy

This repository documents the public development history of the Modular Medium Format Camera project.

It is not currently intended to contain the complete manufacturing, CAD, optical, simulation, or reconstruction source for the camera.

The public repository follows an **open-development, controlled-release** approach.

---

## Release Categories

Project material should be classified into one of the following categories before publication.

### PUBLIC

Material that may be published directly.

Typical examples include:

- project overview documentation
- architecture descriptions
- development history
- design-decision records
- sanitized engineering summaries
- selected renders
- selected comparison images
- diagrams that describe functional relationships without manufacturing detail

Public material should communicate design intent and development history without exposing unnecessary reconstruction details.

---

### SANITIZE BEFORE PUBLIC

Material that may be useful publicly but contains details that should be reviewed before release.

Typical examples include:

- engineering review reports
- simulation summaries
- interface discussions
- optical studies
- CAD screenshots
- section views
- tolerance results
- service diagrams

Before publication, these materials should be checked for:

- exact manufacturing dimensions
- detailed tolerance values
- complete optical prescriptions
- exact interface geometry
- datum coordinates
- reconstruction parameters
- internal file paths
- personal information
- third-party copyrighted material

A sanitized public version should be created rather than modifying the original engineering record.

---

### PRIVATE

Material that should remain in the private engineering workspace unless a future release decision is made.

This includes:

- native CAD files
- manufacturing-ready drawings
- STEP / SAT / STL geometry
- full parameter registers
- complete optical prescriptions
- detailed interface geometry
- calibration geometry
- tolerance source models
- simulation source data
- internal reconstruction scripts
- complete system interface definitions
- unreleased prototype designs

Examples of file types that are normally private include:

```text
.dwg
.dxf
.step
.stp
.sat
.stl
.npz
```

The file extension alone does not determine sensitivity. Text, JSON, CSV, or source-code files may also contain complete reconstruction information and should be reviewed accordingly.

---

### ARCHIVE

Historical engineering material that should be preserved but does not belong in the public repository.

Examples include:

- superseded CAD revisions
- internal review packages
- complete audit packages
- intermediate builds
- rejected detailed designs
- engineering evidence bundles
- historical simulation runs

These files may remain valuable for traceability even when they are no longer active development material.

---

### DO NOT PUBLISH

Files that should not be placed in the public repository.

Examples include:

- temporary files
- autosaves
- caches
- build artifacts
- local logs
- crash reports
- duplicate packages
- local runtime paths
- personal photographs not intended for publication
- third-party manuals or catalogs without confirmed redistribution permission

Typical examples include:

```text
*.bak
*.raw
*.log
__pycache__/
*.pyc
*.nbc
*.nbi
```

---

## Third-Party Material

Reference material from manufacturers, publishers, vendors, catalogs, manuals, or other external sources should not automatically be redistributed through this repository.

Where useful, public documentation should reference the source rather than copy the original material unless redistribution rights are clearly established.

---

## Public Documentation vs. Internal Development

The public repository may intentionally lag behind the latest internal engineering work.

A subsystem described publicly as the current documented architecture does not necessarily represent the latest private experiment or internal revision.

This allows development history to remain visible without requiring immediate publication of unreleased engineering details.

---

## Manufacturing Status

Unless explicitly marked otherwise, material in this repository should not be considered:

- manufacturing-ready
- production-released
- physically validated
- dimensionally frozen
- safety-certified
- commercially supported

Status labels such as `CONCEPT`, `SIMULATION`, `CANDIDATE`, `PROTOTYPE`, and `VALIDATED` should be used where appropriate.

---

## Release Review

Before adding engineering material to the public repository, ask:

1. Does this file reveal exact geometry or parameters needed to reconstruct the design?
2. Does it expose an unreleased subsystem or alternative design?
3. Does it contain complete optical or mechanical interface information?
4. Does it contain personal information or local computer paths?
5. Does it contain third-party copyrighted material?
6. Would a screenshot, summary, or sanitized derivative communicate the same development result?

If the answer to any of the first five questions is yes, the material should be reviewed before publication.

---

## Licensing

Publication in this repository does not by itself grant permission to manufacture, reproduce, modify, distribute, or commercially use the engineering designs.

Licensing and possible future open-hardware terms remain under consideration.
