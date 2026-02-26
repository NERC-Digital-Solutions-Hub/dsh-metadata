# Details of data structure to ' Digestate_HF_and_NW_pH_NH4_NO3_v2.csv '

- Scope and origin
  - Supplement to supporting documentation for data series.
  - Dataset from the digestate wheat trial conducted in 2017.
  - Sites: Henfaes Research Center (HF) and North Wyke research station (NW).
  - Collaborating institutions: Bangor University and Rothamsted Research.
  - Focused variables: soil pH, ammonium (NH4) and nitrate (NO3) data.

- Dataset size and contents
  - 8 columns, 950 rows.
  - Variables cover site, sampling date, plot-level design, treatment, and soil chemistry measurements.

- Dataset structure and column definitions
  - Site: HF or NW, indicating sampling location.
  - Date: date soil was sampled from the field.
  - Plot: experimental plot number.
  - Block: blocking factor in the randomized block design (1–5).
  - Treatment: digestate treatment code with values:
    - C = zero N control
    - D = digestate
    - AD = acidified digestate
    - DNI = digestate with nitrification inhibitor (DMPP)
    - ADNI = acidified digestate with nitrification inhibitor (DMPP)
  - Soil_pH: pH of the soil sample.
  - Soil_NH4_mg_kg: NH4 concentration in mg N per kg dry soil.
  - Soil_NO3_mg_kg: NO3 concentration in mg N per kg dry soil.

- Units and measurement context
  - Date: calendar date format (sampling date).
  - Soil_pH: unitless (pH scale).
  - Soil_NH4_mg_kg: mg N per kg dry soil.
  - Soil_NO3_mg_kg: mg N per kg dry soil.

- Experimental design context
  - Plot sizes differ by site:
    - HF: nitrogen addition plots 1.2 m × 6.5 m (harvest area); other plots 1.2 m × 14 m.
    - NW: nitrogen addition plots 2 m × 4.5 m (harvest area); other plots 2 m × 9 m.
  - Design is a randomized block design with blocks 1–5.

- Data quality and completeness
  - NA values denote Not assessed (missing data for certain measurements or plots).

- Data governance and documentation implications
  - Metadata likely references the digestate wheat trial 2017, with two sites and multiple digestate treatments.
  - Requires consistent interpretation of codes (Site, Treatment) and precise date formats for cross-dataset compatibility.
  - Important to preserve provenance linking to the supporting documentation and trial protocols.

- Access, preservation, and future updates (for Data Stewards)
  - Ensure this dataset is catalogued with its metadata and version (v2). 
  - Maintain provenance to the 2017 trial and participating institutions.
  - Establish data sharing policies, including any embargoes and update procedures for future revisions.
  - Validate data quality through range checks (e.g., plausible soil pH, NH4, NO3 ranges) and consistency with the experimental design (Plot, Block, Treatment).