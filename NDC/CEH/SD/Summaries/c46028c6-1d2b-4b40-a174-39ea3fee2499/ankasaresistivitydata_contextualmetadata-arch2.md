# Electrical resistance of trees and soils in Ankasa forest, Ghana

## Overview and purpose
- Dataset measuring tree and soil electrical resistance in the Ankasa Conservation Area, southwestern Ghana.
- Part of the NERC project Lightning: An Invisible Driver of Tree Mortality in the Tropics? (Grant NE/P001564/1).
- Measurements collected in 2019 during wet (March) and dry (September) seasons to support environmental health monitoring and policy-relevant analyses.

## Study design and sample
- 20 trees from different species within a 50 ha forest plot (50 x 1 ha plots; each further divided into 16 subplots of 25 m x 25 m).
- Tree DBH ranged from 17.8 to 77.8 cm; one liana (Connarus africanus) with 7.0 cm DBH included.
- Trees with very pronounced buttressing, multiple stems, or stilt roots were avoided due to measurement constraints.
- Data also collected on soils and tree/soil interactions across wet and dry seasons.

## Data collection methods

- Tree resistance
  - Instrument: Digital Earth Tester DET2/2 (Megger).
  - Method: Adapted Fall of Potential around the tree with eight nails placed around the circumference at two heights (1.40 m and 0.70 m).
  - Configurations: Four nail configurations per height (to yield eight readings per tree).
  - Approach: Reciprocal method used to mitigate influence of finite contact area at nail-tree points; results used to estimate intercept, trunk, and root resistivity.

- Soil resistance
  - Instrument: Digital Earth Tester DET2/2 with Wenner array.
  - Setup: Four electrodes along a line with spacing (a); outer electrodes provide current, inner electrodes measure potential.
  - Depth: Electrode depth equal to 1/20th of the spacing; resistivity calculated as an approximation of soil resistivity at that depth.

- Soil moisture
  - Instrument: SM150T sensor (Delta-T Devices Ltd).
  - Depth: 5 cm.
  - Measurements taken for line spacings of 2 and 3 m (additional spacings possible if time allowed).

## Data files and structure

- TreesResistanceGhana2019.csv
  - Key fields: Species_name, Field_ID, D (diameter), 1.4 mResistance (Wet/Dry), 0.7 mResistance (Wet/Dry), Trunk Resistance (Wet/Dry), Root Resistance (Wet).

- SoilResistanceGhana2019.csv
  - Key fields: Point, date, Hour, Hectare, Subplot, Landcover, Direction, Spike_spacing, Spike_depth, Resistance (Low_current, High_current), Resistivity, Moisture_1, Moisture_2, Moisture_3.

## Quality control and limitations
- Quality control: Values were recorded in the field; no additional QC was performed on the data.
- Limitations: Field-collected data with no further QC; derived resistivity values are approximate and method-dependent; measurements conditioned by site-specific factors and the chosen sampling design.

## Data use, management, and provenance

- Data management: Two CSV files attached containing the measured data.
- Provenance: Collected as part of a broader environmental monitoring effort under the NERC-funded study on lightning and tree mortality.

## Relevance for monitoring and policy performance

- Provides standardized measurements of tree and soil electrical properties and moisture to support monitoring of environmental health and potential drivers of tree mortality.
- Demonstrates a structured, repeatable approach suitable for incorporation into broader environmental datasets and time-series analyses.

## Opportunities and challenges for analysts

- Opportunities: Potential to increase data value by integrating with other environmental datasets (e.g., climate, soil properties) and by making underlying data more accessible.
- Challenges: Ensuring broader data accessibility and interoperability; aligning field methods and units for cross-study comparisons.