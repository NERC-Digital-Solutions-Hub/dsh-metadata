# Method

## Objective and overview
- Investigates the distribution and apparent density of tsetse populations in Mambwe District, Eastern Province, Zambia.

## Study design and sampling period
- Two field surveys conducted in 2013: cold dry season (May/June) and hot dry season (November).
- Sampling follows standard fly-round methods for Glossina morsitans morsitans.

## Transect and sampling approach
- Transect runs from the plateau (east) down to the valley floor near Mfuwe Airport (altitude 900m to 550m).
- Route starts at old tsetse barrier in Wazaza, along the road through Msoro toward Mfuwe, ending at the M'nkanya turning.
- Fly rounds located approximately 1 km apart perpendicular to the road.
- Each fly round is about 6 km long, with stops every 200 m to sample flies.

## Field protocol
- A black screen is carried by two people with fly nets to catch tsetse landing on the screen.
- Screens baited with phenols and acetone to increase sampling efficiency.
- At each stop, any tsetse alighting on the screen or personnel is caught; species and number recorded.
- Geographic coordinates recorded for each stop using a handheld GPS.
- Sampling time standardized to 7 am to coincide with peak tsetse activity.
- Although Glossina pallidipes was sampled, very few were recorded; the dataset contains only Glossina morsitans morsitans data.

## Data management and dataset details
- Dataset available as a CSV file named DDDAC_tsetse_2013.csv.
- NA indicates data not available.

## Data structure and variables
- Code: unique observation identifier.
- Survey: 'One' for May/June survey or 'Two' for November survey.
- ID_Survey: unique identifier for observations within each survey.
- BFR: fly round number.
- Stop: sampling point on each fly round.
- Latitude: decimal degrees; NA if missing.
- Longitude: decimal degrees; NA if missing.
- Date: date of the fly round.
- Result: 1 if tsetse were recorded, 0 if not recorded.
- Count: number of tsetse recorded.

## Geographical extent
- Longitude: 31.826 to 32.094
- Latitude: -13.248 to -13.828

## Data quality and caveats
- Some missing data (e.g., NA Latitude/Longitude).
- Data primarily captures presence/absence and counts of Glossina morsitans morsitans along a fixed transect during two seasons, with sampling standardized by time of day.

## Potential data products and use for data support
- Maps of tsetse presence/absence and counts along the transect with coordinates.
- Season comparison of tsetse counts (May/June vs. November).
- Dashboards enabling self-serve exploration of location-based tsetse density.
- Data cleaning steps: address missing coordinates, validate date formats, harmonize species data (though only G. morsitans morsitans present in this dataset).
- Opportunities to combine with environmental or topographic data (altitude, proximity to road, habitat features) to model tsetse distribution.