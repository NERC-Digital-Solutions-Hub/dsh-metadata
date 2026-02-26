# Records of leaf damage caused by and parasitism of Cameraria ohridella in Britain in 2010 collected with a citizen science approach, plus validation of the data.

## Abstract overview
- Citizen science data collection in Great Britain (2010) for Cameraria ohridella via the Conker Tree Science project.
- Over 3,500 participants contributed national-scale records on leaf damage and parasitism to test two hypotheses about damage and parasitism relative to duration of local presence.
- Leaf damage scored on a 0–4 ordinal scale during summer 2010; parasitism data obtained by rearing and counting leaf mines, adult moths, parasitoids, and other insects.
- Schoolchildren-led activities included non-biased counting due to independent volunteer guidance.
- A subset of samples was expert-validated; long-term Forest Research data used to infer years since arrival; demographic modeling of spread used to augment observed distributions.
- Study supported by the Natural Environment Research Council and conducted at the University of Bristol.

## Data collection and citizen science workflow
- Participants submitted leaf-damage observations via the project website.
- For parasitism, participants reared insects from infested leaves and reported counts after two weeks.
- A random subset of 669 leaf-count samples and 75 parasitoid reports were subjected to expert validation.
- Use of a blinded expert assessment to reduce bias in counts.
- Additional data sources included a long-term Forest Research dataset for arrival timing and a demographic model of spread for short-distance dispersal and potential long-distance events.

## Data files and schemas
- leafdamagerecords.csv
  - LineID: reference line number.
  - SubmissionDate: observation date.
  - ParticipantID: unique participant identifier.
  - LeafDamageScore: 0–4 damage level with provided interpretation images/descriptions.
  - Easting10km, Northing10km: location coordinates at 10 km grid precision.
  - ObservedYearOfArrival, ModeledYearOfArrival3Generations, ModeledYearOfArrival2Generations: years related to arrival and modeled predictions.
- parasitoidrecords.csv
  - LineID, SubmissionDate: as above.
  - Mines, AdultMoths, Parasitoids, OtherInsects: counts at completion of the study.
  - Easting10km, Northing10km: 10 km grid location.
  - VolunteerID, ParticipantID: involvement details; School indicator and class information.
  - ObservedYearOfArrival, ModeledYearOfArrival3Generations, ModeledYearOfArrival2Generations: as above.
- validationdata.csv
  - LineID, VolunteerID, Source (random or extra), SchoolID, ClassID.
  - ReportedMines, ReportedMoths, ReportedParasitoids: counts as reported by volunteers.
  - TrueMines, TrueMoths, TrueParasitoids: counts when validated by an expert.
  - TrueMinotetrastichusFrontalis: parasitoid identification detail where applicable.
- Modeled distribution documentation
  - Observed year of arrival from Forest Research used to model predicted distribution.
  - A demographic model (from Gilbert et al.) used to simulate short-distance spread; long-distance dispersal treated as data-informed events rather than parameterized in the model.
  - Modeling performed on a 2.5 km grid; two scenarios (2 generations/year and 3 generations/year) were run.
  - Distribution updated after each second/third generation with observed distribution; moth presence assumed in all 16 cells within a recorded 10 km grid cell.

## Spatial and temporal coverage
- Temporal scope: 2010 field data collection (summer 1 July–15 October 2010); arrival timing data up to and including 2010.
- Spatial scope: Great Britain; leaf-damage data linked to 10 km grid squares; modeling grid at 2.5 km resolution to refine predicted distribution.

## Data quality and privacy considerations
- Quality statement: raw counts submitted by the public with no correction or general validation.
- Parasitoid counts are binned for higher values (e.g., 26–30, 31–40, etc.) and mapped to representative counts.
- Location data privacy: full locations withheld; data provided at 10 km grid square resolution.
- Validation: a subset of samples re-counted by experts to verify counts; additional validation data included in validationdata.csv.
- Arrival timing data sourced from an external Forest Research dataset and used with permission.

## Modeling approach
- Modeled distribution of Cameraria ohridella in 10 km squares by augmenting observed distribution with a probabilistic short-distance diffusion component (exp(-0.025 × d^2), where d is distance to nearest occupied square).
- Long-distance dispersal not explicitly parameterized in the model; potential long-range expansions inferred from data.
- Two modeling scenarios: two generations per year and three generations per year.
- Model updates occur at the end of every second or third generation, based on yearly observed distributions.

## Supporting documentation and references
- Modeled distribution details and links to Forest Research arrival data (observed year of arrival) are provided; data used with permission.
- Citations and methodological notes reference Gilbert et al. (2004, 2005) on demographic spread models and related ecological modeling approaches.

## Practical GIS considerations
- Multiple datasets with spatially explicit 10 km grid locations and 2.5 km modeling grid for distribution; suitable for creating maps of leaf damage intensity and parasitism across Britain.
- Privacy-preserving data release (coarse spatial resolution) must be considered when visualizing at finer scales.
- Data quality caveats due to citizen science provenance and binning of high-count records; validation data supports assessment of reliability.
- Modeling approach provides a framework for updating species distribution with new observations and for comparing scenarios with different generation rates.