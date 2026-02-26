# Summary Experimental Design/Sampling Regime

- Purpose: Document a field-based sampling regime to study earthworm presence, biomass, and community structure across hedges, margins, and field interiors, with accompanying soil properties, for GIS-based data products.

## Study locations and sampling design

- Sites and land uses
  - Little Langton (LL): organic arable (A1) and organic arable paired with organic ley (B1, B2)
  - Hutton Wandesley (HW): conventional ley (A1) and conventional arable (A2)
  - Overton (OV): conventional arable (A)
  - Whenby (WH): organic ley (A) and organic arable (B)
- Transect layout
  - One transect per sampling unit, laid at 90 degrees from the hedge into the field
  - Transects located mid-field length where possible; paired transects for WH/HW in appropriate fields; LL transects positioned on opposite sides of the hedge
  - Start points chosen where hedge condition was good
- Sampling points and distances
  - Along each transect: hedge position (0 m), field margin, and distances at 2 m, 4 m, 8 m, 16 m, 32 m, and 64 m into the field
- Sample identifiers and land-use pairings
  - Sample IDs include A1, A2 (organic arable), B1, B2 (organic ley/arable pairings)
  - Notes describe field conditions and pairing context (e.g., paired transects; margins; hedge conditions)

## Field collection methods

- Soil pit sampling
  - 18 × 18 × 15 cm pits along transect at hedge, margin, and specified distances
  - Mustard solution used to extract earthworms from pits
  - Collected earthworms preserved in ethanol and identified using Sims and Gerard field key
- Measurements taken at each pit
  - Soil moisture: three readings at 5 cm and 10 cm depths (in millivolts, mV)
  - Soil temperature: 5 cm and 10 cm depths (°C)
  - Soil bulk density: 5 cm and 15 cm depths (g/cm³) using 118 cm³ rings; density calculated on oven-dry basis
- Recorded values
  - Number of earthworms
  - Biomass (grams)
  - Distance from hedge (metres)
  - Depth indicators: Hedge (H) vs Margin (M)

## Data structure and files

- Earthworm landscape data files (9 files)
  - HWA1_EW_landscape.csv
  - HWB_EW_landscape.csv
  - LLA1_EW_landscape.csv
  - LLA2_EW_landscape.csv
  - LLB1_EW_landscape.csv
  - LLBS_EW_landscape.csv
  - OV7_EW_landscape.csv
  - WHA_EW_landscape.csv
  - WHB_EW_landscape.csv
- Structure of EW landscape files
  - Each file contains 30 columns with headings including:
    - Date, Field, Transect, Distance, Hedge (H) or Margin (M) indicator, Depth (Mustard = P or Topsoil = S), Sample type (A = abundance/count, B = biomass)
    - Code, Species name, and a column for each recorded species (e.g., Allolobophora chlorotica, Aporrectodea caliginosa, Eisenia fetida, Lumbricus terrestris, etc.), including endogeic, epigeic, and anecic groupings
- Soil data file
  - Landscape2016_soil_data.csv
  - 14 columns including: Date, field name, code, distance_m, hedge/margin designation, moisture readings (5 cm and 10 cm depths), soil temperature (5 cm and 10 cm), soil bulk density (5 cm and 15 cm)
- Miscellaneous reference
  - Earthworm functional groups mapping (Endogeic, Epigeic, Anecic) with example species
- Species coding and names
  - Codes and species mapping provided (e.g., Al-chl Allolobophora chlorotica; Ad-esi Allolobophoridella eiseni; Ap-cal Aporrectodea caliginosa; Eiseniella tetraedra; Lumbricus terrestris; etc.)

## Species groups and functional types

- Endogeic (soil-living, horizontal burrowing)
- Epigeic (litter-living)
- Anecic (soil-living, deep vertical burrows)
- Species are listed with corresponding codes in the dataset (e.g., Allolobophora chlorotica, Eisenia fetida, Lumbricus terrestris, etc.)

## References

- Sims & Gerard (1999) Earthworms (as the reference for identification and classification)

## GIS-focused implications and data products

- Spatial data layers to support map-based analyses
  - Sampling points: hedge-line and margin points, along transects at specified distances
  - Transects: line features representing 90-degree transect paths from hedges into fields
  - H/M attribute layer: binary indicator for whether a sample is from hedge or margin
  - Depth and type attributes: Mustard vs Topsoil designations; A/B sample types
  - Abundance/biomass attributes: per-species columns to derive species composition and functional-group distributions
  - Temporal dimension: date of sampling to enable time-series visualization
  - Soil properties: moisture, temperature, and bulk density associated with each pit location
- Potential map products
  - Hedge-edge vs interior soil biota distribution maps
  - Distance-based gradients of earthworm abundance/biomass and species composition
  - Layered views combining earthworm data with soil moisture and temperature
- Data quality and standards considerations
  - Aligning field identifiers and site codes across EW landscape files
  - Consistent coding for Hedge (H) vs Margin (M) and Mustard (P) vs Topsoil (S)
  - Handling missing data (blank cells indicate no data available)
  - Clear documentation for unit definitions and measurement methods to support reproducibility and interoperability
- Usage suggestions for GIS analysts
  - Integrate with spatially-referenced hedge and field boundary data
  - Create interactivity to filter by land-use type, distance from hedge, or depth
  - Combine with other agronomic layers (soil type, drainage, crop type) for environmental and policy analyses