# Electrical resistance of trees and soils in Ankasa forest, Ghana

## Overview
- A dataset comprising measurements of tree resistance to ground and soil resistivity, collected in the Ankasa Conservation Area, southwestern Ghana, in 2019.
- Includes data for 20 trees from different species (plus one liana) within a 50 ha forest plot, sampled in both wet (March) and dry (September) seasons as part of the NERC project Lightning: An Invisible Driver of Tree Mortality in the Tropics.

## Data and methods
- Tree resistance measurements
  - Method: Adapted Fall of Potential using a Digital Earth Tester (DET2/2) with eight nails around the tree at two heights (1.40 m and 0.70 m).
  - Configurations: Various nail groupings to derive intercepts, stem, and root resistivity estimates.
  - Output: Eight readings per tree (four nail configurations × two heights) yielding estimates such as Trunk and Root Resistance (Wet and Dry).
- Soil resistance measurements
  - Method: Wenner array with four electrodes along a line (line traverse), using DET2/2; outer electrodes provide current, inner electrodes measure potential.
  - Depth: Spikes inserted to depth equal to 1/20th of spike spacing (a); results give soil resistivity.
- Soil moisture
  - Instrument: SM150T sensor; volumetric water content measured at 5 cm depth.
  - Line spacings: 2 m and 3 m (with potential for additional spacings if time allowed).
- Temporal scope
  - Measurements taken in both wet (March) and dry (September) seasons of 2019.

## Data files and structure
- Two CSV files:
  - TreeResistanceGhana2019.csv
    - Key fields: Species_name, Field_ID, Diameter (D) at 130 cm, 1.4 m Resistance (Wet/Dry), 0.7 m Resistance (Wet/Dry), Trunk Resistance (Wet/Dry), Root Resistance (Wet/Dry), among others.
  - SoilResistanceGhana2019.csv
    - Key fields: Point, date, Hour, Hectare, Subplot, Landcover, Direction, Spike_spacing, Spike_depth, Resistance (Low_current/High_current), Resistivity, Moisture_1/2/3.
- Quality control: No post-collection QC beyond field recording.

## Spatial and environmental context
- Location: Ankasa Conservation Area, southwestern Ghana.
- Site layout: A 50 ha forest plot divided into 50 plots (1 ha each), further subdivided into 16 subplots of 25 m × 25 m (0.0625 ha).
- Relevance for GIS: Data are tied to plot/subplot identifiers and include directional and land cover metadata, enabling mapping of resistivity and moisture patterns across the study area.

## Data quality and limitations
- Quality control limited to in-field data capture; no additional QC/validation reported.
- Sample size is small (20 trees plus one liana), which may limit generalizability.
- Measurements are specific to experimental heights (1.40 m and 0.70 m) and a single study area, with potential site-specific influences (e.g., buttressing, root architecture).

## Potential GIS applications
- Create map-based visualizations of tree-ground resistivity and soil resistivity across the plot.
- Link resistivity and moisture patterns to landcover/subplot classifications and measurement directions.
- Integrate with other GIS layers (e.g., species distribution, DBH) to explore relationships between tree traits and soil/ground resistance.
- Use temporal (wet vs dry season) data to analyze seasonal variations in soil and tree resistivity.

## Access and provenance
- Authors: Stivanello, Silvio; Clark, David; Adu-Bredu, Stephen; Haddad, Manu; Hill, Timothy.
- Project context: Part of the NERC project Lightning: An Invisible Driver of Tree Mortality in the Tropics (Grant NE/P001564/1).