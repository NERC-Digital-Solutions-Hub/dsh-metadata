# Soil protozoan diversity data from Sourhope field experiment site, Scotland, 1999-2000 [NERC Soil Biodiversity Programme]

## Overview
- Presentation of soil protozoan abundance and diversity data collected at Sourhope field site (Scotland) during 1999–2000.
- Part of the NERC Soil Biodiversity Thematic Programme, aimed at linking soil biodiversity to key ecological processes, especially carbon and nitrogen turnover.
- Data assembled from 25 plots across 5 blocks, with multiple sampling occasions, and standardised enumeration methods.

## Background and aims
- Programme established in 1999 to understand both soil biota diversity and functional roles in soil processes.
- This dataset specifically documents protozoan communities (abundance and diversity) as part of broader soil biodiversity analyses.
- Aimed to enable cross-site comparisons and integration with other dataset components (biomass, diversity, and ecosystem processes).

## Site details
- Location: Sourhope Research Station, Macaulay/Lan Use Research Institute (now James Hutton Institute), near Kelso, Southern Scotland (grid reference NT8545019630).
- Habitat: Mid-altitude temperate upland grassland; base-poor, damp mineral soils; average annual rainfall ~950 mm.
- Soils: Shallow brown forest soils with local gleying; pH 4.54–4.81; mean total soil carbon ~7.6%, nitrogen ~0.56%.
- Experimental design: 5 blocks along a downslope gradient; each block contains 6 main plots; total ~1 ha; stock excluded since 1998.

## Sampling and site protocol
- Sampling occasions: March 2, May 4, July 7, September 7, 1999 and July 17, 2000.
- Each occasion: soil collected within a 2 x 2 m sub-plot; randomised sampling locations.
- Within each sampling event: three sub-samples per designated location; depth ~5 cm; samples stored cool for lab processing.
- Testate vertical distribution: shallow cores (0–60 mm) collected for distribution profiling.

## Protozoa enumeration and analysis methods
- Testate amoebae: air-dried soil, incuba­tion, fixation with phenolated aniline blue, counting live and empty tests at 100x magnification.
- Naked amoebae and flagellates: slurry incubation, culture in nutrient agar wells, monitoring at 14 and 35 days; interpretation of positive wells for presence/absence.
- Ciliates and flagellates: slurry incubation, counts in droplets under microscope; enrichment cultures used for species identification.
- Output units: abundances expressed as numbers per gram oven-dried soil (where applicable).
- Laboratory work: Centre for Ecology & Hydrology, Windermere (Cumbria).

## Datasets included (data structure and content)
- Dataset 1050: All Protozoa Abundance July 2000 (P2130_PROTOZOA_ABUND_JULY2000.csv)
  - Variables include: SUID, BLOCK, MAIN_PLOT, TREATMENT, SAMPLE_NUMBER, NAKED_AMOEB_A, FLAGELLATES_DIRECT, FLAGELLATES_INDIRECT, FLAGELLATES_AVERAGE, TESTATE_AMOEBA_LIVE, TESTATE_AMOEBA_EMPTY, CILIATES, etc.
  - Content: enumeration of protozoa from re-wetted soil on a single occasion across 25 plots.
- Dataset 1051: All Protozoa Abundance (P2130_PROTOZOA_ABUNDANCE.csv)
  - Six sampling occasions (1999–2000) across 25 plots.
  - Variables structured similarly to 1050, with repeated measures (NAKED_AMOEBA, FLAGELLATES_DIRECT/INDIRECT, FLAGELLATES_AVERAGE, TESTATE_AMOEBA_LIVE/EMPTY, CILIATES).
- Dataset 1052: Protozoa Species Size Distribution (P2130_PROTOZOA_SPECIES_SIZE.csv)
  - Size-class distribution (12 size classes) for naked amoebae, flagellates, testate amoebae, and ciliates; includes abundance and species counts per size class.
- Dataset 1053: Protozoa Size Distribution (P2130_PROTOZOA_SIZE_DIST.csv)
  - Cell-length-based averaging across six occasions; includes naked amoeba, flagellates, testate amoebae, and ciliates with per-class abundances and species counts.
- Dataset 1054: Protozoan species diversity by plot (130_PROTOZOAN_SPEC_DIVERSITY.csv)
  - Per-plot protozoan group data (protozoan group, genus, species, species occurrence, and number of plots where detected) across six sampling occasions.
- Data structure notes: datasets conform to comma-separated values with clearly defined fields (SUIDs, sampling dates, plot/treatment metadata, abundance figures, and species-level descriptors).

## Quality control and data rights
- Quality assurance included numeric range checks, data formatting checks, and logical integrity checks.
- Data are provided with QA steps, but no warranty of accuracy or fitness for a particular purpose; no liability accepted by NERC for data use.
- Data are intended for broad reuse beyond a single output, with provisions to access underlying data used to create final outputs.

## Relevance for environment-monitoring analysts
- Demonstrates standardized data collection, processing, and storage across plots and time, enabling trend analysis of protozoan communities in soil.
- Facilitates integration with other soil biodiversity and biogeochemical datasets to evaluate ecosystem processes (carbon and nitrogen turnover).
- Data are suitable for spatial (plot-level) and temporal (six occasions) monitoring, with clear documentation of methods and QA procedures.
- Provides a clear template for converting complex field outputs into interoperable CSV datasets for environmental health assessments and policy evaluation.