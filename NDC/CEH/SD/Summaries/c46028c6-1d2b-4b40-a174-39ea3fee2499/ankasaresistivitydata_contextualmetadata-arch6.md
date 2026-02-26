# Electrical resistance of trees and soils in Ankasa forest, Ghana

## Overview
- A dataset from Ankasa Conservation Area in southwestern Ghana, including measurements on 20 trees (plus one liana) across two seasons in 2019 (wet March and dry September).
- Measurements cover tree resistance to ground and adjacent soils, soil resistivity, and surface soil moisture.
- Part of the NERC project Lightning: An Invisible Driver of Tree Mortality in the Tropics (grant NE/P001564/1).
- Data are provided as two CSV files: TreeResistanceGhana2019.csv and SoilResistanceGhana2019.csv.

## What data are included
- TreeResistanceGhana2019.csv
  - Tree-related measurements per tree: species, field ID, diameter (D) at 130 cm height.
  - Resistance to ground at two stem heights (1.4 m and 0.7 m) for Wet and Dry seasons.
  - Inferred trunk resistance (per meter of stem) and inferred root resistance (Wet).
- SoilResistanceGhana2019.csv
  - Soil measurement metadata and results: measurement point, date, hour, hectare/subplot/location, land cover, measurement direction, spike spacing and depth.
  - Low-current and high-current resistance measurements, computed resistivity of soil.
  - Surface soil moisture at three positions (Moisture_1, Moisture_2, Moisture_3).

## Data collection methods
- Tree resistance to ground
  - Instrument: Digital Earth Tester DET2/2 (Megger).
  - Method: adapted Fall of Potential for trees; eight nails placed around the tree circumference at two heights (1.40 m and 0.70 m).
  - Measurements: four nail configurations per height, yielding eight readings per height; reciprocal approach used to account for finite contact area.
  - Outputs: intercepts and resistance estimates for trunk (stem) and root to ground resistivity.
- Soil resistance
  - Instrument: Digital Earth Tester DET2/2 with Wenner array in a line traverse.
  - Four electrodes aligned; current via outer pair (C1/C2), potential via inner pair (P1/P2).
  - Depth/spacing: electrode depth equal to 1/20 of the spacing; depth and spacing follow the Wenner configuration.
  - Output: apparent soil resistivity at measurement depth.
- Soil moisture
  - Instrument: SM150T sensor (Delta-T Devices).
  - Depth: 5 cm.
  - Line spacings: 2 m and 3 m (plus additional spacings if time allowed).

## Study design and sampling
- Plot and tree selection
  - 20 trees representing dominant species within a 50 ha forest plot (50 plots of 1 ha each; subplots of 0.0625 ha).
  - DBH range: 17.8 to 77.8 cm for measured trees; one liana (Connarus africanus) with 7.0 cm DBH included.
  - Preference to avoid trees with pronounced buttressing, multiple stems, or stilt roots due to measurement practicality.
- Seasonality
  - Measurements conducted during wet (March) and dry (September) seasons of 2019.
- Context
  - Data collection linked to broader study on the role of lightning as a driver of tree mortality in tropical forests.

## Data structure details
- Two CSV files are provided:
  - TreeResistanceGhana2019.csv
    - Columns include: Species_name, Field_ID, D (diameter), 1.4 mResistance (Wet), 0.7 mResistance (Wet), Trunk Resistance (Wet), Root Resistance (Wet), 1.4 mResistance (Dry), 0.7 mResistance (Dry), Trunk Resistance (Dry) (and corresponding descriptions/units).
  - SoilResistanceGhana2019.csv
    - Columns include: Point, date, Hour, Hectare, Subplot, Landcover, Direction, Spike_spacing, Spike_depth, Resistance (Low_current), Resistance (High_current), Resistivity, Moisture_1, Moisture_2, Moisture_3 (and corresponding descriptions/units).
- Quality control
  - Values are field-recorded; no additional quality control was performed beyond field measurement procedures.

## Practical guidance for data use
- Potential analyses
  - Compare wet vs. dry season tree resistances to assess seasonal effects on stem/root resistance.
  - Explore relationships between tree diameter (D) and resistance measurements to infer size-related trends.
  - Link soil resistivity and surface moisture to tree/soil resistance measures, potentially examining spatial patterns across hectares and subplots.
  - Derive-derived metrics such as differences between heights (1.4 m vs 0.7 m) or between trunk and root resistances.
- Data integration and preparation
  - Join TreeResistanceGhana2019.csv and SoilResistanceGhana2019.csv by common contextual identifiers (e.g., field IDs, tree locations if available) where appropriate.
  - Ensure consistent unit handling (ohms for resistance, ohm m for resistivity, percentage for moisture).
  - Consider small sample size (20 trees) when performing inferential statistics; descriptive guidance and visualization may be most robust.
- Outputs and sharing
  - Possible dashboards and reports could present seasonally differentiated resistance profiles by species, with interactive filters for height, location, and soil moisture/resistivity.

## Notes and considerations
- The dataset provides rich field-based measurements with explicit methodological detail on measurement heights, nail configurations, and Wenner array setup, enabling reproducibility and transparent interpretation.
- No post-field QC means users should be mindful of potential measurement variability due to environmental conditions, equipment calibration, or field constraints.