# Soil metals data 1998 [Countryside Survey], Great Britain

## Overview
- A dataset of soil metal concentrations from 1km square samples across Great Britain, surveyed in 1998/1999 as part of the Countryside Survey (CS).
- Contains up to 256 1km squares with data for 5 plots per square (PLOT within SQUARE).
- Metals measured: Cadmium (CD), Chromium (CR), Copper (CU), Nickel (NI), Lead (PB), Zinc (ZN) — reported in ppm (mg/kg, μg/g).
- Additional metadata: land classification (LC07, LC07_NUM), environmental zone (EZ_DESC_07), country (COUNTRY), and administrative area (COUNTY07).
- Data usage requires acknowledgment of Countryside Survey data owned by NERC-Centre for Ecology & Hydrology.

## Data structure and variables
- Core identifiers: SQUARE (1km square code), PLOT (plot within square), YEAR (survey year).
- Measured metals: CD, CR, CU, NI, PB, ZN (ppm).
- Metadata fields: LC07 (ITE Land Class 2007), LC07_NUM, COUNTRY (ENG, SCO, WAL), COUNTY07, EZ_DESC_07.
- File provenance and usage rights embedded in the dataset’s documentation.

## Spatial and temporal scope
- Geographic coverage: Great Britain (England, Scotland, Wales).
- Spatial resolution: 1km square sampling units; up to 256 squares.
- Temporal scope: Survey conducted in 1998/1999; dataset references 1998 sampling year.

## Laboratory methods and quality assurance
- Sample preparation: Air dried, sieved to <2 mm; sub-sampled for ball milling (non-metallic agate).
- Digestion: Aqua regia digestion (3 g soil to 100 ml) per specified method.
- Measurement: ICP-OES (JY38plus) with high power/low flow; some samples measured by ICP-MS; calibration with matrix-matched solutions.
- Quality control: Use of Certified Reference Materials and samples from international soil exchange; traceability to NBS/CRMs (e.g., Estuarine Sediment 1646, Lake Sediment 280); batches included internal QC samples, blanks, and duplicates.
- Data handling: Analytical batches of 20 samples plus QC and blanks; limited detections below limit of detection (12 measurements across Cd, Cr, Ni).

## Data quality notes
- A minority of measurements fall below detection limits (12 observations total for Cd, Cr, Ni).
- QA procedures emphasize method verification, reference materials, and matrix-matched calibration to ensure data reliability.

## Licensing, attribution, and access
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement statement required: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”; copyright note and rights.
- Documentation and methodologies are linked (CS2000 Field Survey Handbook; associated references).

## Data provenance and references
- Related documentation and methodologies available via Countryside Survey resources.
- Key references include:
  - MASQ: Monitoring and Assessing Soil Quality in Great Britain (2002)
  - ITE Merlewood Land Classification of Great Britain (1996; 1981)
  - ITE Land Classification of Great Britain 2007 (dataset)
  - Countryside Survey UK results (2008)
- Soil metal analysis methods and broader Countryside Survey methods are described in the listed publications and CEH/NERC resources.

## Implications for Data Leaders
- Demonstrates a well-documented, governance-ready data product with clear provenance, performance notes, and attribution requirements—exemplary for data stewardship and discoverability.
- Rich metadata (land classification, environmental zones, geographic identifiers) enables cross-domain analyses and integration with other datasets (e.g., land use, pollution modules).
- Highlights the importance of robust QA/QC, traceability to certified materials, and clear data usage rights to support trustworthy analytics and dissemination.
- Provides a baseline for temporal analyses when linked with later Countryside Survey results (e.g., 2007 UK results) to assess trends in soil metal concentrations.

## Use cases and next steps
- Baseline assessment of soil metal concentrations across Great Britain for 1998/1999; potential comparisons with later surveys to identify spatial and temporal trends.
- Cross-analysis with land classification (ITE LC07) and environmental zones to explore associations between metal concentrations and land cover types.
- Support for soil quality and pollution-related research, policy evaluation, and dissemination through properly attributed publications and reports.
- Consider linking this dataset with other CS data to build a multi-year, multi-variable view of soil health and contamination.