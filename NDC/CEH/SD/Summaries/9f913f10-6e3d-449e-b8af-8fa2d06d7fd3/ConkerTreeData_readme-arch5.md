# Records of leaf damage caused by and parasitism of Cameraria ohridella in Britain in 2010 collected with a citizen science approach, plus validation of the data

## Scope and purpose
- Citizen science project (Conker Tree Science) collected national-scale data in Great Britain on the invasive horse-chestnut leaf-mining moth Cameraria ohridella Deschka & Dimic (Lepidoptera: Gracillariidae) during 2010.
- Aimed to test two hypotheses: (1) leaf damage levels on Aesculus hippocastanum leaves and (2) parasitism levels of C. ohridella larvae were greatest where the pest had been present the longest.
- Data were gathered via a project website and involved both public participants and school-based activities.

## Data collection and governance
- Involvement of over 3,500 participants across Great Britain; data submission through the project website.
- Participants reported leaf damage on an ordinal scale (0-4) during summer (1 July–15 October 2010).
- For examining parasitism, participants reared insects from infested leaves, with a team of eight trained volunteers coordinating school engagement and guiding lessons.
- Data collection included a random subset for validation and privacy-preserving measures (full location data reduced to 10 km square; location details masked).
- Data submission and curation followed a structured process with guidance to participants; some datasets were later verified by experts.

## Data products and structure
- leafdamagerecords.csv: Records of leaf damage submitted by the public.
  - Key fields include LineID, SubmissionDate, ParticipantID, LeafDamageScore (0-4), 10 km grid coordinates (Easting/Northing), ObservedYearOfArrival, ModeledYearOfArrival for 2 and 3 generations.
- parasitoidrecords.csv: Records of adult C. ohridella and parasitoids from leaves provided by participants.
  - Key fields include LineID, SubmissionDate, counts of Mines, AdultMoths, Parasitoids, OtherInsects, 10 km coordinates, VolunteerID/ParticipantID, School, and ObservedYearOfArrival, ModeledYearOfArrival (2 and 3 generations).
- validationdata.csv: Subset of data used to validate counts.
  - Key fields include LineID, VolunteerID, Source (random or extra), SchoolID, ClassID, ReportedMines/Moths/Parasitoids, TrueMines/TrueMoths/TrueParasitoids, and TrueMinotetrastichusFrontalis (where applicable).
- Location privacy: Full location data retained by participants; public release provides only 10 km square resolution.
- Supporting modeling data: Distribution modeling used Forest Research arrival data and a two-component demographic spread model (short-distance diffusion plus optional long-distance events inferred from data); models run on a 2.5 km grid with two scenarios (2 vs 3 generations per year).

## Modeling and provenance
- Observed year of arrival at 10 km squares sourced from Forest Research (with permission) and used to calibrate distribution models.
- Demographic model parameters adapted from continental Europe studies, incorporating both short-distance diffusion and evidence for long-distance dispersal.
- Modeling updates occurred at the end of each modeled generation (2007–2010), expanding presence within previously occupied grid cells.

## Data quality, validation, and limitations
- Quality statement: Counts submitted by the public via the project website were not corrected or validated for accuracy in the primary dataset.
- Validation: A random subset of samples (validationdata.csv) was blindly recounted by experts to assess accuracy; some additional samples with reported parasitoids were also validated.
- Data transformations: High counts (above 25) were binned by participants (e.g., 26–30, 31–40, etc.) and later converted to fixed values for analysis; validation data include both reported and true counts.
- Limitations and biases:
  - Counts are not corrected for observer error or misidentification in the main dataset.
  - Under-sampling in the observed distribution after 2006, requiring modeling to infer spread.
  - Privacy-preserving location reduction may affect fine-grained spatial analyses.
  - Reliance on school and volunteer-led data collection introduces potential variability in methodology and supervision.
  - Model calibration depends on available historical data and assumptions about generation counts.

## Access, usage, and attribution
- Data are presented as CSV files (leafdamagerecords.csv, parasitoidrecords.csv, validationdata.csv) with accompanying documentation and modeled distribution notes.
- Supporting materials reference data sources used under permission (e.g., Forest Research) and project funding (Natural Environment Research Council) and institutional affiliation (University of Bristol).
- Users should be mindful of the privacy reductions, data binning, and validation status when combining with other datasets or conducting fine-scale analyses.

## Implications for data stewardship
- Demonstrates a scalable approach to collecting large-scale ecological data via public participation, with explicit data governance considerations (privacy, validation, and model-informed interpretation).
- Highlights the need for clear data dictionaries, consistent metadata, and documented provenance to enable discovery, reuse, and reproducibility.
- Emphasizes balancing openness with privacy, and the value of validation datasets to quantify observer-based uncertainties in citizen science data.