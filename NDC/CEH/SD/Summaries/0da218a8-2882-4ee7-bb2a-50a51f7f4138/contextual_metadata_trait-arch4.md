# Data set description

## Overview
- Provides information on six functional traits of woody plants: Leaf Area, Specific Leaf Area (SLA), Leaf Dry Matter Content (LDMC), Leaf Thickness (Lth), Wood Density (WD), Bark Thickness (BT).
- Includes concentrations of C, N, P, Ca, Mg, and K in leaves; leaf fresh mass and leaf dry mass; and fresh wood volume and dry wood mass to compute Wood Density.
- Covers plot location data and locality parameters across 27 forest monitoring plots (0.5 ha each) in five locations along an altitudinal gradient (lowland, mid-elevation, highland) and a forest perturbation gradient (low, medium, high perturbation) in the Colombian Andes.
- Data collected 2019–2022 under the BioResilience project; funded by the UK Natural Environment Research Council (NE/R017980/1).

## Aim and context
- Investigates whether expression of woody-plant functional traits varies along perturbation and how traits relate to ecosystem processes.
- Aims to understand drivers of variation in forest resilience and perturbation impacts on ecosystem functioning.
- Part of a transdisciplinary effort to understand forest resilience after Colombia’s post-conflict period.

## Experimental design and sampling regime
- Permanent monitoring plots: 27 plots of 0.5 ha along an altitudinal gradient.
- Altitude categories:
  - Lowlands: 0–1200 m
  - Midlands: 1200–2200 m
  - Highlands: 2200–3200 m
- Sites include Quinchas (lowlands), Pedro Palo and Encino (midlands), Encenillo and Martos (highlands).
- Perturbation gradient categories:
  - Low perturbation (>30 years since last disturbance)
  - Medium perturbation (20–30 years)
  - High perturbation (<20 years)
- Sampling intensity:
  - Lowlands: 20 random individuals per plot
  - Other locations: 5 individuals per plot from the most abundant species
  - Total sampled individuals: 825
- Selection criteria emphasize dominance and accessibility, with standardized sampling across plots to capture representative species.

## Traits and nutrient data collected
- Leaf traits: Leaf Area, SLA, LDMC, leaf Thickness (average), Leaf mass (fresh/dry), and related leaf measurements.
- Wood traits: Wood Density (based on branch wood mass and volume), Volume_fresh (water-displacement), Wood_mass_dry (after oven-drying).
- Bark trait: Bark Thickness (five measurements per individual; average).
- Nutrients in leaves: Carbon (C), Nitrogen (N), Phosphorus (P), Calcium (Ca), Magnesium (Mg), Potassium (K); units in mg/g.
- Sample scope:
  - Ten leaves per individual for all leaf traits
  - Wood and bark samples collected from the same branches
  - bark and wood measured with multiple replicates to derive averages
- Field-to-lab workflow aligns with Salgado-Negret et al. (2016) methodology.

## Data files and structure
- Four CSV files:
  - traitnoreplicatesbr: plot/location metadata and overall leaf/wood/bark trait values (23 columns)
  - traitleafreplicatesbr: ten-leaf replicates per individual (11 columns)
  - traitleafpartreplicatesbr: leaf thickness measurements (three leaf sections per leaf; replicates) (9 columns)
  - traitbarkreplicatesbr: bark thickness measurements (five replicates) (9 columns)
- Core variables (examples):
  - Plot_code, Altitude, Perturbation, Locality, Tag_No, Family_Name, Species_Name
  - C, N, P, Ca, Mg, K (mg/g)
  - SLA, LDMC, leaf_thickness_ave, leaf_area_ave, leaf_mass_fresh_ave, leaf_dry_mass_ave
  - Volume_fresh, Wood_mass_dry, Wood_density, Bark_thickness_ave
  - For replicates: leaf_area_1, leaf_fresh_mass_1, leaf_dry_mass_1; leaf_thickness_1; bark_thickness_1
- Locality and plot metadata include categorical descriptors for altitude band and perturbation level.

## Measurements, units, and data ranges
- Nutrients (mg/g):
  - C: 364–1200
  - N: 0–50.9
  - P: 0–9.6
  - Ca: 0–65
  - Mg: 0.4–9.5
  - K: 0–21.9
- SLA: 0.932–82.017 mm2/mg
- LDMC: 19.38–850 mg/g
- leaf_thickness_ave: 0.09–1.36 mm
- Wood_density: 0.04–0.81 g/cm3
- Bark_thickness_ave: 0.33–7.56 mm
- leaf_area_ave: 35.4–335,673 mm2
- leaf_mass_fresh_ave: 0.01–95.62 g
- leaf_dry_mass_ave: 0.01–36.89 g
- volume_fresh: 330–41,180 mm3
- wood_mass_dry: 0.192–16.21 g
- Replicate data exist for leaves (ten per individual), leaf sections (base/middle/top), and bark (five measurements).

## Fieldwork, instrumentation, and procedures
- Equipment list reflects standard plant functional trait protocols:
  - Pole pruners, pruning shears for material collection
  - Bags for sample storage; masking tape, indelible markers for labeling
  - Plastic bottles for field transport; chlorine for sample preservation
  - Scalpels for bark removal; oven drying (65°C) for leaves/wood
  - Silica gel for interim moisture control; precision balances (0.001 g)
  - Water displacement for volume; cylindrical vessels; thread/needle for density measurement
  - Canon Scan LiDE 200 for leaf area imaging; Mitutoyo micrometers for thickness
- Calibration and measurement: instruments calibrated beforehand; accuracy verified; external validation of data structure and metadata.

## Calibration, quality control, and data provenance
- Calibration steps ensured prior to measurement; routine instrument accuracy checks.
- Quality control (QC) procedures:
  - Independent review of databases and metadata by personnel outside the trait team
  - Checks for missing/null fields, data completeness, correct typing, and removal of duplicates
  - Metadata validation for accuracy and consistency with database fields
- Emphasis on reliability, completeness, and discoverability of data.

## Nature and structure of the dataset
- Four CSV files with clearly defined columns and replicates:
  - traitnoreplicatesbr: 23 columns (location, plot, specimen, and trait values)
  - traitleafreplicatesbr: 11 columns (replicate leaf measurements)
  - traitleafpartreplicatesbr: 9 columns (leaf thickness measurements)
  - traitbarkreplicatesbr: 9 columns (bark thickness measurements)
- Data capture covers both cross-plot and within-plot replicates, enabling trait-wide analyses across altitude and perturbation gradients.

## Geographic scope and sites
- Five locations across the Colombian Andes, covering lowland to highland forests.
- Detailed plot coordinates and localities provided in the dataset (Table 1 reference).
- Plots distributed to represent the altitudinal gradient and perturbation categories.

## References and data provenance
- Methodological foundation aligned with Salgado-Negret et al. (2016) trait measurement protocol.
- Project context linked to BioResilience; supported by multiple Colombian and international sources, including Avella-M, CAR, Cuatrecasas, Holdridge, and others cited in the document.