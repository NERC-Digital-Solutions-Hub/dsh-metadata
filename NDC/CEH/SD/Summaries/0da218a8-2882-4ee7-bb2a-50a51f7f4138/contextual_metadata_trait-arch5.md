# Data set description

## Overview
- Describes a woody plant functional trait dataset collected in the Colombian Andes as part of the BioResilience project (2019–2022).
- 27 permanent forest plots (0.5 ha each) across an altitudinal gradient (lowlands, midlands, highlands) and a perturbation recovery gradient (low, medium, high).
- Aimed to assess how functional traits vary with perturbation and relate to ecosystem processes and forest resilience.
- Data collection funded by the UK Natural Environment Research Council (NE/R017980/1).

## Study design and scope
- Plot layout: 27 plots in three altitude categories with three perturbation levels, distributed across five localities.
- Localities: Quinchas (lowlands), Pedro Palo and Encino (midlands), Encenillo and Martos (highlands).
- Sampling timeline: trait measurements gathered after plot installation (2019–2022; trait data collected mainly in 2019–2022; nutrients analyzed in 2022).
- Sampling units: 825 individuals sampled in total; sampling intensity varied by location (20 individuals per plot in lowlands and Encino Midlands; 5 individuals per plot in other locations; selection based on dominance and canopy accessibility).

## Traits and measurements
- Functional traits (woody plants): Leaf Area, Specific Leaf Area (SLA), Leaf Dry Matter Content (LDMC), Leaf Thickness (Lth), Wood Density (WD), Bark Thickness (BT).
- Foliar nutrients: Carbon (C), Nitrogen (N), Phosphorus (P), Calcium (Ca), Magnesium (Mg), Potassium (K).
- Other leaf/wood data: Leaf fresh mass, leaf dry mass, fresh wood volume, dry wood mass (used to compute Wood Density).
- Purpose: determine if trait expression differs along the perturbation gradient and how traits relate to ecosystem processes and forest resilience.

## Data collection and protocols
- Protocols: Following Salgado-Negret et al. 2016 for plant trait measurement.
- Field collection: 
  - Trees selected per plot to reach sun-exposed branches; sampling criteria vary by location.
  - Leaves: 10 leaves per individual; leaves scanned for area; thickness measured at base/middle/top; leaves dried for mass.
  - Wood: one branch per individual for density calculations; wood volume measured by water displacement; bark thickness measured with a micrometer.
- Nutrient analysis: 
  - C by elemental analysis; N by Dumas method; P by phosphomolybdo-vanadate colorimetry; Ca, Mg, K by acid digestion and atomic absorption.
- Calibration and quality control:
  - Instruments calibrated beforehand; external review of databases and metadata for accuracy, completeness, consistency, and duplication; metadata validation performed.

## Data files and structure
- Four CSV files:
  - traitnoreplicatesbr: 23 columns, includes Plot_code, Altitude, Perturbation, Locality, Tag_No, Family_Name, Species_Name, and trait measurements (C, N, P, Ca, Mg, K, SLA, LDMC, leaf_thickness_ave, wood_density, bark_thickness_ave, leaf_area_ave, leaf_mass_fresh_ave, leaf_dry_mass_ave, volume_fresh, wood_mass_dry).
  - traitleafreplicatesbr: 11 columns, includes Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_part, Leaf_area_1, Leaf_fresh_mass_1, Leaf_dry_mass_1.
  - traitleafpartreplicatesbr: 9 columns, includes Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_Part, leaf_thickness_1.
  - traitbarkreplicatesbr: 9 columns, includes Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_Part, Bark_thickness_1.
- Variable details include units and value ranges:
  - Nutrients (C, N, P, Ca, Mg, K) in mg/g with specified min/max.
  - SLA (mm2/mg), LDMC (mg/g), leaf_thickness_ave (mm), wood_density (g/cm3), bark_thickness_ave (mm), leaf_area_ave (mm2), leaf_mass_fresh_ave (g), leaf_dry_mass_ave (g), volume_fresh (mm3), wood_mass_dry (g).
  - For replicates data, leaf_area_1, leaf_fresh_mass_1, leaf_dry_mass_1, leaf_thickness_1, bark_thickness_1 measured at replicate level.
- Plot and sample identifiers:
  - Plot_code, Tag_No, locality, altitude category, perturbation category; coordinates provided for plots.

## Fieldwork and instrumentation
- Equipment used: pole pruners, pruning shears, bags (plastic/paper), masking tape, indelible markers, plastic bottles, sodium hypochlorite solution, scalpel, oven, silica gel, balances, thread and needle, cylindrical glass containers, and scanning equipment (Canon Scan LiDE series) and Mitutoyo micrometer.
- Sample handling: samples dried in university lab; fungi/fungal growth minimized with chlorine storage where needed; volume and density measurements via Archimedes principle.

## Data management and quality assurance
- Calibration steps: instruments prepared and calibrated prior to measurements; regular checks to ensure measurement accuracy.
- Quality control: external review of databases and metadata focusing on structure, completeness, typing, duplicates, and metadata consistency; validation to ensure reliability and usefulness of the data.

## Units, documentation, and metadata
- Clear documentation of measurement units, valid value ranges, and data provenance.
- Metadata and data structure align with the described four-file schema, enabling replication and cross-site comparison.

## Context and references
- Data generated within BioResilience framework, focusing on resilience of Andean forest ecosystems post-conflict in Colombia.
- Supporting references include ecological and biogeographical sources (Holdridge life zones, Low Montane Very Humid Forest, páramo systems, etc.).