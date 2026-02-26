# Overview of data

- Study aim and scope
  - Describes ant colour and body size across vertical forest strata (subterranean, ground, understory, canopy) in a lowland tropical rainforest.
  - Examines spatial patterns of cuticle colour and tests predictions of three eco-geographical hypotheses (thermal-melanism, melanism-desiccation, photoprotection).
  - Includes additional intraspecific variation data and environmental measurements (soil temperature, UV-B) collected as part of the NERC HMTF Programme.

- Datasets included (six CSV files)
  - AntSpeciesData.csv: Morphological traits (colour, Weber's length) for ant assemblages across four strata and plots; includes abundance and proportional abundance; dominant colour as a single category per assemblage; colour linked to RGB/HSV values.
  - IntravarColourData.csv: Intraspecific colour variation for a subsample of 20 species; 50 specimens per species; colour recorded per specimen/part (head, mesosoma, gaster) by a single observer.
  - IntravarSizeData.csv: Intraspecific variation in Weber's length for the same 20 species as IntravarColourData.csv; 50 specimens per species.
  - SoilAbioticData.csv: Soil temperature (depth ~10 cm) recorded at 25 points per plot on a single day in October 2016.
  - UVBData.csv: UV-B radiation measured at 5 m vertical intervals on the largest sampled trees per control plot in Oct–Nov 2018, plus ground-level readings and open-area proxy readings; includes cloud cover data.
  - (Cross-file context: All data relate to the same experimental framework and plots described below.)

- Study site and experimental design
  - Location: Maliau Basin Conservation Area, Sabah, Malaysia (old-growth dipterocarp rainforest).
  - Plot setup: Twelve 50 x 50 m plots within a 42-ha area; central 50 x 50 m sampled; 4 control, 4 ant-suppression, 4 termite-suppression plots with edge-buffer and distance between plots.
  - Treatments (2014–2017): 
    - Ant suppression using two baits (Synergy Pro and imidacloprid-containing custom bait) under an integrated pest management approach.
    - Termite suppression via physical mound removal and soil treatment with imidacloprid and fipronil using treated half TPRs and tea bags; treatments re-applied semi-annually.
  - Ant colour analyses: Data for colour and size of workers collected only from control plots to describe natural spatial patterns without suppression effects.

- Data collection and methods (highlights)
  - Colour assignment: Eye-based dominant colour per species (across head, mesosoma, gaster), ignoring hair colour; Colour linked to RGB and converted to HSV.
  - Size measurement: Weber's length (pronotum-to-propodeum) with ocular micrometers; measurements to 0.01 mm; limited to worker caste.
  - Sampling design: 4 strata per plot; up to 12 individuals per species for colour in AntSpeciesData.csv; dedicated subsamples for intraspecific tests in IntravarColourData.csv and IntravarSizeData.csv.
  - Environmental measurements: Soil temperature captured once per plot in 2016; UV-B measured on canopy and ground readings in 2018; standard instruments and protocols noted (e.g., Solarmeter for UV-B).

- Data structure and key fields (summary by file)
  - AntSpeciesData.csv
    - Plot, Strata, Assemblage, Subfamily, Genus, Species
    - Abundance, Prop abund
    - Dom colour, R, G, B, h, s, v
    - Mean Weber length
  - IntravarColourData.csv
    - ID, Subfamily, Species, Vial, Strata, Trait (Head/Mesosoma/Gaster)
    - Colour, R, G, B, h, s, v
  - IntravarSizeData.csv
    - ID, Subfamily, Species, Vial, Strata, Webers length
  - SoilAbioticData.csv
    - Date, Plot, Soil temp (°C)
  - UVBData.csv
    - Date, Time, Location, Height (m), Strata, UVB (mW/cm2), Cloud cover

- GIS-relevance and potential products
  - Spatial visualization of ant assemblages and colour traits across vertical strata within plots.
  - Map-ready layers: assemblage-level colour (dominant colour per strain), species abundances, Weber's length distributions by species and strata.
  - Environmental overlays: soil temperature maps per plot, canopy vs. ground UV-B exposure, and cloud cover context.
  - Temporal framing: multi-year sampling (2014–2018) enables trend and gradient analyses along vertical microclimatic gradients.

- Considerations for use
  - Color data are visually assigned; there is an element of subjectivity.
  - Intraspecific datasets (IntravarColourData.csv, IntravarSizeData.csv) provide variation context but are limited to a subsample of 20 species.
  - Ant colour analyses are restricted to control plots; suppression effects are described for other plots but not used in the main colour analysis.
  - Coordinate-level GIS integration will rely on plot and stratum identifiers rather than precise GPS coordinates, unless supplementary location data are provided elsewhere.

- Temporal and provenance notes
  - Field data collected 2014–2016 (plots setup and ant/termite suppression); UV-B data collected 2018; soil temperature data collected in 2016.
  - Part of the NERC Human-modified tropical forest (HMTF) Programme.