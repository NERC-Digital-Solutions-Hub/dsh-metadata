# Soil chemical properties from a field experiment in the Conwy Valley, North Wales, UK (20156)

## Overview
- Metadata for Soil_properties.csv from a field experiment conducted in May 2016 in the Conwy Valley, North Wales, UK.
- Study focus: soil chemical properties across transects with depth-specific sampling; data intended to support analysis of soil chemical status, carbon and nitrogen pools, microbial indicators, and phosphorus dynamics.

## Experimental design and sampling regime
- Three transects, each 75 m long, 20 m apart, across a hillslope and perpendicular to the river.
- Along each transect, intact soil cores were extracted at 2, 12, and 75 metres.
- Core lengths were prepared as 1 m, 2 m, and 3 m lengths corresponding to depth exposure (row 1 = 1 m, row 2 = 2 m, row 3 = 3 m; total cores n = 18 × 1 m lengths across sampling).
- Cores collected in May 2016 using a Cobra percussion hammer corer; cores wrapped to preserve integrity and stored at 4°C prior to analysis.

## Collection, fieldwork and laboratory instrumentation
- Field sampling: Cobraq percussion hammer corer used for intact soil core extraction.
- Laboratory location: Bangor University, School of Environment, Natural Resources and Geography.
- Storage: samples kept at 4°C before analysis.

## Analytical methods
- Soil water content: gravimetric (24 h, 105°C).
- Soil organic matter: loss-on-ignition (LOI) at 450°C (16 h).
- pH and electrical conductivity (EC): measured in 1:2.5 soil-to-deionised water suspension using standard electrodes.
- Nutrients in 0.5 M K2SO4 extracts (1:5 w/v):
  - NH4-N and NO3-N via colorimetric methods (Mulvaney 1996; vanadate method).
  - PO4-P via ascorbic acid-molybdate blue method (Murphy and Riley 1962).
- Total carbon (TC) and total nitrogen (TN): TruSpec elemental analyzer.
- Dissolved organic C (DOC) and total dissolved N (TDN): 1:5 soil-to-0.5 M K2SO4 extracts with TOC analyzer (Multi N/C 2100).
- Microbial biomass C and N: chloroform fumigation (72 h; k_ec = 0.45, k_en = 0.54).
- Phospholipid fatty acids (PLFA): 96-well high-throughput method (Buyer and Sasser 2012).
- Phosphorus sorption: 1.0 g soil shaken in CaCl2 with known P concentrations, spiked with 33P tracer; 2 h equilibration; measurement via liquid scintillation counting; adsorption inferred from difference in initial vs. final activity; Langmuir isotherm-based estimation of P adsorption maxima (Pmax).

## Data columns and units
- Transect: Transect identifier (refers to cage/location).
- Row: Row within transect (refers to precise cage location).
- Depth: Depth of soil sampled (cm).
- pH: pH (unitless).
- EC: Electrical conductivity (µS/cm).
- MC: Moisture content (%).
- LOI: Loss on ignition (%).
- TOC: Total organic carbon (mg/g).
- TDN: Total dissolved nitrogen (mg/g).
- Microbial_C: Microbial carbon (mg/g).
- Microbial_N: Microbial nitrogen (mg/g).
- PO4_P: Soluble reactive phosphorus (mg/kg).
- NH4_N: Ammonium-N (mg/kg).
- NO3_N: Nitrate-N (mg/kg).
- CtoN_ratio: Carbon-to-nitrogen ratio (dimensionless).
- TC: Total carbon (g/kg).
- TN: Total nitrogen (g/kg).
- Pmax: Maximum phosphorus adsorption (mg/kg).
- NH4Adsorp: Ammonium adsorption (mg/kg).
- Depth, Transect, Row define the sample location; Empty cells indicate no data.

## Quality control
- All samples analyzed in triplicate.

## Supporting documents and data structure references
- Plot_locations.csv: Details of plot locations.
- Plot_locations_metadata.rtf: Description of Plot_locations.csv.

## Data access and usage notes
- The dataset includes extensive metadata linking each measurement to precise transect, row, and depth coordinates.
- Measurements cover soil physicochemical properties, organic matter content, nutrient pools, microbial indicators, and phosphorus sorption dynamics.
- Suitable for cross-dataset analyses of soil health, nutrient cycling, and microbial community responses across depth and transect locations.
- Be aware of unit distinctions across variables (e.g., mg/g vs g/kg vs mg/kg) and depth-specific sampling structure when combining with other datasets.