# Method

- Purpose: Field surveys to investigate the distribution and apparent density of tsetse populations in Mambwe District, Eastern Province, Zambia.
- Surveys: Two campaigns in 2013 — May/June (cold dry season) and November (hot dry season).
- Target species: Glossina morsitans morsitans (G. pallidipes present but rarely recorded; dataset focuses on G. morsitans morsitans).

## Study Design and Sampling Methods

- Transect route: From the plateau (east Luangwa Valley, ~900 m) down to the valley floor near Mfuwe Airport (~550 m), starting at the old tsetse barrier in Wazaza, following the road through Msoro to Mfuwe, ending at M'nkanya turning.
- Fly rounds: Located approximately 1 km apart perpendicular to the road.
- Round length: Each fly round ~6 km (variable due to terrain/accessibility); sampling stops every 200 m.
- Sampling gear: Black screens carried by two people with fly nets; screens baited with phenols and acetone to increase sampling efficiency.
- Time of sampling: Conducted at the same time of day each day, starting at 7 am to align with peak tsetse activity.
- Species capture: Tsetse alighting on the screen or personnel captured; species and count recorded at each stop.

## Data Collected and Structure

- Dataset format: CSV file named DDDAC_tsetse_2013.csv.
- Key variables:
  - Code: unique observation identifier
  - Survey: 'One' for May/June survey, 'Two' for November survey
  - ID_Survey: unique identifier within each survey
  - BFR: fly round number
  - Stop: sampling point on each fly round
  - Latitude / Longitude: geographic coordinates (decimal degrees; NA indicates missing)
  - Date: date of fly round
  - Result: 1 if tsetse recorded, 0 if not
  - Count: number of tsetse recorded
- Data quality notes:
  - NA indicates data not available in the corresponding cell
  - Latitude/Longitude may contain missing values for some stops

## Geographical and Temporal Coverage

- Geographical extent:
  - Longitude: 31.826 to 32.094
  - Latitude: -13.248 to -13.828
- Temporal scope: Data collected during two 2013 field campaigns (May/June and November)

## Data Quality, Limitations, and Governance Considerations

- Focus: Predominantly G. morsitans morsitans; very few Glossina pallidipes recorded.
- Field variability: Fly rounds length and accessibility varied with terrain, potentially affecting sampling uniformity.
- Data completeness: Some coordinates and data fields may be missing (as indicated by NA).
- Metadata implications for data stewards:
  - Clear identification of data collection methods, sampling intervals, and GPS-based locations supports discovery and re-use.
  - The dataset would benefit from explicit metadata on coordinate reference system (decimal degrees is stated, but the CRS is not explicitly specified).
  - Documentation of data provenance (who collected, when, and under what conditions) would aid governance and reproducibility.