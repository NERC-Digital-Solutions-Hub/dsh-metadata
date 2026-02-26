# Soil physico-chemical properties 1998 [Countryside Survey], Great Britain

- A dataset from the Countryside Survey (1998/1999) covering soil physico-chemical properties across up to 256 1km squares in Great Britain
- Key properties include pH, loss on ignition (LOI), carbon concentration and stock (from LOI), total nitrogen, and Olsen phosphorus
- Geographic scope includes 1km square sampling sites with associated plot, land class, country, county (or council), and environmental zone descriptors

## Data file and structure

- File: CS1998_SOIL_PHYSICOCHEM.csv
- Columns and data types:
  - SQUARE (text): 1km square sampling site code
  - PLOT (text): Plot identifier within each square (one of 5)
  - YEAR (number): Year of survey
  - PH (number): Soil pH
  - LOI (number): Percentage loss on ignition
  - C_CONC_LOI (number): Carbon concentration from LOI (g/kg) using 0.55 x LOI
  - C_STOCK_LOI (number): Carbon stock (t/ha) using 0.55 x LOI
  - N_PERCENT (number): Total nitrogen percentage
  - PO4_OLSEN (number): Olsen phosphorus (mg/kg)
  - LC07 (text) / LC07_NUM (number): ITE Land Class 2007
  - COUNTRY (text): England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY07 (text): County or council
  - EZ_DESC_07 (text): Countryside Survey Environmental Zone description
- Data use must be acknowledged per the citation below

## Measurement and processing methods

- LOI methods
  - LOI measured on 10 g soil (top 15 cm) from 1998 samples
  - Procedure: dry at 375°C for 16 hours; combust 1 g sub-sample at 550°C for 3 hours; LOI (%) calculated from weight loss
  - Carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI) derived using a conversion factor of 0.55 (g C per g LOI); adopted after review of LOI data (initially 0.5 used)
  - LOI is used to estimate soil organic matter and soil organic carbon concentration
- Soil pH
  - Measured in deionised water (suspension method)
  - Protocol: mix soil with water (1:2 w:w), stir, rest 30 minutes, measure pH after 30 seconds
- Total nitrogen
  - Up to 1280 samples analyzed with Elementar Vario-EL analyzer
  - Process: oxidative combustion, thermal conductivity detection; calibration with standards; QA with in-house reference materials
- Olsen phosphorus
  - Up to 1280 cores analyzed
  - Method: extract 5 g air-dried soil with 0.5 M NaHCO3 (pH 8.5); determine P colorimetrically using molybdenum blue (880 nm) with a dialysis step
  - QA with in-house reference materials

## Quality, context, and references

- LOI-to-C conversion factor updated to 0.55 based on analysis of 1998 and 2007 data; this value is used for all Countryside Survey estimates of soil C concentration and carbon density
- Lab and methodology provenance:
  - LOI and pH analyses conducted at ITE Merlewood
  - Total nitrogen and Olsen-P analyses conducted at ITE Merlewood
  - Method references include Allen (1989) for general chemical analysis methods and Carey et al. (2008) for Countryside Survey UK results
- Related datasets and classifications:
  - ITE Merlewood Land Classification (1996, 1981, 2007) referenced for LC07 classification
  - Land Classification and environmental zone descriptors linked to the database entry

## Usage, acknowledgement, and references

- All use of Countryside Survey data must be acknowledged
- Acknowledgement text:
  - Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © NERC-Centre for Ecology & Hydrology. All rights reserved
- Key references and links for methodologies and context:
  - Countryside Survey project overview: http://www.countrysidesurvey.org.uk
  - Major methodological references include Allen (1989), Black et al. (2002 MASQ), Bunce et al. (1996, 1981, 2007 ITE Land Classification), Carey et al. (2008 UK results)
  - Specifics on LOI and conversion factors: CS methodology notes and Carey et al. (2008) UK results
- Data publication and provenance notes:
  - The dataset forms part of the Countryside Survey data products (1998/1999 survey) with versioning and copyright maintained by CEH/NERC