# Overview of data

- Purpose and scope:
  - Describes spatial patterns of ant cuticle colour (lightness) across a vertical microclimatic gradient in lowland tropical rainforest.
  - Tests three eco-geographical hypotheses: thermal-melanism, melanism-desiccation, and photoprotection.
  - Data collected between 2014 and 2016 across 12 plots; analyses for ant colour variation use only data from the four control plots (no insecticide treatment).

- Data assets (six CSV files):
  - AntSpeciesData.csv: species-level colour and body size across four vertical strata and plots; includes abundance, proportional abundance, dominant colour (RGB and HSV), and mean Weber’s length.
  - IntravarColourData.csv: intraspecific colour variation for a subsample of 20 species; 50 specimens per species; colour recorded per body part (head, mesosoma, gaster) and per specimen; colour assigned by eye; supporting RGB/HSV values.
  - IntravarSizeData.csv: intraspecific variation in Weber’s length for the same 20 species; 50 specimens per species; Weber’s length measurements.
  - SoilAbioticData.csv: soil temperature (depth ~10 cm) at 25 points within each plot, data collected in October 2016.
  - UVBData.csv: UV-B radiation measurements at 5 m vertical intervals from ground to canopy in 2018; includes ground and canopy proxy measurements; additional cloud cover data.
  - There are accompanying methodological details clarifying data collection, processing, and measurement techniques.

- Experimental design and sampling:
  - Location: old-growth dipterocarp rainforest, Maliau Basin Conservation Area, Sabah, Malaysia.
  - Plot arrangement: 12 plots (50 x 50 m) within 42-ha area, with 80 x 80 m treated area; central 50 x 50 m sampled to avoid edge effects.
  - Treatments: 4 control, 4 ant suppression, 4 termite suppression; maintained Oct 2014–Oct 2017.
  - Ant suppression: two bait types (Synergy Pro® and Whiskas soaked in sugar with imidacloprid).
  - Termite suppression: physical mound removal + soil treatment with imidacloprid; use of poisoned toilet paper rolls and tea bags with fipronil to target wood-feeding termites.
  - All colour and size data for the colour variation analysis come from the four control plots.

- Data collection and measurement methods:
  - Ant colour (AntSpeciesData and IntravarColourData):
    - Colour classified categorically by eye against a predetermined colour set; focus on cuticle colour (hair colour ignored).
    - Colour recorded for head, mesosoma, and gaster for up to 12 individuals per assemblage; single dominant colour per species (modal colour across body parts and individuals).
    - RGB values assigned from a colour wheel using Paint.NET; RGB converted to HSV (h, s, v).
    - Size measured as Weber’s length (distance between specified anatomical points) to 0.01 mm; measured on the entire mesosoma using high magnification; analyses based on worker castes.
  - Intraspecific variation (IntravarColourData and IntravarSizeData):
    - Subsample of 20 species; 50 specimens per species; colour recorded by a single observer; species selection criteria ensure coverage across strata, size, and genera.
  - Soil abiotic data (SoilAbioticData):
    - Soil temperature recorded on a single day per plot at ~10 cm depth using a digital probe.
  - UV-B radiation (UVBData):
    - Measurements taken in Oct–Nov 2018 on the largest trees in control plots at 5 m intervals; readings also collected at ground points and a sky-open canopy proxy region.
    - Instrument: Solarmeter Model 6.0; readings in mW/cm2; documentation includes cloud cover estimates.

- Data structure and key fields (high-level):
  - AntSpeciesData.csv: Plot, Strata, Assemblage, Subfamily, Genus, Species, Abundance, Prop abund, Dom colour, R, G, B, h, s, v, Mean Webers length.
  - IntravarColourData.csv: ID, Subfamily, Species, Vial, Strata, Trait (Head/Mesosoma/Gaster), Colour, R, G, B, h, s, v.
  - IntravarSizeData.csv: ID, Subfamily, Species, Vial, Strata, Webers length.
  - SoilAbioticData.csv: Date, Plot, Soil temp.
  - UVBData.csv: Date, Time, Location, Height, Strata, UVB, Cloud cover.
  - Strata definitions: Subterranean (24 cm below ground), Ground, Understory (below first branch), Canopy (above first branch).

- Temporal and spatial coverage:
  - Ant colour and size data: sampling across four control plots, 2014–2016 (with parallel insecticide experiments 2014–2017); central sampling area designed to minimize edge effects.
  - Soil temperature: October 2016.
  - UV-B: October–November 2018.
  - Spatial gradient: vertical strata from subterranean to canopy within each plot; four plots per treatment, but colour analysis uses controls only.

- Data governance, quality, and caveats:
  - Colour data involve expert-based categorical classification and measurement subjectivity; transparent documentation of colour assignment and RGB/HSV conversion provided.
  - Intraspecific variation studies rely on limited subsamples (20 species) with fixed specimen counts.
  - Measurements include precise anatomical references and methods; units and measurement precision explicitly stated (mm for Weber’s length, 0.01 mm for Weber’s length, etc.).
  - Data organization enables cross-dataset linking by Plot, Strata, Species, and Vial/ID identifiers.
  - Data provenance acknowledges authors and contributors responsible for collection and interpretation.

- Provenance and potential reuse:
  - Part of broader ecological and phyto-mysological investigation; credits listed for data collection and interpretation.
  - Datasets provide a rich resource for trait-based analyses (colour, size) across vertical habitat gradients, integration with abiotic environmental data (soil temperature, UV-B) for testing eco-geographical hypotheses.
  - Suitable for data-system improvements: metadata completeness, standardization across trait datasets, and integration within broader data networks for cross-study reuse.