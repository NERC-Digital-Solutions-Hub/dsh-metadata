# Survival of human pathogens bound to microplastics during transfer through the freshwater-marine continuum

## Overview
- Dataset describing a study on the survival of human pathogens bound to microplastics as they move through the freshwater–marine continuum.
- Two mesocosm experiments conducted at the University of Stirling, Scotland, in April–June 2022.
- Experiments simulate: (1) direct discharge of microplastics from wastewater treatment plants (WWTPs) into freshwater or seawater; (2) downstream transport from WWTP discharge through river, estuary, marine, to beach environments.
- Pathogens studied: Escherichia coli, Enterococcus faecalis, and Pseudomonas aeruginosa.
- Data are organized as 14 CSV files describing background water characteristics, bacterial concentrations, and biofilm measurements for plastic and glass particles.

## Data collection and study design
- Location: Mesocosm experiments located at the University of Stirling, Scotland.
- Experiment 1: Direct WWTP effluent introduction into freshwater or seawater; sampling sites in the Forth Catchment (Dunblane, Bridge of Allan, Kirkcaldy). 30 cages per mesocosm; 20 cages used per sampling event; 12 L mesocosm volumes.
  - Bacteria introduced to effluent and then added to mesocosms; initial concentrations quantified by plating.
  - Conditions: 15 °C, 30 rpm shaking.
  - Timepoints: 1, 2, 3, 4, 5, 6, 7, 9, 12, 17, 22, 27 days.
- Experiment 2: Downstream transport simulation from effluent through river water, estuary water, seawater, and beach sand.
  - Similar mesocosm setup with sequential tank movement to simulate downstream progression.
  - Biofilm on particles quantified by crystal violet staining (absorbance at 550 nm).
  - Sand treatment quantified by measuring CFU per 100 ml (water) or per 100 g dry sand.
  - Timepoints include hours for biofilm measurements and days for CFU analyses.

## Data collected and formats
- Data describe survival and biofilm formation of bacteria on microplastics (polyethylene beads) and glass beads (2 mm diameter).
- Inoculation: exponential-phase bacteria introduced to WWTP effluent; then transferred to mesocosms.
- Measurement types:
  - Background water characteristics (pH, electrical conductivity, turbidity, salinity, temperature).
  - Water characteristics during experiments.
  - Initial bacteria added to mesocosms (CFU per 10 µL; dilutions used).
  - Bacterial concentrations in water (CFU per 100 mL).
  - Bacterial concentrations on plastic and glass particles (CFU per dilution factor; total CFU).
  - Biofilm on plastic and glass (Crystal Violet absorbance at 550 nm).
  - Sand dry weight and related metrics (before/after drying, weight differences, percentage change).
- Units include CFU, pH, EC (mS), turbidity (NTU), salinity (%), temperature (°C), absorbance (550 nm), hours, days, and grams.

## Data completeness and quality
- Data checked for anomalies and boundary values; no missing data reported.

## Data authorship and provenance
- Data collection and interpretation led by Rebecca Metcalf.
- Grants: UKRI NERC “Microbial hitchhikers of marine plastics: the survival, persistence & ecology of microbial communities in the Plastisphere” NE/S005196/1; NERC-GCRF SPACES NE/V005847/1.

## File contents (14 CSV files)
- BackgroundWaterCharacteristics_Mesocosm1: background water characteristics for mesocosms (water type, date, replicate, pH, EC, turbidity, salinity, temperature).
- ExperimentWaterCharacteristics_Mesocosm1: water characteristics during Experiment 1 (water type in tank, time, replicate, pH, EC, turbidity).
- InitialBacteriaAdded_Mesocosm1: bacteria added to mesocosms (species, replicate, CFU_per_10µL, dilution, dilution_factor).
- WaterCFU_Mesocosm1: bacterial concentrations in water over time (water type, species, replicate, CFU_per_100mL).
- PlasticCFU_Mesocosm1: bacterial concentrations on plastic (material, time, replicate, water_type, CFU at various dilution factors, Total_CFU).
- GlassCFU_Mesocosm1: bacterial concentrations on glass (material, time, replicate, water_type, CFU at various dilution factors, Total_CFU).
- BackgroundWaterCharacteristics_Mesocosm2: background water characteristics for mesocosms (water type, date, replicate, pH, EC, turbidity, salinity, temperature).
- InitialBacteriaAdded_Mesocosm2: bacteria added to mesocosms for Experiment 2 (species, replicate, CFU_per_10µL, dilution, dilution_factor).
- CrystalViolet_Plastic_Mesocosm2: crystal violet biofilm on plastic (material, time in hours, replicate, water_type, Absorbance_550nm).
- CrystalViolet_Glass_Mesocosm2: crystal violet biofilm on glass (material, time in hours, replicate, water_type, Absorbance_550nm).
- SandDryWeight_Mesocosm2: sand weight metrics (replicate, before_drying_g, after_drying_g, difference_g, percentage_change).
- BackgroundCFU_Mesocosm2: background CFU data for mesocosm2 (water_type, timepoint_hours, replicate, CFU_DF0, CFU_DF10, CFU_DF100, CFU_DF1000, CFU_DF10000).
- PlasticCFU_Mesocosm2: CFU on plastic for Experiment 2 (species, material, time_days, replicate, water_type, CFU at multiple dilution factors, Total_CFU).
- GlassCFU_Mesocosm2: CFU on glass for Experiment 2 (species, material, time_days, replicate, water_type, CFU at multiple dilution factors, Total_CFU).

## GIS-relevant considerations and potential uses
- Use your spatial data skills to map sampling locations (e.g., Dunblane, Bridge of Allan, Kirkcaldy, Torryburn) within the Forth Catchment and link to catchment features (rivers, estuaries, beaches).
- Integrate time-series CFU and biofilm data with environmental layers to explore spatial-temporal patterns of microbial hitchhikers along the freshwater-marine continuum.
- Create visualizations of pathogen survival on microplastics across different water types (freshwater vs seawater vs beach sand) and along downstream progression.
- Data can support risk assessments and policy discussions on plastic-associated microbial transport in coastal environments when combined with additional geospatial context.