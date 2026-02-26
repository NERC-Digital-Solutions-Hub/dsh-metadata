# Headwater stream macrophyte data 2007 [Countryside Survey] Dataset description

## Overview
- Dataset describing macrophyte presence and extent in headwater streams from the Countryside Survey 2007.
- Data owned by NERC - Centre for Ecology & Hydrology (CEH).
- Collected using the Mean Trophic Rank (MTR) protocol with an expanded plant species checklist.
- Fieldwork conducted in 100 m stream reaches; data captured on tablet computers with custom software.

## Data collection and methods
- Protocol: Standard MTR method (Holmes et al. 1999) for presence and abundance of macrophytes in a 100 m reach.
- Scope: More extensive plant species checklist than required for typical MTR use.
- Data capture: Tablet-based recording during survey.

## Dataset structure (STREAM_MACROPHYTES_07.csv)
- SQUARE: 1 km square sampling site code (text).
- YEAR: Year of survey (text).
- SITE_ID: Site identifier (numeric).
- SURVEY_DATE: Date of survey (date).
- PLANT_NAME: Scientific name of plant (text).
- PROPORTION: Proportion (%) of the 100 m stretch covered by the plant (text).
- LC07: Land class 2007 (text); LC07_NUM: Land class 2007 (numeric code).
- EZ_DESC_07: Environmental zone (text).
- COUNTY07: County (or council area) (text).
- COUNTRY: England, Scotland, or Wales (text).

## Usage and citation notes
- Data use requires clear acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Countryside Survey © data rights apply; all copies and outputs (publications, presentations) must include the acknowledgement.
- Related documentation and context:
  - Murphy, J.; Weatherby, A. 2008. Countryside Survey. Freshwater Manual.
  - Dunbar, M. et al. 2010. Countryside Survey: Headwater Streams Report from 2007.
  - Holmes N.T.H. et al. 1999. Mean Trophic Rank: A users' manual.
- Access/where to read more:
  - CS Headwater Streams Report from 2007 (online resource).
  - CEH/NERC datasets and documentation referenced in the accompanying materials.

## Related considerations for data support
- Visibility and reuse: Ensure outputs are promoted for wider sharing and re-use.
- Data quality: Verify consistency between the expanded plant checklist and standard MTR records; ensure consistent interpretation of PROPORTION values and land class codes.
- Data integration: Consider linking SQUARE/SITE_ID with other Countryside Survey tables for broader analyses (e.g., cross-referencing environmental zones and land classifications).
- Licensing and attribution: Adhere to the CS data acknowledgment and copyright notice on all outputs.