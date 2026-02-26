# Data set description

- A dataset describing functional traits of woody plants collected across 27 forest monitoring plots in the Colombian Andes (2019–2022), part of the BioResilience project.
- Traits cover leaves, wood, and bark, plus leaf nutrient concentrations, collected to understand how trait expression varies with altitude and perturbation, and their relation to ecosystem processes and forest resilience.
- Data collected in a gradient of altitude (lowlands, midlands, highlands) and perturbation (low, medium, high); plots span multiple localities and were sampled using standardized protocols. The work is UK NERC funded.

## Overview

- Functional traits included: Leaf Area, Specific Leaf Area (SLA), Leaf Dry Matter Content (LDMC), Leaf Thickness (Lth), Wood Density (WD), Bark Thickness (BT); leaf concentrations of Carbon (C), Nitrogen (N), Phosphorus (P), Calcium (Ca), Magnesium (Mg), and Potassium (K); leaf fresh mass, leaf dry mass; and for wood, fresh volume and dry mass to derive Wood Density.
- Experimental scope: 27 plots × 0.5 ha each, sampled 2019–2022 across altitudinal and perturbation gradients to assess trait variation and its relation to ecosystem processes.
- Project context: BioResilience, a transdisciplinary study of forest resilience after Colombia’s post-conflict period; funded by the UK Natural Environment Research Council (NE/R017980/1).

## Spatial and sampling design

- Plot design: 27 permanent monitoring plots of 0.5 ha; distributed along altitude categories:
  - Lowlands: 0–1200 m
  - Midlands: 1200–2200 m
  - Highlands: 2200–3200 m
- Perturbation gradient: Low (>30 years since disturbance), Medium (20–30 years), High (<20 years).
- Localities include Quinchas (lowlands), Pedro Palo and Encino (midlands), and Encenillo and Martos (highlands).
- Sampling details:
  - One census per plot; selection based on dominance and accessibility criteria; branch and leaf material collected from selected trees.
  - Leaves: 10 leaves per individual; wood sample from the same branch; samples labeled with plot code and tree tag.
  - Intensity: 20 individuals per plot in the lowlands and Encino Midlands; 5 individuals per plot at other locations; total across all plots: 825 individuals.
- Spatial data: Plot coordinates provided (latitude/longitude) for mapping and GIS integration.

## Data files and structure

- Four CSV files:
  - traitnoreplicatesbr
    - 23 columns: Plot_code, Altitude, Perturbation, Locality, Tag_No, Family_Name, Species_Name, C, N, P, Ca, Mg, K, SLA, LDMC, leaf_thickness_ave, wood_density, bark_thickness_ave, leaf_area_ave, leaf_mass_fresh_ave, leaf_dry_mass_ave, volume_fresh, wood_mass_dry.
  - traitleafreplicatesbr
    - 11 columns: Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_part, Leaf_area_1, Leaf_fresh_mass_1, Leaf_dry_mass_1.
  - traitleafpartreplicatesbr
    - 9 columns: Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_Part, Leaf_thickness_1.
  - traitbarkreplicatesbr
    - 9 columns: Altitude, Perturbation, Locality, Plot_code, Tag_No, Family_Name, Species_Name, Sample_Part, Bark_thickness_1.
- Data are organized by replicates:
  - traitnoreplicatesbr: one record per plot per species for overall trait metrics.
  - traitleafreplicatesbr: ten leaves per individual (replicate-level leaf metrics).
  - traitleafpartreplicatesbr: leaf thickness measured in three leaf sections (base, middle, top) across replicates.
  - traitbarkreplicatesbr: five bark thickness measurements per individual (replicate-level bark data).

## Variables, units, and value ranges

- Altitude: categorical gradient (lowlands 0–1200 m, midlands 1200–2200 m, highlands 2200–3200 m).
- Perturbation: Low, Medium, High.
- Locality: Quinchas (lowlands), Pedro Palo/Encino (midlands), Encenillo/Montunos (highlands) (names may vary by site).
- Plot_code: 1–27.
- Taxonomy: Family_Name (APG III), Species_Name (Genus species).
- Nutrients (in traitnoreplicatesbr): C, N, P, Ca, Mg, K measured in mg/g.
  - C: 364–1200 mg/g
  - N: 0–50.9 mg/g
  - P: 0–9.6 mg/g
  - Ca: 0–65 mg/g
  - Mg: 0.4–9.5 mg/g
  - K: 0–21.9 mg/g
