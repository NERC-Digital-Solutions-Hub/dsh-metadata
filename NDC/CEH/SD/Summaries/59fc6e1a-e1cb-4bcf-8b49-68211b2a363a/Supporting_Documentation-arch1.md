# Method

## Study aim and context
- Field surveys in Mambwe District, Eastern Province, Zambia (2013) to investigate distribution and apparent density of tsetse populations.
- Two seasonal surveys: cold dry season (May/June) and hot dry season (November) in 2013.
- Focus on Glossina morsitans morsitans; Glossina pallidipes were present but very few.

## Field sampling design
- Sampling transect from the plateau region of the eastern Luangwa Valley (altitude ~900 m) down to the valley floor near Mfuwe Airport (altitude ~550 m).
- Start at the old tsetse barrier in Wazaza; follow the road via Msoro to Mfuwe; end at the M'nkanya turning.
- Fly rounds located approximately 1 km apart perpendicular to the road.
- Each fly round ~6 km long; stops every 200 m to sample (with some variation for terrain/accessibility).
- Equipment: black screen carried by two people with fly nets; screens baited with phenols and acetone to increase sampling efficiency.
- Sampling time: 7 am each day to align with peak tsetse activity.

## Data collection protocol
- At each stop, tsetse alighting on the screen or on personnel were caught; species and count recorded.
- Geographic coordinates recorded for each stop using handheld GPS.

## Data specifics and structure
- Dataset name/file: DDDAC_tsetse_2013.csv.
- Data quality notes: NA indicates missing data.
- Key variables:
  - Code: unique observation identifier
  - Survey: "One" for May/June, "Two" for November
  - ID_Survey: unique identifier within each survey
  - BFR: fly round number
  - Stop: sampling point on each fly round
  - Latitude / Longitude: decimal degrees (NA if missing)
  - Date: date of the fly round
  - Result: 1 if tsetse were recorded, 0 if not
  - Count: number of tsetse recorded

## Geographic extent
- Longitude: 31.826 to 32.094
- Latitude: -13.828 to -13.248

## Data access and notes for analysis
- Data derived from field sampling along the transect with GPS coordinates enabling spatial analyses.
- The dataset supports presence/absence and counts by stop, fly round, and survey season, enabling seasonal comparisons and transect-based density assessments.