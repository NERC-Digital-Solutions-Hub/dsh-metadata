# Extensive_Intensive_Spatial_README.docx

- Overview
  - This is a single time point spatial dataset of site characteristics, soil parameters, and soil greenhouse gas (GHG) emissions for two sites: Extensive and Intensive.
  - Extensive site: 11.5 ha with 115 sampling points (112 on a 30 m × 30 m grid plus 3 random points).
  - Intensive site: 1.78 ha with 99 sampling points (78 on a 15 m × 15 m grid plus 21 on a 25 m × 25 m grid).

- Sampling design and collection
  - Locations captured in the field with GeoXT handheld GPS (Extensive) or RTK surveying with Trimble R6/R8 (Intensive).
  - Gas sampling uses airtight static chambers at both sites; headspace samples collected at 0 and 60 minutes (Extensive) or 40 minutes (Intensive).
  - Chamber types: smaller cylindrical chambers (Extensive) and larger cuboid chambers (Intensive).
  - Sampling performed within a tight time window to minimise diurnal effects and avoid photosynthesis (CO2 flux reflects soil+plant respiration only due to opaque chambers).

- Measurements and analyses
  - GHG fluxes
    - N2O_flux: µg N2O-N m-2 h-1
    - CO2_flux: mg CO2-C m-2 h-1
    - CH4_flux: µg CH4-C m-2 h-1
  - Soil physical properties
    - Bulk_density (g cm-3)
    - WFPS (soil water-filled pore space, %)
    - Soil_moisture (% gravimetric)
    - Organic_Matter (%)
    - Soil_pH
  - Soil chemical properties
    - Soil_NO3N (mg NO3--N kg-1 soil DW)
    - Soil_NH4N (mg NH4+-N kg-1 soil DW)
    - Total_C (% dry soil)
    - Total_N (% dry soil)
    - CtoN
  - Spatial and site context
    - Elevation (m a.s.l), Slope (degrees), CTI (Compound Topographic Index), Aspect (degrees)
    - Veg_type/Org_Spread (vegetation type at Extensive; organic farmyard manure spread at Intensive)
  - For the Intensive site, total C and N analyses were done with an elemental analyzer linked to isotope ratio mass spectrometry; for the Extensive site, a TruSpec analyzer was used.

- Data headers and units
  - Site, Sample_ID, Grid, Easting, Northing, N2O_flux, CO2_flux, CH4_flux
  - Bulk_density, WFPS, Soil_moisture, Organic_Matter, Soil_pH
  - Soil_NO3N, Soil_NH4N, Total_C, Total_N, CtoN
  - Elevation, Slope, CTI, Aspect, Veg_type/Org_Spread
  - Units closely tied to each variable as described above (e.g., fluxes in µg N2O-N m-2 h-1, mg CO2-C m-2 h-1, etc.)

- Soil sampling and processing details
  - Bulk density cores and soil samples collected within chamber areas and stored at 4°C prior to analysis.
  - SOM calculated via loss-on-ignition with site-specific temperatures and durations.
  - pH measured using slightly different extraction media between sites (Extensive: water; Intensive: deionised water after air-drying and grinding).
  - Nutrient extractions:
    - Extensive: 0.5 M K2SO4 extraction; NO3-/NH4+ via colorimetric methods.
    - Intensive: 2 M KCl extraction; NO3-/NO2- via photometric methods; NH4+ via indophenol/Berthelot-type reaction.
  - Total C/N: Elemental analysis or isotope ratio mass spectrometry (Intensive).

- Spatial context and covariates
  - Elevation, slope, and aspect derived from 1 m LiDAR data.
  - CTI (Compound Topographic Index) calculated from LiDAR-derived topography.

- Data usage and accessibility
  - Data headers and methods enable linking GHG fluxes to soil properties, moisture, and topographic context.
  - Notes indicate standard references for methods and instrumentation; data provenance and metadata are aligned with field practices and analytical protocols.

- References and methodological context
  - Key methodological references for chamber techniques, soil analyses, and topographic calculations (e.g., De Klein & Harvey 2012; Chadwick et al. 2014; Ball 1964; Moore et al. 1991; Searle 1984; Krom 1980; etc.).

- Potential uses for analysts
  - Identify correlations between soil properties (moisture, organic matter, C/N, pH, extractable N forms) and soil GHG fluxes (N2O, CO2, CH4).
  - Develop predictive models of GHG fluxes under different management regimes (Extensive vs Intensive) considering topographic context (CTI, elevation, slope, aspect).
  - Compare measurement approaches and their impact on derived soil indices due to site-specific protocols.
  - Integrate with LiDAR-derived covariates to assess spatial patterns and drivers of GHG fluxes at local scales.

- Limitations and considerations
  - Represents a single time point; temporal variability and diurnal/seasonal effects are not captured.
  - Different extraction methods and pH measurement approaches between sites may introduce methodological differences that require harmonization for cross-site comparisons.
  - Two sites employ distinct sampling grids and chamber modalities, which should be accounted for in cross-site analyses.
  - Some NOx measurements rely on approximations (e.g., NO2- approximated as total oxidised nitrogen) due to low concentrations.