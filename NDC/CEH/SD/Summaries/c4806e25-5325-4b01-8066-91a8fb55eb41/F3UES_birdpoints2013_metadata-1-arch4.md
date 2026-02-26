# F3UES_birdpoints2013 data description

- Overview
  - Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project within the Biodiversity and Ecosystem Service Sustainability (BESS) framework.
  - Aims to characterize variation in breeding bird fauna across urban forms in Bedford, Luton, and Milton Keynes, focusing on green space vs. built (sealed) cover.
  - Also investigates birds detectable during times of day when people are more active, recording accompanying human activity during observation periods.

- Survey organisation
  - Design and implementation led by Gavin Siriwardena and Kate Plummer of the British Trust for Ornithology (BTO).
  - Contact details provided for the two researchers and BTO address.

- Survey methods
  - Bird surveying: point count method at predefined survey points; 6–7 visits per tile between May and August 2013.
  - Time of day: two morning visits (06:00–10:00) for morning abundances; remaining visits (May–Aug) 10:00–18:00 for afternoon abundances.
  - 10-minute counts per point; during approach, birds within 10 m recorded; then a 10-minute observation with birds recorded in defined distance bands (0–20 m, 20–40 m, 40–60 m, 60–100 m, 100–200 m) and in flight; singing vs non-singing recorded separately.
  - Best estimate recorded if total present differs from sum of counts.
  - Survey location: 116 tiles (500 m × 500 m) in Bedford, Luton, and Milton Keynes, selected via stratified sampling; four survey points per tile, ≥200 m apart and ≥100 m from tile edges; some points inaccessible and excluded.
  - Surveying people: observers counted people within 200 m of the point, categorized by activity type (e.g., children, dog walking, working).
  - Other species: opportunistic, record mammals and butterflies near the survey point; not a formal aim but entered into the dataset.
  - Survey conditions recorded: start time, Beaufort wind, rainfall, cloud cover, visibility, noise level (affecting detection).
  - Data handling: multiple inputters digitized, followed by error checking and validation.

- Data description
  - The dataset FU3UES_birdpoints2013.zip contains two dataframes:
    - Bird observations dataframe (FU3ES_birdpoints2013_obsdata.csv): records per 10-minute point count, with a unique point count id (pcid) and species-specific counts across time segments, distance bands, and singing versus non-singing status.
    - Survey details dataframe (FU3ES_birdpoints2013_surveydata.csv): contains contextual information for each point count (city, observer, tile, visit, point, month, time of day, date, start time, and environmental/observer variables) plus counts of people by category and opportunistic counts of other taxa.
  - Key identifiers: pcid (unique point count id) used to merge the two dataframes; NA indicates missing data.
  - Example variables (bird observations dataframe): spcode (2-letter BTO species code), species (common name), counts across mins 1–2, 3–4, 5–6, 7–8, 9–10 for various distance bands (20 m, 40 m, 60 m, 100 m, 200 m) and for singing/non-singing and in flight; bestest (best estimate) flag.
  - Example variables (survey details dataframe): city, observer, tile, visit, point, month, tod (time of day: am/pm), date, time, wind, rain, cloud, vis, temp, noise; counts for different people categories (children, commuting, cycling, dogwalking, etc.); opportunistic counts for butterflies and mammals.

- Supporting data and glossary
  - Supporting tile locations: F3UES_birdsurvey_tile_locations.csv provides tile coordinates (OSGB 1936) with tile id, city, easting, and northing.
  - Glossary of species: Table 4 provides a mapping of BTO two-letter codes to species names (e.g., BT Blue Tit, Pheasant, Blackbird, etc.), including an entry for feral/hybrid mallard and goose codes.
  - Notes on data structure: two dataframes can be merged on pcid to link observation data with survey conditions and contexts.

- Data access and usage notes
  - Data are provided for the 2013 survey period (May–August 2013) across 3 urban areas.
  - Data include an extensive set of count variables by time, distance, and singing status, enabling analysis of detection probability and abundance in relation to urban form and human activity.
  - Access considerations: some survey points may be missing due to inaccessibility; some fields are opportunistic (e.g., mammals, butterflies) and not part of the core survey aims.
  - Data quality: multiple inputters involved with subsequent error checking and validation; a clear identifier structure allows robust merging and analysis.