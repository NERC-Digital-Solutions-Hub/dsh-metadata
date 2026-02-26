# Soil metals data 1998 [Countryside Survey], Great Britain

## Summary
- A dataset of soil metal concentrations from 1998/1999 Countryside Survey across Great Britain, captured in up to 256 1km squares.
- Measurements cover Cadmium (CD), Chromium (CR), Copper (CU), Nickel (NI), Lead (PB), and Zinc (ZN) with site metadata (SQUARE, PLOT, YEAR) and classification fields (LC07, COUNTRY, COUNTY07, EZ_DESC_07).
- Data are provided in CS1998_SOIL_METALS.csv; data use requires formal acknowledgement to NERC - CEH.
- Laboratory methods include aqua regia digestion and ICP-OES analysis, with rigorous QA/QC and traceability to Certified Reference Materials.

## Data model and key fields
- SQUARE: 1km square sampling site code (text)
- PLOT: Plot identifier within each square (text)
- YEAR: Year of survey (numeric)
- CD: Cadmium concentration (ppm; mg/kg; µg/g)
- CR: Chromium concentration (ppm; mg/kg; µg/g)
- CU: Copper concentration (ppm; mg/kg; µg/g)
- NI: Nickel concentration (ppm; mg/kg; µg/g)
- PB: Lead concentration (ppm; mg/kg; µg/g)
- ZN: Zinc concentration (ppm; mg/kg; µg/g)
- LC07: ITE Land Class 2007 (text)
- LC07_NUM: ITE Land Class 2007 (numeric code)
- COUNTRY: Country (ENG, SCO, WAL)
- COUNTY07: County or Council (text)
- EZ_DESC_07: Countryside Survey Environmental Zone description

## Collection, laboratory methods, and QA
- Samples: Soil collected per CS2000 Field Survey Handbook; air-dried and sieved to <2 mm; coned and quartered for sub-sampling.
- Digestion and analysis: Aqua regia digestion; 3 g samples dissolved and diluted to 100 ml; metals measured by ICP-OES (JY38plus). Some samples measured by ICP-MS at a secondary lab.
- Detection and calibration: Calibration with matrix-matched solutions; traceability to Certified Reference Materials (e.g., NBS Estuarine Sediment 1646, BCR Lake Sediment No 280).
- QA/QC: Always include certified reference materials, international soil exchange samples, blanks, and duplicates; batches of 20 samples with 2 QC samples and 2 blanks per batch; internal QC and random duplicate checks.
- Note on detection: Very few measurements fall below the limit of detection (12 observations in total across Cd, Cr, Ni).

## Access, attribution, and provenance
- All CS data usage must include the following acknowledgment: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Data are sourced from Countryside Survey materials and methods, with references and methodologies available via CEH and associated publications.
- Primary methodological references and project links provided (e.g., Countryside Survey website, ITE Land Classification publications, MASQ soil quality framework).

## Potential uses and data products (Data Support perspective)
- Create self-serve analyses and dashboards showing spatial patterns of soil metal concentrations by 1km square, year, and land classification.
- Combine with LC07 land classification and environmental zone descriptors (EZ_DESC_07) to explore associations between land use/class and metal concentrations.
- Support environmental monitoring and policy work related to soil contamination and soil quality trends in Great Britain.
- Provide transparent data provenance and QA documentation to end users, enabling reproducible analyses.

## Limitations and considerations
- Patchy data in some elements due to detection limits; a small subset of measurements fall below detection limits.
- Data collected in 1998/1999; cross-temporal analyses require careful alignment with later surveys (e.g., 2007 UK Results).
- Data may involve multiple analytical laboratories; ensure harmonization notes are considered when performing cross-lab comparisons.
- Usage requires proper acknowledgment and adherence to data licensing terms.

## References and related resources
- Countryside Survey project pages and methodologies
- ITE Merlewood Land Classification publications (ITE Land Classification of Great Britain)
- MASQ: Monitoring and Assessing Soil Quality in Great Britain
- Countryside Survey: UK Results from 2007
- Laboratory analysis references and standard methods for trace metals in soils