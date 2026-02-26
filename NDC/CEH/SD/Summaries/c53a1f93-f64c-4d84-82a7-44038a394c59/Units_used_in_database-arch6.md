# Please note that the units used in the data base are as listed below.

## Overview
- This document provides a data dictionary for a water chemistry database covering the Conwy catchment spatial water chemistry.
- It notes that the units in the database may differ from the units quoted by chemical analysts, as reflected in a separate metadata file.

## Data structure
- Columns include: Master_Site, Site_Code, Date, Rep, followed by a series of chemical variables with accompanying Qual (quality) fields.
- Each variable is paired with a specified unit in the table, highlighting how values are stored in the database versus analyst-specified units in metadata.

## Variables and typical units
- Major ions (cations/anions) and equivalents:
  - Ca, Mg, Na, Cl, SO4, K: generally in micro-equivalents per litre (ueq/l).
  - pH and related quality flags (pHQual) are listed, with pH typically represented via a quality flag rather than a unit in this row.
- Alkalinity and aluminum:
  - Alkalinity: ueq/l.
  - Al: ug/l.
  - Al27 (and other Al isotopes if present): ug/l.
- Nitrogen and phosphorus species:
  - NO3, NO2, NH4: units indicated as ueq/l (with corresponding Qual fields like NO3Qual, NH4Qual, NO2Qual).
  - TON (Total Organic Nitrogen), PO4_P (phosphate phosphorus): PO4_P in mg/l; TON and related qualifiers noted.
  - DOC (dissolved organic carbon): mg/l; DOCQual present.
- Carbon and particulates:
  - POM (particulate organic matter), POC (particulate organic carbon): mg/l; with corresponding POMQual / POCQual.
  - Salinity: mg/l; SalinityQual present.
- Conductivity and silica:
  - Conductivity: us/cm (µS/cm).
  - Si (silica): mg/l; SiQual present.
- Trace metals and other elements:
  - Fe, Mn, Cr, Ni, Cu, Zn, Co, Ba, Pb, Cd, Sb, Cs, Li, Be, U, S, S-containing species, Se, As, Rb, Sr, Mo, W, Ti, Sn, Nb/Sc, La, Ce, Pr, V, Ti, Nb/Sc, etc.
  - Most trace metals reported in ug/l (with Qual fields such as FeQual, MnQual, Ni58Qual, etc.).
  - Some elements appear as isotopes or specific oxidation states (e.g., Fe57 ug/l, Ni60 ug/l).
  - Fluoride (F) and other non-metal ions appear with mg/l or ug/l depending on the element.
- Additional notes:
  - Several items include Qual fields, indicating data quality or method flags (e.g., CaQual, NO3Qual, etc.).
  - The table includes entries where units vary by variable (ueq/l, mg/l, ug/l, or µS/cm), reflecting differences in measurement type.

## Data quality and metadata considerations
- Column 1 lists the variable names; Column 2 lists their units.
- Units in the database may differ from the units used by chemical analysts, as documented in the linked metadata file: Metadata_Analytical methods_conwy catchment spatial water chemistry.xlsx.
- Data may be patchy and come from multiple systems; quality flags (Qual fields) are used to denote data quality/measurement specifics.

## Implications for data support
- When integrating or comparing data, harmonize units across variables (ueq/l vs mg/l vs ug/l; conductivities in µS/cm).
- Leverage Qual fields to assess reliability and filter data as needed.
- Maintain traceability by using Master_Site, Site_Code, Date, and Rep to correctly align observations.
- Refer to the external metadata file for details on analytical methods and any unit conversions or method-specific notes.