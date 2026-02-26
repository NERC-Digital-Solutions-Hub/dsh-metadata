# Soil chemical properties from a field experiment in the Conwy Valley, North Wales, UK (20156)

## Overview
- Metadata for Soil_properties.csv from a field experiment in the Conwy Valley, North Wales (20156).
- Data capture soil chemical properties with spatial context to support map-based GIS visualization.
- Plot locations and metadata are provided to describe spatial references and plotting.

## Experimental design and sampling
- Three transects, each 75 m long and 20 m apart, running perpendicular to the river.
- Along each transect, intact soil cores were extracted at 2, 12, and 75 metres.
- Cores collected as 1 m lengths (with total core lengths up to 3 m as needed by soil depth); intact cores wrapped in thin-walled polyethylene sleeves and stored at 4°C prior to analysis.
- Field collection used a Cobra percussion hammer corer.

## Analytical methods and laboratory instrumentation
- Soil water content determined gravimetrically (24 h at 105°C).
- Soil organic matter (OM) by loss-on-ignition (450°C, 16 h).
- pH and electrical conductivity (EC) measured in a 1:2.5 soil-to-deionised water suspension.
- Nutrients and C/N measures:
  - NH4-N and NO3-N: 0.5 M K2SO4 extracts with colorimetric methods.
  - P: 0.5 M acetic acid extracts with ascorbic acid-molybdate blue method.
  - Total C (TC) and Total N (TN): TruSpec elemental analyzer.
  - Dissolved organic C (DOC) and Total dissolved N (TDN): 1:5 soil-to-0.5 M K2SO4 extracts with TOC analyzer.
- Microbial analyses:
  - Microbial biomass C and N via chloroform fumigation (72 h).
  - Phospholipid fatty acids (PLFA) via high-throughput 96-well method.
- Phosphorus sorption:
  - 1.0 g field-moist soil shaken with CaCl2 solution containing known P concentrations and 33P tracer.
  - After 2 h, supernatant measured by liquid scintillation counting to derive P adsorption.
  - Langmuir isotherms used to estimate P adsorption maxima (Pmax).
- Quality control: all samples analyzed in triplicate.

## Data structure and variables
- Column details include:
  - Transect (numeric), Row (numeric) identifying precise location.
  - Depth (cm) of soil sampled.
  - pH; EC (µS/cm); MC (percent moisture content); LOI (percent loss on ignition).
  - TOC (mg/g); TDN (mg/g).
  - Microbial_C (mg/g); Microbial_N (mg/g).
  - PO4_P (mg/kg); NH4_N (mg/kg); NO3_N (mg/kg).
  - CtoN_ratio; TC (g/kg); TN (g/kg).
  - Pmax (mg/kg); NH4Adsorp (mg/kg).
- Empty cells indicate missing data.
- Supporting location data:
  - Plot_locations.csv provides plot coordinates.
  - Plot_locations_metadata.rtf describes Plot_locations.csv.

## GIS relevance and use
- Data are aligned for map-based visualization of soil chemical properties across hillside transects.
- Georeferenced via plot/location metadata and transect/row coordinates.
- Depth-specific measurements enable 3D or layered GIS analyses of soil chemistry and related factors (e.g., P sorption, microbial biomass).

## Summary of key attributes for GIS integration
- Spatial resolution: transects with location codes and depths.
- Variables cover soil chemistry (pH, EC, moisture, OM, C/N, nutrient species), carbon/nitrogen pools, microbial indicators, and phosphorus dynamics.
- Units provided to support accurate mapping and cross-dataset joins (e.g., EC in µS/cm, LOI %, TOC mg/g, TC TN in g/kg).