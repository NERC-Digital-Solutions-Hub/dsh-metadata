# Details of data structure to ' HF_NW_herbage_quality.csv '

## Overview
- Supplement to supporting documentation for data series detailed in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Dataset: 13 columns, 96 rows, containing the herbage quality data.
- Data origin: grassland fertiliser trial 2016 conducted at Henfaes Research Station (Bangor University) and North Wyke Research Station (Rothamsted Research).

## Dataset structure and content
- Sample handling and laboratories:
  - Henfaes: pre-dried samples sent to Sciantec Analytical (Stockbridge Technology Centre).
  - North Wyke: fresh samples sent to Trouw Nutrition GB.
- Analytes and method:
  - Dry matter, acid-detergent fibre (ADF), ash, crude protein, metabolisable energy (ME), non-digestible fibre (NDF) measured using near-infrared spectrometry.
- Digestibility:
  - D = ME/0.16.
- Units:
  - All values expressed on a dry weight basis in g kg-1, except ME in MJ kg-1.
- Column headers and explanations (structure):
  - Date: Date of grass cut
  - Site: HF|NW (Henfaes or North Wyke)
  - N_app: Fertiliser applications (1|2|3); 1st & 2nd at 90 kg ha-1, 3rd at 60 kg ha-1
  - Block: Blocking factor of randomized block design (1|2|3|4)
  - Plot: Harvested plot (1–16)
  - Treatment: N fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea (agrotain), C = 0N control)
  - Dry_matter: g kg-1
  - ADF: g kg-1
  - Ash: g kg-1
  - Crude_Protein: g kg-1
  - ME: MJ kg-1
  - NDF: Neutral detergent fibre - cellulose, lignin and hemi-cellulose (listed as MJ kg-1 in this document)
  - D: Digestibility metric (%)

## Data provenance and handling
- Data are drawn from two trial sites within a single 2016 dataset, with clear sourcing of samples and subsequent lab analyses.
- Documentation cross-references the broader CINAg experiments and supporting materials (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf).

## Metadata and column definitions
- Clear definitions for each column to support discovery and reuse.
- Units clearly stated (dry weight basis; g kg-1; ME in MJ kg-1).
- Note: NDF units appearing as MJ kg-1 may be a documentation inconsistency; should be verified for accuracy.

## Data quality, standards, and governance considerations
- Ensure metadata aligns with dataset structure and units for consistent discovery.
- Verify and correct any potential unit inconsistencies (notably NDF).
- Maintain provenance by recording sample origin, lab pathway, and analysis method (NIR).
- Link to and align with the broader Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Plan for updates and sharing: upload to relevant data portals and catalogues; document any data processing or transformations performed.