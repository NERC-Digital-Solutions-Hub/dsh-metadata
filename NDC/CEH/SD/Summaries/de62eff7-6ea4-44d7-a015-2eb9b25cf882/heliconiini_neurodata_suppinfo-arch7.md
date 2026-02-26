# Taxonomic data, neuropil volume measurements, and mushroom body calyx kenyon cell and synapse count data of Heliconiini butterflies, Central and South America, 2012-2016

## Overview
- Dataset of neuropil volumes, Kenyon cell counts, and synapse counts in the mushroom body calyx of Heliconiini butterflies.
- Purpose: enable analyses of evolutionary expansion of mushroom body size in Heliconius butterflies and relatives; associated with Couto et al. (2023).
- Measurements include mushroom body volumes, central brain, medulla, antennal lobe, Kenyon cell estimates, synapse density, and microglomeruli.

## Geographic and temporal scope
- Geographical coverage: Central and South America (multiple countries and localities).
  - Costa Rica: La Selva Biological Station, Las Cruces Biological Station, Le Leona eco-lodge, Orosí (various elevations).
  - Panama: Pipeline Road, Gamboa; Soberanía National Park.
  - French Guiana: Cayenne area (urban sites and forest edge habitats).
  - Ecuador: Estación Científica Yasuní, Parque Nacional Yasuní (Orellana), Vilcabamba, Balsas Canton (Southern Ecuador).
  - Peru: Tarapoto region (Escalera, Schucshuyacu, Abra Patricia, cataracts and other sites) and Excalera (2014–2015).
- Elevation range: sea level to ~2500 m.
- Sampling approach: wild-caught wild individuals with permits, plus additional insectary-reared specimens for some analyses.
- Temporal span: data collected 2011–2016, with published analyses in 2023.

## Data files and key variables
- Table 1: Heliconiini_NeuroData_Table1_Neuropil_Volumes.csv
  - Fields include: GENUS, CLADE, SPECIES, SEX, COUNTRY OF ORIGIN; VOLUMES for Visual system (VISUAL), Central Brain (CBR), Medulla (MEDULLA), Ventral Lobes (VLOB), Antennal Lobe (AL), Mushroom Bodies (MBCA, MBPED, MBLOBES, MBLOPE/LBOPE), TOTAL MB, rCBR (rest-of-Central Brain), BODY SIZE traits (BODY LENGTH, WINGSPAN, BODY MASS).
- Table 2: Heliconiini_NeuroData_Table2_Kenyon_Cell_Counts
  - Fields include: INDIVIDUALS, SPECIES, CALYX VOLUME, ESTIMATED KENYON CELL NUMBER, LOG10(CALYX VOLUME), LOG10(KC NUMBER), KC DENSITY.
- Table 3: Heliconiini_NeuroData_Table3_Synapse_Counts
  - Fields include: SYNAPSE COUNTS (two variants), AGE, SPECIES, CALYX VOLUME, SYNAPSE NUMBER/CUBE, SYNAPSE DENSITY, ESTIMATED SYNAPSE NUMBER; MICROGLOMERULI COUNTS, MICROGLOMERULI DENSITY, etc.
- Metadata and processing details described (in-line with population/phylogenetic scope and measurement methods).

## Methods (highlights relevant to geospatial data use)
- Sampling and specimen handling
  - Wild-caught across diverse habitats and elevations to ensure phylogenetic breadth.
  - Additional insectary-reared specimens for certain cellular analyses.
- Fixation and preservation
  - Zinc-formalin fixative; methanol/DMSO dehydration; long-term storage in methanol.
- Neuropil and neuronal staining
  - Anti-SYNORF1 for neuropil; HRP for Kenyon cell identification; DAPI nuclear staining.
- Neuronal tracing and sectioning
  - Dextran-based neuronal tracers injected into calyx, antennal lobe, and optic lobe regions to map visual/olfactory projections.
  - 80 µm thick brain sections prepared; 3D reconstruction via serial sectioning.
- Imaging and 3D analysis
  - Confocal microscopy (10X and 63X objectives) with multi-channel acquisition; 3D segmentation in Amira; volume and density estimation.
  - Calibration corrections for refractive index differences using calibration beads.
  - Kenyon cell density (via nuclei counts in 25 x 25 x 15 µm cubes) multiplied by cluster volume to estimate total Kenyon cells per hemisphere.
  - Synapse density and microglomeruli counts via 3D Object Counter; subset analyses with manual counts where applicable.
- Quality control
  - Damaged or poorly stained samples excluded; methods aligned with Montgomery et al. 2016; data derived from 318 wild-caught individuals (41 species) plus insectary-reared subsets.

## Practical notes for GIS-focused use
- Geospatial relevance
  - Rich, multi-country sampling with explicit locality names and elevation context; suitable for linking brain structure data to habitat, climate, and phylogenetic variables.
  - Country-of-origin and site-level metadata enable spatial analyses of brain morphology across environmental gradients.
- Data structure for mapping
  - Three primary numeric datasets (volumes, Kenyon cell counts, synapse/microglomeruli data) linked to species, individuals, and locations.
  - Potential to join with external GIS layers (habitat type, altitude, land cover, protected areas) for landscape-genomic or brain morphology-environment studies.
- Suitability for cross-disciplinary analyses
  - Combines neuroanatomical measurements with species-level and location metadata, enabling analyses of evolutionary neuroanatomy in a geospatial context.

## References
- Couto A, et al. Rapid expansion and visual specialisation of learning and memory centres in the brains of Heliconiini butterflies. Nature Communications. 2023.
- Montgomery SH, Merrill RM, Ott SR. Brain composition in Heliconius butterflies, posteclosion growth and experience-dependent neuropil plasticity. J Comp Neurol. 2016.