# Records of leaf damage caused by and parasitism of Cameraria ohridella in Britain in 2010 collected with a citizen science approach, plus validation of the data.

## Aim and scope
- Investigates leaf damage and parasitism by Cameraria ohridella in Britain during 2010 using a citizen science approach (Conker Tree Science project).
- Tests two hypotheses: (1) leaf damage levels are greatest where C. ohridella has been present the longest; (2) larval parasitism levels are greatest where presence has persisted longer.
- Data collected nationally across Great Britain; data submission via a dedicated project website.

## Methods and data collection
- Leaf damage data
  - Over 3,500 participants submitted observations of leaf damage on horse-chestnut trees (Aesculus hippocastanum).
  - Damage recorded on an ordinal scale from 0 to 4 during summer (1 July – 15 October 2010).
- Parasitoid data
  - School children (ages 8–11) and volunteers collected data by rearing parasitoids from leaves infested with C. ohridella.
  - Participants counted leaf mines, adult moths, parasitoids, and other insects after a two-week period.
  - A team of eight trained volunteers led lessons in schools; volunteers provided non-directive guidance to avoid bias.
  - A randomly selected subset of 669 samples (plus 75 samples with reported parasitoids) was blind-validated by an expert.
- Presence and spread context
  - Long-term presence data for arrival timing obtained from Forest Research, used with permission.
  - Demographic model of spread (two components: short-distance diffusion and rare long-distance movements) used to model predicted year of arrival.
  - Models run on a 2.5 km grid, with two and three generations per year, updating distributions as new observed data became available (2006–2010).
- Project support
  - Funded by the Natural Environment Research Council (NERC); conducted at the University of Bristol, UK.

## Datasets and data structure
- leafdamagerecords.csv
  - LineID, SubmissionDate, ParticipantID
  - LeafDamageScore (0–4) with standardized illustrations/descriptions
  - Easting10km, Northing10km: location at 10 km grid resolution
  - ObservedYearOfArrival, ModeledYearOfArrival3Generations, ModeledYearOfArrival2Generations
- parasitoidrecords.csv
  - LineID, SubmissionDate
  - Mines, AdultMoths, Parasitoids, OtherInsects: counts at start and end of study
  - Easting10km, Northing10km
  - VolunteerID, ParticipantID
  - School (binary), plus ObservedYearOfArrival, ModeledYearOfArrival3Generations, ModeledYearOfArrival2Generations
- validationdata.csv
  - LineID, VolunteerID
  - Source (random or extra), SchoolID, ClassID
  - ReportedMines, ReportedMoths, ReportedParasitoids (counts with binning for high values)
  - TrueMines, TrueMoths, TrueParasitoids (expert-validated counts)
  - TrueMinotetrastichusFrontalis (parasitoid species count when applicable)
- Supporting documentation
  - Modeled distribution details and methodology
  - Observed vs modeled arrival data; 2.5 km grid approach
  - Original sources for model parameters (Gilbert et al., 2004; 2005)

## Quality assurance, validation, and limitations
- Quality statement
  - Data are raw counts submitted by the public with no initial correction or validation (except targeted validation samples).
  - Parasitoid counts are binned in the public submission; a subset was validated against expert counts.
  - Location data were provided at 10 km grid for privacy reasons.
- Validation
  - Random subset of 669 samples plus 75 additional samples used for verification of counts.
  - Validation data include true counts from expert assessments.
- Data limitations and biases
  - Under-sampling of C. ohridella range after 2006; modeling incorporated observed distribution and a demographic spread model.
  - Absence of precise long-distance dispersal parameter in modeled distribution; long-distance events inferred from data.
  - Public, non-random sampling may introduce biases; privacy constraints reduce spatial precision.
  - Data quality varies by participant and requires careful interpretation for fine-scale analyses.

## Modeling, provenance, and governance
- Modeled year of arrival
  - Based on Forest Research arrival data and a demographic spread model, augmented with short-distance diffusion and (informally) long-distance events.
  - Model run for 2 and 3 generations per year on a 2.5 km grid; annual updates using observed data up to 2010.
- Data provenance and reuse
  - Data originate from a citizen science project with volunteer validation and expert oversight on a subset.
  - Full data and metadata are accompanied by documentation describing data sources, processing steps, and modeling assumptions.
- Privacy and dissemination
  - Location data blurred to 10 km squares to protect privacy; project data shared under permissions associated with the contributing organizations.

## Key takeaways for data leaders
- Demonstrates value of large-scale citizen science for ecological monitoring and hypothesis testing, with clear protocols for data collection, validation, and modeling.
- Highlights the importance of multi-layer data governance: raw public submissions, targeted expert validation, privacy-preserving location data, and transparent modeling assumptions.
- Shows how to couple crowdsourced presence data with a demographic spread model to estimate arrival timing and spatial distribution over time.
- Underlines need for supporting documentation and metadata (data structure, field definitions, and transformation rules) to enable reuse and cross-study comparability.
- Emphasizes trade-offs between data richness and quality control, and the role of validation datasets in strengthening confidence in public-sourced ecological data.