# Supporting information

- Document overview
  - Supporting information for the dataset BLEL_Stream_nutrients.csv
  - Collected by Emma Gray for the project NEC05744

- Dataset contents
  - Nutrient concentrations (mg/L) measured in Blelham Tarn water
  - Analytes: nitrate, silica, total nitrogen (TN), total phosphorus (TP), soluble reactive phosphorus (SRP)

- Sampling details
  - Location: main buoy at 1 m depth; inflows/outflows and lake site
  - Inflow/outflow sites: Wray Beck (inflow), Blelham Beck (outflow), Fish Pond Beck (inflow), Ford Wood Beck (inflow)
  - Sampling period: June–December 2016 and January–December 2017
  - Sampling frequency: monthly

- Analytical procedures (key methods)
  - Soluble Reactive Phosphorus (SRP)
    - Filtration in the field (47 mm GF/C)
    - Colorimetric determination using ammonium molybdate and antimony potassium tartrate
    - Blue complex read at 880 nm; calibration curve with standards (10–100 µg/L)
    - Quality control: AQC stock (50 µg/L) diluted to 10 µg/L for validation
  - Total Phosphorus (TP)
    - Potassium persulphate digestion with subsequent colorimetric molybdenum blue
    - Unfiltered samples digested and measured with SEAL AQ2; blanks used for correction
  - Total Nitrogen (TN)
    - Acidification with HCl, purge to remove inorganic carbon
    - Measurement with Shalar Formacs CA16 (ND25)
  - Nitrate
    - Ion chromatography (Dionex ICS2100) after 0.45 µm filtration
    - QC samples every 10 samples
  - Silica
    - Colorimetric method using ammonium molybdate; reduced with ascorbic acid
    - Blue complex read at 880 nm; background corrected with blanks

- Data structure and metadata
  - Columns: Date (dd/mm/yyyy), Site (inflow/outflow/lake), nitrate, silica, total nitrogen, total phosphorus, soluble reactive phosphorus (all mg/L)

- Quality assurance and documentation
  - Detailed procedural notes for each analyte to support reproducibility
  - Calibration curves and QA/QC steps described (e.g., AQC, blanks, QC intervals)

- Figures and mapping
  - Fig.1: Map of Blelham Tarn inflows and outflows (referenced in the document)

- Data governance considerations for data stewards
  - provenance: dataset collected for NEC05744; attributed to Emma Gray
  - metadata richness: explicit methods, sites, sampling schedule, and units
  - potential governance needs:
    - ensure consistent site naming and temporal coverage
    - preserve full methodological metadata for re-use
    - consider date formats and unit consistency (mg/L)
    - establish data update and versioning workflows
    - plan for portal/catalogue deposition and access control as appropriate

- Access and usage notes
  - Data ready for discovery, with clear structure and documented methods
  - Useful for water quality assessments, hydrology studies, and ecosystem monitoring related to Blelham Tarn