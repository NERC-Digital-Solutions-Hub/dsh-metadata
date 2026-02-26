# Overview of data

- Aim and scope
  - Describe spatial patterns of ant colour across a vertical microclimatic gradient (subterranean to canopy) in lowland tropical rainforest.
  - Test three eco-geographical hypotheses: thermal-melanism, melanism-desiccation, and photoprotection.
  - Use multi-dataset, multi-plot data collected between 2014 and 2018 to link ant traits with environmental context.

- Datasets included
  - AntSpeciesData.csv: morphometric colour (dominant cuticle colour) and Weber's length for worker ants across four strata and four plots; includes abundance and proportional abundance.
  - IntravarColourData.csv: intraspecific colour variation for a subsample of 20 species (50 specimens per species) recorded for Head, Mesosoma, or Gaster.
  - IntravarSizeData.csv: intraspecific variation in Weber's length for the same subsample of 20 species (50 specimens per species).
  - SoilAbioticData.csv: soil temperature (≈10 cm depth) recorded at 25 points per plot in 2016.
  - UVBData.csv: UV-B radiation measured at 5 m vertical intervals from ground to canopy in 2018, plus ground-level readings and open-area proxy; cloud cover recorded.

- Experimental design and context
  - Location: Maliau Basin Conservation Area, Sabah, Malaysia (old-growth dipterocarp rainforest).
  - Plot scheme: 12 plots (50 m x 50 m) within a 42-ha area; central 50 x 50 m sampled to avoid edge effects; 4 control, 4 ant suppression, 4 termite suppression plots.
  - Treatments (Oct 2014–Oct 2017): 
    - Ant suppression via two bait types (Synergy Pro® and imidacloprid in sugar solution-treated bait) using grid-based deployments and integrated pest management.
    - Termite suppression via removal of mounds plus application of imidacloprid-containing solutions and fipronil-treated materials (to target wood-feeding termites) using half toilet paper rolls and tea bags.
  - For the ant colour analysis of this dataset, only data from the four control plots were used to study natural variation without treatment interference.

- Data collection and measurement approaches
  - Colour assessment (AntSpeciesData.csv and IntravarColourData.csv):
    - Dominant colour assigned by eye across head, mesosoma, and gaster; colour focused on cuticle (hair colour ignored).
    - RGB values extracted from image software and converted to HSV (h, s, v) values.
    - Intra-species colour variation tested by sampling 50 specimens per species (20 species) by a single observer.
  - Morphometrics (Weber’s length):
    - Size measured as Weber’s length (pronotum pronodorsal margin to propodeum posterior margin) to 0.01 mm using calibrated ocular micrometers; data based on worker ants.
  - Environmental context (SoilAbioticData.csv and UVBData.csv):
    - Soil temperature measured on a single day in Oct 2016 at 25 points per plot (≈10 cm depth).
    - UV-B radiation measured in 2018 at multiple heights (canopy to ground) with supplementary ground/open-area readings; cloud cover recorded.

- Data structure and metadata
  - AntSpeciesData.csv keys
    - Plot, Strata, Assemblage, Subfamily, Genus, Species, Abundance, Prop abund, Dom colour, R, G, B, h, s, v, Mean Weber length.
  - IntravarColourData.csv keys
    - ID, Subfamily, Species, Vial, Strata, Trait (Head/Mesosoma/Gaster), Colour, R, G, B, h, s, v.
  - IntravarSizeData.csv keys
    - ID, Subfamily, Species, Vial, Strata, Webers length.
  - SoilAbioticData.csv keys
    - Date, Plot, Soil temp.
  - UVBData.csv keys
    - Date, Time, Location, Height, Strata, UVB, Cloud cover.
  - The dataset provides explicit column definitions and measurement protocols to support reuse and integration with other monitoring data.

- Data quality, limitations, and governance considerations
  - Strengths:
    - Multi-layer data linking ant traits with vertical habitat gradients and abiotic factors (soil temperature, UVB, cloud cover).
    - Detailed trait measurements (dominant colour, intraspecific variation, body size) with standardized methods.
    - Clear documentation of sampling design, plot layout, and measurement procedures.
  - Limitations and caveats:
    - Dominant colour determined by visual assessment; potential observer bias and reliance on a single observer for IntravarColourData.
    - Intraspecific variation samples are limited to 20 species and 50 specimens per species, with measurements taken on a subset of body parts.
    - Soil and UVB data are snapshot measurements (single-day for soil; specific survey periods for UVB), which may not capture temporal variability.
    - Ant colour analyses restricted to control plots, which may limit generality across treatments.
  - Governance and reuse considerations:
    - Data are richly described with metadata, promoting reuse and cross-study linking, though licensing and access specifics are not detailed in the descriptions.
    - Provenance and investigators are cited, supporting traceability and proper attribution in monitoring frameworks.