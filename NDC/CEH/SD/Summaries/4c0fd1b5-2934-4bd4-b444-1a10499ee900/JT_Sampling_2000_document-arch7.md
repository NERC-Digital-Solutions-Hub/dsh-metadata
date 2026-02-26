# Soil profile descriptions, biomass data and vegetation species from a joint sampling event at Sourhope, Scotland, 2000 [NERC Soil Biodiversity Programme] Buckland, S., Cornish, C., Ray, N., Bruneau, P., Dawson, L., Ross, J.,

## Overview
- Describes the NERC Soil Biodiversity Programme and a joint sampling event (27–28 July 2000) at Sourhope, Sourhope Rigg Foot Field Experiment Site, to study soil biota diversity and functional processes.
- Documents three linked datasets generated from the event: Root Cores, Vegetation Survey, and Soil Survey (with associated metadata, methods, and quality controls).

## Study Site and Timing
- Location: Sourhope Field Experiment Site, Scottish Borders (Grid NT8545019630).
- Design: Coordinated sampling across main plots (A–F) and sub-plots (S, T, U, V) within each main plot; excluding Control 2 plots.
- Sampling window: 27–28 July 2000.
- Sampling units: Blocks 1–5; 18 × 18 cm soil blocks extracted per sub-plot, with sub-samples distributed to participants for various measurements.

## Datasets Available

- Root Cores Dataset (JT_SAMPLING_2000_ROOTS.csv)
  - Content: Biomass data for roots, shoots, and litter from soil cores; sub-sample cores ~4 × 4 × 8 cm.
  - Methods: Wet sieving (0.5 mm) to separate soil; oven-dried for 48 hours at 80°C; analyses by MLURI, Aberdeen.
  - Key fields: SUID, Sub_sample_ID, Sampling_Date, Treatment_Type, Block, Main_plot, Sub_plot, X_Cell, Y_Cell, Height, Width, Breadth, Vol_core, Vol_litter, DWTSHDENS, DWTDENS*, etc.
  - Data structure notes: Includes multiple derived density/volume metrics and dry weights for litter and roots.

- Vegetation Survey Dataset (JT_SAMPLING_2000_VEG.csv)
  - Content: Species abundance data for each soil block’s turf, recorded as abundance classes linked to 18 × 18 cm blocks; indicates presence/absence and relative abundance.
  - Abundance encoding: Abundance class with % cover mapping (e.g., not present, <5%, 6–25%, 25–50%, 50–75%, 75–100%).
  - Key fields: SUID, Sampling_Date, Treatment_Type (Control 1, Lime, Nitrogen, Nitrogen+Lime, Biocide), Block, Main_plot, Sub_plot, X_Cell, Y_Cell, Species, Abundance, %Cover.

- Soil Survey Dataset (JT_SAMPLING_2000_SOIL.csv)
  - Content: Soil profile descriptions by horizon (horizon types and depths) with pH and moisture measurements per horizon; includes field and lab procedures for pH and moisture.
  - Methods: pH measured with standard Sourhope protocol; moisture via Thetaprobe (volumetric moisture % after calibration).
  - Key fields: SUID, Sampling_Date, Treatment_Type, Block, Main_plot, Sub_plot, X_Cell, Y_Cell, Horizon_type, Horizon_subreg, Depth_upper, Depth_lower, Moisture_voltage, PC_Moisture, pH_H2O, etc.
  - Metadata notes: References to Soil Survey Field Handbook (Harpenden, 1974) and calibration details; dataset provenance includes MLURI and University of Stirling.

## Data Structure and Metadata Highlights
- Shared identifiers: SUID (Unique Sampling Unit Identifier) ties across datasets; includes Block, Main_plot, Sub_plot, X_Cell, Y_Cell, date, and sampling unit type.
- Sub-sampling details: Sub_sample_ID and core dimensions indicate nested sampling within each soil block.
- Qualitative and quantitative measures: Biomass weights (g), volumes (cm3), densities (g/m2 or mg/cm2); vegetation abundance classes; horizon-based soil chemistry (pH, moisture).
- Data standards and provenance: Dataset creators/curators include Macaulay Land Use Research Institute (now James Hutton Institute) and University of Stirling; references to Scott et al. (2003) and Hodgson & Avery (1974) for data handling and classification; creation dates in 2000–2001.

## Methods and Quality Control
- Biomass processing: Oven-drying, wet sieving, and lab analyses conducted at MLURI.
- Soil measurements: pH_H2O measured with deionised water; moisture content derived from Thetaprobe readings with calibration curves.
- QA/assurance: Numeric range checks, formatting checks, and logical integrity checks performed; data quality assurance applies, but no warranty of accuracy; liability disclaimer for use.
- Documentation: Data described as part of the SOURHOPE FIELD DATA HANDBOOK (Scott et al., 2003) and supported by CEH records.

## Practical Considerations for GIS Specialists
- Integrating datasets: Use SUID for cross-dataset joins; spatial context given by X_Cell and Y_Cell grid coordinates to map measurements to 2D locations within each block.
- Spatial resolution: Fine-scale blocks (18 × 18 cm) with horizon-level soil profiles; potential to create 2D maps (biomass, vegetation presence/abundance) and 3D soil layers by horizon depth.
- Data preparation: Transform sub-sample records into GIS-ready features; normalize and harmonize treatment codes and horizon categories; handle missing values and control-plot exclusions.
- Potential GIS analyses: Spatial distribution of biomass components, species distributions across blocks, horizon-specific pH/moisture patterns, and integration with other soil or biodiversity layers.
- Limitations to note: Exclusion of Control 2 plots in some datasets; resolution and scope limited to Sourhope site; data accuracy not guaranteed by the providing organization.

## Provenance and Access
- Original producers: Macaulay Land Use Research Institute (MLURI) and University of Stirling; Contact points include J. Buckland, L. Dawson, P. Bruneau.
- Dataset creation: Root Cores (26-02-2001), Vegetation (5-10-2000), Soil (27-09-2000).
- Key references: Scott et al. 2003; Stace 1997; Hodgson & Avery 1974.
- Usage note: Data carry liability disclaimer; suitable for research and GIS-based visualization with appropriate data handling and attribution.