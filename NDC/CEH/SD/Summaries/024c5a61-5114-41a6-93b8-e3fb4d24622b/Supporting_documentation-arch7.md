# Experimental design/Sampling regime:

- Sampling design
  - Within each household, three fertility zones: Home (close to house, higher inputs), Near (between home and far), and Far (furthest from house, more extensive production).
  - Random positioning of soil cores within each zone; three replicates per area.
  - Farms selected across four kebeles: Asore, Lay Arisho, Konicha, and 1st Choroko; 18 farms per kebele.

- Spatial and sample scale
  - Across the study: 72 households total (36 per dataset group), spanning 4 kebeles.
  - Fertility zones per household: 3 (total zones observed across households: 6 due to replicates design in the dataset summary).
  - Measurement sites: 216 total (108 per dataset group; two groups: BREAD and IPORE).
  - Replicates per fertility zone: 3 (per dataset group; total replicates 6 in the summarized design).
  - Total samples: 648 (324 per dataset group; 648 overall).

- Data collection and site layout
  - Data collected from households with varied wealth status (poor, medium, rich).
  - Sampling areas cover both near-household fields and owner fields, in four kebeles.

- Field procedures
  - Soil cores collected at two depths: surface 0–20 cm and subsoil 20–50 cm.
  - Randomly positioned soil cores within each fertility zone.
  - Three replicates per area; samples from different wealth-status farms.

- Sample handling and transport
  - Samples stored in cool conditions, transported to Aberdeen for analysis, with protocols to preserve integrity on arrival.

- Analytical methods (soil properties and nutrients)
  - Carbon and nitrogen: Percent C and N by CNS elemental analyzer (no ball-milling).
  - pH: 1:5 soil in CaCl2, measured with a pH meter; temperature recorded.
  - Mineral N: Nitrate and ammonium determinations using KCl extraction; colorimetric plate-reader methods for NO3−/NO2− and NH4+.
  - Soil moisture: Measured at sampling; also moisture at -10 kPa matric potential (described for some sites); disturbed soils repacked when in country limitations prevented in-country analysis.
  - Texture: Percent silt, sand, and clay by laser diffraction (Beckman-Coulter LS 13 320) with standard dispersion and pretreatment steps.
  - Aggregate stability: Wet sieving to determine water-stable aggregates; calculations based on weights of stable and unstable fractions.
  - Additional measures: Particle size analysis and aggregate stability data collected for Asore and Lay Arisho sites; detailed procedural steps noted for reproducibility.

- Data products and file organization
  - Metadata and two dataset groupings (BREAD and IPORE) with linked sample identifiers.
  - Data files included:
    - Metadata.csv
    - BREAD-Master_data.csv
    - BREAD-Mineral_N_data.csv
    - BREAD-Soil_C_N_and_pH.csv
    - BREAD-Soil_moisture.csv
    - BREAD-Particle_size_analysis.csv
    - BREAD_Aggregate_stability.csv
    - IPORE-Master_data.csv
    - IPORE-Mineral_N_data.csv
    - IPORE-Soil_C_N_and_pH.csv
    - IPORE-Soil_moisture.csv

- Considerations for GIS use
  - Data are organized around households, kebeles, and defined fertility zones, enabling map-based visualization of spatial patterns in soil properties.
  - Linkage between Master_data and site-specific analyses supports geospatial joins to locations (households, farms, kebeles) for GIS-based analysis and visualization.
  - Coordinate-level geolocation and standard data standards are essential for integrating these datasets into GIS products; ensure consistent identifiers across files for accurate spatial joins.