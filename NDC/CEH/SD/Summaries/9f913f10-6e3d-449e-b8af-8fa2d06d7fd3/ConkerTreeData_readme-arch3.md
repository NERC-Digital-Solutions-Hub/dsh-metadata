# Records of leaf damage caused by and parasitism of Cameraria ohridella in Britain in 2010 collected with a citizen science approach, plus validation of the data.

## Overview
- National-scale citizen science project (Conker Tree Science) collected data in Britain in 2010 to assess leaf damage by Cameraria ohridella and larval parasitism.
- Two hypotheses: leaf damage levels and parasitism levels are greatest where the moth has been present the longest.
- Data collection via participants reporting via a project website; participation included school children and volunteers; data underpin modeling of species distribution and arrival timing.
- Project funded by the Natural Environment Research Council and conducted at the University of Bristol.

## Data collection and citizen science approach
- Over 3,500 participants contributed data across Great Britain.
- Leaf damage recorded on an ordinal scale (0-4) during summer 2010.
- Parasitoid and moth counts obtained by participants rearing insects from infested leaves; a subset of samples (669 counted by children and 75 with reported parasitoids) was expert-validated blindly to avoid supervision bias.
- School children involvement enhanced through trained volunteers who supervised classes but did not direct counting.
- Long-term presence data from Forest Research used to inform arrival timing; data gaps acknowledged and addressed with modeling.

## Datasets and data structure
- leafdamagerecords.csv: records of leaf damage with fields including LineID, SubmissionDate, ParticipantID, LeafDamageScore, location (Easting/Northing), and observed/modeled arrival years.
- parasitoidrecords.csv: records of leaf mines, adult moths, parasitoids, and other insects; includes Sample location, VolunteerID/ParticipantID, School, and observed vs. modeled arrival years.
- validationdata.csv: subset used to validate counts; includes true counts from experts and corresponding participant-reported counts, with fields for School/Class identifiers and source (random or extra).
- Data encoding notes:
  - Counts above 25 are binned by participants (e.g., 26-30, 31-40) and recoded to representative values (e.g., 28, 35, 45, 55, 65).
  - Location data provided at 10km squares for privacy; full coordinates otherwise available to the researchers.
  - Observed year of arrival and modeled arrival years are provided per sample.

## Quality, validation, and metadata
- Main dataset (parasitoidrecords.csv) comprises unadjusted counts from public submissions with no formal correction or validation.
- Validation data (validationdata.csv) includes a randomly selected subset for blind re-count by volunteers to assess accuracy.
- Privacy considerations lead to location anonymization (10km grid) while still enabling spatial analyses.
- Data sources include participant observations, school-led activities, and expert-validated samples; long-term arrival modeling depends on Forest Research data with permission.

## Analytical modeling and distribution
- Modeled distribution of C. ohridella used a demographic spread model parameterized from continental Europe, focusing on short-distance dispersal (diffusion) with long-distance events inferred from data rather than the model.
- Short-distance dispersal parameter: probability of presence = exp(-0.025 × d^2), where d is distance to the nearest occupied square.
- Two modeling scenarios: two generations per year and three generations per year; models run on a 2.5km grid and updated annually (end of every second or third generation).
- In updating distributions, moth presence was assumed in all sixteen 2.5km cells within a 10km grid square where it had been observed.
- Observed distribution data (2006-2010) were used to inform model updates.

## Data governance, sharing, and documentation
- Data were shared publicly through citizen science channels, with underlying data governance ensuring privacy (10km grid) and usage permissions.
- Some datasets were complemented by external data (Forest Research arrival records) with permission.
- Supporting documentation (modeled distribution and arrival details) references published methods and prior parameterizations (Gilbert et al., 2004; 2005).

## Implications for monitoring frameworks
- Demonstrates the viability of citizen science for national-scale environmental monitoring when coupled with:
  - Clear data schemas and metadata for different data types (damage scores, insect counts, arrivals).
  - Validation datasets and blind verification to quantify data quality.
  - Transparent handling of privacy (location anonymization) and data governance.
  - Use of external datasets to anchor long-term trends (arrival timing) and demographic models.
- Highlights the importance of addressing data barriers relevant to monitoring frameworks:
  - Managing data completeness and standardization across participants.
  - Providing raw vs. validated data with appropriate documentation.
  - Ensuring openness while balancing privacy and consent considerations.

## Challenges and considerations for monitoring frameworks
- Data gaps and under-sampling after 2006 necessitated modeling to infer distributions.
- Public counts require careful validation and error assessment; binning of high counts introduces measurement uncertainty.
- Ensuring metadata quality and ease of data transformation remains essential for reuse.
- Balancing public data sharing with privacy protections (location anonymization) and data governance standards.