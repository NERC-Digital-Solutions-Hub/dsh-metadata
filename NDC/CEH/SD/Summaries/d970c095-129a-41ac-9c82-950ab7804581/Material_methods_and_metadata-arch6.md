# Materials, methods and metadata for Denitrification and greenhouse gas emissions in natural and semi-natural terrestrial ecosystems [LTLS]

- Overview
  - A comprehensive data package describing denitrification and greenhouse gas (GHG) flux measurements across natural and semi-natural terrestrial ecosystems in two UK river catchments: Conwy (N. Wales) and Ribble-Wyre (NW England).
  - Aims to quantify in situ N2 and N2O fluxes from denitrification and associated CH4 and CO2 fluxes, withlinked soil property data for contextual analysis.

- Data content and structure
  - Study sites and land-use types (per catchment):
    - Conwy: C-PB (peat bog, OS), C-UG (unimproved grassland, SIG), C-IG (improved grassland, IG), C-MW (mature mixed woodland, MW)
    - Ribble-Wyre: R-UG (unimproved grassland, SIG), R-IG (improved grassland, IG), R-HL (heathland, OS), R-DW (deciduous woodland, DW)
  - Metadata fields for locations (example replicated locations across fields):
    - Catchment, Land use Type, Latitude (Degrees, Minutes, Decimal), Longitude (Degrees, Minutes, Decimal), X_BNG, Y_BNG, Grid Reference
  - Data files (CSV format) and contents:
    - Denitrification_data_N20.csv: N2O flux data (micrograms N2O-N m-2 h-1)
    - GHG_data_CH4.csv: CH4 flux data (micrograms CH4-C m-2 h-1)
    - GHG_data_CO2.csv: CO2 flux data (mg CO2-C m-2 h-1)
    - GHG_data_DN20TN2O.csv: Denitrification-derived N2O fraction (DN2O/TN2O, %)
    - GHG_data_N2O.csv: Total N2O flux (micrograms N2O-N m-2 h-1)
    - Soil_propertes_Nitrate.csv: Nitrate-N (mg/m2 at 10 cm)
    - Soil_propertes_Total_dissolved_nitrogen.csv: Total dissolved nitrogen (mg/m2 at 10 cm)
    - Soil_properties_Ammonia.csv: NH4-N (mg/m2 at 10 cm)
    - Soil_properties_Bulk_density.csv: Dry bulk density (g/cm3)
    - Soil_properties_Carbon_to_nitrogen_ratio.csv: C/N ratio
    - Soil_properties_Dissolved_organic_carbon.csv: DOC (g/m2 at 10 cm)
    - Soil_properties_moisture_content.csv: Soil moisture (%) (wet basis)
    - Soil_properties_Organic_matter_content.csv: Organic matter content (%)
    - Soil_properties_Soil_pH.csv: Soil pH
    - Soil_properties_Soil_temperature.csv: Soil temperature (°C)
    - Soil_properties_Water_filled_pore_space.csv: Water-filled pore space (%)
  - Units are provided in each file’s metadata and headers; consistent with standard GHG measurement conventions.

- Sampling design and methods
  - Sampling period: April 2013 to October 2014 (17 months total); missing sampling in November 2013 and January 2014.
  - Plot and chamber setup:
    - Five plots per study site per catchment; total 40 plots per monthly campaign.
    - PVC collars inserted ~10 cm (15 cm for some plots) to allow gas-tight chamber incubation.
    - Chambers fitted with acrylic covers and reflective foil to minimize heating.
  - 15N tracer application:
    - Labelled 15N-NO3 (98 at.%) applied at low rates (0.03–0.50 kg N ha-1), via grids, to simulate natural deposition or low-level fertilization depending on land use type.
    - Tracer injection performed in multiple small volumes; tracer content adjusted to soil moisture.
  - Gas sampling and analysis:
    - Gas samples collected at 0 h (immediately after tracer injection), 1 h, and 2 h during chamber incubation; two 20 mL samples per time point; stored in pre-evacuated vials.
    - Two analytical approaches:
      - CF-IRMS: in-house continuous-flow isotope ratio mass spectrometry for 15N-N2 and 15N-N2O to derive N2 and N2O fluxes and DN2O/TN2O.
      - Gas chromatography: total N2O (14+15N-N2O), CH4, and CO2 from the same samples.
  - Flux calculation and QA/QC:
    - Fluxes calculated by linear regression of chamber headspace concentrations (adjusted for T and P) over 0–2 hours, scaled by chamber volume and area.
    - Minimum detectable concentrations (MDCD) defined for each gas; only samples above MDCD used; others treated as zero flux.
    - Flux precision: instrument precision <1% RSD for N2O, CH4, CO2.
    - Denitrification-derived N2O (DN2O) estimation, including handling of negative TN2O, zero TN2O, or DN2O > TN2O scenarios per established rules.
  - Annual and relative fluxes:
    - Monthly fluxes interpolated to annual estimates; GWP calculated for 100-year horizon (CO2e) using IPCC factors (N2O = 298, CH4 = 34).
  - Soil sampling:
    - Composite soil samples (0–10 cm) collected at end of each sampling period for ancillary soil properties.

- Data processing and analysis
  - Factor analysis (FA) used to cluster sites into land-use groups (OS, IG, SIG, MW, DW) based on emission patterns and soil/vegetation context.
  - Data integration:
    - Linkage between gas flux data, 15N tracer-derived values, and soil properties to enable cross-site comparisons and interpretation of controls.
  - Derived metrics:
    - DN2O/TN2O ratio for denitrification contribution to N2O emissions.
    - Yearly averages of N2O, CH4, CO2 fluxes per land-use type.
    - GWP (CO2e) for each land-use type, inclusive of climate–carbon feedbacks.

- Temporal and spatial coverage
  - Spatial coverage:
    - Two catchments: Conwy (14 study sites across 4 land-use types) and Ribble-Wyre (4 study sites across 4 land-use types), with site-specific coordinates and grid references provided.
  - Temporal coverage:
    - 17 months of monthly measurements between Apr 2013 and Oct 2014 (with two months not sampled).
  - Map links provided for Conwy and Ribble catchments to locate C-ML, C-RG, C-IG, C-WL, R-ML, R-WL, R-RG, R-IG sites.

- Metadata and provenance
  - Detailed location metadata for replicates and grid coordinates (including X_BNG, Y_BNG, and grid references) to support spatial analyses and replication.
  - Explicit notes on missing data: empty cells indicate sampling or analytical failures.
  - Land-use categories and site descriptors aligned with referenced LTLS materials.

- Data access and potential uses
  - Data products suitable for:
    - Self-serve dashboards comparing GHG fluxes across land-use types and catchments.
    - Integrated analyses linking gas fluxes with soil properties and 15N tracer data.
    - Scenario analysis of nitrogen cycling and climate feedbacks in natural and semi-natural ecosystems.
  - Map-based exploration using provided Conwy and Ribble map links to identify site locations and data gaps.

- Limitations and considerations
  - Some months lacked sampling; flux estimates rely on interpolation to annual means.
  - Spatial variability at plot level is high; DN2O/TN2O estimates incorporate standardized assumptions about incubation time.
  - Missing data in some cells reflect sampling or analytical failure; users should account for gaps in analyses.

- References
  - IPCC guidelines and multiple LTLS-related methodological papers (Sgouridis, Ullah, and colleagues; Mosier and Klemedtsson; Paye; etc.) supporting tracer methodology, flux calculations, and data interpretation.