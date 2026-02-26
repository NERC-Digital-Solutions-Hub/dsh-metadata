# Experimental design/Sampling regime

- Within each household, three fertility zones were sampled: home garden (close to house, higher inputs), near field (between home and far field), and far field (farther from house, more extensive production).
- Sampling design used random positioning of samples within each zone.
- Fieldwork spanned 4 kebeles (Asore, Lay Arisho, Konicha, 1st Choroko) with different wealth statuses (poor, medium, rich).
- Replication scheme:
  - Total households: 72
  - Fertility zones per household: 3
  - Replicates per zone: 3
  - Measurement sites: 216
  - Samples: 648
  - Kebeles: 4
- Data structure reflects two BREAD datasets (e.g., Asore/Lay Arisho vs Konicha/1st Choroko) with a total of 72 households and 216 sites.

## Study scope and sampling framework

- Households categorized by socioeconomic status (BREADIPORE) and soil types across kebeles.
- Four kebeles sampled with 18 farms per kebele, encompassing land managed at different wealth levels.
- Each farm contributed samples from three fertility zones, enabling spatial and management-level comparisons.

## Measurement design and replication

- Three fertility zones per household, with three replicates per zone, yield 648 total samples.
- Depths for soil cores: surface (0-20 cm) and sub-surface (20-50 cm).
- Random selection of sample positions within zones to mitigate bias.

## Field collection and sample handling

- Soil cores collected in the field from each zone and depth.
- Samples stored in a cool location, transported in cool boxes to preserve integrity.
- In-country limitations prevented intact core collection in some locations; disturbed soils were used where needed.
- Samples sent to Aberdeen for analysis; cold chain maintained to ensure sample integrity.

## Analytical methods and measurements

- Soil carbon and nitrogen
  - Measured as percent C and N using CNS elemental analyser without ball-milling.
- Soil pH
  - Measured in a 1:5 soil:CaCl2 suspension with temperature recorded.
- Soil mineral nitrogen
  - Nitrate and ammonium (NO3-, NO2-, NH4+) determined after KCl extraction from 10 g soil with 1 M KCl, followed by colorimetric analysis in a 96-well plate.
  - Nitrate/nitrite: standard preparation and color development with Sulphanilamide and NED; absorbance read at 540 nm.
  - Ammonium: indophenol method with specified reagents and a plate reader at 620 nm.
- Soil moisture
  - Field moisture recorded; -10 kPa matric potential moisture measured by repacking disturbed soils in collars when in-country equipment was unavailable.
- Soil texture
  - Percent silt, sand, and clay measured by laser diffraction (Beckman-Coulter LS 13 320) after sample pre-treatment (organic matter removal with H2O2, dispersion with sodium hexametaphosphate).
- Aggregate stability
  - Water-stable aggregates assessed by wet sieving, using a NaOH-assisted step to determine stable vs unstable fractions.
- Data collection and processing
  - Data were organized into multiple CSVs with metadata and site-specific measurements; standardization and quality checks applied during analysis.

## Data management and files

- Metadata.csv: Metadata for the study.
- BREAD-Master_data.csv: Sample identifiers for Asore and Lay Arisho.
- BREAD-Mineral_N_data.csv: Soil mineral nitrogen measurements for Asore and Lay Arisho.
- BREAD-Soil_C_N_and_pH.csv: Soil carbon, nitrogen, and pH for Asore and Lay Arisho.
- BREAD-Soil_moisture.csv: Soil moisture data for Asore and Lay Arisho.
- BREAD-Particle_size_analysis.csv: Particle size analysis for Asore and Lay Arisho.
- BREAD_Aggregate_stability.csv: Aggregate stability data for Asore and Lay Arisho.
- IPORE-Master_data.csv, IPORE-Mineral_N_data.csv, IPORE-Soil_C_N_and_pH.csv, IPORE-Soil_moisture.csv: Corresponding data for Konicha and 1st Choroko.

## Practical considerations and limitations

- In-country equipment limitations affected some measurements (e.g., intact cores for Ethiopia); adjustments included using disturbed soils and soil moisture methods suitable to available equipment.
- No single uniform dataset across all sites due to logistical constraints; data are organized by region/group (Asore/Lay Arisho vs Konicha/1st Choroko) with corresponding files.
- Data collection emphasized randomization, replicates, and standardized lab protocols to support cross-site comparisons and potential modeling.

## Potential data use and analytical opportunities

- Analyze correlations among soil carbon, nitrogen, pH, mineral N, moisture, texture, and aggregate stability across zones and wealth groups.
- Explore effects of proximity to home and management intensity on soil fertility indicators.
- Develop predictive models of soil fertility metrics based on depth, zone, and land-use intensity.
- Access to metadata and structured CSVs supports reproducible analyses, data cleaning, and integration with other environmental or socioeconomic datasets.