# Units used in the database

- Purpose
  - States that the database stores values with specific units as listed in the table.
  - Notes that these database units may differ from the units in which variables are quoted by chemical analysts, as seen in a separate metadata file.

- Structure and content
  - Two-column format: Variable and Units.
  - Covers a wide range of chemical and water-quality parameters (e.g., Ca, Mg, Na, NO3, NH4, Cl, SO4, PO4_P, Al, Alkalinity, pH, Conductivity, Si, Fe, Mn, Zn, Cu, Ni, Cr, Se, As, U, etc.) with associated qualifiers (e.g., CaQual, NO3Qual, etc.).
  - Units commonly used include ug/l, mg/l, ueq/l, and us/cm; some entries reference qualitative qualifiers or missing/implicit units.

- Reference note
  - Mentions that the units in the database may differ from those used by chemical analysts, as documented in a separate file: Metadata_Analytical methods_conwy catchment spatial water chemistry.xlsx.

- Implications for data management (Data Leaders perspective)
  - Importance of clear unit consistency and documentation to prevent misinterpretation during analysis.
  - Need for robust metadata linking between the database and analyst-reported units to support correct data interpretation and reuse.
  - Potential requirement for unit harmonization or explicit conversion rules during data ingestion, analysis, and reporting.

- Recommended actions for data governance
  - Maintain a canonical unit standard within the data dictionary and provide conversion factors to analyst-reported units where needed.
  - Link database variables to their corresponding entries in external metadata (e.g., the indicated Excel file) to ensure traceability.
  - Implement data quality checks to identify and flag unit mismatches or conversion issues.
  - Communicate any known unit discrepancies in data release notes and ensure end-users understand the units used in the database.