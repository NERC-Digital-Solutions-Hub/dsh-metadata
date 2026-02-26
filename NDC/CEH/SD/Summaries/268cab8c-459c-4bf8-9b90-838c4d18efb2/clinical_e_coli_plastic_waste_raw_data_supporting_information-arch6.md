# Data on the persistence of Escherichia coli on plastic and cotton, virulence in Galleria mellonella, and antimicrobial resistance

- Scope: A dataset examining clinically relevant Escherichia coli pathotypes’ ability to colonise and persist on plastic waste (cotton and HDPE), plus antimicrobial resistance and virulence assessments.
- Data files: 8 CSV files capturing molecular, growth, persistence, virulence, environmental water properties, inocula details, and MICs.

## What is recorded
- Luciferase_expression_WT_and_lux_transformed_strains.csv: comparison of luciferase expression between wild-type and lux-transformed E. coli strains.
- Growth_curves_WT_and_lux_transformed_strains.csv: growth (OD600) for WT and lux-transformed strains.
- Persistence_of_WT_and_lux_transformed_strains_on_plastic_and_cotton.csv: persistence levels on plastic vs. cotton over time.
- Virulence_in_Galleria_mellonella_model.csv: larval survival after challenge with recovered strains.
- Properties_of_surface_water_used_in_each_replicate_tank.csv: environmental water properties used to generate biofilms.
- Inocula_used_in_frames.csv: concentrations of E. coli used to inoculate cotton and plastic frames.
- Inocula_used_in_galleria_challenge.csv: concentrations used for Galleria mellonella challenge.
- Minimum_inhibitory_concentrations_WT_and_lux_E_coli.csv: MICs of erythromycin for WT and lux-transformed strains.

## Where and when data were collected
- Location: Scotland, UK.
- Time period: Experiments conducted January–June 2023.

## How the data were collected
- Experimental design: E. coli inoculated onto cotton and HDPE in nutrient-rich and surface-water environments.
- Sampling: 7, 14, 21, and 28 days after inoculation (DAI).
- Persistence assessment: transfer of material to LB with erythromycin; growth (OD600) and luciferase expression thresholds used to confirm persistence.
- Virulence assessment: Galleria mellonella larvae challenged with recovered bacteria; survival monitored for 72 h.
- MIC testing: isolates tested across erythromycin dilutions (16 mg/ml to 0.25 mg/ml) to determine resistance.
- Replication: biological triplicates; multiple technical replicates per assay.

## Why the data were collected
- To study adhesion, persistence, antimicrobial resistance, and virulence of pathogenic E. coli on plastic waste under environmentally relevant conditions.
- To satisfy UKRI NERC grants: Microbial hitchhikers of marine plastics (Plastisphere) and SPACES project.

## Provenance and responsible personnel
- Collected and interpreted by Michael Ormsby.
- Part of grant-supported research; data quality checked for anomalies; missing data recorded as ND.

## Completeness and data quality
- Data checked for upper/lower limits and anomalies.
- Missing data documented as ND.
- Calibration and standard laboratory controls described (e.g., plate reader calibration, positive/negative controls).

## Data structure and variable details
- Data are organized into separate CSV files, each representing a specific experimental variable.
- Key columns include:
  - Strain, Material (cotton, plastic; or Wild-type), Replicate, Time (hours or days), and associated measurements.
  - Luciferase_expression (relative units), Growth (OD600), Survival (percentage), Concentration (CFU), Erythromycin (mg/ml), Optical_density (OD measurements).
  - Auxiliary columns describe units and experimental factors.

## Data provenance and grants
- Source details tied to UKRI NERC grants NE/S005196/1 and NE/V005847/1.
- Data recorded in a controlled laboratory setting with standard procedures (e.g., 96-well plates, incubators, Galleria mellonella sourcing).

## How the data can be used
- Integrate multilayer data (growth, persistence, virulence, MICs) to model colonisation dynamics of E. coli on textiles and plastics.
- Compare wild-type vs. lux-transformed strains in expression and growth.
- Analyze virulence changes after persistence on different materials.
- Assess correlations between surface-water properties and biofilm/persistence outcomes.
- Reuse MIC and virulence data for antimicrobial resistance studies and Plastisphere-related research.