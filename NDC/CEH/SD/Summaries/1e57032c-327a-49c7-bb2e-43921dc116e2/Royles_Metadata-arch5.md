# Physiological and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements.

## Overview
- Field and laboratory study investigating moss physiology and stable isotope ecology to model spatial and temporal climatic signals.
- Fieldwork conducted monthly from April 2017 to September 2018 across multiple sites: Dersingham Bog, Brandon Country Park, and Wicken Fen.
- Target moss species chosen to represent diverse lifeforms and conditions; voucher specimens verified by bryologists.
- Measurements include in-field chlorophyll fluorescence, water content, and a range of isotope analyses on moss and water samples.

## Data and methods at a glance
- In-field measurements (from moss tips): chlorophyll fluorescence (F, Fm, F', Fm'), PAR, electron transport rate (ETR), and derived metrics such as photochemical yield and non-photochemical quenching.
- Water content: field relative water content (RWC) calculated from fresh and dry weights; cellulose extraction from dry moss; cryogenic distillation for water extraction.
- Isotope analyses: hydrogen (δD) and oxygen (δ18O) from fresh moss distillates and water samples; carbon isotopes (δ13C) from moss cellulose. All isotope data reported as per mille (‰); calibration against VSMOW/IAEA standards with vetted inter-laboratory standards.
- Supporting metadata: precise sampling dates, locations, habitat descriptions, and species identifications; sample numbering and linkages across datasets.

## Datasets and data structure
The dataset consists of four CSV files, with fields designed to interlink samples, locations, and analyses:
- Royles_Field_data_by_time
  - Tracks sample metadata and field measurements (e.g., location, date, session, month, species, description, field type, collection notes).
  - Key components include location, species, collection session/date, and field-measured value types (e.g., cellulose, RWC, C13, O18).
- Royles_RWC_and_Isotope_data
  - Contains quantitative results for water content and isotope metrics linked to each sample (sample-cellulose number, reference number, wet/dry weights, dry tube weight, RWC, C13, δ13C/12C, δ18O/16O).
  - Facilitates cross-dataset joins via sample reference numbers.
- Royles_Sample_Number_Key
  - Provides a mapping between numeric sample references and descriptive fields (date, location, species, herbarium status, etc.).
- Royles_Water_Samples
  - Documents water sample metadata (date, location, water type, source) and isotope values (δ18O, δD), including any notes about missing data.

## Metadata, provenance, and standards
- Field sites and collection permissions recorded prior to fieldwork; vouchers verified by bryologists.
- Isotope analyses conducted at multiple laboratories with explicit calibration standards:
  - δD and δ18O measured via IRMS with standard references (VSMOW, IAEA).
  - δ13C measured via elemental analyzer coupled to IRMS with IAEA standards.
- Precision targets:
  - δD: ±1‰; δ18O: ±0.5‰; oxygen isotope precision better than 0.4‰; δ13C precision better than 0.1‰.
- Lab methods and references cited to enable reproducibility (e.g., small-wood cellulose processing, water extraction times).

## Quality assurance and data processing
- Field measurements replicated (three measurements per sample in the field, plus three dark-adapted measurements) with mean and standard error calculated.
- Water content derived from precise mass measurements and drying to constant mass.
- Cellulose extraction and subsequent isotope analyses follow established protocols, with blanks and standards interspersed.
- Data are organized to support traceability from field collection to laboratory results, with explicit sample numbers and reference numbers to enable dataset joins.

## Data governance, sharing, and maintenance
- Data are organized into clearly named CSVs with documented field codes and descriptions to support dataset discoverability and reuse.
- The inclusion of a Sample Number Key file facilitates accurate linking across field measurements, isotopic results, and water analyses.
- Data steward considerations:
  - Ensure consistent metadata completeness (locations, dates, species, habitat, collection sessions).
  - Maintain stable, versioned identifiers for samples and references.
  - Document any data gaps or missing values due to sampling or analytical issues.
  - Consider depositing in a data repository with a formal data dictionary and licensing to enable broad reuse.
- Potential data sharing constraints should be noted where applicable (e.g., permissions, cross-laboratory data integration).

## Practical notes for reuse
- How to combine datasets:
  - Use sample reference numbers to merge Royles_Field_data_by_time with Royles_RWC_and_Isotope_data.
  - Use Royles_Sample_Number_Key to enrich entries with date, location, species, and herbarium information.
  - Link Royles_Water_Samples via the water sample metadata for Δ18O/ΔD comparisons.
- Units and notations:
  - Isotope values reported in per mille (‰) relative to standard scales (VSMOW/IAEA).
  - δ13C values in per mille; RWC as a proportion of dry weight.
- Spatial and temporal scope:
  - Data cover multiple field sites in eastern England across 2017–2018, enabling spatial-temporal modelling of moss physiology and isotope signals in relation to climate.

## Key challenges and recommendations for Data Stewards
- Challenge: Incomplete or inconsistent user needs regarding metadata depth and data availability.
  - Recommendation: Establish a minimal metadata schema (station, site, habitat, coordinates, sampling date, species, method) and enforce during deposition.
- Challenge: Timely data delivery from multiple field sites and labs.
  - Recommendation: Define data submission timelines and verify data completeness prior to publication; implement a data QA checklist.
- Challenge: Heterogeneous data formats and legacy field notes.
  - Recommendation: Standardize data templates; convert legacy records to the agreed CSV structure; maintain a data dictionary.
- Challenge: Interoperability across different systems and laboratories.
  - Recommendation: Use consistent measurement units, codebooks, and standard reference materials; document lab-specific protocols in metadata.
- Challenge: Managing large, multi-table datasets with complex joins.
  - Recommendation: Provide a robust data schema with a data dictionary; consider a central catalog or relational database to support scalable queries.