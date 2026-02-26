# Electrical resistance of trees and soils in Ankasa forest, Ghana

## Overview
- Dataset from Ankasa Conservation Area, southwestern Ghana, focusing on electrical resistance measurements in trees and surrounding soils.
- Collected in 2019 as part of the NERC project Lightning: An Invisible Driver of Tree Mortality in the Tropics? (Grant NE/P001564/1).
- Sample: 20 trees from different species (DBH 17.8–77.8 cm) and one liana (7.0 cm DBH) within a 50 ha forest plot (50 x 1 ha plots, subdivided into 25 m x 25 m subplots).
- Measurements taken in both wet (March) and dry (September) seasons.

## What the data contain
- Tree resistance data (TreeResistanceGhana2019.csv):
  - Species_name (binomial), Field_ID (tree code), D (DBH in cm).
  - Resistance to ground at 1.4 m and 0.7 m heights, for wet and dry seasons.
  - Inferred Trunk Resistance and Root Resistance (wet and dry).
- Soil resistance and moisture data (SoilResistanceGhana2019.csv):
  - Measurement points with identifiers (Point, date, Hour, Hectare, Subplot, Landcover, Direction).
  - Electrical measurements: Spike_spacing, Spike_depth, Resistance (Low_current, High_current), Resistivity.
  - soil moisture readings: Moisture_1, Moisture_2, Moisture_3 (percent).
- Soil moisture measured at 5 cm depth; line spacings include 2 m and 3 m, with other spacings possible depending on time.

## Data collection methods
- Tree resistance:
  - Instrument: Digital Earth Tester DET2/2 (Megger).
  - Method: Adapted Fall of Potential around a tree; eight nails placed around circumference at 1.40 m height, then at 0.70 m height.
  - Configurations: Eight nails, then subsets (4 nails, 2 nails) to estimate intercept, stem, and root resistivity.
- Soil resistance:
  - Instrument: DET2/2 with Wenner array configuration and line traverse method.
  - Setup: Four electrodes in line, spaced at known distance; outer electrodes supply current, inner electrodes measure potential.
  - Output: Apparent soil resistivity (and depth approximation equal to spacing a).
- Soil moisture:
  - Instrument: SM150T sensor (Delta-T Devices).
  - Depth: 5 cm, recorded at recorder line spacings of 2 m and 3 m (with potential for additional spacings).

## Data structure and files
- TreeResistanceGhana2019.csv
  - Columns include: Species_name, Field_ID, D, 1.4 mResistance (Wet), 0.7 mResistance (Wet), Trunk Resistance (Wet), Root Resistance (Wet), 1.4 mResistance (Dry), 0.7 mResistance (Dry), Trunk Resistance (Dry).
- SoilResistanceGhana2019.csv
  - Columns include: Point, date, Hour, Hectare, Subplot, Landcover, Direction, Spike_spacing, Spike_depth, Resistance (Low_current), Resistance (High_current), Resistivity, Moisture_1, Moisture_2, Moisture_3.
- Quality control: Measurements were recorded in the field; no further quality control was performed.

## Data quality and governance considerations for Data Leaders
- Sample size is limited (20 trees + 1 liana), which may affect generalizability to broader forest contexts.
- No post-collection QC beyond field recording; users should consider validation or cross-checks when integrating with other datasets.
- Metadata is provided via column headers and descriptions; ensure consistent interpretation of units (ohms for resistance, ohm-m for resistivity, percent for moisture) and the two-season context.
- Provenance: linked to a defined project/grant; consider licensing, attribution, and versioning for reuse.

## Potential value and use cases for data leadership
- Evaluate tree and soil electrical properties in tropical forests; study relationships between tree diameters, species, and resistivity.
- Analyze seasonal variations in trunk/root resistance and soil resistivity/moisture to inform forest health and mortality models.
- Integrate with other environmental or geophysical datasets to enhance understanding of subsurface properties in forest plots.
- Support data system planning: demonstrates how to document multi-modal measurements (biophysical, soil, moisture) and related metadata for discoverability and reuse.

## Practical considerations for data management and reuse
- Data discoverability: two CSV files with explicit column descriptions; consider hosting a data dictionary and DOI to improve traceability.
- Data integration: ensure harmonization of units and measurement contexts when combining with other datasets (e.g., resistivity vs. resistance, season labels).
- Data lifecycle: plan for versioning and potential updates if follow-up measurements are added; document any preprocessing steps if applied in future analyses.

## Limitations and recommended next steps
- Expand sampling to include more individuals and species for broader generalization.
- Implement formal data quality checks and validation procedures; document uncertainties and measurement errors.
- Enhance metadata with licensing, access rights, and a detailed data dictionary beyond column headers.
- Consider linking to geographic coordinates (if available) to enable spatial analyses and cross-dataset comparisons.