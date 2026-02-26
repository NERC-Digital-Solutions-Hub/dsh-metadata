# Overview of data

- This document describes a multi-dataset study on ants in lowland tropical rainforest, focusing on colour (cuticle lightness) and body size across vertical strata, and testing predictions from three eco-geographical hypotheses: thermal-melanism, melanism-desiccation, and photoprotection.
- Datasets cover interspecific patterns and intraspecific variation, plus abiotic environmental context (soil temperature and UV-B radiation).
- Data were collected across four experimental plots (within a 12-plot setup) in Maliau Basin, Sabah, Malaysia, between 2014 and 2018 as part of the NERC HMTF Programme. The ant-colour focus uses data from the four central control plots.

## Study area, design and treatments

- Location: Maliau Basin Conservation Area, Sabah, Malaysia (lowland old-growth dipterocarp rainforest).
- Experimental setup (Oct 2014):
  - 12 plots within a 42-hectare area, each 50 x 50 m, with 15 m buffers; central 50 x 50 m sampled to avoid edge effects.
  - Plot roles: 4 control, 4 ant-suppression, 4 termite-suppression; at least 100 m between plots.
  - Ant-suppression: two baits (Synergy Pro® and imidacloprid-laced Whiskas) with integrated pest management.
  - Termite-suppression: removal of mounds and soil treatment with imidacloprid; use of poisoned toilet paper rolls and tea bags with fipronil to target wood-feeding termites.
  - Ant and termite suppression maintained through Oct 2017; the ant-colour analysis uses data from the four control plots.
- Abiotic data collection:
  - Soil temperature: measured in Oct 2016 at 25 points per plot (depth ~10 cm).
  - UV-B radiation: measured in Oct–Nov 2018 on canopy trees (5 m intervals) and ground-level readings (random points), with additional open-area proxy readings.

## Datasets included and their contents

- AntSpeciesData.csv
  - Inter-species assemblage data across four strata and plots.
  - Columns include Plot, Strata, Assemblage, Subfamily, Genus, Species, Abundance, Prop abund, Dom colour, RGB, HSV values, and Mean Weber’s length.
  - Colour classified by eye as a dominant colour across head/mesosoma/gaster; Weber’s length measured on workers to 0.01 mm.

- IntravarColourData.csv
  - Intraspecific colour variation for 20 species.
  - 50 specimens per species; colour recorded for head/mesosoma/gaster from a single observer.
  - Columns include ID, Subfamily, Species, Vial, Strata, Trait (Head/Mesosoma/Gaster), Colour, RGB, HSV (h, s, v).

- IntravarSizeData.csv
  - Intraspecific size variation (Weber’s length) for 20 species (same specimens as IntravarColourData).
  - Columns include ID, Subfamily, Species, Vial, Strata, Webers length.

- SoilAbioticData.csv
  - Soil temperature data (October 2016) at 25 points per plot.
  - Columns: Date, Plot, Soil temp (°C).

- UVBData.csv
  - UV-B radiation data (October–November 2018) at canopy and ground levels.
  - Columns: Date, Time, Location (plot or Open), Height (m above ground), Strata, UVB (mW/cm2), Cloud cover (%).

## Key measurement methods and data quality

- Colour and size:
  - Colour: dominantly assigned by eye, based on cuticle colour (ignoring hair colour); RGB values obtained from Paint.NET and converted to HSV (h, s, v).
  - Size: Weber's length measured with ocular micrometers; recorded to the nearest 0.01 mm; measurements taken on the entire mesosoma under high magnification.
- Intraspecific data:
  - IntravarColourData.csv and IntravarSizeData.csv sample 20 species with 50 specimens each, selected to cover stratum diversity and size/lightness range.
- Abiotic measurements:
  - Soil temp: single-day measurement per plot at ~10 cm depth using digital probe.
  - UV-B: readings at multiple vertical heights and random points to capture canopy vs ground exposure; readings taken near solar noon.

## Temporal and spatial coverage

- Spatial:
  - 12 plots in a 42-ha area; central 4 plots used for the ant-colour analysis in this description.
  - Strata sampled: Subterranean, Ground, Understory, Canopy.
- Temporal:
  - Ant/colour data: collected 2014–2016 (with suppression plots through 2017; colour-focused sampling on control plots).
  - Intraspecific colour/size data: same specimens as IntravarColourData.csv (no explicit separate years listed).
  - Soil temperature: October 2016.
  - UV-B radiation: October–November 2018.

## How this supports environmental monitoring and data reuse

- Standardised, multi-layer environmental dataset:
  - Combines biological trait data (colour, size) with abiotic context (soil temperature, UV-B) across vertical habitat gradients.
  - Facilitates testing of eco-geographical hypotheses related to environmental stressors (temperature, desiccation, photoprotection) and trait variation.
- Data quality and accessibility:
  - Data are organized into clearly described CSV files with explicit column definitions.
  - Emphasizes verification, quality assurance, and documentation of data transformations and methods.
  - Provides opportunities to integrate datasets (e.g., linking ant assemblages with soil and UV-B context) to enhance insights beyond single-use analyses.
- Relevance to policy and monitoring:
  - Demonstrates how standardized environmental datasets can support longitudinal monitoring of ecological health and trait-environment relationships across spatial scales.
  - Highlights practical considerations for data sharing and reuse in monitoring programs (dataset interoperability, metadata detail, and cross-dataset linkage).

## Notes on limitations and considerations

- Colour data rely on manual, eye-based classification, which may introduce observer bias; complemented here by quantitative RGB/HSV values.
- Intraspecific datasets sample a subset of species (20) and individuals (50 per species), which may limit estimates of full intraspecific variation.
- Some datasets cover different timeframes (2014–2016 for ant-colour across plots vs. 2016 soil data and 2018 UV-B data), which should be accounted for in time-series or cross-dataset analyses.