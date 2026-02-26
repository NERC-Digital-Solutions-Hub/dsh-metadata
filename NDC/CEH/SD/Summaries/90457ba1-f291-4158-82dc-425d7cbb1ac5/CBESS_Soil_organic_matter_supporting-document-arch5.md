# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) soil organic matter content from three soil depths on saltmarsh sites at Morecambe Bay and Essex

## Overview
- Dataset documenting soil organic matter content (LOI method) from three depths (0–10 cm, 10–20 cm, 20–30 cm) at saltmarsh sites in Essex and Morecambe Bay.
- Field campaign conducted in Winter and Summer 2013; Essex winter samples collected in an additional window (2–6 March 2013).
- Staff responsible: Hilary Ford.
- Purpose aligned with CBESS goals to support understanding of coastal biodiversity and ecosystem services.

## Location and sampling context
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS); a third site is listed as West Plain (WP) in the dataset.
- Site descriptions reflect contrasting soil types (clay in Essex; sandy in Morecambe Bay) and differing inundation, creek structure, and vegetation.
- Grazing regimes differ by site: Essex sites heavily grazed by over-wintering Brent geese; Morecambe Bay sites heavily grazed by sheep with additional pink-footed geese grazing; one site lightly grazed.
- Location coordinates are provided for each site.

## Methods and measurement
- Measurement: soil organic matter (%), assessed via Loss-on-Ignition (LOI) from bulk density samples.
- Sampling apparatus: bulk density rings (3.1 cm height, 7.5 cm diameter) used to extract samples at three depths within each quadrat.
- Depths: 0–10 cm, 10–20 cm, 20–30 cm (subject to how OM variables are labeled in the dataset).
- Sample processing: soils dried at 105°C for 72 hours; a sub-sample dried at 375°C for 16 hours to determine OM percentage of dry soil.
- Calibration procedures: not specified.
- Data quality control: data checking procedures noted but not described in detail; calibration procedures listed as None.

## Data structure and formats
- File format: Excel workbook.
- Data completeness: NA cells indicate missing data.
- Dataset fields (highlights):
  - Row Number (nominal sort order)
  - Season (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A: 1 m; B: 1–10 m; C: 10–100 m; D: 100–upper limit)
  - OM_10-20 (OM at 0–10 cm vs 10–20 cm depth; notation in dataset)
  - OM_20-30 (OM at 20–30 cm depth)
- Metadata notes: dataset includes site descriptions, habitat context, and field descriptions to support interpretation of OM measurements.

## Data quality, provenance, and limitations
- Provenance: records from a defined field campaign with explicit site-level context and sampling windows.
- Data quality notes: explicit QA procedures are acknowledged but not detailed; no calibration procedures reported.
- Potential limitations:
  - Some ambiguity in field naming (e.g., OM_10-20 versus depth labeling) requiring careful interpretation during reuse.
  - Data provided in Excel format, which may necessitate additional metadata or conversion for machine-actionable use.
  - Temporal alignment across sites varies due to differing sampling windows (e.g., Essex winter samples collected in March 2013).

## Access, reuse, and stewardship considerations
- Accessibility: provided as an Excel workbook; no repository or license information specified.
- Reuse considerations:
  - Ensure comprehensive metadata and a data dictionary accompany the dataset for interoperability.
  - Verify coordinate reference system and units; confirm depth definitions align with user expectations.
  - Maintain data provenance by preserving original measurement methods (LOI, bulk density rings) and sample processing steps.
  - Consider publishing a machine-readable metadata file to complement the Excel workbook and enable indexing in data portals.
- Updates and maintenance: establish a clear process for documenting updates or corrections and for versioning the dataset.

## Recommendations for Data Stewards
- Create or attach a detailed data dictionary clarifying column names, units, and depth definitions to prevent misinterpretation.
- Document coordinate reference system, site coordinates, and any GPS-derived positions used.
- Include provenance metadata (who collected data, when, at what site) and a brief methods appendix describing LOI and sample processing steps.
- Consider providing a parity of formats (e.g., CSV/JSON alongside Excel) to improve machine readability and long-term preservation.
- Implement data quality checks and record QA outcomes (e.g., missing data notes, outlier handling) to accompany the dataset.
- Ensure licensing and data usage rights are explicit to facilitate sharing and reuse within the CBESS and broader research communities.