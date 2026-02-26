# Metadata for 4_Hot_Particle_Activity.csv

## Overview
- Metadata describing a dataset of hot particle activity measurements from Chernobyl-related samples and Polish samples.
- Each row links a unique particle to spatial, physical, visual, and radiological characteristics, plus measurement dates and activities for multiple radionuclides.
- The dataset supports classification, comparison, and modeling of hot particles’ isotopic content, burnup, and physical attributes.
- References provided anchor the metadata to established literature on hot particles.

## Data schema and key fields
- Code: database serial number (unique ID).
- Identifier: UIAR unique label (chemical analysis number).
- Angle_degree: polar coordinate angle of the sampling point around ChNPP (clockwise; 0°/360° is North).
- DIST_km: distance from the sampling point in the polar coordinate system; Polish samples have an approximate distance of 500 km noted.
- MAXSIZE_um / MINSIZE_um: particle size range in micrometers.
- Burnup_MW_d_kg-1: burnup level, categorized into 17 groups based on activity ratios of low-mobile refractory radionuclides and Cs isotopes.
- VIEW / COLOR / FORM / STRUCT: descriptors of how the particle appears visually and its physical structure; STRUCT includes sample origin notes (e.g., Mikolajki, Warsaw, Lomza, Bialystok, Suwalki) and HP type classification (fuel vs condensed).
- DATE_Gamma / DATE_Alpha / DATE_Beta: dates of gamma, alpha, and beta measurements (dd-mmm-yyyy).
- Activity_of_XXX_Bq / STD_of_XXX_Bq: total activity (in becquerels) and its standard deviation at 95% confidence for numerous radionuclides (e.g., 95Zr, 95Nb, 106Ru, 125Sb, 134Cs, 137Cs, 144Ce, 154Eu, 155Eu, 54Mn, 60Co, 241Am, 90Sr), with corresponding notes on units.
- The dataset includes a detailed set of isotopic activities and their uncertainties, alongside metadata about measurement dates and particle characteristics.

## Sampling geometry and localization
- Sampling points are described in a polar framework centered on the ChNPP (Chernobyl Nuclear Power Plant).
- Angle_degree provides directional information; DIST_km provides radial distance from the center.
- Notes indicate variations in sample location, including near the ChNPP shelter/sarcophagus and Warsaw-area references for certain samples.

## Particle classification and grouping
- Poland particles are grouped into three categories:
  - Group A: dominated by Ru-103 and Ru-106.
  - Group B: richer in Ru-103, Ru-106, Ce-141, Ce-144, Zr-95, Nb-95, Cs-134, Cs-137.
  - Group C: similar to Group B but with higher Ru abundance (an intermediate between A and B).
- This grouping reflects the isotope contents and helps in interpreting burnup and origin.

## Measurements and data quality considerations
- A wide panel of radionuclides is tracked with total activities and associated standard deviations (uncertainties) across gamma, alpha, and beta measurements.
- Dates of measurements enable temporal context for the activities.
- The Burnup_MW_d_kg-1 variable compresses complex activity ratios into discrete groups, aiding comparative analyses.
- Polish sample distance is noted as approximate, highlighting potential spatial uncertainty at larger scales.
- The metadata implies a need to unify data from multiple sources and formats, with attention to provenance and repeatability.

## Provisional analytical use-cases
- Classify hot particles by isotopic composition (Group A/B/C) and explore links to burnup and physical characteristics (size, form, structure).
- Investigate correlations between particle size range (MIN/MAX SIZE) and total activities of key isotopes.
- Assess spatial patterns of isotopic signatures using angular and distance coordinates relative to ChNPP.
- Model temporal evolution of activity dates and decay-adjusted activities across particles.
- Compare measurements across Polish and Chernobyl-origin particles to infer source terms and processing history.

## References
- Begichev et al. (1990): Preprint on Reactor Fuel of Unit 4 of the Chernobyl NPP.
- Kashparov et al. (1996, 1997): Formation of hot particles and assessment of annealing temperatures.
- Kuriny et al. (1993): Particle-associated Chernobyl fallout in local and intermediate zones.
- Zhurba et al. (2009): The hot particles data base and related work.

## Access, provenance, and reproducibility
- Data fields include identifiers, viewing notes, and measurement dates to support traceability.
- References anchor the dataset to established scientific work, aiding interpretability and potential replication.
- Metadata suggests uploading datasets to data portals with accompanying metadata to improve discoverability and reuse.