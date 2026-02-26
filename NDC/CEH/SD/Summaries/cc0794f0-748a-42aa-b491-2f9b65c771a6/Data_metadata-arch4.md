# Multiple adaptive and non-adaptive processes determine responsiveness to heterospecific alarm calls in African savannah herbivores

- The document describes a multi-method ecological study on vigilance, predator responses, and alarm-call reactions among savannah herbivores, with data organized into four primary datasets and a species-count dataset.

## Purpose and scope
- Quantifies vigilance behavior, responses to predator models, and reactions to heterospecific alarm calls.
- Assesses relative abundance and grouping patterns across three study plains over multiple censuses.
- Provides detailed datasets to enable cross-species comparisons and meta-analysis of alarm-call responsiveness.

## Datasets and key variables

- Data_VigilanceBehaviour
  - Purpose: quantify vigilance rates within monospecific foraging groups.
  - Key fields:
    - Species: focal species identity
    - NumberHeadUps: mean number of head-raises per individual
    - VigilancePerMinute: mean time spent vigilant per minute (seconds)
    - GroupSize: number of individuals in the observed group

- Data_PredatorSimulations
  - Purpose: measure responses to predator silhouettes (alarm-call elicitation by predator models).
  - Key fields:
    - Species: focal species presented with a model
    - Date: date of experiment
    - Model: predator type or reedbuck control
    - Call: occurrence of alarm calls within 5 minutes (1/0)
    - DistanceModel: distance to model (meters)
    - GroupSize: number of individuals in the group
    - NumberOffspring: number of young individuals in the group

- Data_PlaybackResponse
  - Purpose: assess responses to heterospecific alarm calls via playback.
  - Key fields:
    - FocalSpecies: species receiving playback
    - CallerSpecies: species whose call was used
    - Date: date of experiment
    - Response: behavioral change within 10 seconds after playback (1/0)
    - FirstResponse: latency to first response (seconds)
    - DurationResponse: time until foraging resumes (seconds)
    - SpeedHeadUp: speed of head-raising (seconds)
    - NOScratch, NOShake, NOHeadUps, NOAlarm: counts of behaviors before resuming foraging
    - Wind: wind speed (m/s)
    - Temperature: ambient temperature (°C)
    - GrassHeight: estimated grass height (cm)
    - DistanceCover: distance to cover (m)
    - DistanceFocal: distance to loudspeaker (m)
    - GroupSize: number of individuals in the focal group
    - Full: indicates all parameters are available

- Data_SpeciesCounts
  - Purpose: estimate relative abundance and grouping patterns across plains and species.
  - Key fields:
    - Date: date of count
    - StudyPlain: study site identifier
    - Group: group number (inter-group distance > 100 m)
    - Tho, Gra, Imp, War, Zeb, Top, Wil, Har, Ela, Gir, Buf, Ost: counts for each species
  - Note: includes Thomson gazelles, Grant gazelles, impalas, warthogs, zebras, topi, hartebeest, eland, giraffe, buffalo, ostrich

## Study design and data collection

- Vigilance behavior
  - Monospecific foraging groups recorded on video for at least 5 minutes.
  - For each visible individual: record vigilance bouts (head-raising duration and frequency).

- Predator simulations
  - Life-sized 2D predator photographs displayed beside the vehicle to elicit alarm calls.
  - Observations of reaction within 5 minutes of exposure.

- Playback experiments
  - Alarm calls from other study species played back to focal herbivores; dove non-alarm calls used as control.
  - Three recordings per stimulus category; focal animal chosen from relaxed, foraging individuals.

- Species counts
  - 66 censuses across three plains, totaling 54 km^2.
  - Pre-defined transects; records include species identities within groups and group sizes.

## Data standards, quality, and metadata

- Each dataset includes explicit variable definitions, units, and explanations to support discoverability and reuse.
- Datasets capture contextual metadata such as date, location (StudyPlain), environmental conditions (wind, temperature, grass height), and group composition.
- The structure supports cross-dataset linking (e.g., same species identifiers across vigilance, predator simulations, and playback responses).

## Reuse, governance, and collaboration implications for Data Leaders

- Data discovery and integration
  - Clear, labeled datasets with standardized species abbreviations enable cross-study synthesis and broader ecological analyses.
  - Metadata fields (Date, StudyPlain, Group, environmental variables) facilitate linking observations with environmental context and site characteristics.

- Data quality and completeness
  - Potential gaps include:
    - Eland not observed to alarm-call in playback trials (limiting certain cross-species analyses).
    - Variability in data completeness across all parameters (e.g., some fields may be missing in certain records).
  - Emphasis on recording both behavioral outcomes and contextual covariates (wind, temperature, grass height) to support robust modeling.

- Data standards and interoperability
  - Use of consistent variable naming and explicit explanations supports reproducibility.
  - Datasets are structured for potential integration with similar multi-species behavioral studies.

- Applications for data strategy
  - Supports development of co-owned, cross-institutional data products on interspecific alarm responsiveness.
  - Demonstrates the value of combining observational, experimental, and census data to understand complex ecological behaviors.
  - Highlights importance of metadata richness (environmental context) for downstream analytics and policy-relevant interpretation.

## Reference

- Meise, K., Franks, D. W., & Bro-Jørgensen, J. (2018). Multiple adaptive and non-adaptive processes determine responsiveness to heterospecific alarm calls in African savannah herbivores. Proceedings of the Royal Society B: Biological Sciences, 285(1882), 20172676.