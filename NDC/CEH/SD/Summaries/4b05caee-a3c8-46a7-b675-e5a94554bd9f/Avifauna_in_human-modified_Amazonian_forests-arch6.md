# Supporting information for Avifauna occurrence data from a longitudinal experiment in human-modified Amazonian forests affected by the 2015-16 El Niño drought and associated fires

- Overview
  - Longitudinal dataset of bird occurrence across 36 forest plots in Pará, Brazil, spanning a gradient of prior human disturbance and including plots burned during the 2015-16 El Niño drought.
  - Data collected in 2010-2011 (pre-El Niño) and 2016 (post-El Niño, about 12 months after fires) as part of the NERC HTMF program.
  - The dataset aids understanding of how human- and climate-induced stressors influence tropical forest biodiversity.
  - Primary data file: ECOFOR_AFIRE_RAS_birds.csv; associated plot coordinates provided in Table 2; licensing and reuse information available via the DOI link.

- Study region
  - Santarém/Belterra/Mojuí dos Campos municipalities, Pará state, Northeastern Brazilian Amazon.
  - Climate: mean annual temperature ~25°C; mean annual precipitation ~1920 mm.
  - Forests range from undisturbed primary canopies (30–40 m) to disturbed and secondary forests.

- Experimental design and sampling regime
  - 36 primary forest plots categorized by disturbance: undisturbed (N=10), logged (N=10), logged-and-burned (N=10), and secondary forests (N=6).
  - Plots selected based on canopy disturbance history (1988–2010) and prior fire/logging assessments.
  - Two survey periods:
    - CAMP_1 (2010–11): ~6 years before ENSO-related degradation.
    - CAMP_2 (2016): ~12 months after ENSO fires.
  - Surveys conducted at identical locations and using the same sampling protocols in both periods.

- Data collection methods
  - Faunal surveys along 300-m forest plots, with three sampling points per plot (0, 150, 300 m).
  - At each point: two repetitions of three 15-minute, 75-m fixed-width point counts.
  - Survey window: before dawn to 09:30, on days without persistent rain or strong winds.
  - Observations recorded via audio and/or visual detections; recordings captured with solid-state recorders.
  - Temporal/seasonal variation in bird vocal activity minimized by rotating repetitions across catchments and plots.
  - Permitting: verbal permissions from landowners; official surveys in protected areas per Brazilian law and SISBIO permits (2010–11 and 2016).

- Data structure and content (ECOFOR_AFIRE_RAS_birds.csv)
  - Key fields include:
    - CAMP_1 / CAMP_2: survey period (pre- vs post-El Niño)
    - Plot: forest plot identifier
    - Point: sampling point within the plot
    - Date / Time: when the record was made
    - Observer: recorder (e.g., A. Lees, J. Barlow, etc.)
    - Family: family classification
    - Binomial: genus and species
    - Auditory / Visual: method of detection
  - The dataset records species occurrences (sightings and/or audios) across all plots and both time periods.

- Plot-level geographical coordinates
  - Table 2 provides coordinates for each plot, including:
    - Municipality (e.g., Santarém, Belterra, Mojuí dos Campos)
    - UTM_X and UTM_Y (UTM zone 21M)
  - Example plots span multiple municipalities with precise X/Y coordinates for spatial analyses.

- Access, licensing, and reuse
  - Data and licensing information available at the dataset DOI: https://doi.org/10.5285/4b05caee-a3c8-46a7-b675-e5a94554bd9f
  - Supporting information and citation details provided within the data centre entry.
  - Data collected under funding and collaboration from NERC HTMF, Darwin Initiative, EMBRAPA, CNPq, CAPES/CNPq/PELD-RAS, INCT Biodiversidade e Uso da Terra na Amazônia, and Formas (Sweden).

- Context and references
  - Study design and taxonomy referenced to Piacentini et al. (2015) for Brazilian bird checklist framework.
  - The data support biodiversity assessments under climate- and human-driven disturbance scenarios in tropical forests.