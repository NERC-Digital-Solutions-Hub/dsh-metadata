# EIDC dataset 2: Caterpillar masses from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

- Purpose and context
  - Dataset accompanies methods from the Science Advances study on street lighting impacts on local insect populations.
  - Aims to compare caterpillar communities in lit vs unlit transects across two habitat types (hedgerows and grass margins) using matched-pairs design, to infer long-term effects of artificial light at night (ALAN).

- Field sites and matching design
  - 26 lit-unlit site pairs (plus 1 triplet) across Oxfordshire, Buckinghamshire, and Berkshire, UK.
  - Habitat types: hedgerows and grass margins; lit and unlit sections separated by ≥60 m (median 118 m).
  - Site matching ensured comparable habitat: same transect length, similar vegetation structure, hedgerow trees presence, and comparable agricultural management.
  - Lit transects illuminated with LED, HPS, or LPS for at least five years prior to sampling; all sites fully lit through the night during the study.

- Lighting treatments and measurements
  - Light types: LED (n=14), HPS (n=11), LPS (n=2).
  - Lux measurements taken at five points along each transect at heights relevant to caterpillars: 1.25 m (hedgerows) and 0.25 m (grass margins).
  - Grass margins also assessed with a spectrometer; Correlated Colour Temperature (CCT) values reported for LED, HPS, and LPS (LED 2700–4000 K; HPS ~2200 K; LPS ~1800 K).
  - Unlit transects estimated to be <0.01 lux on overcast nights.

- Caterpillar sampling and processing
  - Two sampling methods:
    - Hedgerow beating (spring) for woody feeders; 3 points per transect, 14 m segments; use drainpipes or beating trays; five strikes per segment.
    - Grass margins sweep netting (late autumn/winter) for noctuid caterpillars on grasses and low-growing plants; typically 14 m transects; repeats across multiple visits due to low caterpillar counts.
  - Sampling windows chosen to minimize phenological artefacts (late spring and early spring for hedgerows; winter for grass margins).
  - Sampling cadence: usually multiple visits per site; attempts ensured lit and unlit transects were sampled equally.
  - Specimen handling: all caterpillars weighed (mg); total counts: 826 grass-margin and 1021 hedgerow caterpillars; 34 day-flying Lepidoptera included due to potential nocturnal larval stages; provisional identifications used, with 20 hedgerow taxonomic units and 16 grass-margin units.
  - Mass distribution: grass margin caterpillars mean 98 mg; hedgerow caterpillars mean 43 mg.

- Data management and quality control
  - Field data collected on standardized forms and entered into Excel with dropdowns to ensure consistency; entries double-checked for errors.
  - Samples kept at -20°C (with Covid-19 restrictions affecting retention in 2020).
  - Data linked to unique site and visit identifiers; careful matching criteria maintained to ensure valid lit vs unlit comparisons.
  - Taxonomic identifications performed by the lead author using prior knowledge and literature.

- Data structure and content
  - Main data files:
    - Boyes_et_al_2021_hedgerows_mass.csv (hedgerow caterpillar masses)
    - Boyes_et_al_2021_grass_mass.csv (grass margin caterpillar masses)
  - Key columns (examples):
    - Visit_ID, Site_ID, Treatment (unlit, LED, HPS, LPS), Sample_number, Provisional_ID, ID2, Caterpillar_mass_mg, DaysSince (grass margins)
  - Field site data file:
    - Contains site-level metadata: sampling method (Grass margin, Hedgerow, or both), light type, transect centroids, geographic coordinates, hedge characteristics, vegetation metrics, distance between transects, urbanization metrics at 100/250/500 m radii, and related coverage statistics.
  - Linkage between datasets enables analyses of ALAN effects on prey communities across lighting types, with metadata on habitat, location, and surrounding urbanization.

- Relevance for monitoring and policy
  - Provides standardized, quality-controlled measures of caterpillar abundance and size under varied street-lighting conditions.
  - Enables assessment of ALAN impacts across habitat types and lighting technologies, informing environmental health monitoring and policy decisions on street lighting.
  - Demonstrates data governance practices (transparent methods, detailed metadata, open data potential, and explicit data structure), addressing typical monitoring framework challenges such as data gaps, interoperability, and clear communication of results.
  - Supports cross-study comparisons by aligning with broader literature on light pollution and insect populations.

- References
  - Boyes, D.H., Evans, D.M., Fox, R., Parsons, M.S., & Pocock, M.J.O. (2021) Is light pollution driving moth population declines? A review of causal mechanisms across the life cycle. Insect Conservation and Diversity, 167-187.
  - Longcore, T. & Rich, C. (2004) Ecological light pollution. Frontiers in Ecology and the Environment, 2, 191-198.
  - Maudsley, M., Seeley, B., & Lewis, O. (2002) Spatial distribution patterns of predatory arthropods within an English hedgerow in early winter in relation to habitat variables. Agriculture, Ecosystems & Environment, 89, 77-89.
  - Merckx, T. & Van Dyck, H. (2019) Urbanization-driven homogenization is more pronounced and happens at wider spatial scales in nocturnal and mobile flying insects. Global Ecology and Biogeography, 28, 1440-1455.
  - Porter, J. (2010) Colour Identification Guide to Caterpillars of the British Isles: (Macrolepidoptera). Apollo Books.
  - Staley, J.T. et al. (2016) Little and late: How reduced hedgerow cutting can benefit Lepidoptera. Agriculture, Ecosystems & Environment, 224, 22-28.