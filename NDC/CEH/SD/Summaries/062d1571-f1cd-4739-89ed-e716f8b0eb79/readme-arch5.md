# Movement metrics of singing and silent Hawaiian field crickets (Teleogryllus oceanicus) in a semi-natural arena.

## Purpose and origin
- Dataset originates from tracking multiple groups of crickets during a three-hour period, with results published in Behavioural ecology paper linked by DOI https://doi.org/10.1111/ele.14404.
- Movement metrics were calculated in MATLAB and then compiled in this file.
- Data were collected to compare movement and behavioural metrics across two morph-related treatments.

## Experimental design and sampling
- Eight crickets per trial: four females and four males.
- Treatments: Silent (fw) where all four male crickets are flatwing morphs; Singing (n) where all four male crickets are normal-wing morphs capable of singing.
- Experimental timing: trials started at 08:00 AM to align with time-of-sunset under the reversed light:dark cycle.
- Procedure: each trial uses four release boxes; two crickets of the same sex placed under each box; 5-minute habituation, then simultaneous box release; trials run for 3 hours.
- Trials: 16 total, evenly split across treatments; after each trial, females laid eggs and hatchlings were counted.

## Data captured and units
- Sex: M (male) or F (female).
- Trial: trial number; eight crickets tracked for 3 hours within each trial.
- Treatment: fw (flatwing) or n (normal wing).
- Weight: weight of individual cricket in milligrams.
- Offspring: for females, number of hatchlings counted after the trial.
- Mated: binary indicator whether the female produced any offspring.
- TotalDistance: cumulative distance traveled (pixels). Convert to meters by dividing by 4000.
- MinsStill: minutes spent stationary.
- MinsSocial: minutes spent within 15 cm of other crickets.
- OtherSexPropVar: proportional variation in time spent with crickets of the opposite sex.
- ID: individual tag ID for each cricket during tracking.
- Age: age of each cricket in days.

## Data structure and provenance
- Structure: one row per cricket per tracked trial; includes trial ID and treatment.
- Data origin: movement metrics derived from the overhead camera array and MATLAB calculations; compiled in this README file.
- Related publication: Behavioural plasticity compensates for adaptive loss of cricket song (DOI provided in collection methods).

## Quality control and data edits
- Trials with tag loss or camera malfunction were omitted.
- Post-QC, 7 Silent trials and 6 Singing trials remained (out of the original 16).

## Data governance and stewardship considerations
- Metadata clarity: explicit definitions, units, and data provenance are provided to support reuse and reproducibility (e.g., distance unit conversion, treatment coding).
- Provenance and reproducibility: data were generated via a defined MATLAB workflow; ensure accompanying scripts or documentation are available for full traceability.
- Data accessibility: linked to a published study; maintain clear citation and DOI references; consider versioning of the dataset if reprocessed.
- Handling incomplete data: document trial-level QC decisions (which trials were omitted and why) to support audit trails and proper interpretation.
- Updates and maintenance: provide a process for updating the dataset with new trials or corrections, including clear versioning and changelog.