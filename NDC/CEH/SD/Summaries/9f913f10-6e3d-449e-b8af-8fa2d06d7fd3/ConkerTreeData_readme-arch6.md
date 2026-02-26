# Records of leaf damage caused by and parasitism of Cameraria ohridella in Britain in 2010 collected with a citizen science approach, plus validation of the data

- Aim and scope
  - Investigate leaf damage and parasitism of Cameraria ohridella in Britain (2010) using a citizen science approach.
  - Test two hypotheses: (1) leaf damage levels on horse-chestnut (Aesculus hippocastanum) are greatest where the pest has existed the longest, and (2) parasitism levels of C. ohridella larvae are highest where the pest has been present longest.
  - Data collection conducted via the Conker Tree Science project; participants reported results through the project website.

- Data collection and participants
  - Over 3,500 participants contributed data at a national scale.
  - Leaf damage recorded on an ordinal 0–4 scale during summer 2010 (1 July – 15 October).
  - Parasitism assessment: participants reared larvae from infested leaves to count leaf mines, adult moths, parasitoids, and other insects; targeted school children (ages 8–11) with eight trained volunteers coordinating school activities.
  - Randomly selected subset retained for expert validation: 669 samples for general counts; 75 samples specifically for parasitoid counts.
  - Volunteers conducted counts without direct guidance to avoid bias; efforts supported engagement and public participation.

- Data collection design, timing, and modeling
  - Observational data aligned with the moth’s first generation in 2010; annual timeframe for data submission and rearing activity.
  - Location data contributed by participants; privacy preserved by providing only 10-km square resolution.
  - Long-term Forest Research data used to estimate the year of arrival at each location.
  - Modeled distribution built using a demographic spread model parameterized from continental Europe, incorporating short-distance diffusion and optional long-distance dispersal (not used to create the modeled distribution, but allowed for inferred range expansion). The model was run on a 2.5-km grid with two and three generations per year, updating distributions with observed presence from 2006–2010.

- Data quality and validation
  - Quality statement: public-submitted counts with no general correction or validation; parasitoid counts were binned for some entries (e.g., 26–30, 31–40, etc.) and converted to representative values.
  - A validation dataset (validationdata.csv) contains a randomly selected subset recounted by experts to assess count accuracy.
  - Full location data is provided at 10-km grid resolution to protect privacy.
  - Observed year of arrival and modeled arrival years (for 2 and 3 generations) accompany the records.

- Data files and schema
  - leafdamagerecords.csv: includes LineID, SubmissionDate, ParticipantID, LeafDamageScore (0–4 with provided guidance), Easting10km, Northing10km, ObservedYearOfArrival, ModeledYearOfArrival3Generations, ModeledYearOfArrival2Generations.
  - parasitoidrecords.csv: includes LineID, SubmissionDate, Mines, AdultMoths, Parasitoids, OtherInsects, Easting10km, Northing10km, VolunteerID, ParticipantID, School, and ObservedYearOfArrival, ModeledYearOfArrival3Generations, ModeledYearOfArrival2Generations.
  - validationdata.csv: includes LineID, VolunteerID, Source (random or extra), SchoolID, ClassID, ReportedMines, ReportedMoths, ReportedParasitoids, TrueMines, TrueMoths, TrueParasitoids, TrueMinotetrastichusFrontalis.

- Modeling and supporting documentation
  - Modeled distribution relies on observed year of arrival from Forest Research and a demographic spread model (short-distance diffusion; long-distance moves considered via data-informed expansion). Model runs on a 2.5-km grid; two scenarios (2 vs 3 generations/year) were explored.
  - Documentation references include the Forest Research data source and prior Gilbert et al. (2004, 2005) ecological modeling work informing the diffusion parameterization.

- Usage, applications, and dissemination
  - Data enable analysis of spatial and temporal patterns in leaf damage and parasitism, and validation of model predictions against observed data.
  - Suitable for researchers and practitioners interested in citizen science data quality, data fusion (field observations with modeled distributions), and applications in urban forestry and invasive pest management.
  - Supports development of self-service data products and visualization for broader use and re-use, with careful attention to privacy-protecting location data.