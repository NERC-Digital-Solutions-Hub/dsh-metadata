# Neuropil volumes for sensory structures in ithomiini butterflies from eastern Ecuador

## Overview
- Dataset of neuropil volumes for sensory brain structures in ithomiini butterflies (Lepidoptera, Nymphalidae, Danainae) from a single community in eastern Ecuador.
- Aimed at understanding how sensory environments shape investment in sensory brain centers.
- Includes 392 wild-caught individuals across 49 species, collected mainly in 2011–2012 and 2022; focuses on the relative fluorescent immunostaining and volumetric analyses of brain structures.
- Builds on prior work (Montgomery & Ott 2015; Wainwright & Montgomery 2022; Wainwright et al. 2024) to explore ecological influences on neuroanatomy.

## What the dataset covers
- Relative investment in sensory processing structures measured as brain volumes.
- Major structures analyzed: five primary optic lobe neuropils (medulla, lobula plate, lobula, accessory medulla, ventral lobula) forming the optic lobe; anterior optic tubercle; antennal lobe; with central brain volume used as a reference.
- Lamina not measured due to being extremely thin and frequently damaged; ventral lobula absent in many individuals (especially females).
- Volumes are log10-transformed for all measured regions; a derived "rest of central brain" (calculated by subtracting anterior optic tubercle and antennal lobe from central brain) serves as an allometric control.
- The dataset provides raw volumes (before transformation) and the derived log10-transformed values for subsequent analyses.

## Data collection and field site
- Field site: Estación Científica Yasuní, Parque Nacional Yasuní, Ecuador (approx. 0°40' S, 76°23' W) in primary lowland Amazon rainforest.
- Permits handled through Parque Nacional Yasuní and partner institutions; specimens preserved as wing vouchers; nonretained individuals IDed, sexed, and marked prior to release to avoid resampling.
- Species identification based on wing venation and locally available race ID sheets.

## Neuroanatomy measurements and imaging workflow
- Tissue preparation: dissection in HEPES-buffered saline; fixation in ZnFA; storage in methanol/DMSO; shipping to the UK for processing.
- Immunostaining: synapsin antibody (anti-SYNORF) used to label pre-synaptic regions; standard immunohistochemistry workflow including secondary antibody and extensive washes.
- Clearing and imaging: brains cleared in methyl salicylate; imaged with confocal microscopy (Leica SP5/SP5-II) across anterior and posterior sides; image stacks merged with Amira software.
- Segmentation and volume reconstruction: manual segmentation of neuropils every third section based on synapsin signal; interpolation for unsegmented sections; volumes extracted using measure statistics in Amira.
- Normalization: z-dimension adjusted to correct for imaging artifacts; volumes (for five optic lobe neuropils and two central brain structures) are log10 transformed for analyses.

## Data processing and analysis pipeline
- Neuropil volumes reconstructed for:
  - Central brain (rest of central brain via subtraction)
  - Medulla
  - Lobula plate
  - Lobula
  - Accessory medulla
  - Ventral lobula
  - Antennal lobe (olfactory)
  - Anterior optic tubercle (visual)
  - Combined optic lobe volume (sum of key visual neuropils)
- Rest of central brain used as allometric control in statistical models.
- Data preparation steps include:
  - Multiplying specific volumes by two (for paired neuropils)
  - Log10 transformation of all volumes
  - Exclusion of lamina due to measurement issues
- Dataset designed to support cross-species comparisons and ecological hypotheses about sensory investment.

## Quality control
- Multiple measures per species at the individual level.
- Excluded damaged or poorly stained samples.
- Measurements aligned with previously published methodologies (Montgomery & Ott 2016; related studies).
- Data entries include Year collected, Individual ID, Subtribe, Species, Sex, Mimicry ring, and log-transformed volumes for each neuropil.

## Data schema and variables (columns)
- Year collected
- ID (individual identifiers)
- Subtribe
- Species
- Sex
- Mimicry ring (based on Elias et al., 2008)
- log10(rest of central brain volume)
- log10(medulla volume)
- log10(lobula plate volume)
- log10(lobula volume)
- log10(accessory medulla volume)
- log10(ventral lobula volume)
- log10(antennal lobe volume)
- log10(anterior optic tubercle volume)
- log10(optic lobe volume) (combined optic lobe volumes)

## Provenance and references
- Data created as part of NERC Independent Research Fellowship NE/N014936/1.
- Related foundational works:
  - Elias et al. 2008 (mimicry and ecological niches)
  - Montgomery & Ott 2015 (brain composition related to olfactory information)
  - Wainwright & Montgomery 2022; Wainwright et al. 2024 (neuroanatomical and ecological divergence, sensory convergence)

## Reuse considerations for data leaders
- Data system fit:
  - Comprehensive metadata including collection years, taxonomic identifiers, mimicry rings, and final measured variables supports discoverability and re-use across networks.
  - Clear provenance and links to prior studies enhance traceability and comparability.
- Data quality and standards:
  - Standardized protocols across sampling periods and species enable cross-study comparisons, important for broader data ecosystems.
  - Some anatomical structures could not be measured in all individuals (e.g., lamina, ventral lobula absent in many females) which should be accounted for in analyses and documentation.
- Data gaps and granularity:
  - Variability in species sample sizes (some with very few individuals) may affect statistical power; consider weighting or caution in cross-species inferences.
- Access and governance:
  - Field permits and specimen handling details are documented; for broader reuse, ensure licensing, data sharing permissions, and repository accessibility align with data governance policies.
- Integration potential:
  - The dataset’s allometric control approach and cross-structure volume data facilitate integration with other neuroanatomy and ecological datasets, supporting broader analyses of sensory investment strategies across taxa and environments.