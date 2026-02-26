# Discrimination Ability and Multiple Models experiments

- Overview
  - Two closely related experiments conducted at Madingley Wood, Cambridge: Discrimination Ability (Dec 2021–May 2022) and Multiple Models (Oct 2022–Apr 2023).
  - Feeding stations with lids and 3D-printed insect-like stimuli; wild birds (primarily Great tits) could open lids to access mealworms in some dishes.
  - Aimed to understand how mimetic similarity influences predation decisions and whether a second model type improves protection for certain mimics.

- Study design and setting
  - Field site: Madingley Wood, Cambridgeshire, UK; resident great tits with PIT tags.
  - Feeding stations: 7×7 dish arrays on boards, enclosed in cages with a single entrance linked to a PIT-tag reader; motion cameras mounted above.
  - Experiment structure:
    - Discrimination Ability: training to associate a fly stimulus with reward and a common wasp stimulus with no reward; tested with novel mimetic stimuli of varying similarity to the unrewarding wasp.
    - Multiple Models: added a second unrewarding wasp type (and a second treatment with two models, 2M); tested whether a second model type enhances protection for certain mimics.
  - Treatments:
    - 1M: one model type
    - 2M: two model types
  - Data collection cadence: researchers visited every 1–2 days to observe, download video/logger data, and reset sessions; stimuli assignments/random configurations generated in R and stored for cross-referencing.

- Data collection and instrumentation
  - Sensors and recording:
    - Motion-sensitive cameras to capture bird behavior.
    - PIT-tag readers at feeder entrances to log individual birds.
    - Data loggers connected to antennas for timestamped events.
  - Data management:
    - Stimuli assigned to dishes in random configurations per feeder/session.
    - Cross-referencing between video, logger events, and PIT-tag database where possible; some gaps remain due to ambiguous or missing triggers.
    - Data cleaned and formatted with custom R scripts (R v4.3.2).
  - Outputs and formats:
    - Datasets provided per experiment (discrim_ and multimod_ variants) detailing sessions, dishes, logger data, and bird info.

- Stimulus design
  - Stimuli derived from scanned 3D images of real insects; mixed to form mimetic transects across endpoints with intermediate and extrapolated phenotypes.
  - Naming convention:
    - Code format: [species1][contribution][species2][contribution][variant]
    - Examples: M25V75 (25% Mesembrina meridiana, 75% Vespula vulgaris); variants a/b/c denote different specimens.
  - Endpoints and transects:
    - Discrimination Ability: transects ending at V. vulgaris with varying similarity to fly endpoints (M. meridiana, S. ribesii, Chrysotoxum).
    - Multiple Models: transect from Argogorytes mystaceus to V. vulgaris with intermediates (25%, 50%, 75%) and extrapolations beyond endpoints; include non-mimetic M. meridiana M100 as a control.
  - Stimulus assignments:
    - Discrimination: training phase used 15 rewarding fly (M100) and 15 unrewarding wasp (V100); testing phase included 17 unrewarding V100 and 32 rewarding stimuli (including M100 and new phenotypes).
    - Multiple Models: training used 25 rewarding fly (M100) and 24 unrewarding wasp stimuli (V100 or mixed V100/A100 by treatment); testing used 20 unrewarding stimuli and 29 rewarding stimuli including M100 and intermediates/extrapolations.

- Experimental phases
  - Habituation:
    - Provided open dishes with mealworms and peanuts to attract visits; lids later painted to hide content; birds learned to flip lids to access mealworms.
    - Observation: only Great tits consistently opened lids; mice and Blue tits appeared in other contexts but were not primary participants in Discrimination Ability.
  - Training:
    - Lids associated with different stimuli; unrewarding wasp stimuli had no food in corresponding dishes; mealworms offered in fly-stimulus dishes.
    - Sessions reset regularly with new random dish configurations; duration: roughly 3 weeks for Discrimination Ability, ~6 weeks for Multiple Models.
  - Testing:
    - Introduced a broader suite of stimuli, including novel mimics with varying mimicry accuracy; all testing stimuli were rewarded to assess discrimination and generalization.

- Data structure and key files
  - discrim_sessions.csv: 303 rows, 14 columns — session-level details for each feeder.
  - discrim_dishes.csv: 7137 rows, 9 columns — dish-level data (stimulus, mealworm status, timepoint, etc.).
  - discrim_logger_data.csv: 7967 rows, 4 columns — logger event records ( arrivals/departures by PIT tag).
  - discrim_bird_info.csv: 53 rows, 8 columns — bird-level summary per phase.
  - multimod_sessions.csv: 633 rows, 15 columns — session-level data for the 2M treatment structure.
  - multimod_dishes.csv: 17885 rows, 10 columns — dish-level data for multiple models.
  - multimod_logger_data.csv: 2627 rows, 4 columns — logger events for the 2M design.
  - multimod_bird_info.csv: 50 rows, 8 columns — per-bird per-phase summaries.
  - Column details cover: dates, feeder IDs, phase, time stamps, lids status, counts of mealworms/peanuts, dish model codes, timepoints, dish opening identifiers, PIT-tag cross-references, species, sex, and experimental phase.

- Field site, organisms, and data provenance
  - Location: Madingley Wood, Cambridgeshire, UK (coordinates provided in dataset overview).
  - Target organisms: resident great tits (Parus major), some PIT-tagged; occasional blue tits and mice observed but not primary participants in Discrimination Ability.
  - Data provenance and accessibility:
    - Primary data generated with field observations, video analysis, and automated PIT logger data.
    - Related dataset for stimuli design and 3D imagery available via separate DOI, enabling reproduction of stimulus generation.

- Quality control and limitations
  - Quality checks:
    - Summary data examined for correct coding and plausible value ranges.
    - Missing data patterns assessed to distinguish genuine absences from transcription losses.
  - Limitations and gaps:
    - Gaps in cross-referencing between video and logger data; some birds’ identities could not be linked to every event.
    - Some feeders/dropouts occurred in the Discrimination Ability phase; data from those feeders were omitted from certain analyses.
    - Metadata completeness and burden of transforming raw formats into a consistent dataset were noted as challenges.

- Additional context
  - Stimulus development and supplementary materials:
    - Full description and digital files for the 3D image stimuli are available in a linked dataset (dois provided).
  - Data processing tools:
    - Analyses and data handling performed in R (v4.3.2) with stored configurations to enable reproducibility across sessions and dishes.