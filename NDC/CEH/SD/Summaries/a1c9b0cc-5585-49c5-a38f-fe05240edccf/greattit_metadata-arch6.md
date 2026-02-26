# OVERVIEW

- The dataset comprises two related experiments using similar methods conducted at Madingley Wood, Cambridge: Discrimination Ability (Dec 2021–May 2022) and Multiple Models (Oct 2022–Apr 2023).
- Goal: study how wild birds (primarily Great tits) learn and respond to mimic stimuli associated with rewards (mealworms) versus unrewarded wasp-like stimuli, and how the presence of a second model type affects protection for certain mimics.
- Birds accessed feeding stations with petri dishes covered by lids, some containing mealworms and others not, to assess discrimination and generalization to novel mimics.

## Study design and aims

- Discrimination Ability experiment:
  - Birds trained to associate a fly-like stimulus with reward and a wasp-like stimulus with no reward.
  - Tested with a range of novel mimetic stimuli varying in similarity to the unrewarded wasp stimulus to measure misclassification thresholds.
- Multiple Models experiment:
  - Extended design with a second unrewarding wasp stimulus; included conditions with one model (1M) or two models (2M).
  - Assessed whether a second model type improved protection for intermediates between two wasp-like stimuli.
- Habituation, training, and testing phases structured to assess learning and generalization across progressively diverse stimuli.

## Field site, subjects, and apparatus

- Field site: Madingley Wood, Cambridgeshire, UK; habitat and feeding stations described.
- Subjects: PIT-tagged birds (primarily Great tits) with data linked to species, sex, and ringing history via the Madingley Ringing Group.
- Feeding stations:
  - 7 × 7 array of 30 mm dishes on a board, enclosed in a cage with a single entrance for PIT-tag detection and video capture.
  - Motion-sensitive cameras and PIT-tag readers logged bird visits; researchers periodically checked and downloaded data.

## Stimulus design and stimuli generation

- Stimuli based on scanned 3D images of real insects, combining features to create mimetic continua along transects.
- Stimulus naming uses codes for species contributions (percent compositions) and variants a, b, c representing intraspecific variation.
- Discrimination Ability stimuli (training set): 15 rewarding fly-like (M100) and 15 unrewarding wasp-like (V100); testing included a mix of unrewarding and rewarding phenotypes, including intermediates (e.g., M75V25, S75V25, C75V25) and extrapolations.
- Multiple Models stimuli: transect from Argogorytes mystaceus (A) to Vespula vulgaris (V), with intermediates (25/50/75%) and extrapolations; non-mimetic M100 used as a separate control.
- Stimuli were implemented on lids of Petri dishes; in habituation, mealworms were initially visible, then hidden beneath lids to train lid-opening behavior.

## Data collection and generation

- Data collection methods:
  - Video recordings and logger data from PIT-tag antennas; ordering and timing of dish openings captured when possible.
  - Cross-referencing video with PIT-tag logs to identify individual birds; gaps addressed where triggers were missed or timing was ambiguous.
  - Bird metadata linked to PIT-tag information (species, sex, ringing date) from the field team database.
- Data handling:
  - Data cleaned and formatted using custom R scripts (R v4.3.2); routines included validation, handling missing values, and standardizing codes.
- Cross-referencing:
  - PIT-tag data cross-referenced with ringing group records for species/sex details; video and logger data merged where possible.

## Datasets and structure

- Two experimental schemas with parallel datasets:
  - Discrimination Ability datasets:
    - discrim_sessions.csv: 303 rows × 14 columns (session-level details per feeder)
    - discrim_dishes.csv: 7137 rows × 9 columns (dish-level outcomes per session)
    - discrim_logger_data.csv: 7967 rows × 4 columns (logger events at feeder entrance)
    - discrim_bird_info.csv: 53 rows × 8 columns (bird-level phase summaries)
  - Multiple Models datasets:
    - multimod_sessions.csv: 633 rows × 15 columns
    - multimod_dishes.csv: 17885 rows × 10 columns
    - multimod_logger_data.csv: 2627 rows × 4 columns
    - multimod_bird_info.csv: 50 rows × 8 columns
- For each dataset, detailed field descriptions are provided (see below), including date ranges, feeder IDs, phase identifiers, dish positioning, stimulus codes, mealworm indicators, timepoints, and cross-reference IDs.

## Nature and units of recorded values (highlights)

- Sessions (discrim and multimod):
  - date_start, date_end; feeder; treatment (1M or 2M in multimod); phase; time_start, time_end; logger_start; lids_start/end; lids_note; mealworms_start/end; peanuts_start/end.
- Dishes (discrim and multimod):
  - start_date, end_date; phase; feeder; timepoint (discrim: rank 1–49; multimod: timestamp); model (stimulus code); mealworm (TRUE/FALSE); id (opening status, e.g., B, GT, BT, MOUSE, LID, NA, OFF AT START).
- Logger data (discrim and multimod):
  - feeder; datetime; PIT_tag; species.
- Bird info (discrim and multimod):
  - PIT_tag; species; sex; date_ringed; phase; N_records; N_days; N_feeders.

## Data quality control and limitations

- Quality checks:
  - Summary data reviewed for valid codes and plausible ranges.
  - Missing data patterns examined to distinguish genuine missingness from transcription loss.
- Limitations and gaps:
  - Not all birds triggered the logger or were captured on video; some events could not be confidently linked to individual birds.
  - Some recordings had ambiguous dish-opening timing (especially in multimodal video footage).

## Processing and accessibility notes for data users

- Data processing environment:
  - Custom R scripts (R v4.3.2) used for cleaning, formatting, and cross-referencing.
- Data provenance:
  - Stimuli design and 3D imagery linked to an additional dataset (Scanned 3D images and 3D printable images) with a DOI reference.
- Output formats:
  - CSV files with defined fields; cross-reference keys across sessions, dishes, log events, and bird information.

## Field site and study organisms

- Location: Madingley Wood, Cambridgeshire, UK (coordinates provided in the document).
- Primary species: Great tit (Parus major) and occasional blue tit; PIT-tagged individuals form the basis of cross-referenced datasets.
- Habitat features and feeder design described to support reproducibility and data alignment with field context.

## Experimental protocol overview

- Habituation phase:
  - Dishes initially open with mealworms visible; lids placed to require opening for access; birds learn lid-flipping behavior.
- Training phase:
  - Stimuli attached to lids; rewarded dishes contain mealworms only for fly stimuli (M100); no reward for wasp stimuli (V100 or A100 in 2M).
  - Sessions occur every 1–2 days with random dish configurations; period lasts about 3 weeks (6 weeks for multimod).
- Testing phase:
  - Expanded stimulus set including novel mimics with varying mimetic accuracy; all newly introduced stimuli are rewarded.
  - Duration: ~5 weeks (10 weeks for multimod).

Data Support-oriented takeaway

- The dataset enables analysis of learning and generalization in avian mimicry contexts, across two experimental designs, with rich cross-referenced behavioral, environmental, and individual-level data suitable for dashboards, summaries, and deeper explorations of patterns in mimicry recognition and protection conferred by multiple model types.