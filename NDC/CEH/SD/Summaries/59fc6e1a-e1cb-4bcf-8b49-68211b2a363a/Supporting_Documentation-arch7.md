# Field surveys were conducted in Mambwe District, Eastern Province, Zambia in order to investigate the distribution and apparent density of tsetse populations.

- Overview
  - Purpose: Investigate distribution and apparent density of tsetse flies in Mambwe District, Zambia.
  - Time frame: Two field surveys conducted in 2013—cold dry season (May/June) and hot dry season (November).
  - Target species: Primarily Glossina morsitans morsitans; Glossina pallidipes detected but data rare.

- Methods
  - Sampling design
    - Transect along the Luangwa Valley from the plateau (approx. 900 m) to the valley floor near Mfuwe Airport (approx. 550 m).
    - Start: old tsetse barrier in Wazaza; followed road through Msoro to Mfuwe; ending at M'nkanya turning.
    - Fly rounds located at ~1 km intervals perpendicular to the road.
    - Each fly round length about 6 km (variation due to terrain/accessibility); stops every 200 m to sample.
  - Data collection
    - Equipment: two people with a black screen and fly nets; screens baited with phenols and acetone to increase sampling efficiency.
    - At each stop: capture any tsetse alighting on screen or personnel; identify species and count.
    - GPS coordinates recorded for each stop; sampling started at 7:00 am to coincide with peak tsetse activity.
  - Records
    - Season-specific surveys: May/June (Survey = 'One') and November (Survey = 'Two').
    - Predominant species: G. morsitans morsitans; very few G. pallidipes.

- Geographical extent
  - Longitude: 31.826 to 32.094
  - Latitude: -13.248 to -13.828

- Data structure
  - File: DDDAC_tsetse_2013.csv
  - NA denotes missing data
  - Variables
    - Code: unique observation identifier
    - Survey: 'One' (May/June) or 'Two' (November)
    - ID_Survey: observation identifier within each survey
    - BFR: fly round number
    - Stop: sampling point on each fly round
    - Latitude: decimal degrees (NA if missing)
    - Longitude: decimal degrees (NA if missing)
    - Date: date of fly round
    - Result: 1 if tsetse recorded, 0 if not
    - Count: number of tsetse recorded

- Data quality and notes
  - Missing coordinates (NA) possible for some stops
  - Temporal consistency: sampling at the same time of day across surveys
  - Focused on a single transect along a road; spatial coverage limited to surveyed route

- References
  - Ford J et al., 1959
  - Van den Bossche P & De Deken R, 2002
  - Shereni W, 1984

- GIS usage considerations
  - Import as point features with attributes (Code, Survey, ID_Survey, BFR, Stop, Date, Result, Count)
  - Use coordinates to map appearances and counts; create seasonal comparisons between Survey One and Survey Two
  - Optionally derive transect lines along the road if needed for spatial context
  - Address missing data (NA) in coordinates during analysis and visualization

- Applications
  - Assess spatial-temporal patterns of tsetse presence and abundance
  - Inform strategies for tsetse surveillance and control in the region
  - Support ecological or epidemiological studies related to tsetse distribution in Eastern Province, Zambia