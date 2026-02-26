# Experimental design/Sampling regime

- Purpose: Social survey conducted in Puding County, China (2018) via interviews to local farmers and leaders to understand learning preferences and current KM methods.
- Language and setting: Interviews conducted in Chinese, with participants from Puding County.

## Collection methods

- Interviews were recorded and transcribed after obtaining participant consent.
- No fieldwork instruments, calibration steps, or analytical methods documented (labeled as N/A).

## Nature and units of recorded values

- Recorded data consist of verbatim interview transcripts.

## Details of data structure

- Dataset comprises 31 .rtf transcript files:
  - Chenqi_x.rtf for x = 1–7 (16–55 KB)
  - Houzhai_x.rtf for x = 1–10 (15–22 KB)
  - Jinhe_x.rtf for x = 1–8 (17–21 KB)
  - Maguan_x.rtf for x = 1–5 (15–19 KB)

## Quality control

- Not applicable or not provided (N/A).

## GIS relevance and potential visualisation

- The data are non-spatial text transcripts; not directly mappable.
- Opportunities for GIS integration:
  - Extract structured attributes (e.g., learning preferences, KM methods) via coding/text analysis.
  - Link transcripts to spatial units by village/area name (Chenqi, Houzhai, Jinhe, Maguan) to enable area-based aggregation.
  - Create a geospatial layer for Puding County areas and map thematic distributions (e.g., KM practices) derived from transcripts.
  - Potential to pair with external spatial datasets (demographics, resources) for spatial insights.

## Processing steps for GIS workflow

- Data preparation: transcribe and code transcripts into a structured dataset (fields: area, transcript_id, speaker_role, themes, etc.).
- Spatial linkage: map each area name to approximate coordinates (e.g., village centroids) or administrative boundaries within Puding County.
- GIS integration: join coded data to the spatial layer; produce maps showing distribution of learning preferences and KM methods by area.
- Quality and privacy: anonymize respondents as needed; document limitations due to lack of precise location data.

## Metadata and provenance

- Timeframe: 2018.
- Geography: Puding County, China.
- Language: Chinese.
- Data format: 31 transcript files in .rtf; filenames indicate area (Chenqi, Houzhai, Jinhe, Maguan) and sequence.