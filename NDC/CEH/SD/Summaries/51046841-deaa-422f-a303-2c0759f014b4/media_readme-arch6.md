# Text

## Overview
- Describes two data frames containing experimental setup, conditions, and flow/fraction measurements from evolving bacterial communities.
- Data frames: flow_data.txt and fraction_data.txt.
- Each row documents an experimental run with fields for Experiment, Treatment, Ratio, Replicate, and Transfer.
- Two overarching experiments:
  - CompEvo (first set of runs with various bacterial strain combinations and mercury treatment)
  - HostAvail (second set of runs exploring available vs occupied hosts with different strain/plasmid combinations)
- Treatments capture starting community composition and mercury presence; BLANK represents a control with no bacteria.
- Ratio indicates the starting proportion of available vs occupied hosts; Transfer denotes the 24-hour (days) interval at which bacteria are transferred to fresh media.
- Replicate identifies biological replicates of each treatment.

## Data frames and key columns

- flow_data.txt
  - Machine: Beckman Coulter Cytoflex.
  - Signals and thresholds (used to identify bacterial events):
    - FSC.H (Forward Scatter): threshold ~1e3.
    - SSC.H (Side Scatter): threshold ~1e3.
    - PB450.H: threshold ~1e3.5.
    - FITC: threshold ~1e3.5 (detects GFP/YFP).
    - ECD: threshold ~1e3.5 (detects tdTomato variants; used with PE filtering).
    - PE: threshold ~1e3.4 (detects red/orange reporters).
  - Purpose: classify events as bacterial and filter by fluorescence markers to identify specific reporters (GFP, YFP, dTomato, tdTomato).

- fraction_data.txt
  - Total.Count: total events per sample passing basic thresholds (size/gating) to be considered bacteria.
  - Fraction_Red: proportion of events classified as red (surpassing PE threshold but not FITC).
  - Fraction_Yellow: proportion of events classified as yellow (surpassing FITC threshold but not PE).
  - Fraction_Orange: proportion of events surpassing both PE and FITC thresholds.
  - Fraction_Blue: proportion of events not surpassing PE or FITC thresholds.

## Experimental design details

- Experiment
  - CompEvo: multiple sub-treatments (A, B, C, D) and single-strain/four-strain combinations across different mercury conditions; specific strain configurations described in each sub-label.
  - HostAvail: treatments A–D describing combinations of host strains with plasmids/reporter markers; variations across configurations, sometimes including mercury-free or mercury-present contexts.
- Treatment
  - BLANK: control in plate, no bacteria.
  - Other entries: starting composition of the evolving community and whether mercury is added (varies by sub-treatment and experiment).
- Ratio
  - Proportion of Available vs Occupied hosts at the start point.
- Replicate
  - Biological replicate of each treatment.
- Transfer
  - Timepoint (in days) at which bacteria are transferred to fresh media; transfers occur every 24 hours.

## How the data can be used (Data Support perspective)

- Enables self-serve analysis by linking experimental conditions to flow-based bacterial detection and reporter signals.
- Facilitates combining data frames to explore how starting host availability (Ratio) and treatment conditions affect:
  - Cell populations detected via flow (flow_data.txt).
  - Reporter-tagged subpopulations and their proportions (fraction_data.txt).
- Supports cross-tabulation of Experiment, Treatment, Replicate, and Transfer with flow/fraction metrics to track dynamics over time.
- Useful for quality assurance and data provenance, given two separate runs (CompEvo and HostAvail) with potentially patchy formats and diverse gating thresholds.
- Aligns with Data Support practices by enabling dashboard-style exploration, data cleaning/normalization across experiments, and sharing early prototypes or derived products.