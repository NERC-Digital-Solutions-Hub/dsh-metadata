# Extensible_Intensive_Spatial_README.docx

## Overview
- Single time point spatial dataset of site characteristics, soil parameters and soil greenhouse gas (GHG) emissions for two sites: Extensive and Intensive.
- Designed for GIS workflows: enables map-based visualization and spatial analysis of GHG fluxes and soil properties.
- Data collected on grid-based sampling with precise geolocation; includes LiDAR-derived topography (elevation, slope, aspect) and a compound topographic index (CTI).

## Sampling design and coverage
- Extensive site: 11.5 ha with 112 points on a 30 m × 30 m grid plus 3 random points (n = 115).
- Intensive site: 1.78 ha with 78 points on a 15 m × 15 m grid plus 21 points on a 25 m × 25 m offset grid (n = 99).
- Field locations captured with high-accuracy GNSS (GeoXT and RTK Trimble receivers).

## Measurements and responses
- Soil GHG fluxes measured at chamber closure and subsequent times (varies by site):
  - N2O_flux: µg N2O-N m-2 h-1
  - CO2_flux: mg CO2-C m-2 h-1
  - CH4_flux: µg CH4-C m-2 h-1
- Soil and site properties:
  - Bulk_density (g cm-3)
  - WFPS (water-filled pore space, %)
  - Soil_moisture (% gravimetric)
  - Organic_Matter (%)
  - Soil_pH
  - Soil_NO3N (mg NO3-N kg-1 soil DW)
  - Soil_NH4N (mg NH4-N kg-1 soil DW)
  - Total_C (% dry soil)
  - Total_N (% dry soil)
  - CtoN (carbon to nitrogen ratio)
- Spatial and topographic context:
  - Elevation (m asl)
  - Slope (degrees)
  - CTI (Compound Topographic Index)
  - Aspect (degrees)

## Methods and data processing highlights
- Gas sampling:
  - Extensively uses air-tight chambers with 0 and 60 min samples (Extensive) or 0 and ~40 min (Intensive), with two-point sampling justified by throughput.
  - Sampling conducted within a narrow time window to minimize diurnal effects.
  - CO2 and CH4 measured with PerkinElmer Clarus 580 GC (FD for CO2/CH4; ECD for N2O).
- Soil sampling and lab analyses:
  - Bulk density and soil sampling specifics differ slightly between sites (core sizes and depths).
  - Gravimetric moisture via oven-drying; LOI for organic matter; pH via site-specific methods.
  - Extractable N forms determined using standard extractants (0.5 M K2SO4 or 2 M KCl) and colorimetric/photometric analyses.
  - Total C and N measured with elemental analyzer (and isotope ratio mass spectrometry for Intensive site).
  - nitrate/n nitrite concentrations derived via standard reduction and colorimetric methods; nitrate assumed equal to total oxidised nitrogen due to low NO2-.
- Topography:
  - Elevation, slope, and aspect derived from 1 m LiDAR data.
  - CTI derived following established hydromorphometric methods.
- Data integration:
  - Data headers align with site and grid metadata to enable spatial joins and map-ready outputs.

## Geospatial components and data integration
- Georeferenced fields:
  - Grid, Easting, Northing
  - Elevation, Slope, CTI, Aspect
  - Veg_type/Org_Spread indicating vegetation type or manure-spreading context (Extensive vs Intensive site)
- LiDAR-derived context enables spatial analysis of microtopography and hydrological positioning.
- Ready for GIS analyses and map-based visualization of:
  - Spatial patterns in GHG flux (N2O, CO2, CH4)
  - Variation in soil properties across grids and between sites
  - Topographic influence on emissions and soil processes

## Data headers (key variables)
- Site: Extensive or Intensive
- Sample_ID: Unique sample reference
- Grid: Grid size (e.g., 30 m × 30 m, 15 m × 15 m, etc.)
- Easting, Northing: Grid coordinates
- N2O_flux, CO2_flux, CH4_flux: Emission fluxes with respective units
- Bulk_density
- WFPS, Soil_moisture
- Organic_Matter
- Soil_pH
- Soil_NO3N, Soil_NH4N
- Total_C, Total_N, CtoN
- Elevation, Slope, CTI, Aspect
- Veg_type/Org_Spread: Vegetation or organic matter spreading context

## Data provenance and references
- Methods and measurement approaches draw on a suite of established references for soil and gas analyses, chamber methodologies, and LiDAR-derived topography.
- Key references include: Ball (loss-on-ignition), Chadwick et al. (gas sampling methods), Davies (LOI), De Klein and Harvey (chamber guidelines), Moore et al. (DTM/CTI), LiDAR-based datasets for CTI and elevation.

## Practical GIS use considerations
- Ideal for producing maps of soil GHG fluxes across two contrasting management regimes (Extensive vs Intensive).
- Enables cross-site comparisons of soil chemistry and physical properties alongside topographic context.
- Requires careful handling of differing sampling grid resolutions when performing spatial aggregations or modeling.
- Data quality hinges on precise geolocation, consistent data standards across sites, and robust QA/QC during data integration.