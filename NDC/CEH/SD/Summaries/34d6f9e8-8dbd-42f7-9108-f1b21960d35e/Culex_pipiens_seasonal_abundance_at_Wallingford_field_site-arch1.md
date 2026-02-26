Seasonal abundance of Culex pipiens at the CEH Wallingford field site (2015)

## Overview
- Dataset documenting seasonal abundance of Culex pipiens life stages (eggs, larvae, pupae, adults) at the CEH Wallingford field site in 2015.
- Immature stages monitored three times per week (March–October 2015); adults monitored four times per week (April–October 2015).
- Includes environmental context: water temperature data and precise field-site locations.

## Experimental design and sampling regime
- Immature sampling
  - Four 450 litre circular water butts located within ~20 yards of each other.
  - Butt 1 & 2: exposed with some north-side cover; direct sunlight most of the day.
  - Butt 3: more sheltered; direct sunlight until late afternoon.
  - Butt 4: sheltered under a tree; direct sunlight only in the morning.
  - Hay infusion: 2 kg hay in each butt from January to March; removed after March.
  - Temperature: HOBO surface water temperature logger in each butt, hourly.
  - Egg rafts: counted at 10 am on Mon/Wed/Fri from 2 March–5 October 2015.
  - Larvae/pupae sampling: 500 ml dips from north/south/east/west edges (not the middle); counts for 1st/2nd instar larvae (L1/2), 3rd/4th instar larvae (L3/4), and pupae.
  - Handling: large counts photographed; counts performed on computer (Microsoft Paint) and samples returned to butts to avoid removal effects.
  - Identification: monthly sampling of 4th instar larvae for species identification via microscopy; larvae killed with boiling water before exam.

- Adult sampling
  - Four John W. Hock Miniature Downdraft Blacklight (UV) traps baited with dry ice.
  - Run nightly from 14 April to 2 October; 5 consecutive empty collections ends the period.
  - Frequency: four traps run four nights per week (Mon–Thu) overnight (1700–0900).
  - Trap locations: around the water butts (distance ~80–200 m from water).
  - Post-collection: adults frozen and identified to species in the lab; males not recorded.

- Site and instruments
  - Field site: CEH Wallingford (coordinates provided in the document).
  - Weather context: adjacent CEH weather station referenced.

## Nature and units of recorded values
- Egg abundance: counts of egg rafts by butt and date.
- Larval and pupal abundance: counts by date and butt, with larval stage split (L1/2 vs L3/4) and “larva” vs “pupa” categories.
- Adult abundance: counts of adult female Cx. pipiens (and other species) by trap and date; no male data.
- Temperature: hourly water temperature (°C) per butt and date/time.

## Data structure and files
Six CSV files:
- Egg_abundance_2015_Wallingford.csv
  - Columns: Date, Butt n (1–4); egg raft counts.
- Larval_abundance_2015_Wallingford.csv
  - Columns: Date; Corner/edge indicators (N/E/S/W); L1/2 counts; L3/4 counts.
- Pupal_abundance_2015_Wallingford.csv
  - Similar structure to larval data; includes pupal counts by date and butt.
- Adult_abundance_2015_Wallingford.csv
  - Columns: Date, Location (trap), Cx. pipiens (adult female count), other species counts (e.g., Cs. annulata, Ae. Geniculatus); NA for unavailable traps.
- Larval_identification_2015_Wallingford.csv
  - Details of 4th instar identifications: dates of identification, number identified, how many were Cx. pipiens, and butt origins.
- Water_temperatures_2015_Wallingford.csv
  - Columns: Date, Time, Butt (butt identifier), Temperature (°C).

## Quality control and data processing
- Larval/pupal counts validated by cross-checking photo-based counts with direct counts on the first two sampling days; estimates were consistent.
- Specimens identified via microscopy in the laboratory; standard dissection and microscopy protocols referenced.

## Data usefulness and potential analyses
- Enables time-series analysis of life-stage dynamics (eggs, larvae, pupae, adults) across multiple microhabitats.
- Opportunities to correlate stage abundances with micro-environmental conditions (water temperature) and trap locations/distances from the breeding site.
- Supports development of predictive models for Cx. pipiens abundance and potential risk assessments for vector dynamics in similar settings.
- Data granularity allows exploration of spatial variation among the four butts and temporal variation across the breeding season.