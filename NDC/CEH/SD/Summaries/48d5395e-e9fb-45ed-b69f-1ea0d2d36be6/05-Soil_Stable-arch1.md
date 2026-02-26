# Supporting documentation for 05-Soil_Stable.csv

## Overview
- Provides the data dictionary and metadata for the 05-Soil_Stable.csv dataset.
- Records are soil samples with metadata on location, description, collection date, and sample size (dry matter basis).
- Focuses on concentrations of stable elements in the topsoil (0–10 cm depth).

## Key metadata fields
- Sample_Code: unique sample identifier.
- Sample_Type: soil.
- Location: name of the collection site.
- Sample_Description: additional details; notes soil collected at depth 0–10 cm.
- Collection_Date: date of sample collection (dd-mm-yyyy).
- Sample_size_g_dm: amount of sample analyzed (g dry matter).

## Measured variables and units
- Cs_mg/kg_dm, Sr_mg/kg_dm, K_mg/kg_dm, Na_mg/kg_dm, Ca_mg/kg_dm, Mg_mg/kg_dm, P_mg/kg_dm, Pb_mg/kg_dm, U_mg/kg_dm, Th_mg/kg_dm
  - All are concentrations on a dry matter basis; units are mg per kg dry mass.
  - Each variable has associated Unc_<element>_mg/kg_dm (combined uncertainty) and Detection_Limit_<element>_mg/kg_dm (detection limit).
  - Notes indicate that blank values mean concentrations were below the detection limit.
  - Th_mg/kg_dm indicates multiple fields (1, 2, 3) to accommodate additional measurements per sample; each has corresponding uncertainty and detection limit fields (e.g., Unc_Th_mg/kg_dm, Detection_Limit_Th_mg/kg_dm).

## Uncertainty and detection information
- Unc_<element>_mg/kg_dm provides combined uncertainty for each concentration.
- Detection_Limit_<element>_mg/kg_dm provides the detection limit for each measurement.
- Some fields explicitly state that blanks denote non-detects (below detection limit).

## Data quality and formatting notes
- Several variables are described with parenthetical clarifications (e.g., “on a dry matter basis”) and inconsistent phrasing (e.g., Ca_mg/kg_dm lines with extended labels).
- The presence of non-detect indicators requires careful handling in analyses (treatment of censored data).
- Th_mg/kg_dm includes multiple subfields (1, 2, 3) to support multiple measurements or replicates per sample.

## Potential analytical applications
- Correlation analyses among stable element concentrations (e.g., Ca vs Mg, K vs Na).
- Spatial analysis across locations using the Location field.
- Temporal analysis possible via Collection_Date if multiple samples exist over time.
- Handling non-detects using reported Detection_Limit values or uncertainty bounds.
- Modeling concentrations as a function of sample metadata (depth 0–10 cm assumed constant here) and location.

## Accessibility and provenance considerations
- Emphasizes tracking data sources and metadata; suggests making datasets discoverable with metadata.
- Provides explicit measurement metadata (units, uncertainties, detection limits) to support rigorous statistical methods.
- Highlights common soil data challenges relevant to analysts (non-detects, scale differences, data formatting inconsistencies).