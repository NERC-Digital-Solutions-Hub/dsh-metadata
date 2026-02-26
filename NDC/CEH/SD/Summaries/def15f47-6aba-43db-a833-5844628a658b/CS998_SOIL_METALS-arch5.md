# Soil metals data 1998 [Countryside Survey], Great Britain

## Overview
- Historic dataset of soil metal concentrations from samples across up to 256 1km squares in Great Britain, surveyed in 1998/1999.
- Source: Countryside Survey, NERC - Centre for Ecology & Hydrology (CEH).
- Dataset version: 1; date: 02-06-2016.
- Use must be acknowledged as Countryside Survey data owned by NERC-CEH; rights reserved.

## Data content and structure
- Dataset file: CS1998_SOIL_METALS.csv.
- Key variables (columns):
  - SQUARE: 1km square sampling site code (text).
  - PLOT: Plot identifier within each square (text).
  - YEAR: Year of survey (numeric).
  - CD, CR, CU, NI, PB, ZN: Cadmium, Chromium, Copper, Nickel, Lead, Zinc concentrations (ppm; equivalent to mg/kg and µg/g).
  - LC07: ITE Land Class 2007 description (text).
  - LC07_NUM: ITE Land Class 2007 numeric code.
  - COUNTRY: Country of square (ENG, SCO, WAL).
  - COUNTY07: County or Council for SCO; Eng/Wal for others (text).
  - EZ_DESC_07: Countryside Survey Environmental Zone description.
- Units: concentrations in parts per million (ppm), corresponding to mg/kg and µg/g.
- Data usage obligations: all CS data usage must be acknowledged.

## Laboratory methods and quality control
- Sample preparation:
  - Air-dried and sieved to <2 mm; cone-and-quartering for sub-sampling; ball milling with non-metallic agate mill.
- Digestion and analysis:
  - Total metal concentrations determined after aqua regia digestion under reflux.
  - 3 g soil digested, diluted to 100 mL; analysis by ICP-OES (JY38plus) with high power and low flow.
  - Some samples measured by ICP-MS at EA NLS (Llanelli).
  - Calibration with 12.5% HNO3 solutions matched to soil digestion matrix using Ca, Mg, Fe, and Al.
  - Batch structure: 20 samples per batch plus 2 QC samples and 2 blanks; digestion in groups of 12 (10 samples, 1 QC, 1 blank).
- Quality control and traceability:
  - Certified Reference Materials and samples from international soil exchange schemes used to verify methods.
  - Methods aligned with established references for metals in soils and plants.
  - Results traceable to Certified Reference Materials (NBS Estuarine Sediment 1646; BCR Lake Sediment No 280) via internal QC samples.
  - With each batch of 25 analyses, includes 2 internal reference samples, blanks, and a random duplicate.
- Notable data limitations:
  - Very few measurements fall below the detection limit; 12 observations below LOD across Cd, Cr, Ni.

## Data governance, documentation, and provenance
- Field procedures followed CS2000 Field Survey Handbook.
- Metadata supported by Countryside Survey framework (land class, environment zones, geographic context).
- Acknowledgement and copyright requirements apply to all copies, publications, and presentations using the data.
- References and methodologies linked to a broad set of Countryside Survey and CEH publications for traceability and reproducibility.

## Access, sharing, and reuse considerations
- Data are part of the Countryside Survey data holdings; sharing should comply with CEH/NERC policies and require proper acknowledgment.
- Dataset designed to be usable with standard soil metal concentration conventions (ppm mg/kg), suitable for integration with related Countryside Survey datasets and LAN classification data.

## Endnotes and references
- Field and laboratory methodologies referenced in CS publications and standard soil analysis texts (e.g., MASQ, ITE Land Classification).
- Key references include Countryside Survey documentation and related CEH/NERC data centre records.
- Access considerations and further methodological details are documented via CEH/Countryside Survey resources and linked publications.