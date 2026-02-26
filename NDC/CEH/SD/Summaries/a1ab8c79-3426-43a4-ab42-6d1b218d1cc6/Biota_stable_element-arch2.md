# Supporting documentation for Biota_Stable_Element.csv

- Purpose: Metadata and data dictionary for Biota_Stable_Element.csv to support consistent recording and later scrutiny of environmental health and policy performance.
- Context: Designed for organisations with set monitoring responsibilities; emphasizes standardised, QA-friendly data suitable for reports, maps, and portal storage.

## Key scope and structure

- Sample identifiers and metadata:
  - Sample_Code: unique sample identifier.
  - RAP: sample type based on ICRP Reference Animals and Plants (RAPs).
  - Sample_Description: additional details; note that RCN119, RCN120, and RCN121 are replicate soil samples; units are centimetres for description.
  - Collection_Date: date of soil sample collection (format: dd-mmm-yyyy).
- Measurement data:
  - For each element (e.g., I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U):
    - <Element>_mg_kg_fw: concentration on a fresh mass basis; units are milligrams per kilogram.
    - Detection_Limit_<Element>_mg_kg_fw: the detection limit for that element in the given sample; same units.
  - Notes on detection: blank values indicate concentrations were detectable (per the accompanying notes) or below detection limits; the dataset uses a structured convention to indicate when a value is below detection or detectable.
- Special formatting notes:
  - Several elements include paired descriptions indicating how detection limits and detectability are recorded (e.g., “Detection_Limit_<Element>_mg_kg_fw” with accompanying guidance).
  - Replicate and data provenance details are incorporated to support quality assurance and traceability.

## Data quality, standardisation and reuse

- Data QA/cleaning: fields are designed to be verified, cleaned, and transformed in line with standard environmental monitoring practices.
- Outputs enabled: clear formatting for environmental health indicators against standards, with potential for mapping, charting, and reporting.
- Data management: emphasis on storing and uploading datasets to appropriate portals to facilitate long-term accessibility and reuse.

## Practical implications for analysts

- Facilitates comparison over time and across sites by providing a uniform data dictionary and consistent unit conventions (mg/kg_fw).
- Supports transparency about detection limits, enabling informed interpretation of non-detects.
- Replicate samples are identifiable, aiding assessment of measurement precision and measurement uncertainty.
- RAP metadata links samples to recognized reference organisms/plants, supporting broader ecological interpretation.