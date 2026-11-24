# MaCH4 2026

Methane (CH₄) and CO₂ fluxes across the flood pulse at Mamirauá, Brazil, 2026 field campaigns (March, May, July, November): tree stems, soils, open water (diffusion and ebullition), stable isotopes, incubations, water chemistry, and the eddy-covariance tower.

Each component has its own code repository. Code repositories are private for now and visible to project members only. Raw data is kept separately, one folder per component, and each folder will become its own data-repository deposit at publication. The code reads that data from a single configurable location, so the same scripts run on the shared copy today and on the published deposits later.

## Repositories

| repository | component | status |
|---|---|---|
| `mach4-trees` | tree-stem CH₄/CO₂ fluxes (LI-7810, goFlux) | rebuilt from raw data |
| `mach4-soil` | soil collars, riparian gradient, repeated collars, substrates | rebuilt from raw data |
| `mach4-common` | shared helpers (R package `mach4common`), tree master list, campaign calendar, instrument registry | built |
| `mach4-diffusion` | floating chambers and dissolved-gas syringes | March 2026 rebuilt from raw data (original method reproduced, plus goFlux fork) |
| `mach4-bubbles` | ebullition traps and bubble composition | March, May, July 2026 rebuilt (original sheets reproduced, raw LI-7810 injections, trap-level fluxes incl. July); some raw LI-7810 periods still to export |
| `mach4-isotopes` | δ¹³C-CH₄ sampling and analyses | March–July sheets reproduced; recalibrated and compared |
| `mach4-incubations` | soil/litter incubations, water CH₄ oxidation | planned |
| `mach4-water-chem` | water chemistry and depth profiles | planned |
| `mach4-tower` | eddy-covariance tower and profiler | planned |
| `mach4-docs` | how-to guide for the team | planned |

## Conventions

- **Reproducible from raw data.** Each repository has a `run_all.R` that rebuilds every result from the raw files. Analysis decisions, such as the chosen measurement windows and excluded closures, are versioned CSVs, not hand edits.
- **Instrument serials everywhere.** Raw analyzer files are stored in one folder per instrument serial number. Every result table carries the serial of the analyzer that made the measurement.
- **Raw data is never edited.** Corrections are made in code. Every data folder has a SHA-256 manifest and a provenance record linking each file to its original.
