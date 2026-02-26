# Supporting Information

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on soil biodiversity and nitrogen cycling.
- Field study conducted at Sourhope, Scottish Borders, examining how land-management practices influence nitrite-oxidising bacteria, nitrification/denitrification processes, and N2O flux.
- Data represent static chamber measurements of nitrous oxide flux collected from May 2000 to November 2001 by CEH Edinburgh scientists.

## Study setting and data collection
- Site: upland agricultural grassland soil at Sourhope; randomised block treatments.
- Treatments: Control, Lime, Nitrogen, Nitrogen & Lime (plus a Biocide category in data dictionary).
- Experimental design: randomised allocation of treatments to sampling areas within sub-plots; sampling areas S, T, U, V considered along ridges to avoid moisture gradients from furrows.
- Chamber setup: 40 cm diameter polypropylene chambers, 20 cm length, with sealed gas sampling tubes and tight lids; randomised area assignment for each replicate and treatment.
- Sampling scope: field measurements of N2O flux to assess effects of land management on nitrogen cycling.

## Methods of analysis
- Gas analysis: nitrous oxide measured via gas chromatography (Chrompak CP 9000 with Poropak Q column; electron capture detector at 350°C).
- Sampling: gas from chamber headspace collected in Tedlar bags or 10 mL syringes; calibration standards (typically 1 ppm N2O in 80% N2 and 20% air) used to convert millivolts to ppm.
- Quality control: calibration runs at the start/end to account for drift; backflushing and interference management (e.g., water) during GC analysis.
- Output metric: N2O flux expressed as net production/emission rate per unit cross-sectional area, in micrograms N2O-N m^-2 h^-1.

## Data structure and fields
- Dataset: 1006 - Soil Nitrous oxide field flux data (P2118_SOIL_N2O_FIELD_FLUX_DATA.csv).
- Coverage: static chamber measurements in the field from May 2000 to Nov 2001; contributed by CEH Edinburgh.
- Core fields and descriptions:
  - EXP_ID: Block/Main plot/Sub-plot identifier (text).
  - EXP_DATE: Sampling date (date).
  - BLOCK: Block number (1-5) (number).
  - MAIN_PLOT: Main plot letter (A-F) (text).
  - SUB_PLOT: Sub-plot (text).
  - CELL_X: Cell grid X coordinate (number).
  - CELL_Y: Cell grid Y coordinate (number).
  - TREATMENT: Soil treatment type (Control, Lime, Nitrogen, Nitrogen & Lime, Biocide) (text).
  - NITROUS_OXIDE_FLOW: Net production of N2O (flux) in micrograms N2O-N m^-2 h^-1 (number); missing values are Null.
- Data types and units:
  - EXP_DATE: Date.
  - NITROUS_OXIDE_FLOW: Number; detection limit noted as 30-40 ppb for N2O.
- Documentation notes:
  - The dataset includes explicit metadata for discovery and reuse, including treatment types and grid coordinates.

## Quality assurance and data rights
- Quality assurance: numeric range checks, formatting conformity, and logical integrity checks.
- Data rights: NERC cannot warrant the accuracy of the data or the fitness for a particular purpose; no liability for use of the data. Data provided for research with standard QA caveats.

## Provenance and references
- Related sources and context:
  - Davies, C.A. (2005). Nitric and nitrous oxide production and emission from an upland agricultural grassland soil (doctoral dissertation, University of Edinburgh).
  - Scott et al. (2003). SOURHOPE FIELD DATA HANDBOOK 2003.
  - Usher et al. (2006). Understanding biological diversity in soil: UK Soil Biodiversity Research Programme.
- These references provide background on site, methodology, and broader data governance and metadata context.

## Data governance and stewardship implications
- Discoverability: ensure metadata includes site, dates, treatments, and data structure to enable discovery and integration with other datasets.
- Interoperability: be mindful of methodological specifics (chamber design, GC setup, flux units) when combining with other datasets.
- Documentation: maintain clear provenance, data dictionary, and data quality notes to support reuse and proper interpretation.
- Licensing and access: include explicit usage terms and attribution; document any embargo or licensing constraints.
- Update and provenance tracking: maintain versioning and traceability for any reprocessing or updates to the dataset.