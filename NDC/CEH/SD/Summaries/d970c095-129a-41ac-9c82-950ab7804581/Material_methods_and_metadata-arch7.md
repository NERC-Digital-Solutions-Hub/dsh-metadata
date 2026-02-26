# Materials, methods and metadata for Denitrification and greenhouse gas emissions in natural and semi-natural terrestrial ecosystems [LTLS]

## Overview
- Describes study design, locations, sampling, and metadata for denitrification and greenhouse gas (GHG) emissions in natural and semi-natural terrestrial ecosystems.
- Focuses on two UK catchments: Conwy (N Wales) and Ribble-Wyre (NW England); aims to quantify N, C and P fluxes between soil, water and air under climate change and C cycle perturbations.
- Data are organized for GIS-based map visualisation and cross-site comparisons, with explicit geospatial coordinates and map links.

## Study sites and geography
- Catchments:
  - Conwy: area ~345 km²; coordinates around 52.99 N, 3.77–3.80 W.
  - Ribble-Wyre: area ~1145 km²; coordinates around 53.00–54.00 N, 2.39–3.77 W.
- Land-use types at study sites:
  - Conwy: peat bog (C-PB), unimproved grassland (C-UG), improved grassland (C-IG), mixed woodland (C-MW).
  - Ribble-Wyre: unimproved grassland (R-UG), improved grassland (R-IG), heathland (R-HL), deciduous woodland (R-DW).
- Geospatial data per site:
  - Decimal latitude/longitude, National Grid (BNG) coordinates (X_BNG, Y_BNG), and grid references (e.g., SH 79125 45448).
  - 1–5 replicate locations per site (C-ML, C-RG, C-WL, C-IG, R-ML, R-WL, R-RG, R-IG, etc.).
- Map links provided:
  - Conwy Map Link and Ribble Map Link to gridreferencefinder.com for site coordinates.

## Data collection and methods
- Gas flux measurement timeline:
  - Monthly sampling from Apr 2013 to Oct 2014 (17 months total); no sampling in Nov 2013 and Jan 2014.
- Field sampling design:
  - Five plots per study site, across catchments (total 40 plots per monthly campaign).
  - PVC collars inserted at 10 cm depth (15 cm in R-HL and C-PB); chamber covers create gas-tight headspace.
  - 15N tracer (K15NO3) applied at rates 0.03–0.50 kg N ha⁻¹ via 10–15 cm grid injections, with adjustments for soil moisture.
- Gas sampling protocol:
  - Samples taken at T = 0 h (immediately after tracer injection), T = 1 h, and T = 2 h.
  - Samples stored in pre-evacuated glass vials and analysed within 8 weeks.
- Analytical methods:
  - 15N-N2 and 15N-N2O analyzed with a continuous flow isotope ratio mass spectrometer (CF-IRMS); DN2O/TN2O ratios derived from these data.
  - Total N2O (14N+15N), CH4, and CO2 analysed by GC methods.
- Flux calculation and detection limits:
  - Fluxes calculated from linear regression of headspace concentrations over 0–2 h, adjusted to standard T and pressure, and normalized by chamber area and incubation time.
  - Minimum detectable concentration differences (MDCD) defined per gas; only values above MDCD used for flux calculations; below treated as zero flux.
  - Minimum detectable fluxes: N2O 0.34 μg N2O-N m⁻² h⁻¹, CH4 0.68 μg CH4-C m⁻² h⁻¹, CO2 67.14 μg CO2-C m⁻² h⁻¹.
- Denitrification interpretation:
  - DN2O/TN2O ratio estimated; special rules applied for negative TN2O or zero TN2O; when DN2O exceeds TN2O, all N2O attributed to denitrification; if DN2O not measured, ratio omitted.
  - For samples with DN2O > TN2O in about 10% of cases, 100% of N2O assigned to denitrification.
- Annual and GWP calculations:
  - Annual GHG fluxes estimated by interpolating monthly data; 100-year Global Warming Potential (GWP) calculated for N2O and CH4 with IPCC factors (N2O = 298, CH4 = 34).
- Soil sampling:
  - Composite soil samples (0–10 cm) collected at 50 cm radius around each plot after gas sampling; stored on ice, analyzed later.

## Data products and structure
- Data files (CSV) and content:
  - Denitrification_data_N20.csv: N2 flux; N2O flux (μg N m⁻² h⁻¹).
  - GHG_data_CH4.csv: CH4 flux (μg CH4-N m⁻² h⁻¹ or related units).
  - GHG_data_CO2.csv: CO2 flux (mg CO2-C m⁻² h⁻¹).
  - GHG_data_DN20TN2O.csv: DN2O/TN2O ratio (%).
  - GHG_data_N2O.csv: Total N2O flux (μg N2O-N m⁻² h⁻¹).
  - Soil_propertes_Nitrate.csv: NO3--N (mg m⁻² at 10 cm).
  - Soil_propertes_Total_dissolved_nitrogen.csv: TDN (mg m⁻² at 10 cm).
  - Soil_properties_Ammonia.csv: NH4--N (mg m⁻² at 10 cm).
  - Soil_properties_Bulk_density.csv: Dry Bulk density (g cm⁻³).
  - Soil_properties_Carbon_to_nitrogen_ratio.csv: C/N ratio.
  - Soil_properties_Dissolved_organic_carbon.csv: DOC (g m⁻² at 10 cm).
  - Soil_properties_moisture_content.csv: Soil moisture content (% wet basis).
  - Soil_properties_Organic_matter_content.csv: Organic matter (%).
  - Soil_properties_Soil_pH.csv: Soil pH.
  - Soil_properties_Soil_temperature.csv: Soil temperature (°C).
  - Soil_properties_Water_filled_pore_space.csv: WFPS (%).
- Data conventions:
  - Empty cells indicate missing data due to sampling or analytical failure.
  - Land-use types and study-site classifications align with FA clustering results (OS, IG, SIG, MW, DW).
  - Units are specified per file (e.g., μg N2O-N m⁻² h⁻¹, mg m⁻², g cm⁻³).
- GIS-relevant attributes:
  - Precise coordinates (Decimal Lat/Lon), Grid References, X_BNG and Y_BNG for mapping.
  - Land-use type per replicate site to enable spatial comparisons.
- Data provenance:
  - Sampling dates span 2013–2014; multiple sources cited for methods and analyses (LTLS, Sgouridis et al., Ullah & Moore, IPCC 2013, etc.).

## Data quality, constraints and usage
- Spatial and temporal variability: high within-site variability necessitates replication and careful interpretation.
- Data gaps: some months with no sampling; some sites have missing measurements due to sampling or analytical failure.
- Analytical thresholds: MDCD criteria ensure only robust flux estimates are used.
- GIS usage: data are designed for map-based visualization and cross-site comparisons, with explicit geospatial coordinates and map links to facilitate integration into GIS workflows.

## References and provenance
- Core methodological references spanning 15N-Gas Flux methods, tracer applications, and greenhouse gas analyses (Sgouridis et al., Ullah & Moore, IPCC guidance, etc.).