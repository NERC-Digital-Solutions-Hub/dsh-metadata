# Electrical resistance of trees and soils in Ankasa forest, Ghana

## Overview
- Study of electrical resistance in trees and soils within the Ankasa Conservation Area, southwestern Ghana.
- 20 trees from different species (dominant species in a 50 ha forest plot; DBH 17.8–77.8 cm) plus 1 liana (Connarus africanus, 7.0 cm DBH) were sampled.
- Measurements taken in two seasons: wet (March) and dry (September) in 2019.
- Part of the NERC project Lightning: An Invisible Driver of Tree Mortality in the Tropics? (Grant NE/P001564/1).

## Data collected and scope
- Tree measurements: resistance to ground at two stem heights (1.40 m and 0.70 m) and derived trunk/root resistances, for wet and dry seasons.
- Soil measurements: resistance to ground and calculated resistivity using a Wenner array; line traverse method; depth linked to spike spacing.
- Additional environmental data: soil moisture content measured near electrode locations.
- Measurements cover the same 20 trees across two seasons, within a 50 ha plot subdivided into 50 x 1 ha plots and further into 16, 25 m × 25 m subplots.

## Data collection methods
- Tree resistance to ground
  - Instrument: Digital Earth Tester DET2/2.
  - Method: adapted Fall of Potential for trees; eight nails around the tree circumference at two heights (1.40 m and 0.70 m).
  - Configurations: eight readings from different nail configurations; results interpreted with a reciprocal approach to reduce contact-area bias.
- Soil resistance and resistivity
  - Instrument: DET2/2 with Wenner array (four electrodes in line).
  - Procedure: outer electrodes provide current; inner electrodes measure potential; depth ≈ 1/20 of spike spacing.
  - Outputs: resistance values and calculated soil resistivity.
- Soil moisture
  - Instrument: SM150T sensor (Delta-T Devices).
  - Measurement: volumetric water content at 5 cm depth, along line transects with specified electrode spacings (2 m and 3 m; other spacings if time allowed).

## Data structure and contents
- Files provided:
  - TreesResistanceGhana2019.csv
    - Species_name; Field_ID; D (diameter at 1.30 m height) in cm.
    - 1.4 m Resistance (Wet) and 1.4 m Resistance (Dry).
    - 0.7 m Resistance (Wet) and 0.7 m Resistance (Dry).
    - Trunk Resistance (Wet) and Trunk Resistance (Dry).
    - Root Resistance (Wet). (Additional fields correspond to related measurements.)
  - SoilResistanceGhana2019.csv
    - Point; date (dd/mm/yyyy); Hour (HH); Hectare (Location ID); Subplot (Sublot ID).
    - Landcover; Direction (E-W or N-S); Spike_spacing (m); Spike_depth (m).
    - Resistance (Low_current); Resistance (High_current); Resistivity (Ω·m).
    - Moisture_1, Moisture_2, Moisture_3 (volumetric moisture content, %).
- Quality control note: values recorded in the field; no additional QC performed.

## Quality control and limitations
- Only field-recorded data; no post-collection QC beyond field measurements.
- Limitations include small sample size (20 trees plus 1 liana), single site, and potential measurement uncertainties inherent to in-field electrical resistance methods.
- Selection excludes trees with pronounced buttressing, multiple stems, or stilt roots.

## Potential analyses and applications for data analysts
- Correlation analyses between tree resistances (trunk/root) and soil resistivity; examine seasonal differences (wet vs dry).
- Relationships between tree diameter (D) and resistance measurements to explore size-dependent conductivity or grounding properties.
- Assess links between soil moisture (Moisture_1–3) and resistivity/ground resistance.
- Multivariate modeling to predict tree-ground resistance from tree traits, soil properties, moisture, season, and location within the plot.
- Explore spatial patterns across the 50 ha plot by linking Hectare/Subplot to resistance and soil metrics.
- Compare species-level differences in resistance responses if species identifiers permit grouping.

## Data accessibility and context
- Data originate from a field study linked to a larger project on lightning-driven tree mortality.
- Two CSV datasets encapsulate both biological (tree) and edaphic (soil) measurements, enabling integrated analyses of biotic–abiotic interactions related to ground resistance and moisture.