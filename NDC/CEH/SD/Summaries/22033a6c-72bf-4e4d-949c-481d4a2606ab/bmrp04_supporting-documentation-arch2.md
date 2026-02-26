# Banded Mongoose Research Project

## Aim and Context
- Long-term study of a wild banded mongoose population (Mungos mungo) on Mweya Peninsula, Queen Elizabeth National Park, Uganda, ongoing since 1995.
- Population typically comprises 10–12 social groups, ~20 adults plus offspring per group.
- Data collected to observe life history, reproductive and cooperative behaviours, and responses to social/experimental stimuli; outputs contribute to understanding environmental/social dynamics over time and support standardized monitoring approaches.

## Study Design and Sampling Regime
- Individual mongoose identification via unique fur marks; regular trapping every two months to maintain marks.
- Groups monitored via radio collars on 1–2 individuals per group; most groups habituated to observers (approach within <5 m).
- Field visits every 1–3 days for at least 20 minutes to record group composition, life history, reproduction, and cooperative behaviours.
- Reproduction is highly synchronized within groups with pregnancy dates recorded; pup births tracked precisely.
- Experimental intrusion trials conducted in five focal groups (Mar 2016–May 2017) to simulate intergroup conflict using olfactory (faeces, scent marks), auditory (war cries), and visual cues (rival individuals in traps).
- Each focal group exposed to stimuli from a neighboring rival group; 22 simulated intrusion trials and 22 control trials overall; trials spaced at least two weeks apart to prevent habituation.
- Video recording of focal groups during stimulus presentations to capture behavioural responses.

## Experimental Design
- Intrusion stimuli: rival faeces, urine, scent marks (collected morning of presentation), and 30-second playback of rival war cries with standardized amplitude.
- Rival males from the focal group’s rival captured, transported, and reintroduced for 5 minutes in the focal group presentation; control trials used focal-group-derived stimuli (faeces, scent, close calls) and four focal-group males trapped as non-threatening controls.
- Stimuli presented in a semi-circle around a designated presentation site; timing and sequence standardized per trial.
- Control trials mirrored intrusion procedures but with focal-group-origin stimuli to assess baseline responses.

## Fieldwork Instrumentation
- Data collection app: Mongoose 2000 on Samsung Galaxy tablets for life history data; data stored in MS Access.
- Tracking: radio collars (~30 g) with 20 cm whip antenna.
- Acoustic stimuli: war cries recorded with H1 Zoom, Sennheiser mic; playback via hidden portable speaker.
- Visual stimuli: rival males presented via traps covered with black cloth; videos captured with tablets or a Panasonic camera.

## Calibration and Quality Assurance
- Field instruments calibrated to factory settings.
- Observational data collected by a single observer; audio-free viewing used to reduce bias, followed by watching videos with sound to annotate stimulus timing.
- Sampling protocol: 30-second interval scans from 30 seconds after first group member within 2 m of stimulus, up to ~3 minutes 30 seconds; require at least two samples per stimulus type per trial; non-blind to treatment due to logistical constraints.
- Data quality controls embedded in Mongoose 2000; data checks in MS Access and bespoke R code to detect inconsistencies (e.g., multiple death records for an individual).

## Analytical Methods and Metrics
- Behavioural data coded from video into six behaviours: stationary, walking/running, digging, standing upright, scent marking, attacking.
- Defensive vs. non-defensive classifications used for analyses.
- Metrics derived from sampling points per video:
  - Spatial cohesion: mean proportion of group members within 2 m of the stimulus; consider core vs non-core territory placement.
  - Participation in collective defence: mean proportion of individuals acting defensively (standing upright, scent marking, attacking).
  - Homogeneity of behavioural response: mean behavioural diversity (H-index) across group members.
- Additional context recorded: number of foraging group members out on the trip, location relative to core territory.

## Data Structure and Outputs
- Data stored in three CSV files, each with standardized fields:
  - Proportion within 2 m of stimulus (mean per video): includes video ID, group, stimulus type (intruder vs control), location (core vs non-core), group size, and mean defensive proportion.
  - Mean proportion of group exhibiting defensive behaviour (stimulus response data): includes video ID, group, stimulus type, location, group size, and mean defensive proportion.
  - Mean H-index of behavioural diversity (stimulus response data): includes video ID, group, stimulus type, location, group size, and mean H-index.
- Columns capture: video, focal group ID, stimulus type (intruder/control and specific stimulus), location, group size, and the computed metrics (prop within 2 m, prop defensive, H-index).

## Relevance for Environmental Monitoring Analysts
- Demonstrates standardized, repeatable data collection and analysis for animal behavioural responses to intra- and intergroup stimuli.
- Provides clear, comparable metrics (spatial cohesion, collective defence participation, behavioural diversity) that can be tracked over time to monitor ecological and social stressors.
- Emphasizes data quality controls, documentation, and stored data structures to facilitate reuse and integration with other environmental datasets.
- Illustrates handling of core vs non-core spatial delineations to assess habitat-use context within monitoring outputs.