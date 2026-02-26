# Butterfly and Lepidoptera data from a mown boundary experiment within the Stonehenge landscape, UK-1

## Overview
- Raw data sets describe behaviour and distribution of Lepidoptera (butterflies and day-flying moths) at the Stonehenge Landscape in 2012.
- Adapted from Grace Twiston-Davies’s PhD thesis on landscape connectivity and habitat restoration.
- Data focus on individual Lepidoptera flight paths, species identification, and associated vegetation and nectar resources.
- Data quality assurance included searching for outliers/anomalies using species occurrence expectations and exploratory analysis (details not shown).

## Study site and experimental design
- Location: National Trust Stonehenge Landscape within the Stonehenge World Heritage Site, Wiltshire, UK.
- Context: Long-term landscape-scale grassland restoration; chalk grassland seed sourced from Salisbury Plain and sown on ex-arable fields (2000–2012).
- Landscape composition: Chalk grassland fragments on barrows, grassland restoration fields of varying ages, semi-improved pasture, arable land, and woodland.
- Experimental setup (Seven Barrows field):
  - Two large grassland areas (40 m x 50 m) with eight 20 m survey boundaries (boundaries 1–8).
  - Four treatment boundaries at the edge of a mown area; four control boundaries in continuous grass with dummy boundaries.
  - Two blocks: sheltered (un-mown side to the west) and exposed (un-mown side to the east).
  - Distances maintained to minimise confounding effects; mown area kept ≤ 400 m²; experimental area fenced to ≤ 100 m.
  - Boundaries surveyed 24 July–23 August 2012.

## Lepidoptera surveys
- Procedure: Surveyor follows a Lepidoptera flight path within 10 m on either side of a boundary or dummy boundary.
- Observation: Each insect’s flight path observed for 3 minutes; boundary surveyed until the insect left the 20 m x 20 m area or remained stationary for >3 minutes.
- Effort: Each boundary surveyed for 20 minutes per survey period; three survey periods over five weeks, randomly sequenced to ensure balanced effort.
- Boundaries: Random order of boundaries within periods; time-of-day randomized to reduce bias.
- Target conditions: Surveys conducted under weather conditions deemed acceptable by the UK Butterfly Monitoring Scheme.

## Environmental variables
- Vegetation: Eight 0.5 m x 0.5 m quadrats per boundary (four in unmown, four in mown sides, plus corresponding control sides) to measure vegetation height and density (drop-disc method).
- Nectar resources: Number of flowering units by nectar plant families (Asteraceae, Fabaceae, Dipsacaceae); surveys at three times (19 Jul, 10 Aug, 23/24 Aug).
- Weather: Average wind speed and direction from the nearest station (Boscombe Down); cloud cover assessed visually.

## Nomenclature and data structure
- Plants: Follows Stace (2010) for British flora.
- Lepidoptera: Follows standard references; field identifications use Field Studies Council guides.
- Data columns (ButterflyMownBoundaries dataset): DATE, TEMPERATURE, WIND SPEED, WIND DIRECTION, CLOUD COVERAGE, GRID SQUARE, PLOT, SURVEY EDGE, START TIME, END TIME, SPECIES, SPECIES CODE, SEX, BEHAVIOUR, START HABITAT TYPE, END HABITAT TYPE, DIRECTION OF MOVEMENT, NOTES, NECTARING ON.
- Additional data sheets (e.g., 7_Barrows_Resources_2012) include columns for edge/control, habitat type, quadrat details, and nectar/flowering unit measurements.
- Species and plant tables provide codes and common names for Lepidoptera and flowering plants.

## Data interpretation and potential outputs
- Enables analysis of edge effects and boundary influence on Lepidoptera exit/entry behaviours (Cross, Follow, Avoid, Stay).
- Facilitates exploration of relationships between Lepidoptera flight paths and:
  - Habitat type (chalk restoration vs. arable vs. restoration edge)
  - Vegetation structure (density/height)
  - Nectar flower availability (flowering units by family)
  - Weather conditions (temperature, wind, cloud cover)
- Potential data products:
  - Interactive dashboards showing species-specific responses to boundary type and habitat.
  - Spatial maps of flight path distributions by boundary and block.
  - Summaries of behavioural frequencies by species, boundary type, and environmental covariates.

## Limitations and considerations
- Short survey window focused on peak imago abundance for select species (e.g., Maniola jurtina, Zygaena filipendulae); may not capture full seasonal dynamics.
- Boundary proximity and fencing could influence Lepidoptera responses (possible edge effects beyond the intended boundary).
- Replication is limited to two blocks and eight boundaries; spatial confounding factors (edge placement, woodlands) should be considered in analyses.

## References
- Related methodological and ecological references used to frame the study, including Pollard & Yates (1993), Ries & Debinski (2001), Rodwell (1992), Stace (2010), and others cited in the document.