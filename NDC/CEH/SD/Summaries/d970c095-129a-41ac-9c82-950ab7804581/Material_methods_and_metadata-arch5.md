# Materials, methods and metadata for Denitrification and greenhouse gas emissions in natural and semi-natural terrestrial ecosystems [LTLS]

## Purpose and scope
- Describes methods, metadata, and data products for measuring denitrification-derived nitrogen fluxes and greenhouse gas emissions (N2O, N2, CH4, CO2) in natural and semi-natural terrestrial ecosystems across UK catchments.
- Aims to enable standardized storage, sharing, discovery, and reuse of rich multi-site, multi-year data within LTLS.

## Study sites and sampling design
- Study area includes two river catchments: Conwy (N. Wales) and Ribble-Wyre (NW England).
- Conwy sites: C-PB (peat bog), C-UG (unimproved grassland), C-IG (improved grassland), C-MW (mixed woodland).
- Ribble-Wyre sites: R-UG (unimproved grassland), R-IG (improved grassland), R-HL (heathland), R-DW (deciduous woodland).
- Site metadata: each site has replicate locations (C-ML, C-RG, C-WL, C-IG, R-ML, R-WL, R-RG, R-IG) with location coordinates (degrees, minutes, decimals, and decimal Lat/Lon), grid references, and land-use type.
- Sampling schedule: monthly gas flux measurements from Apr 2013 to Oct 2014 (17 months in total); missing months include Nov 2013 and Jan 2014.
- Sampling design: 5 plots per study site, total of 40 plots per monthly campaign; PVC collars installed at ~10 cm depth (15 cm for some plots) and capped with a chamber for gas sampling.
- Data collection includes both gas flux measurements and associated soil samples (0–10 cm) collected at the end of the monitoring period.

## Data collected and data products
- Gas flux data files:
  - Denitrification_data_N20.csv (N2 flux, N2O flux)
  - GHG_data_CH4.csv (CH4 flux)
  - GHG_data_CO2.csv (CO2 flux)
  - GHG_data_DN20TN2O.csv (ratio of denitrification-derived N2O to total N2O; DN2O/TN2O)
  - GHG_data_N2O.csv (total N2O flux)
- Soil and site property files:
  - Soil_properties_Ammonia.csv
  - Soil_properties_Bulk_density.csv
  - Soil_properties_Carbon_to_nitrogen_ratio.csv
  - Soil_properties_Dissolved_organic_carbon.csv
  - Soil_properties_moisture_content.csv
  - Soil_properties_Organic_matter_content.csv
  - Soil_properties_Soil_pH.csv
  - Soil_properties_Soil_temperature.csv
  - Soil_properties_Water_filled_pore_space.csv
  - Soil_propertes_Total_dissolved_nitrogen.csv
  - Soil_propertes_Nitrate.csv
- Metadata fields:
  - Catchment, Land use Type, Latitude/Longitude (Degrees, Minutes, Decimal Lat Lon), Decimal Lat Lon.Lon, X_BNG, Y_BNG, Grid Reference
  - Replicate location identifiers (C-ML, C-RG, etc.) and metadata file references
- Data unit conventions:
  - N2 flux (µg N2 m^-2 h^-1), N2O flux (µg N2O m^-2 h^-1), CH4 flux (µg CH4 m^-2 h^-1), CO2 flux (mg CO2 m^-2 h^-1)
  - DN2O/TN2O as percentage
- Data provenance and context:
  - Sampling dates, field methods, injection rates for 15N tracer, and analysis workflow
  - Links to study-area maps and grid reference resources
- References and methodology notes:
  - Detailed methodology for 15N-Gas Flux method, CFIRMS analyses, MDCD thresholds, and flux calculations
  - Annual GWP estimation at 100-year horizon using IPCC conversion factors (N2O 298, CH4 34)

## Methods and data processing
- Gas flux measurements:
  - Static chamber method with 40 plots per campaign; collars installed 2–4 weeks before sampling
  - 15N tracer (K15NO3) applied at low rates (0.03–0.50 kg N ha^-1) to mimic natural deposition or fertilization
  - Gas samples collected at 0 h (pre-incubation), 1 h, and 2 h after chamber enclosure
  - Gas samples stored in Exetainer vials; analyzed for isotope-labeled N2/ N2O (CFIRMS) and total N2O, CH4, CO2 (GC methods)
- Analytical details and quality criteria:
  - Minimum detectable concentration differences (MDCD) defined for N2O, CH4, CO2
  - MDCD values: N2O ~0.008 ppm, CH4 ~0.036 ppm, CO2 ~3.6 ppm; instrument precision <1% RSD
  - Flux calculations: linear regression of headspace concentrations vs time, adjusted for T and P, divided by chamber area and incubation time
  - Flux detection criteria: only samples above/below MDCD used; below threshold treated as zero flux
- Denitrification and N2O attribution:
  - DN2O fluxes derived from CFIRMS; TN2O fluxes estimated to match a 20-hour incubation period
  - Rules applied for case-by-case interpretations when DN2O vs TN2O values differ (e.g., if DN2O/TN2O > 10%, or TN2O is zero)
- Annual and footprint estimates:
  - Monthly fluxes interpolated to annual estimates; GWP calculated for 100-year horizon including climate-carbon feedbacks
  - GWP values based on IPCC 2013 factors (N2O = 298, CH4 = 34)
- Soil and site characterization:
  - Five composite soil samples per study site collected post-monitoring; analyzed for organic matter, pH, temperature, moisture, bulk density, C/N, DOC, nitrate, ammonium, and other properties
- Data quality notes:
  - Missing data indicated by empty cells due to sampling or analytical failure
  - Acknowledges high spatial variability; several assumptions used to standardize DN2O inference across plots

## Data governance and metadata considerations
- Data structure and metadata:
  - Replicate-level site designations (e.g., C-ML, C-RG) with explicit metadata entries for catchment, land-use type, coordinates, and grid references
  - Clear file naming conventions for datasets (e.g., Denitrification_data_N20.csv, GHG_data_*.csv, Soil_properties_*.csv)
- Units and formats:
  - Consistent units across datasets; detailed column naming to enable straightforward integration and re-use
  - Use of both geographic (Degrees, Minutes, Lat/Lon) and projected coordinates (X_BNG, Y_BNG) with grid references
- Provenance and references:
  - Comprehensive reference list supporting methods, calculations, and previous LTLS work
  - Documentation of sampling dates and methodological steps to support reproducibility and auditability
- Data access and reuse:
  - Data are organized to support discovery by land-use type, catchment, site, and replicate location
  - Map links provided for Conwy and Ribble catchments to facilitate spatial discovery and cross-referencing with grid references

## Practical guidance for reuse and stewardship
- Ensure alignment of external datasets with the LTLS schema (site codes, coordinates, land-use types, units)
- Preserve the replication structure (1–5 replicate locations per site) to maintain data provenance and uncertainty characterization
- Respect missing data flags and document any deviations from standard protocols when integrating with other datasets
- When consuming the data for meta-analyses, account for the monthly sampling gaps and the DN2O/TN2O interpretation rules applied in the original dataset
- Use the provided references to understand methodological decisions (e.g., MDCD thresholds, DN2O attribution, and 15N-tracer application) for correct interpretation and comparability with other LTLS datasets