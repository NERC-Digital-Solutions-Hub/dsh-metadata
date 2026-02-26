# UKCEH Countryside Survey: Soils Metrics 2019

- Purpose and scope
  - Long-running national study to monitor soil condition and function across Britain, linking soil status to vegetation and land management.
  - Rolling, five-year survey cycle (500 squares total per cycle; 100 squares visited each year) to detect spatial and temporal change while buffering against climate variability.
  - Aims include understanding interactions of multiple pressures on soil/vegetation, changes in topsoil carbon, pH responses to pollution/management, compaction, phosphorus availability, and feedbacks between vegetation and soil.

- Survey design and rolling program
  - Based on the Countryside Survey of GB; 1 km squares randomly sampled within strata defined by the Land Classification (ITE 2007).
  - Exclusions: squares with >75% urban land or >90% sea excluded.
  - Sampling framework: 500 squares per five-year cycle, with 100 squares surveyed annually.
  - Historical sampling framework draws on 1978, 1998, and 2007 squares to enable long-term change detection.
  - Sampling within each square focuses on soil and vegetation metrics; in 2019, rolling program emphasizes soil and vegetation changes.

- Sample collection and site relocation
  - Within each annual 1 km square, five soil samples collected from randomly dispersed locations using a 15 cm C-core, aligned with vegetation X-Plots.
  - Historical plot locator markers: maps from 1978, permanent markers added in 1990, with relocations in 1998, 2007, and 2019 to maintain consistency.
  - Soil cores are refrigerated and shipped to the UKCEH Bangor laboratory for analysis.

- Metrics, laboratory protocols and analytical methods
  - Land classification: ITE Land Classification 2007 used for stratification; vegetation metrics available in the accompanying vegetation dataset.
  - Soil carbon groups (LOI-based) and depth classifications:
    - Mineral, Humus mineral, Organo-mineral, Organic soils (via LOI-based groupings).
    - Depth of organic layers, including peaty horizons (peaty topsoil 10–40 cm; peat >40 cm).
    - Soil type groupings: Mineral, FHO horizons (2–10 cm), Organic (LOI > 20%), Peaty topsoil, Peat.
  - Soil properties and measurements:
    - pH: in deionised water (DIW) and CaCl2; quality controls with internal standards and duplicates.
    - Electrical conductivity (EC) of soil slurry.
    - Hygroscopic water content, LOI, CaCO3: determined by thermogravimetric analysis (TGA); LOI corresponds to organic matter content and carbon estimates.
    - Carbon concentration and soil organic carbon (SOC) via loss-on-ignition-derived estimates and elemental analysis (SOP3102 method) with in-house references for QA.
    - Bulk density, porosity, stones and their volume; particle density via mixed densities; porosity derived from bulk and particle densities.
    - Gravimetric and volumetric water contents for the fine-earth fraction.
    - Olsen phosphorus (P Olsen) for arable and improved grasslands; total phosphorus (P total) via H2O2/H2SO4 digestion and colorimetric analysis.
    - Total soil organic carbon (SOC) and total nitrogen (TN) via elemental analysis after removing inorganic carbon.
  - Quality control landmarks:
    - Internal standards and duplicates across batches.
    - Calibration and blanks for chemical analyses; moisture content and standard recovery checks; P analyses include QC references.
  - Data processing notes:
    - LOI-to-carbon conversions follow legacy CS method (0.55 factor or regression-based approach), ensuring compatibility with 2007 CS data.
    - Derived metrics include SOC t/ha, carbon concentrations per kg and per 100 g soil, and related density-based calculations.

- Data structure and accessibility
  - Core dataset: UKCEHCS_SOIL_METRICS_2019.csv
  - Key fields include: SQ_ID (1 km square), PLOT_ID (X-plot), Land Classification (LC07), YEAR, habitat descriptors, depths (AVERAGE_O_DEPTH), LOI groups (SOIL_GP_LOI_CS_1_4), soil groupings (SOIL_GP_1_3, SOIL_GP_1_5), pH values (C_B_PH_DIW, C_B_PH_CACL2), EC (C_B_EC), moisture and LOI-related metrics, CaCO3 (C_FE_CACO3), bulk density (C_FE_BULK_DENSITYGPERCM3), porosity, stone metrics, water content (C_FE_VWC, C_FE_GWC_D, C_FE_GWC_W), Olsen P (C_FE_POLSEN), total P (C_FE_PTOTAL), total C (C_FE_CTOTAL), total N (C_FE_NTOTAL), CN ratio, and derived carbon metrics.
  - Analysis and outputs are part of a rolling program with annual publications and figures illustrating soil change over time (e.g., LOI and pH trends; relationships among porosity, bulk density, pH, and LOI).
  - Summary figures (2019) include relationships and histograms for LOI, pH, bulk density, porosity, and other soil properties across broad habitats.

- Annual analysis and interpretation
  - Rolling program enables year-on-year and long-term trend analyses of soil organic matter and pH, among other metrics.
  - Analyses align with Scott (2008) and Reynolds et al. (2013) methodologies; figures depict relationships among key soil properties and LOI over time.
  - Data intended to inform national-scale soil change assessments and to support policy-relevant insights into soil health, carbon stocks, nutrient dynamics, and the effects of land-use and deposition changes.

- References, collaboration and acknowledgments
  - Methodological and analytical framework draws on extensive CEH/UKCEH documentation, prior Countryside Survey reports (2007, 2017/2019), and foundational soil analysis references.
  - Acknowledges CEH staff, field teams, rolling program coordinators, and UKCEH collaborators who contributed to data management, processing, analysis, and archiving.