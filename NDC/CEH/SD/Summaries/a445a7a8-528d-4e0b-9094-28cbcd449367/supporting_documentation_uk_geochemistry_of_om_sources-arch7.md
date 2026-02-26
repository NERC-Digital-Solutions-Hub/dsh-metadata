# Supporting documentation for data resource UK_geochemistry_of_OM_sources.csv

- Purpose: Metadata for a dataset of bulk elemental and stable isotope composition of organic matter from UK terrestrial, intertidal, and marine environments (2016–2021) to help constrain organic carbon sources (terrestrial vs marine) when used with isotope mixing models.
- Scope of dataset:
  - Samples (n=491) from terrestrial (soil, peat, living and dead biomass), intertidal (saltmarsh vegetation/root, seagrass, mudflat, faecal matter), and marine environments (macroalgae, microalgae, zooplankton, finfish aquaculture waste).
  - Analyzed variables include organic carbon (OC) content, nitrogen content (N), C/N and N/C ratios, and stable isotopes δ13C_org and δ15N.
  - Locations cover the United Kingdom with wide geographic dispersion.

- Spatial coverage and geography:
  - Geographic extent: United Kingdom.
  - Coordinates provided to define observation locations (example points include near 60.97, -8.02 and 49.84, 2.18).
  - Location descriptions indicate sampling across coastal catchments and diverse habitats (terrestrial, intertidal, marine).

- Data collection and laboratory procedures:
  - Sampling conducted across the UK coastal catchments; field descriptions recorded by experts.
  - Sample handling: storage at -20°C until analysis.
  - Sample preparation: oven-dried at 40°C for 72 hours, milled to a fine powder.
  - Stable isotope analysis: approximately 12 mg processed sediment loaded into tin capsules (for N and δ15N) and about 12 mg into silver capsules (for OC and δ13C_org) after carbonate removal via acid fumigation.
  - Instrumentation: EA-IRMS (elemental analyzer coupled to isotope ratio mass spectrometer).
  - Calibration and quality control: isotopic values quality-controlled through repeat analyses of a high OC sediment standard (B2151) with known C and N values; laboratory practices standardized at the University of St Andrews.

- Data structure and formats:
  - File format: .csv.
  - Core variables/parameters observed: δ13C_org (‰), δ15N (‰), OC content (%), N content (%), C/N, N/C.
  - Metadata fields include sampling details, nation (Scotland, England, Wales), and location descriptions.
  - Some cells marked NA to indicate missing data.

- Related/additional dataset:
  - Data resource description for Aboveground_Biomass_Carbon_UK.csv:
    - Structure focuses on sample_id, sample_class (e.g., Terrestrial Vegetation, Soil, Wetland Vegetation, Zooplankton, Seagrass, Phytoplankton, Mudflat, etc.), and detailed sample descriptions.
    - Includes National Vegetation Classification (NVC) and location fields, with nation breakdown (Scotland, England, Wales).
    - Additional fields include detailed sample descriptions and a generic description field, indicating broad applicability for GIS tagging and classification.

- Data quality and provenance notes:
  - QC procedures emphasize repeated analyses of standards; calibration aligns with UK laboratory practices.
  - Some fields are labeled NA where data are not available, indicating incomplete metadata in places.
  - References for methods include Harris et al. (2001) on acid fumigation and Rodwell (2000) on maritime vegetation classification.

- Practical GIS implications:
  - Enables mapping of isotopic and elemental signatures across UK habitats to visualize spatial patterns of organic matter sources.
  - Supports integration with NVC classifications and coastal habitat data for richer spatial analyses.
  - Suitable for creating layers of δ13C_org, δ15N, OC%, N%, CN, and NC across samples, with potential use in isotope-based source apportionment models.
  - Coordinate-based metadata facilitates GIS join operations using sample_id or location fields.

- References:
  - Harris, D., Horwáth, W.R., and Van Kessel, C. (2001). Acid fumigation of soils to remove carbonates prior to total organic carbon or carbon-13 isotopic analysis. Soil Science Society of America Journal, 65(6), 1853-1856.
  - Rodwell, J.S. (2000). vol. 5: Maritime communities and vegetation of open habitats.