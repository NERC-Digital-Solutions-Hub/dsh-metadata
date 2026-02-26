# Soil aggregate stability data from arable and grassland in Countryside Survey, Great Britain 2007

## Overview
- Two CSV data files accompany the Countryside Survey 2007 soil work:
  - Particle_Size_Distribution_data.csv: PSD data for water-stable and post-sonication aggregates from 419 soils across 150 1km squares in Great Britain (survey year 2007).
  - Aggregate_stability_metrics.csv: Derived stability metrics (water-stable vs post-sonication) for the same 419 soils.
- Purpose: quantify soil aggregate stability using laser granulometry and derive disaggregation reduction (DR) metrics across Great Britain.
- Data originate from archived Countryside Survey samples and lab analyses described in the project documentation and associated methodological papers.

## Data structure and content
- Particle_Size_Distribution_data.csv
  - Columns: SQUARE, PLOT, PSIZE, VOL_WS, VOL_SON
  - Measures proportional volume by particle size class for water-stable aggregates (VOL_WS) and post-sonication aggregates (VOL_SON), per soil plot.
- Aggregate_stability_metrics.csv
  - Columns: SQUARE, PLOT, MWD1, MWD2, DR, LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07
  - MWD1: Mean Weight Diameter of water-stable aggregates; MWD2: after sonication; DR: disaggregation reduction (MWD1 minus MWD2).
  - Metadata: land class codes, country, county, and environmental zone descriptions.

## Sampling, provenance, and scope
- Sampling framework: Countryside Survey 2007 stratified GB into Land Classes across environmental gradients to produce representative national statistics.
- Sampling frame: 591 1km squares surveyed; final selection yielded 424 plots, with 419 analyzed for aggregate stability.
- Locations: 150 1km squares across England, Scotland, and Wales; plots within each square (PLOT codes).
- Soil origin and handling: soils were archived from Countryside Survey 2007, air-dried and 2 mm sieved; 15 g subsamples used for analysis.

## Methods and protocol notes
- Measurement approach: laser granulometry to obtain PSD; DR calculated as the difference between MWD before and after a sonication step.
  - Pre-sonication: water-stable aggregates (MWD1)
  - Post-sonication: fundamental particles (MWD2)
  - DR = MWD1 − MWD2 (reported as DR 2000 in this dataset; DR 500 is referenced but not included)
- Protocol changes implemented for this dataset:
  - Increased aggregate mass (1.8× prior mass) and longer PSD measurement (60 seconds)
  - No rescaling of PSD data to <500 µm; both DR 2000 (this dataset) and DR 500 (not included) variants are referenced
  - Less than 30% obscuration threshold maintained;
  - Use of a 7-metre pipe to increase circulating water volume and sample mass, plus controlled energy input during sonication
- Masses used by texture class (for analysis): fine 0.55 g, medium 1.0 g, coarse 1.3 g
- Equipment and steps:
  - Laser granulometer (Beckman Coulter LS 13320)
  - Pre-wetting setup with filter papers and RO water
  - 60-second PSD measurement across 92 size classes (0.375–2000 µm)
  - Sonication: UP100H, 100 W, 5 minutes
  - Temperature monitoring to gauge energy delivery
  - Quality controls with palaeosol reference and standard PSD materials (32 µm and 500 µm)

## Quality control, governance, and documentation
- Field and lab QA:
  - Field staff trained with a sampling manual; rigorous processing protocols
  - Palaeosol reference material analyzed each session
  - Standard PSD materials used to check instrument accuracy; repeat measurements if obscuration > 30% post-sonication
- Quality assurance:
  - UK Centre for Ecology & Hydrology (UKCEH) operates an ISO 9001:2015 certified Quality Management System
- Documentation and references:
  - Data and methods tied to Countryside Survey 2007 reporting and related papers (Rawlins et al. 2013/2015; Emmett et al., Carey et al., Bunce et al.)
  - Detailed methodological background available in referenced CEH reports and journals

## Data usage, access, and licensing
- Data access: Countryside Survey data, including soils, are hosted by UKCEH/CEH and linked through the Countryside Survey website and CEH data catalogue.
- Acknowledgement requirement: All use of Countryside Survey data must be acknowledged with the provided statement:
  - "Countryside Survey data owned by UK Centre for Ecology & Hydrology" and copyright notice.
- Dataset scope and limitations:
  - Aperture limited to 419 soils across 150 squares; derived from archived soils and lab methods described above
  - DR values reflect a non-rescaled PSD approach (DR 2000) and are not the DR 500 variant
  - Metadata include land class (LC07), country, county, and environmental zone descriptions to support cross-border analyses

## Implications for data stewardship
- Governance: robust QA/QC, standardized laboratory protocols, and ISO 9001:2015-compliant processes support data reliability and reproducibility.
- Metadata and interoperability: clearly defined column schemas, units (µm for PSD/MWD), and coded fields (LC07, COUNTRY, etc.) facilitate reuse and integration with other Countryside Survey datasets.
- Data updates and discoverability: data are part of a broader, nationally representative soil dataset; ensure linkage to the Countryside Survey data portal and UKCEH archives for discoverability and versioning.
- Common challenges to consider:
  - Representativeness given archived samples and 2007 sampling scope
  - Consistency across formats and potential future protocol revisions or reprocessing
  - Clear attribution when datasets are used in secondary analyses or publications