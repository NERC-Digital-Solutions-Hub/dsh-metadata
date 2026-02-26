# Method

- Objective: Investigate the distribution and apparent density of tsetse (Glossina morsitans morsitans) in Mambwe District, Eastern Province, Zambia, using two field surveys in 2013 (cold dry season May/June and hot dry season November).

- Sampling design and area:
  - Transect runs from the plateau side of the Luangwa Valley (altitude ~900 m) down to the valley floor near Mfuwe Airport (altitude ~550 m).
  - Route starts at the old tsetse barrier in Wazaza, follows the road through Msoro toward Mfuwe, and ends at M'nkanya turning.
  - Fly rounds located approximately 1 km apart perpendicular to the road; each fly round ~6 km long (variation due to terrain/access).
  - Stops every 200 m to sample; conducted from 7:00 am to align with peak tsetse activity.

- Sampling method:
  - Black screen fly rounds carried by two people with fly nets; screens baited with phenols and acetone to increase sampling efficiency.
  - At each stop, tsetse alighting on the screen or personnel are captured; species and count recorded.
  - GPS coordinates recorded for each stop.

- Target and observations:
  - Focus on Glossina morsitans morsitans; Glossina pallidipes present but rarely recorded in this dataset.
  - Surveys conducted during two periods: May/June (Survey 1) and November (Survey 2).

- Data and data structure:
  - Dataset file: DDDAC_tsetse_2013.csv; NA indicates missing data.
  - Variables:
    - Code: unique observation identifier
    - Survey: 'One' for May/June, 'Two' for November
    - ID_Survey: unique identifier for observations within each survey
    - BFR: fly round number
    - Stop: sampling point on each fly round
    - Latitude, Longitude: decimal degrees (NA if missing)
    - Date: date of fly round
    - Result: 1 if tsetse recorded, 0 if not
    - Count: number of tsetse recorded
  - Geographic extent:
    - Longitude: 31.826 to 32.094
    - Latitude: -13.248 to -13.828

- Data quality and standardization:
  - Sampling follows established field methods for Glossina morsitans morsitans.
  - Data captured with time-standardized sampling and georeferencing to enable temporal and spatial analyses.
  - References supporting the methodology include Ford et al. (1959), Van den Bossche & De Deken (2002), and Shereni (1984).

- Relevance for environmental monitoring:
  - Provides standardized, time-stamped, georeferenced data on tsetse presence and density to assess environmental health and vector risk over time.
  - Structured format supports integration into analytic workflows and maps/dashboards for monitoring policy performance and ecological trends.