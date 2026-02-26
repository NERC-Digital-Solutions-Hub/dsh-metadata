# OVERVIEW: This dataset relates to three closely related experiments conducted using similar methodologies.

- Goal
  - Investigate how different invertebrate predators (praying mantises, jumping spiders, crab spiders) respond to 3D-printed mimetic stimuli that vary in similarity to a negatively conditioned wasp stimulus.
  - Training to associate wasp stimuli with negative experiences; fly stimuli serve as neutral controls.
  - Testing examines how much mimetic similarity is required before a stimulus is treated as the wasp by each predator.

- Data collection and processing
  - Real-time behavioural observations during trials, with some video recordings for reference.
  - Timing measurements recorded with a stopwatch.
  - Data cleaned (invalid/unused points removed) and formatted using custom R v4.3.2 scripts.

- Quality control
  - Summary data checked for valid codes and plausible ranges.
  - Patterns of missing data assessed to ensure gaps reflect true unavailability, not transcription errors.

- Data structure and files
  - mantis_data.csv
    - 88 trials, 7 columns
    - Columns include: species, id, instar, trial, model, phase, time_to_attack
  - jumping_spider_data.csv
    - 1,355 rows, 6 columns
    - Columns include: id, phase, trial, model, behaviour, count
  - crab_spider_data.csv
    - 1,260 rows, 8 columns
    - Columns include: id, sex, colour, day, treatment, model, behaviour, count
  - Detailed descriptions of column meanings and units are provided in the dataset documentation (Nature and units of recorded values).

- Stimulus design and models
  - Stimuli are 3D-printed, based on scanned insect images; created as transects of mimetic similarity between endpoints.
  - Five transect points used in experiments: M100, M75V25, M50V50, M25V75, V100 (M = Mesembrina meridiana; V = Vespula vulgaris).
  - Some experiments included an alternative transect based on Chrysotoxum (hoverfly) for jumping spiders; crabs included stimuli beyond V vulgaris in phenotypic space (e.g., A-25V125, A-50V150).
  - Model naming reflects species contributions and variants (e.g., M25V75, M100, V100, M100V0, etc.), with variants a, b, c capturing intraspecific variation.
  - Full methodology and digital 3D files linked to via a referenced dataset DOI.

- Study organisms and housing
  - Praying mantises: Rhombodera kirbyi, Polyspilota aeruginosa, Pseudoxyops perpulchra; housed individually in 19 × 13 × 8 cm boxes; room at 26°C, 12:12 h light/dark; fed crickets/mealworms twice weekly; trials conducted ~30 h after feeding.
  - Jumping spiders (Phidippus audax): housed individually in similar boxes; room at 26°C; fed as above; trials conducted after acclimation.
  - Crab spiders (Synema globosum): collected from flowers in Portugal; kept at 22°C, no artificial light cycle; not fed for 48 h prior to use.

- Experimental arenas and stimulus delivery
  - Mantises and jumping spiders: trials in a small opaque box with stimuli suspended and moved by fishing-line and motor-driven system (three-dimensional, jerky motion) to mimic prey movement.
  - Crab spiders: larger arena with a flower perch (purple milk thistle) and vertically moving stimuli; similar motorized delivery but arena setup differs.

- Experimental design: training and testing phases
  - Training phase
    - Mantises and jumping spiders: six aversive conditioning trials on separate days; initial stimulus randomly assigned (M100 or V100), then alternated; wasp stimuli punished (thorax prodding) after attack; fly stimuli (M100) neutral.
    - Crab spiders: condensed training with three possible treatments (wasp punishment with no prior exposure, fly punishment, or no punishment); no direct wasp/fly presentations in some cases.
  - Testing phase
    - Mantises and jumping spiders: nine trials per subject; five probe stimuli (points along transect in random order) interleaved with four reinforcement trials (two M100 and two V100); wasp stimuli punished as during training.
    - Spiders: similar testing structure but with varied stimulus sets (Chrysotoxum or M. meridiana transects); some subjects largely did not attack, so latency to attack was not a robust measure for spiders.
    - Crab spiders: each tested once with a single stimulus due to captivity constraints.

- Behavioral measures and analysis notes
  - Mantises: primary metric is time_to_attack (latency from trial start to first attack).
  - Jumping spiders: attacks were infrequent; a range of behaviours recorded (e.g., orientation, alert, display, approach, attack) with counts per trial.
  - Crab spiders: behaviour counts per trial across observed categories; no latency measure due to infrequent attack.
  - Behavior table (descriptions) includes categories such as Bungee, Hide, Orientation, Alert, Display, Approach, Attack, with positive/negative interpretation notes for each species.

- Observational scope and reporting
  - Real-time observations supplemented by video where applicable.
  - Data cleaned and structured to enable cross-species comparisons of mimetic similarity effects on predator responses.
  - The dataset is accompanied by methodological details and links to additional digital stimulus files and descriptions for reproducibility and reuse.