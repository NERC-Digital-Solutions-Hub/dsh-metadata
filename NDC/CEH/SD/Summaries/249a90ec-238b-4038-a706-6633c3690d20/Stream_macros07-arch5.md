# Headwater stream macrophyte data 2007 [Countryside Survey] Dataset description

## Overview
- Dataset from Countryside Survey 2007 focusing on macrophytes in headwater streams.
- Purpose: record presence and extent of macrophytes along a 100 m stream reach using the Mean Trophic Rank (MTR) protocol; includes a broader plant species checklist beyond standard MTR needs.
- Data collection used tablet computers with custom software.

## Data structure and fields
- Table: STREAM_MACROPHYTES_07.csv
- Key fields:
  - SQUARE (Text): 1 km square sampling site code
  - YEAR (Text): Year of survey (CS + Yr)
  - SITE_ID (Number): Site identifier within the 1 km square
  - SURVEY_DATE (Date): Date of survey
  - PLANT_NAME (Text): Scientific name of plant
  - PROPORTION (Text): Proportion (%) cover of the 100 m stretch
  - LC07 (Text): Land classification 2007
  - LC07_NUM (Number): Numeric code for Land Class 2007
  - EZ_DESC_07 (Text): Environmental zone description
  - COUNTY07 (Text): County or equivalent
  - COUNTRY (Text): England, Scotland, or Wales
- Notes: Occurrence and abundance recorded; broader species checklist included for this dataset.

## Data collection and workflow
- Methodology: 100 m stream reach surveyed following MTR protocol.
- Enhanced scope: more extensive plant species checklist than required for standard MTR.
- Data capture: observed data recorded electronically on tablets.

## Metadata, standards and classification
- Land classification source: ITE Land Classification of Great Britain 2007 (LC07).
- Environmental zone and other geographical fields referenced to 2007 classifications.
- Structure uses 1 km square code with site IDs counted within the square.

## Access, usage, and attribution
- All Countryside Survey data must be acknowledged in any copies, publications, or presentations.
- Acknowledgement text required: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and copyright statement with “Countryside Survey © … All rights reserved.”

## Related documentation and references
- Core manuals and reports:
  - Murphy, J.; Weatherby, A. 2008 Countryside Survey. Freshwater Manual.
  - Dunbar, M. et al. 2010 Countryside Survey: Headwater Streams Report from 2007.
  - Holmes N.T.H. et al. 1999 Mean Trophic Rank: Users’ manual.
- Additional resources: Final PDFs and linked documents provided for context and methodology.

## Governance and stewardship implications
- Data standardization: Aligns with MTR protocol but includes a broader species list; ensure metadata clarifies scope and any deviations from standard MTR.
- Metadata completeness: Key fields and classifications are documented; consider maintaining explicit provenance and versioning notes.
- Attribution and licensing: Maintain explicit acknowledgement language in all downstream uses and ensure rights statements are preserved.
- Interoperability: LC07 and EZ_DESC_07 provide crosswalks to classification schemes; ensure consistency when integrating with other datasets.
- Quality assurance: The description highlights data collection methods but does not detail QC procedures; document any QC steps in metadata if managing the dataset.