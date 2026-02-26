# Electrical resistance of trees and soils in Ankasa forest, Ghana

## Overview
- Dataset comprising measurements of tree resistance to ground and soil resistance in the Ankasa Conservation Area, Ghana.
- Two CSV files:
  - TreeResistanceGhana2019.csv: measurements from 20 trees (various species) across 50 ha plot subdivided into 1 ha subplots, collected in wet (March) and dry (September) seasons in 2019.
  - SoilResistanceGhana2019.csv: soil electrical resistance, resistivity, and soil moisture data collected at measurement points within the same study area and time frame.
- Part of the NERC project “Lightning: An Invisible Driver of Tree Mortality in the Tropics?” (Grant NE/P001564/1).
- Data intended to support environmental health monitoring and assessment of ground/soil electrical properties and moisture in tropical forest contexts.

## Data collection and methods
- Tree resistance to ground
  - Instrument: Digital Earth Tester DET2/2.
  - Method: Adapted Fall of Potential for trees; eight nails placed around the tree at two heights (1.4 m and 0.7 m) in various configurations (eight readings per tree).
  - Outputs: intercept, stem (trunk) resistance, and root resistance for wet and dry seasons.
  - Tree selection: 20 trees from a 50 ha plot; representative dominant species; DBH 17.8–77.8 cm; one liana measured (Connarus africanus, 7.0 cm DBH); avoided buttressed/multi-stem/stilt roots due to access limitations.
- Soil resistance
  - Instrument: Digital Earth Tester DET2/2 with Wenner array.
  - Method: Line traverse with four electrodes at a fixed spacing; current injected via outer pair, potential difference measured by inner pair to compute resistance and estimated soil resistivity (depth ~ spacing a).
- Soil moisture
  - Instrument: SM150T sensor (Delta-T Devices).
  - Method: Surface soil moisture at 5 cm depth along measurement lines with spacings of 2 m and 3 m; additional spacings measured if time allowed.
- Study design and timing
  - Plot structure: 50 ha forest plot subdivided into 50 x 1 ha plots, each into 16, 25 m x 25 m subplots (0.0625 ha).
  - Seasons: Measurements conducted in wet (March) and dry (September) seasons of 2019.
  - Data collection scope: Measurements on 20 trees and concurrent soil/ moisture measurements across the study area.

## Data structure
- TreeResistanceGhana2019.csv
  - Species_name: binomial species name.
  - Field_ID: tree code from field.
  - D: diameter at 130 cm height (cm).
  - 1.4 mResistance (Wet), 0.7 mResistance (Wet): resistance to ground at stem heights.
  - Trunk Resistance (Wet): inferred resistance of a 1-meter stem just above ground.
  - Root Resistance (Wet): inferred root-to-ground resistance.
  - 1.4 mResistance (Dry), 0.7 mResistance (Dry): dry-season equivalents.
  - Trunk Resistance (Dry): dry-season trunk resistance.
- SoilResistanceGhana2019.csv
  - Point: measurement point ID.
  - date, Hour: date and hour of measurement.
  - Hectare, Subplot: location identifiers within the plot.
  - Landcover: land cover type.
  - Direction: measurement direction (E-W or N-S).
  - Spike_spacing, Spike_depth: electrode configuration details.
  - Resistance (Low_current), Resistance (High_current): measured soil resistance at different currents.
  - Resistivity: calculated soil resistivity.
  - Moisture_1, Moisture_2, Moisture_3: volumetric moisture content at various segments between electrode spikes.

## Quality control
- All values are field-recorded; no additional quality control (QC) was applied to the data beyond field measurements.

## Data quality and governance considerations for monitoring frameworks
- Metadata and transparency
  - Detailed method descriptions and column definitions are provided, supporting reproducibility and auditability.
- Data gaps and limitations
  - QC is limited to in-field measurements; lack of post-collection QC may affect data reliability.
  - Small sample size for trees (n=20) and potential species/selectivity biases; results may not generalize beyond the study area.
- Data accessibility and sharing
  - Data are organized into two CSV files with accompanying methodological detail; openness is supported by providing explicit measurement procedures and column definitions.
  - Potential barriers to reuse include the need to understand the specific field configurations and calibration details of the DET2/2 device and the Wenner array setup.
- Data governance implications
  - Clear documentation of measurement protocols and seasonal context aids interpretation and integration into monitoring frameworks.
  - The dataset exemplifies the importance of documenting measurement geometry, heights, electrode configurations, and environmental context for environmental health monitoring.

## Relevance for policy scrutiny and decision-making
- Provides baseline measurements of tree and soil electrical properties and surface moisture in a tropical forest, with seasonal contrast.
- Can inform assessments of forest health, root-soil coupling, and moisture dynamics relevant to environmental risk analysis and resilience planning.
- Highlights practical considerations for data collection governance, including the need for metadata completeness, data quality assurance, and sharing practices to enable timely, transparent use in decision-making.