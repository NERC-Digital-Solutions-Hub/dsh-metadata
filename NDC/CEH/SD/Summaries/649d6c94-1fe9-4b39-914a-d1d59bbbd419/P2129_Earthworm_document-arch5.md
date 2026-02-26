# Earthworm data from Sourhope field experiment site, Scotland, 1999 and 2001 [NERC Soil Biodiversity Programme]

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999) focused on soil biodiversity and ecological processes at Sourhope, Scotland.
- Earthworm data collected in 1999 and 2001/2002 (two sampling points) by the Universities of Stirling and Dundee.
- Aimed to document earthworm communities in relation to liming treatments and plot-level management within a larger soil biodiversity study.

## Site and Experimental Design
- Location: Sourhope Research Station, southern uplands of Scotland; upland grassland on Brown Forest Soils (Sourhope series) on glacial till; elevation ~300–320 m.
- Experimental setup: 30 plots (20 m x 12 m) in five randomized blocks; two treatments: Control (unlimed) and Limed (CaCO3 applied at 6 t ha^-1 annually from 1999–2002).
- Plot management: Sheep grazing history (excluded from April 1998); grass mowing monthly May–Sept with cuttings removed.
- Purpose within broader programme: Coordinated soil biodiversity studies across multiple taxa and processes.

## Earthworm Census and Data Collection
- Sampling method: Intact soil blocks (42 cm long, 30 cm wide, 25 cm deep) collected from five limed and five unlimed plots; hand-sorting to extract earthworms (preferred to avoid chemical extraction biases).
- Timing: Sampling conducted in September 1999 (baseline) and September 2002 (endpoint).
- Specimen handling: Earthworms refrigerated for 24 hours to purge guts, blotted dry, killed in 40% ethanol, and identified to species using Sims & Gerard (1985) keys.
- Data scope: Abundances include adults and juveniles, but juveniles that could not be speciated are not included.

## Data Structure and Metadata
- Datasets: 1011 and 1012 (Baseline 1999 and Endpoint 2002 surveys).
- Primary data file: P2129_ALL_SURVEY.csv (earthworm survey data for Sourhope Control and Limed plots).
- Key columns and definitions:
  - SUID: Unique Sampling Unit Identifier (block/main-plot/sub-plot/cell, plus sampling date and sampling unit type/size).
  - SAMPLING_DATE: Date of sampling.
  - BLOCK: Block number (1–5).
  - MAIN_PLOT: Main plot letter (A–F).
  - SUB_PLOT: Sub-plot designation.
  - CELL_X, CELL_Y: Cell grid coordinates.
  - TREATMENT: C = Control, L = Limed.
  - SPECIES: Earthworm species (per Gerard & Sims 1985).
  - ABUNDANCE: Total abundance per m^2 (adults + juveniles).
  - TYPE: Baseline or Endpoint (1999 baseline; 2002 endpoint).
- Additional context: Species and abundance data structured to facilitate treatment-by-time comparisons; dataset aligns with the Sourhope Field Data Handbook (Scott et al., 2003) and related literature.

## Data Quality and Limitations
- Quality control: Numeric range checks, formatting checks, and logical integrity checks employed.
- Limitations and disclaimers: Data are subject to QA procedures, but NERC cannot warrant accuracy or fitness for a particular use; liability for misuse or misinterpretation is disclaimed.
- Species identification: Based on established taxonomic keys; juveniles not speciated may limit certain analyses by life stage.

## Access and Documentation
- Primary data format: CSV (P2129_ALL_SURVEY.csv) with detailed field descriptions.
- Related documentation and sources:
  - Sourhope Field Data Handbook (2003) – supporting information via EIDC catalogue.
  - Bibliography: Bishop et al. 2008; Scott et al. 2003; Usher et al. 2006; Sims & Gerard 1985.
- Data sharing context: Data linked to broader Soil Biodiversity Programme outputs and integrated with other taxa and processes studies.

## References
- Bishop, H. O., Grieve, I. C., Chudek, J. A., & Hopkins, D. W. (2008). Liming upland grassland: the effects on earthworm communities and the chemical characteristics of carbon in casts. European Journal of Soil Science, 59(3), 526-531.
- Scott, R., Bell, J., Kenny, C., Jeffers, J., Buckland, S., & Burt-Smith, G. (2003). Sourhope Field Data Handbook 2003. Available via EIDC catalogue.
- Usher, M.B., Sier, A.R., Hornung, M., & Millard, P. (2006). Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme. Applied Soil Ecology, 33(2), 101-113.
- Sims, R.W., & Gerard, B.M. (1985). Earthworms: keys and notes for the identification and study of the species (Vol. 31). Brill Archive.

## Governance and Data Stewardship Considerations
- Data provenance: Clear linkage to Sourhope field experiment, lime treatment, and block-level design; metadata includes sampling unit identifiers and temporal context.
- Metadata completeness: Includes explicit definitions for SUID, timing, spatial coding, and treatment status; adherence to a documented data handbook enhances interoperability.
- Update and reuse: Two timepoints documented (baseline and endpoint); potential for future updates or additions if additional sampling occurs; ensure alignment with published methodologies.
- Data sharing and liability: Include caution about accuracy and intended use; require users to consult cited references and data provenance for proper interpretation.
- Usability for discovery: Rich metadata enable discoverability by dataset administrators and end users; structure supports filtering by treatment, timepoint, block, and species.