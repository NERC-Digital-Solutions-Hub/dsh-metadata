# raw data sets on the behaviour and distribution of Lepidoptera (butterflies and day flying moths) at the Stonehenge Landscape in 2011

## Overview
- Raw data sets documenting Lepidoptera behaviour and distribution at the Stonehenge Landscape in 2011, adapted from Grace Twiston-Davies’ PhD thesis (2014).
- Data include Lepidoptera flight paths, boundary boundary-crossing behaviours, and botanical context (flowering units and percent cover in quadrats).
- Data quality checks conducted to identify outliers/anomalies using species occurrence expectations; no data are shown here.

## Study site and sampling design
- Location: Stonehenge World Heritage Site, Wiltshire, UK; former arable land managed for chalk grassland habitat creation.
- Landscape: four chalk grassland fragments (Full-moon Bank, Luxenborough Bank, Winterbourne Stoke Group, Fargo Barrow) within the Stonehenge Landscape estate.
- Boundary-based sampling: fourteen survey boundaries (20 m x 20 m) placed on fragment boundaries with adjacent land cover (arable or grassland restoration). Controls surveyed in central fragment areas or adjacent land cover, with dummy boundaries for comparison.
- Boundary setup: two western and two eastern boundaries for north-south fragments; Fargo Barrow had two boundaries (west and north) due to small size.
- Survey area and protocol: 20 m x 20 m survey plots centered on the boundary; markers and a 10 m grid used to estimate butterfly positions and flight paths.

## Lepidoptera surveys and data collection
- Survey period: May to July; conducted 10:00–16:00, with attempts to sample at different times of day.
- Protocol: 3-minute flight-path observations per individual; end conditions included stationary for >3 minutes or exit from survey area (>20 m from edge).
- Replication: each boundary surveyed across three occasions (May, June, July) with equal effort on chalk grassland fragment side and adjacent land cover.
- Behaviour categories (assigned at exit edge):
  - Crossing, Following, Avoiding, Staying (if flight path too convoluted or did not exit area).
- Pseudoreplication mitigation: alternate species/sex for each flight path; ~15 days between replicates per site; no capture/mark-recapture performed.
- Weather: surveys conducted under conditions deemed acceptable by the UK Butterfly Monitoring Scheme (Pollard & Yates, 1993).

## Data collection: vegetation and nectar resources
- Vegetation: eight 0.5 m x 0.5 m quadrats per boundary (four on each side) to measure vegetation height/density (via drop disc method) and percent bare ground.
- Nectar resources: counts of flowering units and tallies by nectar plant families (Asteraceae, Fabaceae, Dipsacaceae). Botanical data collected on two occasions between May and August.
- Meteorological context: average wind speed and direction recorded from the Boscombe Down weather station (6.5 km away, nearest hourly data).

## Data structure and variables
- Lepidoptera data (DATA Lepidoptera Behaviour):
  - Key fields include: DATE, TEMP, WIND SPEED, WIND DIRECTION, Cloud cover, REP (replicate 1–3), MATRIX TYPE (Grassland restoration or Arable), LOCATION, SURVEY (Edge boundary or Control), SURVEY TYPE (Chalk/Restoration/Arable/Edge), SIDE OF LOCATION, SHELTERED/EXPOSED, START TIME, END TIME, SPECIES, SPECIES CODE, SEX, BEHAVIOUR (Avoid, Follow, Cross, or described as Staying), HABITAT TYPE START/END, MOVEMENT DIRECTION, NOTES.
- Plant/nectar resource data (DATA Resources Behaviour):
  - Key fields include: DATE, LOCATION, REP, SHELTERED/EXPOSED, WEST/EAST/CENTRE, HABITAT TYPE, SIDE OF TRANSECT, QUADRAT NO., DROP DISC, BARE GROUND, DEAD VEG, and for resources: SPECIES, SPECIES CODE, PERCENTAGE/COVER, NUMBER OF FLOWERING UNITS, etc.
- Data dictionaries/tables accompany the dataset, including:
  - Key to Lepidoptera and flowering plant species with scientific/common names and abbreviated species codes.
  - Tables listing Lepidoptera species surveyed at Stonehenge Landscape (codes and common names).
  - Tables listing flowering plant species (codes and common names).

## Nomenclature and data codes
- Plant nomenclature follows Stace (2010); Lepidoptera nomenclature follows Langmaid et al. (1989) and Heath & Emmet (1985); field identifications rely on standard field guides.
- Abbreviated species and plant codes are used in data sheets (e.g., Ads.sta for Adscita statices, Pie.bra for Pieris brassicae, etc.).
- Location codes for boundaries and transects (e.g., WSG, Fargo, Full, Lux) and habitat context (Chalk, Restoration, Arable; Chalk/Boundary/Control).

## Data quality and limitations
- Quality assurance included searching for outliers and anomalies via related species expectations and exploratory analysis; specific results are not shown.
- No capture/recapture means potential pseudoreplication addressed only by rotating species/sex across flight paths and ensuring time between replicates.
- Weather and field conditions were standardized to accepted survey standards, but some variability in microclimate and fragment size may influence behavior.

## References
- Hardy et al. 2007; Heath & Emmet 1985; Langmaid et al. 1989; Pollard & Yates 1993; Ries & Debinski 2001; Stace 2010; Stewart et al. 2001; and related field guides for Lepidoptera and flora.