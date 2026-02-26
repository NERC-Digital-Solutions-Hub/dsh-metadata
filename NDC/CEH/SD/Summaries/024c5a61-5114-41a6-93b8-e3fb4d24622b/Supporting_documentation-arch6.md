# Experimental design/Sampling regime

- Study aim: Characterize soil properties around households to understand fertility gradients, using structured sampling across multiple zones and depths.

- Sampling framework
  - Within each household, three fertility zones are sampled: home garden (near the house, intensive management), near field (between home and far), and far field (owner’s field, more extensive production).
  - For each zone, three replicates are collected, yielding nine samples per household.
  - Geographic and sampling scope: 4 kebeles (parishes) with 18 farms per kebele, totaling 72 households.
  - Wealth status coverage: samples collected from households across wealth categories (poor, medium, rich).
  - Measurements are organized per fertility zone (three sites per household), resulting in 216 measurement sites (72 households × 3 zones).

- Field collection and sampling procedure
  - Random positioning within each zone; three replicates per zone.
  - Depths sampled: surface (0–20 cm) and below the plough layer (20–50 cm).
  - Sample handling: collected in cool conditions, stored in cool boxes, and transported to an external lab (Aberdeen) for analysis.
  - In-country limitations: soil moisture measurements were sometimes not possible due to equipment constraints; disturbed soil samples were repacked and equilibrated before analysis where needed.

- Analytical methods
  - Soil carbon and nitrogen: measured as percent C and N using CNS elemental analysis without ball-milling.
  - Soil pH: measured 1:5 in CaCl2 (with soil solution temperature recorded).
  - Soil mineral nitrogen: nitrate and ammonium quantified via chemical extraction with KCl and colorimetric assays:
    - Nitrate/nitrite: standard colorimetric method using sulphanilamide and NED reagents; 540 nm absorbance in microplate reader.
    - Ammonium: indophenol method with appropriate standards and reagents; color developed read at 620 nm.
  - Soil moisture: measured at sampling and at -10 kPa matric potential; where in-country analysis was not feasible, disturbed soils were repacked and saturated for 48 hours before measurement.
  - Soil texture: percent silt, sand, and clay determined by laser diffraction (Beckman-Coulter LS 13 320) after preparing samples to remove organic matter and dispersing soils.
  - Aggregate stability: water-stable aggregates assessed via wet sieving, with unstable and stable fractions quantified and used to compute WSA (water-stable aggregates percentage).

- Data scope and files
  - Metadata and datasets organized by site and kebele, with multiple CSV files:
    - Metadata.csv
    - BREAD-Master_data.csv (sample identifiers for Asore and Lay Arisho)
    - BREAD-Mineral_N_data.csv (soil mineral N measurements for Asore and Lay Arisho)
    - BREAD-Soil_C_N_and_pH.csv (soil C, N, and pH for Asore and Lay Arisho)
    - BREAD-Soil_moisture.csv (soil moisture for Asore and Lay Arisho)
    - BREAD-Particle_size_analysis.csv (particle size analysis for Asore and Lay Arisho)
    - BREAD_Aggregate_stability.csv (aggregate stability for Asore and Lay Arisho)
    - IPORE-Master_data.csv (sample identifiers for Konicha and 1st Choroko)
    - IPORE-Mineral_N_data.csv (soil mineral N for Konicha and 1st Choroko)
    - IPORE-Soil_C_N_and_pH.csv (soil C, N, and pH for Konicha and 1st Choroko)
    - IPORE-Soil_moisture.csv (soil moisture for Konicha and 1st Choroko)

- End-to-end data considerations
  - Data collection spans depth-differentiated samples, multiple zones per household, and replicates to capture variability across wealth status and kebeles.
  - Detailed documentation of methods enhances reproducibility and enables cross-site comparisons.
  - Some measurements required lab facilities outside the country; samples were shipped under controlled conditions to preserve integrity.
  - The design supports self-contained data exploration and the creation of data products for end users, aligning with broader data-support goals.