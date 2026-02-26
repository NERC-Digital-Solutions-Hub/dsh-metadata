# Soil physico-chemical properties 1998 [Countryside Survey], Great Britain Version: 1: 02-6-2016

- Overview
  - Geospatial dataset from Countryside Survey 1998/1999 covering up to 256 one-kilometre squares across Great Britain.
  - Measured soil physico-chemical properties: pH, loss on ignition (LOI), carbon concentration and stock, total nitrogen, and Olsen phosphorus.
  - Data keyed to 1km grid cells with plot identifiers, year of survey, and administrative/land classification attributes.

- Data structure and fields (CSV: CS1998_SOIL_PHYSICOCHEM.csv)
  - SQUARE: 1km square sampling site code (text)
  - PLOT: Plot identifier within each square (text)
  - YEAR: Year of survey (numeric)
  - PH: Soil pH (numeric)
  - LOI: Percentage loss on ignition (numeric)
  - C_CONC_LOI: Carbon concentration from LOI (g/kg) using a 0.55 conversion factor
  - C_STOCK_LOI: Carbon stock from LOI (t/ha) using the 0.55 conversion factor
  - N_PERCENT: Total nitrogen percentage (numeric)
  - PO4_OLSEN: Olsen phosphorus (mg/kg) (numeric)
  - LC07, LC07_NUM: ITE Land Class 2007 (text and numeric code)
  - COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
  - COUNTY07: County or council area ( Eng/Wal) or Sco
  - EZ_DESC_07: Countryside Survey Environmental Zone description

- Methods and conversions
  - LOI methodology: top 15 cm soil, samples from up to 256 squares; 10 g soil after sieving to 2 mm; dried at 375°C for 16 h; 1 g sub-sample combusted at 550°C for 3 h; LOI (%) used to derive soil carbon with a conversion factor evolved from literature (0.50 initially; updated to 0.55 for CS estimates).
  - Carbon metrics: C_CONC_LOI (g/kg) and C_STOCK_LOI (t/ha) derived from LOI with 0.55 conversion factor.
  - Soil pH: measured in water via soil-water suspension (1:2 ratio), following standard protocol (deionised water, 30 min settling, pH reading after 30 seconds).
  - Total nitrogen: up to 1,280 samples analyzed with Elementar Vario-EL; describes combustion and detection via oxidative coupling and calibration against standards; typical sample weights 15 mg.
  - Olsen phosphorus: up to 1,280 cores extracted with 0.5 M NaHCO3 (pH 8.5); colorimetric determination using molybdenum blue with dialysis step; QA with in-house reference materials.

- GIS relevance and usage
  - Provides spatially explicit soil properties at 1km resolution suitable for mapping soil fertility, carbon stocks, and nutrient status.
  - Linked attributes include ITE Land Classification (LC07) and environmental zone descriptions (EZ_DESC_07), enabling contextual GIS analyses.
  - Data can be joined with other Countryside Survey layers and land classifications for policy, planning, or public-facing map products.

- Data quality, QA, and provenance
  - QA includes use of in-house reference materials with each batch; calibration checks described for nitrogen and phosphorus analyses.
  - Acknowledgement and copyright: Countryside Survey data owned by NERC-Centre for Ecology & Hydrology; must be acknowledged on copies, publications, and presentations.

- Usage constraints and acknowledgements
  - All use of Countryside Survey data must acknowledge CS data ownership and copyright.
  - Acknowledgement example: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and citation to CS publications as applicable.

- References and background
  - Methodological and contextual references include Countryside Survey reports (UK results 2007) and related soil analysis manuals (Allen 1989; Carey et al. 2008) and Land Classification publications (ITE Merlewood/Land Classification GB 1981–2007).
  - Provides links to Countryside Survey project documentation and supporting CEH/NERC publications for deeper methodological details.