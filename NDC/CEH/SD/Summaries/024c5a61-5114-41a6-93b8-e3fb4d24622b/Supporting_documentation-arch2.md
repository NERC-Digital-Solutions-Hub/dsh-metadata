# Experimental design/Sampling regime

- Objective and scope
  - Structured soil fertility monitoring across households to capture spatial management gradients (home garden, near field, far field) and variation in inputs.
  - Targets multiple environmental variables (soil carbon and nitrogen, pH, mineral nitrogen, moisture, texture, aggregate stability) to assess soil health and fertility.

- Sampling design and units
  - Within each household, three fertility zones are sampled: home garden (intensively managed near house), near field (between home and far field), and far field (farther from house, more extensive production).
  - Study area includes 4 kebeles with diverse wealth statuses (poor, medium, rich) and 18 farms per kebele, totaling 72 households.
  - Across households, a total of 216 measurement sites (72 households × 3 zones) are used; overall, 648 samples collected (accounting for replicates).

- Replication and coverage
  - Socioeconomic classes represented to capture management differences.
  - Three replicates per fertility zone, with random positioning of samples within each zone.
  - Soil types: 4 distinct types represented; kebeles: 4; measurement sites: 216; total samples: 648.

- Collection methods
  - Sampling locations within each zone chosen randomly; soil cores collected from two depths: 0-20 cm (surface) and 20-50 cm (below plough layer).
  - In each area (home, near, far), samples collected from farms across wealth statuses.
  - Field sites span four kebeles: Asore, Lay Arisho, Konicha, 1st Choroko; 18 farms per kebele.
  - For each area, three replicates collected to form the measurement site set.

- Sample handling and transport
  - Soil samples stored in cool conditions, kept out of sun, and transported to Aberdeen for analysis with maintained cooling.
  - Lab staff notified upon arrival to ensure proper storage and preservation.

- Analytical methods (in brief)
  - Carbon and nitrogen: Percent C and N measured by CNS elemental analyzer without ball-milling.
  - pH: Measured in 1:5 soil:CaCl2 solution with temperature recorded.
  - Mineral nitrogen: Nitrate and ammonium assessed using colorimetric methods (NO3-/NO2- via sulfanilamide and NED; NH4+ via indophenol) with plate-reader detection.
  - Soil moisture: Measured at collection and, where needed, prepared to -10 kPa matric potential; disturbance in some locations due to equipment limits.
  - Texture: Laser diffraction (Beckman-Coulter) after organic matter removal and dispersion steps.
  - Aggregate stability: Wet sieving method to determine water-stable aggregates; calculation of stable fraction and related metrics.
  - Some field and lab steps include reagents preparation, standard curves, and replicate measurements to ensure accuracy.

- Data management and file structure
  - Metadata and multiple data files organized by site group:
    - Metadata.csv
    - BREAD-Master_data.csv (sample identifiers for Asore and Lay Arisho)
    - BREAD-Mineral_N_data.csv
    - BREAD-Soil_C_N_and_pH.csv
    - BREAD-Soil_moisture.csv
    - BREAD-Particle_size_analysis.csv
    - BREAD_Aggregate_stability.csv
    - IPORE-Master_data.csv (sample identifiers for Konicha and 1st Choroko)
    - IPORE-Mineral_N_data.csv
    - IPORE-Soil_C_N_and_pH.csv
    - IPORE-Soil_moisture.csv
  - These files provide dataset-wide identifiers, mineral N data, carbon/N/pH, moisture, texture, and aggregate stability for the two study groups (BREAD and IPORE).

- Context and limitations
  - Field and lab procedures are designed for standardized data generation suitable for monitoring soil health over time.
  - Some country-specific equipment limitations affected certain in-country measurements (e.g., soil moisture handling in the Ethiopian context).

- Relevance for environmental monitoring and data use
  - Provides a robust, repeatable protocol for collecting comparable soil health indicators across households and zones.
  - Data can be integrated with broader environmental health datasets and used to evaluate policy performance on soil fertility and land management.
  - Emphasizes data quality assurance through random sampling, replication, standardized analytical methods, and clear data/file organization, aligning with typical environmental monitoring practices.