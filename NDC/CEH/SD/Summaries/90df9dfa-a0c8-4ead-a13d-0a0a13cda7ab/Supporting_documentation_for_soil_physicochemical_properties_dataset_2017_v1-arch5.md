# This document is a supplement to the supporting documentation for data series detailed in: 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf' Details of data structure to ' CINAg_digestate_experiment_2017_Soil_physicochemical_properties.csv'

## Overview
- Supplements the CINAg supporting documentation and describes the data structure for the CINAg_digestate_experiment_2017_Soil_physicochemical_properties.csv dataset.
- Digestate trial data from 2017; dataset comprises 35 columns and 180 rows.
- Data collected from two sampling times (T1 and T2) across three soil depths (0–15 cm, 15–30 cm, 30–60 cm) at two sites/platforms (NW North Wyke and HF Henfaes Farm).

## Dataset scope and context
- Focus: soil physicochemical properties measured in the 2017 digestate experiment.
- Intended for sharing/archiving and data discovery within CINAg experimental datasets.
- Each row represents a single sample, with a consistent set of 35 variables describing identifiers, sampling, treatments, soil depth, and a range of soil chemical, biological, and physical properties.

## Data structure and metadata (column headers and explanations)
- Core identifiers and sampling context:
  - Sample_ID: unique sample identifier (Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths)
  - Year: year of sampling
  - Site: farm platform (NW = North Wyke, HF = Henfaes Farm)
  - Sampling_date: date of sampling (dd/mm/yyyy)
  - Sampling_time: T1 (beginning after digestate application) or T2 (last harvest)
  - Plot: plot number
  - Treatment: C = Control, D = digestate, ADNI = acidified digestate with nitrification inhibitor DMPP
  - Depth_cm: soil depth (0–15 cm, 15–30 cm, 30–60 cm)
- Soil chemical and biochemical properties (units vary by parameter):
  - NH4_mgN_per_kg_soil; NO3_mgN_per_kg_soil
  - DOC_mgC_per_kg_soil; DON_mgN_per_kg_soil
  - Aminoacids_mgN_per_kg_soil; Peptides_and_proteins_mgN_per_kg_soil
  - MBC_mgC_per_kg_soil; MBN_mgN_per_kg_soil
- Soil physical and structural properties:
  - Aggr_b20µm_perc; Aggr_b250µm_perc; Aggr_b2000µm_perc
  - Sand_perc; Silt_perc; Clay_perc
  - Soil_moisture_perc
  - LOI_perc (loss-on-ignition; soil organic matter)
  - pH_deionised_water; pH_CaCl2
  - EC_µS_per_cm
- Soil carbon and nutrient pools:
  - POXC_mgC_per_kg_soil
  - PO4.P_mgP_per_kg_soil (citric acid extractable P)
  - totC_perc; totN_perc; CN_ratio
  - totP_mgP_per_kg; Olsen_P_mgP_per_kg_soil

## Measurement context and consistency notes
- All data pertain to the 2017 digestate experiment and follow the structure described in the accompanying documentation.
- The dataset uses explicit units for each parameter (as listed above) to support interoperability and reuse.
- Two sampling times (T1 and T2) provide temporal context for treatment effects and soil property changes.

## Data quality, provenance, and governance considerations
- Ensure alignment with the broader CINAg experimental documentation (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf).
- Validate that Sample_ID correctly encodes Year, Experiment, Site, Sampling_time, Treatment, Plot, and Depth information.
- Verify units and measurement methods for all 35 variables; maintain a data dictionary and method references in metadata.
- Handle missing values consistently and document any data suppression or omissions.
- Maintain clear provenance and versioning to support updates and traceability across revisions.

## Access, sharing, and stewardship implications
- Dataset is prepared for upload to data portals and catalogues as part of CINAg data holdings.
- Provide comprehensive metadata and the accompanying data dictionary to facilitate discoverability and reuse.
- Be mindful of any sharing limitations or embargoes (not specified in the excerpt) and document accordingly.
- Ensure ongoing data stewardship by recording updates, changes in treatment definitions, or schema evolution that may affect downstream users.