# Physical and geochemical properties of saltmarsh soils produced from 33 wide diameter gouge cores spanning 19 UK saltmarshes collected between 2018-2021.

## Overview
- Describes physical and geochemical measurements of saltmarsh soils from 33 wide-diameter gouge cores across 19 UK saltmarshes (2018–2021).
- Used to calculate organic carbon burial rates across UK saltmarsh ecosystems.
- Dataset supports cross-site comparison by standardizing sampling and analysis procedures.

## Data collection and methods
- Sampling: 33 gouge cores with 60 mm diameter; cores cut into 1 cm sections (n = 1952 subsamples).
- Location recording: DGPS used to log sample-site coordinates; samples frozen at -20°C until analysis.
- Core descriptions: Classified using Troels-Smith scheme; depth-specific sampling performed.
- Bulk density: Wet and dry bulk densities measured from subsamples (g cm^-3).
- Carbon and nitrogen: Samples milled; TOC quantified with Elementar Soli TOC (temperature gradient method); OC and N quantified; OC measured as percentage by weight.
- Stable isotopes: ~12 mg per capsule for C and N isotopes; acid fumigation to remove carbonates for some analyses; δ13C_org and δ15N determined by EA-IRMS; calibration and QA procedures detailed.
- QA and calibration: TOC calibrated with CaCO3 and standard soils; isotopic values QA’d with high OC standards; lab equipment calibrated per university practices.

## Measurements and analysis
- Key variables: Elevation (m above OD), Troels-Smith substrate classification, wet/dry bulk density, organic carbon content (%), nitrogen content (%), carbon/nitrogen ratios (CN, NC), stable isotopes δ13C_org (‰) and δ15N (‰).
- Isotopic analysis: Acidified samples analyzed for OC and δ13C_org; nitrogen and δ15N analyzed; calibration against standards.
- Data are intended to support comparative analyses of OC stocks and burial dynamics across sites.

## Data structure and fields
- Primary data file: Physical_geochemical_properties_wide_cores.csv.
- Core fields include:
  - Core_ID; Saltmarsh; Marsh_type (Natural, Realigned); Marsh_zone (Low, High); Nation (Scotland, Wales, England).
  - Collection_year; Lat_dec_deg; Long_dec_deg; X_easting; Y_northing; Elevation_above_OD__m.
  - Sample_depth_cm; Mid_Point_depth_cm; Substrate.
  - Wet_bulk_density_g_cm_3; Dry_bulk_density_g_cm_3; OC_perc; N_Perc; CN; NC; d13C_per_mil; d15N_per_mil.

## Location and scope
- Geographic extent: United Kingdom.
- Site distribution intended to represent saltmarsh diversity in terms of sediment types and organic carbon content.
- Coordinates provided in decimal degrees (WGS84) with supporting easting/northing values.

## Data quality and provenance
- Field and lab procedures standardized; core descriptions and locations recorded consistently.
- Calibration standards and QA protocols applied for TOC and isotopic analyses.
- Documentation includes method references and calibration details to support reproducibility.

## Data formats and access
- Data output: CSV format with clearly defined fields and units.
- Documentation includes field descriptions and formats to facilitate reuse and integration with other datasets.

## References
- Dadey, K.A., Janecek, T., Klaus, A. (1992). Dry-bulk density: its use and determination.
- DIN 19539 (2015). Investigation of solids: TOC / ROC / TIC methodology.
- Harris, D., Horwáth, W.R., Van Kessel, C. (2001). Acid fumigation of soils before carbon analysis.
- Natali, C., Bianchini, G., Carlino, P. (2020). Thermal stability of soil carbon pools.
- Smeaton, C., Hunt, C.A., Turrell, W.R., Austin, W.E. (2021). Marine Sedimentary Carbon Stocks of the UK’s EEZ.
- Troels-Smith, J. (1955). Characterization of unconsolidated sediments.