# Extensive_Intensive_Spatial_README.docx

## Overview
- A single time-point spatial dataset for two sites (Extensive and Intensive) including site characteristics, soil parameters, and soil greenhouse gas (GHG) emissions.
- Sampling design:
  - Extensive site: 112 points on a 30 m × 30 m grid across 11.5 ha, plus 3 random points (n = 115).
  - Intensive site: 78 points on a 15 m × 15 m grid plus an offset 25 m × 25 m grid (21 points) for a total of n = 99 across 1.78 ha.
- Location marking:
  - Extensive: GeoXT handheld GPS (Trimble).
  - Intensive: Real Time Kinematic (RTK) surveying with Trimble R6/R8 equipment.
- Gas sampling: Air-tight static chambers; two-point headspace sampling (0 and 60 min for Extensive; approximate initial concentrations using ambient air for Intensive with 40 min post-closure sampling).
- GHG analysis: CO2, N2O, and CH4 quantified with a Perkin Elmer Clarus 580 GC (N2O with electron capture detector; CO2 and CH4 with flame ionisation detector).
- Other measurements: Bulk density, soil moisture, soil organic matter (loss-on-ignition), soil pH, extractable N (NO3– and NH4+), total C and N, and C:N ratio.
- Spatial context: Elevation, slope, aspect, and Compound Topographic Index (CTI) derived from 1 m LiDAR data.
- Data headers define a comprehensive table of sample attributes and measured variables.

## Data collection and processing
- Site characteristics and grid references were assigned to each sampling point with precise coordinates (Easting, Northing).
- Gas sampling times chosen to balance throughput and linearity assumptions; extensive site used 0 and 60 min; intensive site used ambient approximations for 0 min and 40 min post-closure.
- Chamber materials differed by site (smaller chambers at Extensive; cuboid chambers at Intensive) to accommodate sampling scale.
- Bulk density determined from oven-dried cores; WFPS calculated from volumetric water content and porosity (site-specific particle density assumptions: 1.4 g cm^-3 organic and 2.65 g cm^-3 mineral for Extensive; 2.65 g cm^-3 for Intensive).
- Gravimetric soil moisture obtained by oven drying; organic matter via LOI at site-appropriate temperatures.
- Soil pH measured with method variations due to site differences in sample preparation.
- Extractable N forms:
  - Extensive: 0.5 M K2SO4 extraction with colorimetric NO3–/NO2– and NH4+ assays.
  - Intensive: 2 M KCl extraction with Aquakem 250 analyzer; NO2– inferred as total oxidised N due to low NO2– levels.
- Total soil C and N:
  - Extensive: measured on oven-dried, ground soils with a TruSpec elemental analyzer.
  - Intensive: measured on sieved, oven-dried, ground soils with Carlo Erba NA2000 analyzer coupled to a PDZ isotope ratio mass spectrometer.
- Data sources for environmental context (elevation, slope, aspect, CTI) derived from 1 m LiDAR datasets and related soil/topographic literature.

## Data structure and headers
- Site: Extensive or Intensive.
- Sample_ID: Unique sample reference.
- Grid: Grid size used for the sampling point.
- Easting / Northing: Grid-based coordinates.
- N2O_flux, CO2_flux, CH4_flux: Gas flux measurements with specified units.
- Bulk_density: Soil bulk density (g cm^-3).
- WFPS: Water-filled pore space (%).
- Soil_moisture: Gravimetric moisture (%).
- Organic_Matter: Organic matter content (%).
- Soil_pH: Soil pH value.
- Soil_NO3N: Nitrate-N concentration (mg NO3-N kg^-1 soil DW).
- Soil_NH4N: Ammonium-N concentration (mg NH4-N kg^-1 soil DW).
- Total_C: Total soil carbon (% dry soil).
- Total_N: Total soil nitrogen (% dry soil).
- CtoN: Carbon-to-nitrogen ratio (dry soil).
- Elevation: Sampling point elevation (m above sea level).
- Slope: Sampling point slope (degrees).
- CTI: Compound Topographic Index (1 m DTMs).
- Aspect: Slope aspect (degrees).
- Veg_type/Org_Spread: Vegetation type at the Extensive site; manure spreading details at the Intensive site.

## Data quality, limitations, and stewardship
- Methods adhere to established standards and literature references, enabling reproducibility and cross-study comparability.
- Two-site approach uses different measurement and extraction protocols; note potential interoperability considerations (e.g., extraction solvents, pH measurement protocols, and instrument types).
- Temporal aspect: single time-point dataset; users should consider temporal variability when comparing sites or integrating with time-series data.
- Data completeness and consistency are supported by detailed metadata, site annotations, and explicit units for all fields.
- Data provenance includes author list and project/grant information, aiding proper attribution and accountability.

## Data governance and stewardship
- Metadata reflects comprehensive provenance: project name, contributing institutions, and grant numbers.
- Data are structured with explicit field names, units, and standardized coding for categorical fields (e.g., Site, Grid).
- Clear documentation of sampling design, measurement methods, and data processing steps enhances discoverability and reuse.
- Encouraged practices for stewardship:
  - Maintain versioned datasets with changelog and method updates.
  - Preserve raw and processed data alongside metadata to support validation and re-analysis.
  - Facilitate data sharing via appropriate portals, with notes on any usage restrictions or caveats (e.g., site-specific methodological differences).
  - Align with data governance policies to ensure proper storage, access control, and long-term preservation.

## References
- Ball, D.F. (1964); Ben-Dor, E., Banin, A. (1989); Chadwick et al. (2014); Davies, B.E. (1974); De Klein, C.A.M., Harvey, M. (2012); Evans, J.S., et al. (2014); Ferraccioli, F., et al. (2014); Jones, D.L., Willett, V.B. (2006); Krom, M.D. (1980); MAFF (1986); Miranda, K.M., Epsey, M.G., Wink, D.A. (2001); Moore, I.D., Grayson, R.B., Ladson, A.R. (1991); Mulvaney, R.L. (1996); Rowell, D.L. (1994); Searle, P.L. (1984); Sørensen, R., Zinko, U., Seibert, J. (2006).