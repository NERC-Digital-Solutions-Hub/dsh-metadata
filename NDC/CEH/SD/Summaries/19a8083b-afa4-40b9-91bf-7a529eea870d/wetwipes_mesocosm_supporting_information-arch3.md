# Persistence of wet wipes in beach sand and the survival of E. coli on their surfaces

## Overview
- Study aim: assess persistence of wet wipes in beach sand and survival of E. coli on wipe surfaces; evaluate sewage-associated plastic waste as reservoirs for faecal bacteria, potential pathogens, and antimicrobial resistance genes.
- Location and period: mesocosm study at the University of Stirling, May–August 2023.
- Study design: three wet wipe brands representing different compostability categories (A: non-compostable with plastic; B: home compostable; C: commercially compostable). Simulated bathroom-to-beach journey: flushed, discharged to WWTP effluent, exposed to seawater, then settled in beach sand mesocosms.
- Data outputs: five CSV files capturing physical, chemical, and biological measurements across replicates and timepoints.
- Responsible: data collection and interpretation led by Rebecca Metcalf.
- Data completeness: checked for anomalies; no missing data reported.

## Data collection and study design
- Experimental sequence:
  - Wet wipes cut to 7 × 7 cm and subjected to sequential treatments emulating real-world pathways.
  - Inoculated with E. coli at multiple stages; incubated under controlled conditions (15 °C, 80 rpm).
  - Transitioned from water/effluent phases to seawater, then to beach sand mesocosms.
- Sampling regime:
  - Weekly sampling for 15 weeks.
  - Four replicates per wipe type sampled each week.
- Measurements:
  - Microbial: E. coli CFU enumerated from wipes after vortexing and membrane filtration; selective media used for CFU enumeration after 24 h incubation at 37 °C.
  - Physical: Tensile strength of wipes measured with a digital force meter.
- Mesocosm setup:
  - Drainpipe-based sand mesocosms (10 cm sand depth) covered with hessian fabric to control sand loss.
- Rationale: aligned with UKRI/NERC grant aims under the Plastisphere project.

## Data files and contents
- Dry_weight_sand_used_in_wet_wipes_mesocosm.csv
  - Data on the dry weight of sand used for mesocosms; includes replicate, sand weights before/after drying, moisture change, and percentage change.
- Background_bacterial_concentrations_in_wet_wipes_mesocosm.csv
  - Background concentrations used in mesocosms; includes source of E. coli, replicate, CFU per mL, and timepoint.
- Water_characteristics_used_in_wet_wipes_mesocosm.csv
  - Water types used (tap, WWTP effluent, seawater); includes pH, salinity, date, week, replicate, and wipe type.
- Tensile_strength_of_wet_wipes_in_wet_wipes_mesocosm.csv
  - Weekly tensile strength measurements; includes replicate, wipe type, timepoint (week/date), and tensile strength in Newtons.
- Bacterial_concentrations_in_wet_wipes_mesocosm.csv
  - E. coli concentrations on wipes over time; includes replicate, wipe type, timepoint, CFU per mL and per wipe, dilution, and date.

## Methods in detail
- Microbial enumeration:
  - E. coli recovered from wipes by vortexing in PBS, followed by filtration through 0.45 μm membranes.
  - Membranes cultured on MLGA selective media; CFU counted after 24 h at 37 °C.
- Tensile strength:
  - Measured using a 50 N digital force meter; force required to rupture each wipe recorded.
- Inoculation and incubation:
  - Initial inoculation in tap water with sterile feces and E. coli; subsequent inoculations in WWTP effluent; incubation steps at 15 °C with shaking (80 rpm) before transfer to seawater and sand mesocosms.

## Data provenance and quality
- Completeness: data checked for anomalies; no absent data reported.
- Metadata and structure: dataset includes clear replicate identifiers, wipe types, water type, timepoints, and dates to support traceability and reanalysis.
- Use and sharing: datasets are organized for transparency and reuse, with clearly described variables and units.

## Relevance for monitoring frameworks
- Demonstrates how to structure environmental health monitoring data across physical (sand, sand weight, tensile strength) and biological (E. coli concentrations) indicators.
- Provides a reproducible framework for tracking persistence and transfer of litter-associated microbes through a litter-to-environment pathway.
- Includes time-resolved measurements suitable for evaluating policy-relevant questions about plastics, plastic-associated microbes, and potential public health implications.