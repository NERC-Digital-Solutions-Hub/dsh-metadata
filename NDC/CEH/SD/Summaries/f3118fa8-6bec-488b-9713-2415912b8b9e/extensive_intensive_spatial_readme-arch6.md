# Extensive_Intensive_Spatial_README.docx

- Scope: A single time-point spatial dataset detailing site characteristics, soil parameters, and soil greenhouse gas (GHG) emissions for two sites (Extensive and Intensive) associated with Uplands-N 2 O and Rothamsted Research projects and Farm Platform, with specific grant numbers and a team of authors.

- Data content overview:
  - Two study sites: Extensive (11.5 ha) and Intensive (1.78 ha).
  - Site characteristics and soil properties captured at multiple sampling points across grids.
  - Soil GHG flux measurements (N2O, CO2, CH4) alongside soil physical and chemical properties.

- Sampling design and locations:
  - Extensive site: 112 points on a regular 30 m × 30 m grid plus 3 random points (total n = 115).
  - Intensive site: 78 points on a 15 m × 15 m grid plus 21 points on a 25 m × 25 m offset grid (total n = 99).
  - Locations recorded with field GPS/RTK methods (GeoXT for Extensive; Trimble GNSS for Intensive).

- Gas sampling methodology:
  - Air-tight static chambers used at both sites (smaller cylindrical at Extensive; cuboid at Intensive).
  - Sampling times: 0 min and 60 min at Extensive; 0–40 min for Intensive (ambient initial sample).
  - Two-point headspace sampling employed due to large chamber numbers; aimed for linear increases in concentration.
  - Fluxes measured for soil headspace: N2O, CO2, CH4 using Perkin Elmer Clarus 580 GC (ECD for N2O; FID for CO2/CH4).
  - Note: CO2 fluxes represent soil and plant respiration without photosynthesis due to chamber opacity.
  - Sampling window for gas measurements conducted by trained researchers to minimize time-of-day effects.

- Soil sampling and analyses:
  - Bulk density sampling: 100 cm3 cores (0–5 cm Extensive; 0–10 cm Intensive); cores dried and weighed to determine bulk density.
  - Soil samples: Bulked composites within chamber areas; stored at 4°C prior to analysis.
  - Water-filled pore space (WFPS) and gravimetric moisture content (wet mass vs. oven-dried) calculated.
  - Soil porosity and particle density assumptions differ by site (Extensive uses mixed organic/mineral with densities 1.4 and 2.65 g/cm3; Intensive uses 2.65 g/cm3).
  - Soil organic matter (SOM) via loss-on-ignition (LOI) with site-specific temperatures and durations.
  - pH measurement methods differ by site (Extensive: pH in distilled water; Intensive: pH in deionised water after air-drying and grinding).
  - Extractable inorganic N:
    - Extensive: 0.5 M K2SO4 extraction; NO3– and NH4+ measured colorimetrically (Miranda et al. 2001; Mulvaney 1996).
    - Intensive: 2 M KCl extraction; NO2–/NO3– determined via a photometric analyzer (Griess-type reduction for total oxidised nitrogen).
  - Total soil C and N:
    - Extensive: Oven-dried, ground soils analyzed on a TruSpec Analyzer.
    - Intensive: Sieved, oven-dried, ground soils analyzed on a Carlo Erba NA2000 elemental analyzer coupled to a mass spectrometer.
  - Isotopic analyses conducted (Implied via coupled instrument setup for Intensive).

- Geospatial and topographic data:
  - Elevation, slope, and aspect derived from 1 m LiDAR grids from specified repositories.
  - Compound Topographic Index (CTI) calculated from LiDAR data.

- Data headers and variable descriptions:
  - Site: Extensive or Intensive.
  - Sample_ID: Unique sample reference.
  - Grid: Grid size used for sampling.
  - Easting/Northing: Grid coordinates.
  - N2O_flux, CO2_flux, CH4_flux: GHG flux measurements with specified units.
  - Bulk_density: Soil bulk density (g cm-3).
  - WFPS: Water-filled pore space (%).
  - Soil_moisture: Gravimetric soil moisture content (%).
  - Organic_Matter: Soil organic matter content (%).
  - Soil_pH: Soil pH (method varies by site).
  - Soil_NO3N: Nitrate-N concentration (mg NO3-N kg-1 soil DW).
  - Soil_NH4N: Ammonium-N concentration (mg NH4-N kg-1 soil DW).
  - Total_C: Dry soil total carbon (%).
  - Total_N: Dry soil total nitrogen (%).
  - CtoN: Carbon-to-nitrogen ratio.
  - Elevation: Sampling point elevation (m).
  - Slope: Sampling point slope (degrees).
  - CTI: Compound Topographic Index (1 m DTMs-derived).
  - Aspect: Slope aspect (degrees).
  - Veg_type/Org_Spread: Vegetation type at Extensive site; manure spreading location details at Intensive site (not within 2 m of boundary or 10 m of watercourse).

- References and methodological foundations:
  - Ball (LOI for OM/OC), Chadwick et al. (optimized chamber methods), Davies (LOI), De Klein & Harvey (chamber guidelines), Evans et al. (ArcGIS toolbox for terrain modelling), Ferraccioli et al. (LiDAR DSM data), Jones & Willett (DON/DOC quantification), Krom (Berthelot reaction), MAFF 1986 method references, Miranda et al. (nitrate/nitrite detection), Moore et al. (digital terrain modelling), Mulvaney (nitrogen methods), Rowell (soil methods), Searle (Berthelot reaction), Sørensen et al. (topographic wetness index.

- Practical notes for data users:
  - The dataset provides point-based measurements on two contrasting field scales to support comparative analyses of soil GHG fluxes and soil properties.
  - Grid-based sampling coupled with precise geolocation enables spatial analyses (e.g., CTI, elevation, aspect) alongside biogeochemical measurements.
  - Differences in extraction methods, pH determination, and analytical instruments between sites should be accounted for in cross-site comparisons.
  - The dataset emphasizes self-contained measurements per sample, with clear units and methodological context to facilitate data integration and re-use.