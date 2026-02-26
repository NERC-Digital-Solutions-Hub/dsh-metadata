# Countryside Survey: Soils Data 2019

- Purpose and scope
  - National rolling survey of soil condition and function in Great Britain, ongoing since 1978; supports understanding of soil status and dynamics at national scale.
  - Rolling five-year cycle (or 500 squares total per cycle) to detect change and buffer against climate variability; first 2019 cycle established under UKCEH-CS.
  - Focuses on soil and vegetation change with co-located vegetation assessments; aims to address questions about interactions among pressures, carbon pools, pH changes, compaction, phosphorus availability, and vegetation feedbacks.

- Survey design and sampling framework
  - 500 × 1 km squares sampled across GB within strata defined by the Land Classification of Great Britain; 100 squares visited per year.
  - Squares randomly sampled; exclude any square with more than 75% urban land or more than 90% sea.
  - Sample design builds on historic Countryside Survey plots (1978, 1998, 2007) to enable long-term change detection.
  - Sampling is coordinated to maximize site coverage while enabling year-on-year monitoring of spatial and temporal trends.

- Field sampling and site relocation
  - Within each annual 100 square, collect soil samples from 5 predetermined randomly dispersed locations and conduct vegetation X-Plots surveys.
  - Soil cores: 15 cm long C-core collected at locations co-incident with vegetation plots.
  - Historical sampling marker system updated over time (maps/markers created in 1978, relocated in later years); in 2019 plots were moved to the western corner of the inner 2 m × 2 m plot.
  - Samples refrigerated and sent to UKCEH laboratories for analysis.

- Laboratory methods and measured metrics
  - pH: measured in DI water and in CaCl2 (1:2.5 by weight) with QA checks.
  - Electrical conductivity (EC) measured in DI water extract.
  - Loss on Ignition (LOI) and related properties: hygroscopic water, LOI (organic matter loss up to 375°C), CaCO3 content; derived soil carbon concentrations (g C per 100 g soil and g C per kg; soil carbon stocks).
  - Soil carbon groups: classified into Mineral, Humus Mineral, Organo-mineral, Organic soils based on LOI and depth criteria.
  - Depth of organic layers: average depth of F/H horizons; peaty horizons categorized (peat > 4 cm depth considered within groupings).
  - Soil bulk density (from 15 cm core), stone content, and porosity calculations (using particle densities for mineral and organic matter).
  - Water content measures: gravimetric water content (GWC) and volumetric water content (VWC) derived from bulk density; fine earth fraction moisture.
  - Phosphorus: Olsen-P (for improved land uses – arable/improved grassland) via 0.5 M NaHCO3 extraction; total phosphorus (TP) determined by H2O2/H2SO4 digestion with colorimetric analysis.
  - Total soil organic carbon (SOC) and total nitrogen (TN) measured on ball-milled samples after inorganic carbon removal using an elemental analyzer; quality control with in-house references and standard checks.
  - Conversion factors: LOI-derived carbon converted to %C using established factors to maintain compatibility with legacy Countryside Survey data; data structures include calculated carbon densities and stocks (t C/ha).

- Quality control and data integrity
  - Internal standards and duplicates included in each batch; QA thresholds (e.g., pH and LOI standards within defined limits).
  - Calibration checks and reference standards run regularly; moisture corrections and blank corrections applied where applicable.
  - Specific QA for CaCO3 recovery (95–100%), Olsen-P and TP analyses with blanks, standards, and duplicates to ensure reproducibility.

- Data structure and data dictionary
  - Primary dataset: UKCEHCS_SOIL_METRICS_2019.csv with fields such as SQ_ID (1 km square identifier), PLOT_ID (plot number), LC07 (ITE Land Classification code), environmental zone descriptors, year, habitat classifications, soil depth metrics, LOI groups, pH (DIW and CaCl2), EC, LOI, CaCO3, C concentrations, SOC, TN, CN ratio, Olsen-P, TP, bulk density, porosity, stone content, gravimetric and volumetric water content, soil carbon groups, and various derived metrics (per m2, per ha).
  - Data conventions: -9999 denotes missing data; units provided per field (e.g., g/kg, mg/kg, µS/cm, %).
  - Linkages: accompanying field manual; vegetation metrics available in the related UKCEH-CS vegetation data set.

- Data analysis and outputs
  - Rolling program results contribute to annual analyses of soil change since 1978, focusing on LOI and pH time series (pH in water and related metrics).
  - Summary figures published to illustrate relationships and distributions, including:
    - Relationship between porosity and LOI
    - Porosity vs LOI on log scale
    - Bulk density vs LOI
    - pH vs LOI (overall and for broadleaved/mixed/Yew woodland)
    - pH in CaCl2 vs LOI
    - EC vs LOI
    - Calcite vs LOI
    - LOI vs gravimetric water content
    - LOI vs volumetric water content
    - LOI vs porosity
    - LOI and histograms for LOI and pH (water)
  - These figures aid interpretation of soil condition trends and support policy/research applications.

- Context, references and stewardship
  - Methodology builds on long-standing soil survey practices (e.g., Soil Survey Laboratory Methods, LOI methods, pH/EC measurement standards).
  - Grounded in Land Classification (ITE 2007) and prior Countryside Survey reports; results and methods documented in CEH and NERC publications.
  - Data management and field/lab roles are distributed among CEH/UKCEH staff and field teams, ensuring traceability and reproducibility.

- Access and further information
  - Data and methods are supported by accompanying field manuals, data sheets, and published companion reports; the 2019 dataset is positioned for ongoing integration into the rolling Countryside Survey program and public/science use.