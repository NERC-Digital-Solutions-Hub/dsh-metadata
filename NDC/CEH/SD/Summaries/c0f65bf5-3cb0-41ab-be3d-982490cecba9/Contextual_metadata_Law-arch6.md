# Overview of data

- Purpose and scope
  - Describes datasets collected to study ant colour and body size across a vertical microclimatic gradient in lowland tropical rainforest, and to test eco-geographical hypotheses (thermal-melanism, melanism-desiccation, photoprotection).
  - Includes environmental context data (soil temperature and UV-B radiation) to enable integrated analyses of colour, size, abundance, and microhabitat conditions.
  - Data were collected in 2014–2018 within the Maliau Basin Conservation Area, Sabah, Malaysia; analysis of ant colour variation uses data from central control plots.

- Datasets included
  - AntSpeciesData.csv
    - Morphological and colour data for ants across four vertical strata (Subterranean, Ground, Understory, Canopy) and four plots.
    - Abundance and proportional abundance by assemblage; dominant colour per species; RGB and HSV values; mean Weber's length per species.
    - Based on worker castes; colour assigned by eye to a pre-determined colour set; colour wheel values converted to RGB/HSV.
  - IntravarColourData.csv
    - Intraspecific colour variation for a subsample of 20 species.
    - 50 specimens per species; colour recorded for Head, Mesosoma, or Gaster; single observer; RGB/HSV values included.
  - IntravarSizeData.csv
    - Intraspecific variation in Weber's length for the same 20 species as IntravarColourData.csv.
    - Weber’s length recorded for 50 specimens per species.
  - SoilAbioticData.csv
    - Soil temperature (10 cm depth) recorded at 25 points per plot in October 2016.
    - One-date measurement per plot; date and plot identifier included.
  - UVBData.csv
    - UV-B radiation measured in 2018 at 5 m vertical intervals from ground to canopy on largest sampled trees within control plots.
    - Ground readings at 12 random points plus readings in an open area as canopy proxy; data include date, time, location, height, strata, UV-B value, and cloud cover.

- Experimental design and context
  - Study area: old-growth dipterocarp rainforest in Maliau Basin, Sabah, Malaysia.
  - Plots: 12 plots (50 x 50 m) with 4 control, 4 ant suppression, 4 termite suppression; sampling focused on central 50 x 50 m to avoid edge effects.
  - Treatments: ant suppression using two baits (Synergy Pro and imidacloprid via custom bait) and termite suppression using mound removal plus soil-applied pesticides (imidacloprid and fipronil via treated half toilet paper rolls and tea bags); maintained until Oct 2017. For the ant colour variation analysis, only data from control plots were used.
  - Data collection roles: S.J. Law, H.M. Griffiths, L.A. Ashton involved in data collection; multiple researchers contributed to interpretation.

- Methods and measurement details
  - Colour and size (AntSpeciesData.csv)
    - Colour classification: eyes used to assign a single dominant colour per species (modal across body parts and specimens); colour linked to RGB values from Paint.NET and converted to HSV.
    - Size: Weber’s length measured as the distance between defined anatomical margins; measurements to nearest 0.01 mm with stereomicroscopes and ocular micrometers; analyses focused on worker caste.
  - Intraspecific variation (IntravarColourData.csv, IntravarSizeData.csv)
    - Colour recorded for 50 specimens per species, for 20 species; colour recorded for head/mesosoma/gaster; colour by a single observer.
    - Size data drawn from same specimens used for colour tests.
  - Environmental context (SoilAbioticData.csv, UVBData.csv)
    - Soil temperature: measured once per plot in Oct 2016 at 10 cm depth using digital probe.
    - UV-B: measured Oct–Nov 2018 on large trees within control plots (and open ground proxy readings); instrument details and wavelengths noted; cloud cover recorded.

- Data structure and fields (high-level)
  - AntSpeciesData.csv: Plot, Strata, Assemblage, Subfamily, Genus, Species, Abundance, Prop abund, Dom colour, RGB (R, G, B), HSV (h, s, v), Mean Weber length.
  - IntravarColourData.csv: ID, Subfamily, Species, Vial, Strata, Trait (Head/Mesosoma/Gaster), Colour, RGB, HSV.
  - IntravarSizeData.csv: ID, Subfamily, Species, Vial, Strata, Webers length.
  - SoilAbioticData.csv: Date, Plot, Soil temp.
  - UVBData.csv: Date, Time, Location, Height, Strata, UVB, Cloud cover.
  
- How this supports data use and integration
  - Enables analysis of spatial patterns in ant colour and size across vertical strata and plots, testing ecological hypotheses about colour adaptation.
  - Facilitates cross-dataset analyses by combining morphometrics, colour data, abundance, and environmental variables (soil temperature, UV-B).
  - Supports self-serve data exploration and dashboarding opportunities (e.g., by plotting colour distributions by strata, comparing intraspecific variation, linking environmental factors to colour or size).

- Considerations and limitations
  - Colour classification is eye-based and subject to observer bias; IntravarColourData uses a single observer, which may affect comparability.
  - Intra-plot design: data for colour/size derived from control plots only for the main analysis; environmental data collected at specific times/dates (single-day soil temperature; UV-B across October–November 2018) which may limit temporal interpretation.
  - Data provenance and credit: collected as part of the NERC Human-modified tropical forest (HMTF) Programme; several authors responsible for collection and interpretation.