# Sex-differences and temporal consistency in stickleback fish boldness

## Overview
- Investigates sex differences and temporal consistency in boldness (exploratory behavior) of three-spined sticklebacks.
- Primary measure: proportion of time spent out of cover during exploratory tests across two consecutive days.
- Examines long-term consistency by re-catching the same individuals ~9 months later and repeating assessments.
- Predictions tested include whether males are caught sooner than females and whether boldness shows stability over time.

## Subjects and housing
- Subjects: 48 three-spined sticklebacks (Gasterosteus aculeatus): 30 females and 18 males.
- Source: Laboratory population originally caught from the River Cam, UK.
- Individual identification: Visible Implant Elastomer (VIE) tags.
- Housing: Group-housed initially; then individually housed in 2.8 L tanks within a rack system to standardise conditions.
- Environmental controls: 16°C; 8L:16D photoperiod to suppress breeding behaviors; temperatures raised to induce male breeding coloration for sexing after experiments.
- Ethical approvals: Procedures approved by the Ethics and Welfare Committee of the Royal Veterinary College (URN 2011 1084).

## Experimental design and data collection
- Catch ordering: Fish net-caught one-by-one to assign catch numbers (catch order used as a behavioral proxy).
- Longitudinal sampling: Nine months after initial testing, subjects were re-net-caught by a different experimenter to assess temporal consistency (catch#2).
- Exploratory behavior setup: Tests conducted in opaque tanks with four-day cycles; tanks contained lanes with a bank of cover and a feeding area behind a small screen where bloodworms could be placed.
- Testing protocol:
  - Days 1–2: Two bloodworms placed behind the screen; fish introduced individually; movement recorded via above-tank video.
  - Days 3–4: No bloodworms provided; fish fed later in their own tanks.
  - Outcome measure: Proportion of time spent out of cover on days 3 and 4, used as the index of exploratory behavior.
- Data handling: 
  - Initial dataset included 33 fish with complete data after excluding those that failed to locate food on the first two test days.
  - A full-sample analysis (n = 48) also reported to examine robustness.
- Notes on data collection:
  - Bloodworms replaced if consumed; video recording enabled both real-time observation and later verification.
  - Sex, catch order, and exploratory measures were recorded for subsequent analyses.

## Measures and datasets
- Primary variables:
  - PropTimeOut_DAY3 and PropTimeOut_DAY4: Proportion of time out of cover over one-hour test sessions on days 3 and 4.
  - Ave_PropTimeOut: Mean proportion of time out of cover across the two test days.
  - Catch#1: Initial capture order.
  - Catch#2: Capture order nine months later.
  - Sex: Male or Female.
- Data structure: Eight separate data files with multiple entries (both full and subset samples) detailing:
  - Proportions of time out of cover per test day.
  - Mean time out of cover across days.
  - Capture order and temporal consistency data.
  - Sex-based summaries and differences.
- Data metadata: Each file includes column descriptions (e.g., meaning of PropTimeOut_DAY3/DAY4, Ave_PropTimeOut, catch numbers, and sex) to facilitate interpretation and reuse.

## Data quality, analysis notes, and governance
- Data quality and analysis:
  - Excluded individuals that failed to locate food on test days from primary exploratory analyses, acknowledging potential differences in learning versus exploration.
  - Additional analyses conducted on the full sample to assess robustness of findings.
- Temporal and individual consistency:
  - Re-testing after 9 months enables assessment of long-term consistency in bold-like behavior.
  - Use of unique tags and repeat catching enhances reliability of tracking individuals over time.
- Governance and transparency:
  - Detailed documentation of tank conditions, testing procedures, and data column definitions supports reproducibility and data governance considerations for monitoring frameworks.