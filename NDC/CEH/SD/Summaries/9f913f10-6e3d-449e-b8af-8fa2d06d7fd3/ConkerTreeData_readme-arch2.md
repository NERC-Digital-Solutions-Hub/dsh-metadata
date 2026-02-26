# Records of leaf damage caused by and parasitism of Cameraria ohridella in Britain in 2010 collected with a citizen science approach, plus validation of the data

## Aim and context
- Investigates leaf damage and parasitism levels of Cameraria ohridella (horse-chestnut leaf-mining moth) in Britain during 2010.
- Part of the Conker Tree Science citizen science project, engaging up to about 3,500 participants nationwide.
- Tests two hypotheses: (1) leaf damage levels and (2) parasitism levels are greatest where C. ohridella has been present the longest.

## Data collection and methods
- Leaf damage data:
  - Collected in summer 2010 (1 July – 15 October) via the project website.
  - Participants recorded damage on an ordinal scale (0–4).
- Parasitoid data:
  - Participants reared insects from infested horse-chestnut leaves to assess parasitism.
  - Involvement included school children (ages 8–11) guided by eight trained volunteers; counts were recorded after a two-week period.
  - A randomly selected subset of 669 samples (plus 75 samples with reported parasitoids) was blindly assessed by experts.
- Year of arrival modeling:
  - Used a long-term Forest Research dataset to infer years of arrival in each location.
  - Addressed under-sampling after 2006 by applying a demographic model of spread (two components: short-distance diffusion and rare long-distance movements; long-distance parameter not used in the modeled distribution; data used to inform long-distance events).
  - Model run on a 2.5 km grid, tested with two (2 generations/year) and three (3 generations/year) generations.
  - The distribution was updated periodically using observed distributions, assuming presence in all 16 cells of a 2.5 km grid within an occupied 10 km square.
- Data management and ethics:
  - Data were supplied by public participants with no automatic correction or validation (except for a validation subset).
  - Location data are provided at the 10 km square level for privacy reasons.

## Data content and structure
- leafdamagerecords.csv
  - LineID, SubmissionDate, ParticipantID, LeafDamageScore (0–4 with descriptive scale), Easting10km, Northing10km, ObservedYearOfArrival, ModeledYearOfArrival3Generations, ModeledYearOfArrival2Generations.
- parasitoidrecords.csv
  - LineID, SubmissionDate, Mines, AdultMoths, Parasitoids, OtherInsects, Easting10km, Northing10km, VolunteerID, ParticipantID, School (binary), ObservedYearOfArrival, ModeledYearOfArrival3Generations, ModeledYearOfArrival2Generations.
- validationdata.csv
  - LineID, VolunteerID, Source (random or extra), SchoolID, ClassID, ReportedMines, ReportedMoths, ReportedParasitoids, TrueMines, TrueMoths, TrueParasitoids, TrueMinotetrastichusFrontalis.
- Supporting details:
  - Modeled distribution uses observed arrival data and a two-generation/three-generation scenario to estimate arrival years.
  - Location data privacy limits reporting to 10 km squares.

## Quality assurance and validation
- Data quality:
  - Parasitoid counts in parasitoidrecords.csv are binned beyond certain thresholds to preserve participant simplicity; a validation subset validates counts.
  - The validationdata.csv file contains independently counted (true) values for a random subset and extra samples to assess accuracy.
- Privacy and provenance:
  - Full location data retained by participants; only 10 km square resolution is provided publicly.
  - Observed year of arrival sourced from Forest Research with permission and used to calibrate models.
- Methodological transparency:
  - Expert blind assessment used to validate a subset of participatory counts.
  - Clear documentation of data handling and modeling assumptions.

## Supporting documentation and modeling details
- Model of C. ohridella distribution:
  - Based on a demographic spread model parameterized from continental Europe (diffusion-based short-distance spread; long-distance movements treated as random events informed by data).
  - Short-distance dispersal probability used: exp(-0.025 × d^2), where d is distance to the nearest occupied square (in km).
  - Runs on a 2.5 km grid, comparing two vs. three generations per year; distribution updated every second or third generation with observed data.
  - Modeling begins from 2006, updating through 2010; presence in 10 km squares assumed to cover all 2.5 km subcells within occupied areas.
- Supporting data sources:
  - Observed year of arrival obtained from Forest Research (with permission).
  - Data used to inform and validate the modeled distribution.

## Implications for environmental monitoring and reuse
- Demonstrates large-scale citizen science data collection for invasive species monitoring and temporal trend analysis.
- Data can be integrated with other environmental datasets to enhance monitoring value, while acknowledging:
  - Uncorrected citizen-derived counts and the need for careful validation.
  - Privacy-preserving data aggregation (10 km squares) limiting fine-scale analyses.
- Provides a framework for documenting data provenance, validation, and modeling approaches that support scrutiny of environmental health and policy performance over time.