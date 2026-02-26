# NERC Soil Biodiversity Programme: Joint Sampling Event 2000

## Context and Objectives
- NERC Soil Biodiversity Thematic Programme (established 1999) focused on intensive study of soil biota diversity and functional roles in ecological processes.
- Based at Sourhope, Macaulay Land Use Research Institute (now James Hutton Institute) in the Scottish Borders.
- 24 projects studied soil structure, processes (C and N cycles), microfauna, meso-fauna, and macro-fauna to understand soil biodiversity and function.
- The Joint Sampling Event (27–28 July 2000) coordinated sampling across project groups to link data to the same time and space, creating multiple datasets from the same field blocks.

## Sampling Event Details
- Location: Sourhope Rigg Foot Field Experiment Site (Grid NT8545019630).
- Sampling: From main plots, a single soil block per sub-plot (S, T, U, V) across each main plot, excluding Control 2 plots.
- Outcome: Initial 100 sample blocks with sub-samples distributed to participants to collect diverse datasets.
- Datasets collected include biomass (roots, shoots, litter), vegetation species abundance, and soil profile descriptions (horizon types, depths) with pH and moisture by horizon.

## Datasets Overview
- NERC Soil Biodiversity Programme: Joint Sampling Event 2000: Root Cores Dataset (JT_SAMPLING_2000_ROOTS.csv)
  - Content: Biomass data for roots, shoots, and litter from soil cores; sub-samples of larger soil blocks.
  - Methods: Oven-dry at 80°C for 48 hours; wet sieving (0.5 mm) to separate from soil.
  - Period and Location: 27–28 July 2000; Sourhope Rigg Foot Field Experiment Site.
  - Structure: Includes SUID, sampling details, Block/Main_plot/Sub_plot, X/Y cells, core dimensions, various weight/volume measurements, and density metrics.

- NERC Soil Biodiversity Programme: Joint Sampling Event 2000: Vegetation Survey Dataset (JT_SAMPLING_2000_VEG.csv)
  - Content: Vegetation species abundance within each soil block, recorded as abundance classes (Stace 1997 taxonomy).
  - Period and Location: 27–28 July 2000; Sourhope Rigg Foot Field Experiment Site.
  - Structure: SUID, date, treatment type (Control 1, Lime, Nitrogen, Nitrogen+Lime, Biocide), block structure, cell coordinates, species, and abundance/% cover.

- NERC Soil Biodiversity Programme: Joint Sampling Event 2000: Soil Survey Dataset (JT_SAMPLING_2000_SOIL.csv)
  - Content: Soil profile descriptions by horizon with corresponding pH and moisture by horizon.
  - Methods: pH measured in soil-water slurry; moisture via Thetaprobe and laboratory calibration for %vol moisture.
  - Period and Location: 27–28 July 2000; Sourhope Rigg Foot Field Experiment Site.
  - Structure: SUID, date, treatment type, block structure, cell coordinates, horizon category and subregion, depth bounds, moisture readings, and pH data.

## Data Structure and Provenance
- Common identifiers: Unique Sampling Unit Identifier (SUID) tying blocks, plots, sub-plots, cells, dates, and project code.
- Sub-sample identifiers and detailed dimension fields (e.g., X_Cell, Y_Cell, Height, Width, Breadth) aid cross-dataset linking.
- Dataset creators/Originators: Macaulay Land Use Research Institute (MLURI) and University of Stirling; key contacts include J. Buckland, L. Dawson, P. Bruneau.
- References and guidance: Data linked to SOURHOPE FIELD DATA HANDBOOK (Scott et al., 2003).

## Data Quality, Governance, and Usage Notes
- Quality control: Numeric range checks, formatting checks, and logical integrity checks applied.
- Limitations: Data are subject to QA but not warrantied for accuracy; no liability accepted by NERC for use of the data.
- Accessibility context: Datasets are available with supporting information through EIDC catalogue records; provides researchers with metadata and dataset lineage.

## Access, Licensing, and Documentation
- Dataset creation dates: Root Cores (26-02-2001); Vegetation Survey (05-10-2000); Soil Survey (27-09-2000).
- Documentation references: SOURHOPE FIELD DATA HANDBOOK (2003) and related methodological notes; data may be accessed via EIDC catalogue records.
- Contacts: Dataset originators and dataset creation contacts listed per dataset (e.g., Buckland, Dawson, Bruneau).

## Implications for Data Leaders
- Demonstrates handling of multi-source, multi-dataset experiments tied to a common sampling event, highlighting the importance of:
  - Robust, unique identifiers (SUID) for cross-dataset integration.
  - Clear metadata and data dictionaries to enable harmonization across biomass, vegetation, and soil datasets.
  - Standardized data collection and documentation practices (e.g., horizons, treatment codes, sampling blocks).
  - Data quality processes and explicit governance/limitation statements to manage risk and user expectations.
  - Reference to governance and curation resources (handbooks, catalogue records) to bolster discoverability and reuse.