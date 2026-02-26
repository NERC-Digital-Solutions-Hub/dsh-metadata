# Extensive_Intensive_Spatial_README.docx

## Overview
- A single time-point spatial dataset capturing site characteristics, soil parameters, and soil greenhouse gas (GHG) emissions for two field sites: Extensive and Intensive.
- Sampling designs:
  - Extensive site: 112 sampling points on a regular 30 m × 30 m grid across 11.5 ha plus 3 random points (n = 115).
  - Intensive site: 15 m × 15 m grid (78 points) plus a 25 m × 25 m offset grid (21 points) for a total of 99 points across 1.78 ha.
- Measurements include N2O, CO2, and CH4 fluxes, alongside a suite of soil physicochemical properties and topographic variables.
- Data support analysis of soil GHG fluxes within a broader carbon and nitrogen cycling context and soil-plant interactions.

## Data content and structure
- Flux measurements:
  - N2O_flux (µg N2O-N m-2 h-1)
  - CO2_flux (mg CO2-C m-2 h-1)
  - CH4_flux (µg CH4-C m-2 h-1)
- Soil physical and chemical properties:
  - Bulk_density (g cm-3)
  - WFPS (soil water-filled pore space, %)
  - Soil_moisture (% gravimetric)
  - Organic_Matter (%)
  - Soil_pH
  - Soil_NO3N (mg NO3--N kg-1 soil DW)
  - Soil_NH4N (mg NH4+-N kg-1 soil DW)
  - Total_C (%)
  - Total_N (%)
  - CtoN (C:N ratio)
- Site and environmental metadata:
  - Elevation (m asl)
  - Slope (degrees)
  - CTI (Compound Topographic Index)
  - Aspect (degrees)
  - Veg_type/Org_Spread (vegetation type at Extensive; organic farmyard manure spread details at Intensive)
- Geospatial information:
  - Site (Extensive or Intensive)
  - Sample_ID (unique per sample)
  - Grid (grid size)
  - Easting, Northing (grid coordinates)
- Data headers provided for all variables with explicit units and data types.

## Methods and data collection
- Gas sampling:
  - Use of air-tight static chambers at both sites.
  - Extensive site: samples at 0 min and 60 min after chamber closure.
  - Intensive site: headspace initial concentrations approximated from ambient air; samples taken ~40 min after closure.
  - Rationale: two-point sampling suitable for large numbers of chambers; assumption of linear/logarithmic increase in concentrations over time.
  - Time-window for sampling conducted by trained teams to minimize time-of-day effects.
  - Note: CO2 fluxes reflect soil and plant respiration without photosynthesis due to chamber opacity.
- Gas analysis:
  - PerkinElmer Clarus 580 GC with electron capture detector for N2O and flame ionisation detector for CO2 and CH4.
- Soil sampling and processing:
  - Bulk density cores: 100 cm³ (0–5 cm at Extensive; 0–10 cm at Intensive).
  - Soil samples: bulked cores collected within chamber areas; stored at 4°C prior to analysis.
  - Gravimetric moisture: oven-dried at 105°C for 24 h.
  - Organic matter: loss-on-ignition in muffle furnace (450°C or 400°C depending on site).
  - pH: measured using standard methods with site-specific extraction approaches.
- Nutrient analyses:
  - Extensive: 0.5 M K2SO4 extraction; NO3− and NH4+ by colorimetric methods.
  - Intensive: 2 M KCl extraction; NO3−/NO2− via colorimetric methods; NH4+ via modified Berthelot reaction.
  - Total inorganic N (assumed NO3− when NO2− concentrations are low) and related measurements.
- Soil carbon and nitrogen:
  - Extensive: total C and N on oven-dried, ground soils with TruSpec analyzer.
  - Intensive: total C and N on sieved, oven-dried, ground soils with Carlo Erba NA2000; isotope ratio mass spectrometry for further analysis.
- Particle density and related calculations:
  - Extensive: assumed particle densities 1.4 g cm−3 (organic) and 2.65 g cm−3 (mineral).
  - Intensive: particle density assumed 2.65 g cm−3.
- Topography:
  - Elevation, slope, and aspect derived from 1 m LiDAR grids.
  - CTI calculated from LiDAR data; additional sources include Tellus South West project and related datasets.

## Data structure and headers
- Site: Extensive or Intensive
- Sample_ID: Unique sample reference
- Grid: Grid size (e.g., 30 m × 30 m, 15 m × 15 m + offset)
- Easting: Grid easting coordinate
- Northing: Grid northing coordinate
- N2O_flux: N2O flux
- CO2_flux: CO2 flux
- CH4_flux: CH4 flux
- Bulk_density: Soil bulk density
- WFPS: Water-filled pore space
- Soil_moisture: Gravimetric moisture
- Organic_Matter: Organic matter content
- Soil_pH: Soil pH
- Soil_NO3N: Nitrate nitrogen
- Soil_NH4N: Ammonium nitrogen
- Total_C: Total carbon
- Total_N: Total nitrogen
- CtoN: Carbon to nitrogen ratio
- Elevation: Elevation (m)
- Slope: Slope (degrees)
- CTI: Compound Topographic Index
- Aspect: Slope aspect (degrees)
- Veg_type/Org_Spread: Vegetation type or manure spreading context

## Data quality, limitations, and considerations
- Single time point: limited temporal resolution; suitable for snapshot comparisons rather than trends.
- Two-point sampling and approximations (Intensive site) introduce potential measurement uncertainty in gas fluxes.
- Different sampling regimes between sites (0/60 min vs. 0/40 min) and initial ambient estimates at Intensive site may affect comparability.
- Spatial heterogeneity: grid designs capture variability, but micro-site differences and management history (e.g., manure spreading) influence results.
- Metadata richness: comprehensive methods and references provided; detailed data dictionary aids reuse and integration with other datasets.

## Data management and governance implications for Data Leaders
- Metadata quality and discoverability:
  - Ensure a complete data package including methods, data dictionary, and provenance.
  - Explicitly document coordinate reference system (CRS) and units for all geospatial fields.
- Data quality assurance:
  - Maintain QA/QC procedures for gas measurements, sample handling, and laboratory analyses.
  - Record sampling times, durations, and any deviations from protocol.
- Data provenance and lineage:
  - Document authorship, affiliations, and grant numbers; capture data processing steps and any transformations.
- Data accessibility and reuse:
  - Package data with a clear license, citation method, and versioning to enable cross-study reuse.
  - Consider integration with broader data ecosystems (e.g., linking CTI and LiDAR-derived variables with other soil and GHG datasets).
-Future-proofing:
  - Plan for time-series data collection to complement the single-time-point data, enabling trend analyses.
  - Promote standardized metadata practices to facilitate cross-site comparisons and meta-analyses.

## References and methodological sources
- Gas sampling and chamber methodology: Chadwick et al., 2014; De Klein & Harvey, 2012.
- Soil analysis methods: Ball, 1964; Ben-Dor & Banin, 1989; Davies, 1974; Jones & Willett, 2006; Krom, 1980; Mulvaney, 1996; Searle, 1984; Rowell, 1994; Schulte et al., 1991.
- Isotope and elemental analysis: Sercon Ltd. (Mass spectrometry setup); MAFF 1986; MAFF 427 (pH methods).
- Topographic and LiDAR references: Moore et al., 1991; Sørensen et al., 2006; Evans et al., 2014; Ferraccioli et al., 2014.