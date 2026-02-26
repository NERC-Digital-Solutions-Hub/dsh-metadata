# Soil profile descriptions, biomass data and vegetation species from a joint sampling event at Sourhope, Scotland, 2000 [NERC Soil Biodiversity Programme]

## Overview
- The NERC Soil Biodiversity Thematic Programme (established 1999) conducted intensive study of a large field experiment at Sourhope, focusing on soil biota diversity and functional roles in ecological processes.
- On 27–28 July 2000, a joint sampling event coordinated multiple project groups to collect baseline data across sampling blocks, providing linked measurements across biomass, vegetation, and soil profiles.
- Datasets cover: biomass data (roots, shoots, litter), vegetation species abundance, and soil profile descriptions (horizon types, depths, pH, and moisture).

## Datasets included
- NERC Soil Biodiversity Programme: Joint Sampling Event 2000: Root Cores Dataset (JT_SAMPLING_2000_ROOTS.csv)
  - Biomass data for roots, shoots, and litter from soil cores; sub-samples from main plots S–V; methods include oven drying and wet sieving.
  - Key fields include SUID, Sub_sample_ID, Sampling_Date, Treatment_Type, Block/Main_plot/Sub_plot, X_Cell/Y_Cell, core dimensions, various dry weights and density measures.
  - Originator: Macaulay Land Use Research Institute; Creation date: 26-02-2001; Contacts: J. Ross, L. Dawson.
- NERC Soil Biodiversity Programme: Joint Sampling Event 2000: Vegetation Survey Dataset (JT_SAMPLING_2000_VEG.csv)
  - Vegetation species abundance data for 18 cm x 18 cm soil blocks; species listed with abundance classes and percent cover mapped to Stace 1997 taxonomy.
  - Key fields include SUID, Sampling_Date, Treatment_Type (Control 1, Lime, Nitrogen, Nitrogen+Lime, Biocide), Block/Main_plot/Sub_plot, X_Cell/Y_Cell, Species, Abundance, %Cover.
  - Data structure supports linking to the root/core sampling context.
- NERC Soil Biodiversity Programme: Joint Sampling Event 2000: Soil Survey Dataset (JT_SAMPLING_2000_SOIL.csv)
  - Soil profile descriptions by horizon with pH and moisture values; methods for pH and moisture provided; Horizon_type and Depth_upper/lower fields included.
  - Key fields include SUID, Sampling_Date, Treatment_Type (Nitrogen+Lime, Lime, Nitrogen, Biocide, Control1), Block/Main_plot/Sub_plot, X_Cell/Y_Cell, Horizon_type, Depth_upper/depth_lower, pH_H2O, PC_Moisture, Moisture_voltage, etc.
  - Originators: University of Stirling / MLURI; Contact: P. Bruneau; Creation date: 27-09-2000.
  
## Methods, scope, and sampling design
- Field site: Sourhope Rigg Foot Field Experiment Site, Sourhope, Scottish Borders.
- Sampling period: 27–28 July 2000; sub-plots S, T, U, V across main plots A–F; Control 2 plots excluded from sampling.
- Core and sub-sampling: Single soil block per sub-plot per main-plot; cores subdivided and distributed to participants; multiple measurements collected per block.
- Analytical methods:
  - Root cores: oven dried 48 h at 80°C; biomass components (root, litter) measured after wet sieving (0.5 mm).
  - Vegetation: species presence/abundance recorded within each soil block; abundance classes converted to % cover using a defined scale.
  - Soil: horizon descriptions; pH measured via pH_H2O method; moisture via Thetaprobe and calibration to PC_Moisture (% vol); methods and calibration notes provided.
- Data provenance: Datasets created by MLURI and partners; dataset creation dates and dataset originators recorded; contact persons listed per dataset.
  
## Data structure and metadata
- Common schema elements across datasets:
  - SUID: Unique Sampling Unit Identifier (block/main-plot/sub-plot/cell, date, project code, sample type, dimensions).
  - Sampling_Date: Actual sampling date or period.
  - Block/Main_plot/Sub_plot: Plot identifiers; X_Cell and Y_Cell denote cell grid positions.
  - Treatment_Type: Lists of applicable soil treatments (e.g., Control, Lime, Nitrogen, Nitrogen+Lime, Biocide).
- Root Cores Dataset (JT_SAMPLING_2000_ROOTS.csv):
  - Variables include Height, Width, Breadth (core dimensions); Litter_DW, Root_DW (dry weights), Vol_litter, Vol_core, density metrics (DWTSHDENS, DWTDENSLITT, DWTDENSROOT).
- Vegetation Dataset (JT_SAMPLING_2000_VEG.csv):
  - Variables include Species, Abundance, and %Cover; Taxonomic reference: Stace 1997.
- Soil Dataset (JT_SAMPLING_2000_SOIL.csv):
  - Variables include Horizon_type, Horizon_subreg, Depth_upper, Depth_lower, Moisture_voltage, PC_Moisture, pH_H2O; pH and moisture measurement methods documented.
- Documentation and references:
  - Data dictionaries and field handbook references (SOURHOPE FIELD DATA HANDBOOK 2003; Scott et al., 2003) available via EIDC catalogue records.
  
## Quality control and provenance
- Quality control steps:
  - Numeric range checks, data formatting conformity, and logical integrity checks performed.
- Limitations and liability:
  - Data are subject to QA procedures, but NERC does not warrant accuracy or fitness for a particular use; no liability for loss or damage arising from use.
- Documentation and supporting information:
  - The Sourhope Field Data Handbook (2003) and related materials referenced for context and data interpretation.

## Access and governance considerations for Data Stewards
- Provenance and archiving:
  - Datasets linked to a common field experiment with multiple datasets and cross-referencing fields (SUID, Block/Main_plot/Sub_plot, cell coordinates) to enable integrated analyses.
- Metadata completeness:
  - Detailed metadata provided: dataset originator, contact, creation date, sampling period, methods, and data structure definitions to support discoverability and re-use.
- Standards and interoperability:
  - Data structured with explicit field definitions, units, and data types; cross-dataset consistency emphasized via shared identifiers (SUID) and concordant treatment types and plot designations.
- Data sharing and licensing considerations:
  - Clear liability disclaimer; access may be governed by institutional policies and the referenced EIDC records for supporting information.
- Ongoing stewardship:
  - Data described with potential utility for future re-use and cross-study comparisons; references to field handbook and primary publications support interpretability.