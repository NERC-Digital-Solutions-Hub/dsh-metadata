# Experimental design/Sampling regime:

- Study structure
  - Within each household, three fertility zones are defined: Home garden (near the house with more intensive management), Near field (between home and far field), Far field (furthest from the house, more extensive production).
  - Sampling breadth includes 72 households across 4 kebeles (Asore, Lay Arisho, Konicha, 1st Choroko) and 6 wealth-status instances per area, with randomization at multiple steps.
  - Total design yields 648 samples across 72 households, 3 fertility zones per household, and 3 replicates per zone (216 measurement sites with 6 replicates per fertility zone).

- Replicates and stratification
  - Socioeconomic classes sampled to capture wealth-related variability (poor, medium, rich) across sites.
  - Two soil types considered, across kebeles, to expand representativeness.
  - Fertility zones around each household: 3 zones, with replicates resulting in a total of 6 per household across class/zone combinations.

- Collection methods
  - Random positioning used to select sample locations within each fertility zone.
  - Fieldwork conducted in 4 kebeles with 18 farms per kebele; soils sampled from farmers of varying wealth statuses.
  - Three replicates collected per area (zone x wealth status) and depths.

- Field procedure
  - Soil cores collected at two depths: surface 0–20 cm and subsoil 20–50 cm.
  - Randomized positioning of cores within each area to reduce bias.
  - Samples taken from farms belonging to different wealth categories (poor, middle, rich) across the four kebeles.

- Sample handling and transport
  - Samples stored in cool conditions and transported to Aberdeen for analysis, with precautions to minimize light/heat exposure and preserve integrity.

- Analytical methods and measurements
  - Carbon and nitrogen: Percent C and N measured by CNS elemental analyzer (non-ball-milled vs ball-milled tested; no difference observed).
  - Soil pH: Measured in CaCl2 (1:5 soil solution) with temperature recorded.
  - Mineral nitrogen: Nitrate and ammonium determined from 10 g soil with 1 M KCl extraction; multiple standard curves and colorimetric/colorimetric plate-reader measurements for NO3-, NO2-, and NH4+.
  - Nitrogen specifics: Total nitrate (NO3- + NO2-) and nitrite determined via a colorimetric assay; ammonium quantified using the indophenol method with specified reagents and plate-reader measurements.
  - Soil moisture: Measured at sampling and at -10 kPa matric potential; where in-country equipment was unavailable (Ethiopia), disturbed soils were repacked, saturated for 48 hours, and equilibrated to -10 kPa for analysis.
  - Texture: Sand, silt, and clay fractions assessed by laser diffraction (Beckman-Coulter LS 13 320) after pretreatment to remove organics and disperse soils.
  - Aggregate stability: Water-stable aggregates determined via wet sieving and NaOH-assisted stability procedure, with calculation of water-stable aggregates (WSA).

- Data organization and files
  - Metadata and data files organized by site groupings with explicit sample identifiers:
    - Metadata.csv
    - BREAD-Master_data.csv (Sample identifiers for Asore and Lay Arisho)
    - BREAD-Mineral_N_data.csv (Soil mineral N measurements for Asore and Lay Arisho)
    - BREAD-Soil_C_N_and_pH.csv (Soil C, N, and pH for Asore and Lay Arisho)
    - BREAD-Soil_moisture.csv (Soil moisture for Asore and Lay Arisho)
    - BREAD-Particle_size_analysis.csv (Particle size analysis for Asore and Lay Arisho)
    - BREAD_Aggregate_stability.csv (Aggregate stability for Asore and Lay Arisho)
    - IPORE-Master_data.csv (Sample identifiers for Konicha and 1st Choroko)
    - IPORE-Mineral_N_data.csv (Soil mineral N measurements for Konicha and 1st Choroko)
    - IPORE-Soil_C_N_and_pH.csv (Soil C, N, and pH for Konicha and 1st Choroko)
    - IPORE-Soil_moisture.csv (Soil moisture for Konicha and 1st Choroko)

- Key data characteristics
  - Spatial and depth variation captured: four kebeles, two depths, three fertility zones, and wealth-status stratification.
  - Comprehensive soil properties documented: C, N, pH, mineral N (NO3-/NO2-, NH4+), moisture, texture, and aggregate stability.
  - Large, harmonized dataset designed for cross-site comparability, with explicit metadata to enable discoverability and re-use.

- Limitations and considerations for data use
  - Some cores and in-country analyses were not possible due to equipment constraints; certain moisture measurements relied on alternative methodologies (disturbed soils repacked to -10 kPa).
  - Data standardization relies on consistent lab protocols across sites; detailed documentation of methods supports quality assessment and replication.
  - Potential variability due to zone- and wealth-status stratification noted; analysis should account for multi-level structure (household, kebele, zone, depth).

- How this supports data leadership and strategy
  - Demonstrates end-to-end data lifecycle: from field sampling design to laboratory analysis and organized metadata.
  - Provides a multi-site, multi-depth dataset with standardized variables, enabling cross-site analytics, benchmarking, and data products for policy or practice.
  - Highlights data governance aspects: clear data file naming, metadata availability, and recorded collection/analytic procedures to improve discoverability, quality, and reusability.