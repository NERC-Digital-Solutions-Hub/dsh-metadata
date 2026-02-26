# Supporting information for Avifauna occurrence data from a longitudinal experiment in human-modified Amazonian forests affected by the 2015-16 El Niño drought and associated fires

## Overview
- Longitudinal dataset of bird occurrence across 36 forest plots along a disturbance gradient (undisturbed, logged, logged-and-burned, and secondary forests) in the Brazilian Amazon.
- Data collected in two survey periods: 2010-11 (pre-El Niño) and 2016 (post-El Niño fires).
- Same plots and sampling locations used in both periods; aim to assess impacts of human disturbance and ENSO-related fires on tropical forest bird communities.
- Sampled as part of the NERC Human-Modified Tropical Forest (HTMF) programme with multiple funding sources.

## Data access and licensing
- Data and licensing/terms of use available via the DOI: https://doi.org/10.5285/4b05caee-a3c8-46a7-b675-e5a94554bd9f

## Experimental design and sampling regime
- 36 primary forest plots categorized as:
  - Undisturbed (N=10)
  - Logged (N=10)
  - Logged-and-burned (N=10)
  - Secondary forests (N=6)
- Sampling design based on canopy disturbance from 1988–2010 satellite analyses and field assessments of fire scars and logging/charcoal.
- Surveys conducted at identical locations and with identical methods in 2010-11 and 2016.
- Each plot surveyed at three points along a 300-m transect: 0, 150, and 300 m.

## Data collection methods
- Bird records collected via two repetitions of three 15-minute, fixed-width (75 m) point counts per plot.
- Surveys occurred from 15 minutes before dawn to 09:30 on days without persistent rain or strong winds.
- Records captured by solid-state audio recorders; species identified by auditory and/or visual observation.
- Temporal and seasonal variation in vocal activity mitigated by rotating repetitions across catchments and plots.
- Permits and legal compliance:
  - Verbal permission from landowners for private properties.
  - Brazilian legal compliance for protected areas (SISBIO permits: n. 24164 and 53271 for 2010-11 and 2016, respectively).

## Data structure and content
- Data file: ECOFOR_AFIRE_RAS_birds.csv
- Field structure (Table 1 described in the document):
  - CAMP_1 or CAMP_2: survey period (2010-11 pre-El Niño; 2016 post-El Niño)
  - Plot: forest plot identifier
  - Point: sampling point within the plot (0, 150, 300 m)
  - Date and Time: date and time of record
  - Observer: recorder(s)
  - Family: taxonomic family
  - Binomial: genus and species
  - Auditory: record based on auditory observation
  - Visual: record based on visual observation
- Plot-level coordinates (Table 2):
  - Municipality (e.g., Santarém, Mojuí dos Campos, Belterra)
  - UTM_X and UTM_Y coordinates (UTM zone 21M)
  - Geographic plots identified by codes (e.g., 112_12, 160_10, etc.)

## Study region
- Santarém/Belterra/Mojuí dos Campos, Pará state, Northeastern Brazilian Amazon.
- Climate: mean annual temperature ~25°C; mean annual precipitation ~1920 mm.
- Undisturbed forests typically have canopy heights 30–40 m (emergent up to ~50 m).

## Provenance and authorship
- Study design and authors:
  - A. Lees, J. Barlow, T. Gardner designed the study.
  - J. Ferreira, E. Berenguer, F. França selected plots and coordinated landowner permissions.
  - A. Lees, N. Moura, B. Davi, C. Andertti, L. Chesini, S. Dantas collected data.
  - A. Lees, N. Moura, J. Barlow, J. Ferreira, T. Gardner, F. França interpreted results.
- Supporting information prepared to accompany Lees et al. (2018) HTMF dataset.

## Quality, limitations, and notes for reuse
- Methodological consistency maintained across the two survey periods to enable robust longitudinal comparisons.
- Data capture includes both auditory and visual detections; structure explicitly records the detection method.
- The dataset relies on precise plot locations and coordinates to enable spatial analyses across the disturbance gradient.
- Users should reference the provided DOI for licensing terms and data use requirements.

## Funding and affiliations
- NERC HTMF programme (funding sources include NERC, Darwin Initiative, EMBRAPA, CNPq, CAPES/CNPq/PELD-RAS, INCT Biodiversidade e Uso da Terra na Amazônia, Formas).

## References
- Piacentini, V., et al. Annotated checklist of the birds of Brazil; Brazilian Journal of Ornithology (cited as the taxonomic reference for species classification). DOI link provided in the document.
- Data citation: Lees, A.; Moura, N.; Franca, F.M.; Ferreira, J.N.; Gardner, T.; Berenguer, E.; Chesini, L.; Andertti, C.; Barlow, J. (2018). Avifauna occurrence data from a longitudinal experiment in human-modified Amazonian forests affected by the 2015-16 El Niño drought and associated fires. NERC Environmental Information Data Centre. DOI: 10.5285/4b05caee-a3c8-46a7-b675-e5a94554bd9f