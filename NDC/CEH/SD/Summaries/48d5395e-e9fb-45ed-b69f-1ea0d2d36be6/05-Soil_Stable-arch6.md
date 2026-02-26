# Supporting documentation for 05-Soil_Stable.csv

- Purpose
  - Defines the fields and metadata for a soil stable element dataset, enabling interpretation, quality assessment, and self-serve data use.

- Dataset overview
  - Sample metadata includes: Sample_Code, Location, Sample_Description (e.g., soil collected at depth 0-10 cm), Collection_Date (dd-mm-yyyy), and Sample_size_g_dm (g dry matter analyzed).
  - Sample_Type is defined as Soil.

- Key data columns (for each analyte)
  - Analyte concentration on a dry matter basis (mg/kg_dm or mg/kg dry mass, as specified).
  - Unc_<Analyte>_mg/kg_dm: Combined uncertainty of the analyte concentration on a dry mass basis.
  - Detection_Limit_<Analyte>_mg/kg_dm: Detection limit of the analyte on a dry matter basis.
  - Notes: If a field is blank, the corresponding concentration is below the detection limit.

- Analytes included
  - Cs (stable Cs)
  - Sr (stable Sr)
  - K (stable K)
  - Na (stable Na)
  - Ca (stable Ca)
  - Mg (stable Mg)
  - P (stable P)
  - Pb (stable Pb)
  - U (stable U)
  - Th (stable Th)
    - Th data appears with multiple suffixes (Th_mg/kg_dm, 1 and 2; 3 with corresponding Unc and Detection_Limit fields), indicating multiple Th-related columns or sub-entries within the same dataset.

- Measurement and units
  - Concentrations are in mg per kg dry matter (mg/kg_dm) or mg/kg dry mass, depending on the field.
  - Sample_size_g_dm indicates the amount of sample analyzed in grams of dry matter.
  - Collection_Date uses the format dd-mm-yyyy.

- Data quality and interpretation notes
  - Blank values for concentration or uncertainty indicate values below the detection limit.
  - Detection limits are provided per analyte to contextualize non-detects.
  - Some fields use slightly varied phrasing (e.g., “on a dry matter basis” vs. “dry mass basis”) but consistently refer to dry matter concentrations.

- Usage guidance for data support
  - Use this dictionary to understand what each column represents, enabling accurate aggregation, comparison, and visualization.
  - Treat blank values as below detection limits; use Detection_Limit fields to determine reporting thresholds.
  - When building dashboards or reports, reference the metadata to explain units, uncertainty, and detection limits to end users.