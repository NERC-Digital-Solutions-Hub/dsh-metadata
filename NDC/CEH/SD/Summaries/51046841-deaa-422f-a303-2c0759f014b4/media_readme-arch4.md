# Experimental Setup and Data Descriptions for CompEvo and HostAvail Experiments

## Overview
- Describes experimental conditions and data columns for two data frames (CompEvo and HostAvail) and associated flow cytometry data (flow_data.txt) and fraction data (fraction_data.txt).
- Covers experimental runs, treatments, start conditions, data collection methods, andDerived metrics.

## Experimental design

- Experiments
  - CompEvo: first experiment with multiple treatment configurations across two runs.
  - HostAvail: second experiment with its own set of treatments.
- Treatments
  - BLANK: plate control (no bacteria).
  - Treatments describe starting community composition and mercury presence.
  - CompEvo treatments include labeled groups A, B, C, D and F1–F4 with specific strain/plasmid combinations and mercury conditions.
  - HostAvail treatments include A–D with specific host/plasmid configurations; one D condition includes KT2440.KmR as a host.
- Ratio
  - Proportion of Available vs Occupied hosts at the start point.
- Replicate
  - Biological replicate identifiers for each treatment.
- Transfer
  - Timepoints (in days) at which bacteria are transferred to fresh media, every 24 hours.

## Data frames and fields

- For both data frames
  - $Experiment: Indicates CompEvo or HostAvail; two separate runs with distinct treatments.
  - $Treatment: Describes starting community composition and mercury status; BLANK denotes control.
  - $Replicate, $Transfer: As above, used to track experimental replication and timing.

- flow_data.txt (flow cytometry data)
  - Machine: Bećkman Coulter Cytoflex used for data collection.
  - $FSC.H: Forward Scatter signal (height); threshold for bacterial signal ~10^3.
  - $SSC.H: Side Scatter signal (height); threshold for bacterial signal ~10^3.
  - $PB450.H: PB450 signal (Hoescht staining) threshold ~10^3.5.
  - $FITC: GFP/YFP signal; threshold ~10^3.5.
  - $ECD: ECD signal; detects dTomato/tdTomato; used for confirming PE filtering.
  - $PE: PE signal; detects dTomato/tdTomato; threshold ~10^3.4.

- fraction_data.txt (fractions computed from flow data)
  - $Total.Count: Total events per sample passing size thresholds (FSC/SSC/PB450) to distinguish bacteria from background.
  - $Fraction_Red: Proportion of red-classified events (PE threshold surpassed; FITC threshold not surpassed).
  - $Fraction_Yellow: Proportion of yellow-classified events (FITC threshold surpassed; PE not surpassed).
  - $Fraction_Orange: Proportion of orange-classified events (both PE and FITC thresholds surpassed).
  - $Fraction_Blue: Proportion of blue-classified events (neither PE nor FITC thresholds surpassed).

## Data usage notes

- The datasets provide a structured mapping between experimental conditions and measured signals, enabling analysis of how initial community composition and mercury exposure influence bacterial populations over time.
- Flow data includes gating thresholds and fluorescence channels to classify events and verify staining, supporting robust quality control and downstream interpretation of fractions.