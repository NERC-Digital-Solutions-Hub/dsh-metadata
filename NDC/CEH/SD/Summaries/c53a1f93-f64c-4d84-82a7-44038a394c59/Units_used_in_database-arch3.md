# Data Units and Variables in the Conwy Catchment Spatial Water Chemistry Database

- Overview
  - This document is a data dictionary listing column names and their corresponding units for the Conwy catchment spatial water chemistry database.
  - It notes that database units may differ from those used by chemical analysts, referencing a separate metadata workbook (Metadata_Analytical methods_conwy catchment spatial water chemistry.xlsx).

- Structure of the data dictionary
  - Column 1: Column names in the database (e.g., Master_Site, Site_Code, Date, Rep, CaQual, Ca, MgQual, Mg, etc.).
  - Column 2: Units for the database values (e.g., ug/l, mg/l, us/cm, ueq/l, pH, etc.).
  - Some variables have qualitative flags (Qual) accompanying their numeric values to indicate data quality or qualifiers.

- Variables and units (highlights)
  - Major cations and anions and related species:
    - Ca, CaQual; Mg, MgQual; Na, NaQual
    - SO4, SO4Qual; Cl, ClQual
    - NO3, NO3Qual; NH4, NH4Qual; NO2, NO2Qual
    - DOCQual, DOC (documented as an associated chemical parameter)
    - pHQual, pH; AlkalinityQual, Alkalinity (in ueq/l)
  - Nutrients and phosphorus species:
    - Total_NQual, Total_N
    - PO4_P, PO4_PQual
    - TON, TONQual
  - Physical/chemical properties:
    - ConductivityQual, Conductivity (us/cm)
    - AlQual, Al (ug/l)
    - SiQual, Si (mg/l)
    - SalinityQual, Salinity (mg/l)
  - Trace metals and metalloids (numerous entries, many in ug/l or mg/l):
    - FeQual, Fe; MnQual, Mn
    - NiQual, Ni; CoQual, Co
    - CuQual, Cu; ZnQual, Zn
    - AsQual, As; SeQual, Se
    - LiQual, Li; BeQual, Be
    - Al27Qual, Al27; ScQual, Sc
    - VQual, V; CrQual, Cr
    - MoQual, Mo; CdQual, Cd; SbQual, Sb
    - CsQual, Cs; BaQual, Ba; PbQual, Pb
    - UQual, U; BQual, B; SQual, S
    - LaQual, La; CeQual, Ce; PrQual, Pr
    - WQual, W; TiQual, Ti; SnQual, Sn
  - Miscellaneous elements and parameters:
    - POMQual, POM; POCQual, POC
    - FQual, F
    - RbQual, Rb; SrQual, Sr
    - Li, Be, Al27, Sc, V, Cr, Mn, Fe57, Ni58, Ni60, etc. with corresponding units

- Data quality and metadata considerations
  - Qual fields indicate data quality or qualifiers for the corresponding measurements.
  - The document acknowledges potential discrepancies between database units and analyst-reported units, underscoring the need for careful metadata alignment and unit mapping.
  - Metadata availability (link to Metadata_Analytical methods workbook) is essential for interpreting units and methods.

- Implications for monitoring framework design (for authors)
  - Standardization and governance:
    - Use this unit mapping to harmonize data across datasets and ensure consistent reporting.
    - Align database units with the preferred standard units used in policy and reporting.
  - Metadata and provenance:
    - Maintain clear metadata references to the analytical methods and the external workbook to support data interpretation and reuse.
    - Ensure a consistent approach to Qual flags and data quality criteria across all variables.
  - Data accessibility and transformation:
    - Plan for data transformation steps to convert database units to analyst-reported units if needed for transparency or stakeholder communication.
    - Ensure data sharing adheres to governance standards, with underlying data and metadata openly available where appropriate.
  - Data quality assurance:
    - Leverage the wide range of chemical parameters to design quality checks, verify unit conversions, and monitor for missing or inconsistent qualifiers.
  - Stakeholder communication:
    - Present clear, standardized dashboards or reports that reflect the standardized units and quality qualifiers to support policy scrutiny and future decision-making.

- End note
  - The document provides a comprehensive mapping of column names to units for a broad suite of water chemistry parameters in the Conwy catchment, highlighting the importance of metadata alignment, data quality, and governance for effective monitoring frameworks.