LANDWISE Detailed Survey Supporting Documentation (Version 1.4)

- Purpose and scope
  - Documents a dataset of surface and sub-surface hydraulic and hydrological soil properties across the Thames catchment.
  - Includes soil bulk density, estimated porosity, volumetric soil moisture content, and soil moisture retention (to 100 cm suction); surface infiltration rates; and soil saturated hydraulic conductivity (Ksat) at 25 cm and 45 cm depth.
  - Field-scale point data collected from 7 fields at three sites with contrasting geology and land-use practices to characterize heterogeneity under Natural Flood Management (NFM) measures.
  - Sites cover mudstone, chalk (carbonate), and limestone geology with land uses including permanent grassland, arable with grass, and mature woodland.
  - Sampling conducted in representative in-field areas, trafficked and untrafficked zones, with repeats before and after harvest (April 2021 to October 2021).

- Study design and sites
  - LANDWISE Detailed Survey builds on a Broad-scale survey to better characterise field-scale heterogeneity under different land-based NFM measures.
  - Seven fields chosen from Broad-scale survey, grouped into three sites by geology: Mudstone, Carbonate (Chalk), and Limestone.
  - Field IDs and characteristics include: 18_6 (Mudstone, permanent grassland), 44_1 (Mudstone, woodland), 26_1 (Chalk, arable with conventional/controlled traffic), 23_5 (Chalk, arable with conventional traffic), 31_3 (Limestone, arable with conventional till), 27_2 (Limestone, arable with grass/ herbal ley), 27_4 (Limestone, arable with grass/herbal ley).
  - Each site contains fields designed to compare land-use types or management practices (e.g., grassland vs woodland, conventional vs controlled traffic, arable with/without grass).

- Sampling strategy
  - Measurements taken along transects within fields at three location types: TR (trafficked), IN (infield), and UN (untrafficked margins).
  - Each field includes 15 sampling locations (5 TR, 5 IN, 5 UN) to capture spatial heterogeneity.
  - Table 3 lists measurements and timing, including bulk density, soil moisture retention, Ksat, infiltration rate, and soil/vegetation root depth.
  - Table 4 maps measurements to location types (which measurements were taken at which location types).

- Measurements and methods (field and lab)
  - Field sampling
    - Soil samples collected with Eijkelkamp kit (07.53.SC), closed ring holder, Edelman and Stony augers; samples refrigerated on collection.
    - Infiltration measurements with Mini Disk Infiltrometers across arable, grassland, and woodland sites; suction commonly 2 cm (lighter soils) or 0.5 cm (heavier clays); measurements recorded at regular intervals to calculate unsaturated hydraulic conductivity.
    - Saturated hydraulic conductivity measured at 25 cm and 45 cm depth using Guelph Permeameter; two-head method used (two different head heights) for accuracy.
    - Measurements taken at transect locations to avoid disturbances from prior measurements; parallel soil moisture, density, and infiltration data collected along transects.
  - Laboratory analysis
    - Volumetric water content (VWC) obtained by oven-drying soils at 105 °C; VWC calculated from wet/dry masses.
    - Dry bulk density calculated from dry mass and known core volume; porosity estimated from bulk density assuming particle density of 2.65 g/cm3.
    - Soil moisture retention analyzed with Eijkelkamp Sandbox across pF values (0 to 2) to determine water retention characteristics; samples saturated with deionised water, weighed during equilibration.
  - Root depth
    - Soil and vegetation root depth measured with auger and tape measure at each location and sampling event.

- Data structure and contents
  - One CSV file: LANDWISE_detailed_survey_soil_data_2021_updated_v2
  - Contains 70 columns and 380 rows; column definitions align with the dataset documentation (Table 5).
  - Key data types include identifiers (Site, Field, Location), location type (TR/IN/UN), geographic coordinates, sampling dates, depths, and measured values (bulk density, porosity, VWC, pF retention, Ksat, infiltration rates, root depths, etc.).
  - Missing values are represented as NA; some measurements are flagged or omitted due to quality control.

- Fieldwork and instrumentation
  - Equipment and models used:
    - Soil sampling: Eijkelkamp 07.53.SC kit, Edelman and Stony augers.
    - Drying and weighing: Heraeus 105 °C ovens, Precisa 2200C balance, Precisa 5000D balance for sandbox measurements.
    - Infiltration: Mini Disk Infiltrometer (Decagon Devices).
    - Saturated hydraulic conductivity: Guelph Permeameter (Soilmoisture Equipment Corp.).
    - Moisture retention: Eijkelkamp Sandbox.
  - All equipment logged and calibration/check procedures followed to ensure measurement integrity.

- Quality control (QC)
  - Data entry QC: field and lab measurements entered by the recorder, then checked by another person to correct typographical errors.
  - Infiltration QC flags (Infiltration_1_QC_Flag, Infiltration_2_QC_Flag):
    - Good: no issues.
    - Invalid: physically implausible values, removed.
    - A: unsteady infiltration rate progression.
    - B: less than 15 ml infiltrated (criterion for reliable calculation).
    - C: unusually high K values (within upper bounds of typical distributions; may reflect novel soil states or management).
  - Guelph permeameter QC flags (Guelph_Permeameter_QC_Flag):
    - Good: no issues.
    - Invalid: implausible values (e.g., negative, alpha outside 0.01–0.5 cm-1), removed.
  - Guelph permeameter notes indicate use of double-head method preferred; if invalid, two single-head measurements were used and averaged. Details available in device operating instructions.

- Data accessibility and related datasets
  - The dataset is related to the LANDWISE Broad-scale survey dataset for Thames catchment (soil near-surface properties, vegetation observations, land use and management across 1800 locations, 2018–2021).
  - Documentation provides methods, calculations (e.g., Carsel & Parrish 1988 relationships for moisture retention), and references for analysis tools.
  - Dataset versioned as LANDWISE Detailed Survey Supporting Documentation (Version 1.4) with updated field data (2021).

- References and supporting materials
  - Carsel, F., & Parrish, R. S. (1988). Developing Joint Probability Distributions of Soil Water Retention Characteristics.
  - Decagon Devices (2018). METER Environment.
  - METER (2021). MINI DISK INFILTROMETER Manual.
  - Soilmoisture Equipment Corp. (2012, 2020). Guelph Permeameter instructions and Ksat calculator.
  - Zhang, R. (1997). Determination of Soil Sorptivity and Hydraulic Conductivity from the Disk Infiltrometer.