- Leaf traits (traitnoreplicatesbr):
  - SLA: 0.932–82.017 mm2/mg
  - LDMC: 19.38–850 mg/g
  - leaf_thickness_ave: 0.09–1.36 mm
  - leaf_area_ave: 35.4–335,673.4 mm2
  - leaf_mass_fresh_ave: 0.01–95.62 g
  - leaf_dry_mass_ave: 0.01–36.89 g
  - volume_fresh: 330–41,180 mm3
  - wood_mass_dry: 0.192–16.21 g
  - wood_density: 0.04–0.81 g/cm3
  - bark_thickness_ave: 0.33–7.56 mm
- Leaf replicates (traitleafreplicatesbr):
  - Leaf_area_1: 0–4471.37 mm2
  - Leaf_fresh_mass_1: 0.01–181.76 g
  - Leaf_dry_mass_1: 0.004–48.56 g
- Leaf thickness replicates (traitleafpartreplicatesbr): leaf_thickness_1 0.0201–1.994 mm
- Bark thickness replicates (traitbarkreplicatesbr): bark_thickness_1 0.242–13.170 mm
- Data units follow explicit field/unit descriptions in each file (e.g., mg/g for nutrients, mm for thickness, mm2 for area, g for masses, etc.).

## Methods and QA

- Field and lab methods:
  - Leaf area measured by scanning leaves; area and thickness measured on fresh leaves; leaf dry mass determined after oven-drying at 65°C for 3 days.
  - SLA = leaf area per leaf dry mass; LDMC = leaf dry mass per fresh mass.
  - Bark thickness measured with Mitutoyo micrometer; wood density calculated as dry wood mass divided by fresh wood volume (volume via water displacement).
  - Nutrient concentrations determined by elemental analysis and standard chemical methods (C by combustion, N by Dumas, P by phosphomolybdo-vanadate colorimetry, Ca/Mg/K by calcination and atomic absorption).
- Calibration and quality control:
  - Instruments calibrated beforehand; accuracy verified; external review of databases and metadata for completeness, consistency, and data typing; duplicate data removal and metadata validation performed.
- Documentation and data structure:
  - Four CSV files with clearly defined variables and units; replicates documented with plot codes and tag numbers to enable linking across files.

## GIS-ready usage and integration

- Spatial integration:
  - Plot-level coordinates enable mapping of trait aggregates and gradients across altitude and perturbation space.
  - Use Plot_code to join trait data (per-plot metrics in traitnoreplicatesbr) with spatial plots and with replicates (traits from traitleafreplicatesbr, traitleafpartreplicatesbr, traitbarkreplicatesbr) for fine-scale analyses.
- Data organization for GIS:
  - Create a plot-centric point layer with attributes: altitude category, perturbation level, locality, plot_code, and summarized trait metrics (mean SLA, LDMC, leaf area, wood density, etc.).
  - For replicate-level analyses, create related tables or join-on Plot_code and Tag_No to attach leaf-level and bark-level measurements to their plots.
- Potential analyses:
  - Map spatial variation of key traits across altitude and perturbation gradients.
  - Compare trait means by altitude category and perturbation level.
  - Integrate with ecological models to relate trait distributions to ecosystem processes and forest resilience.
- Practical notes:
  - Coordinates are provided; use a consistent CRS (likely WGS84; EPSG:4326) for initial mapping; convert to suitable projections for analysis as needed.
  - Units are specified per file; ensure consistent unit usage when aggregating or comparing across files.
  - Be mindful of replication structure (ten leaves per individual, multiple parts per leaf) when creating summaries or statistical models; maintain links via Plot_code and Tag_No.

## References

- Avella-M, A.; Torres-R, S.; Gómez, W.; Pardo, M. (2014). Los páramos y bosques altoandinos del pantano de Monquentiva o pantano de Martos (Guatavita, Cundinamarca, Colombia): caracterización ecológica y estado de conservación. Biota Colombiana, 15(1), 3-39.
- CAR (2007); CAR & Grupo de Humedales (2013); Cuatrecasas (1958); Fundación Natura Colombia (2021); Gaona Camacho & Pardo Lozano (2014); Holdridge (1982); IDEAM/IGAC et al. (2007); Reina et al. (2010); Rojas et al. (2015); Solano (2006); Melo Pérez (2020).