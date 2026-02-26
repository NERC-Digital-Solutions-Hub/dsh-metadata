# Soil protozoan diversity data from Sourhope field experiment site, Scotland, 1999-2000 [NERC Soil Biodiversity Programme]

- A collection of soil protozoa abundance and diversity data from the Sourhope field experiment in southern Scotland, collected during 1999–2000 as part of the NERC Soil Biodiversity Thematic Programme.
- Aimed at understanding the abundance, diversity and size distribution of protozoa (including naked amoebae, testate amoebae, flagellates and ciliates) and their potential roles in soil carbon and nitrogen turnover.
- Data describe protozoan communities across 25 plots within 5 experimental blocks, sampled on six occasions over the study period, with detailed metadata on sampling design and plot treatments.

## Site, sampling design and context

- Location: Sourhope Field Experiment Site, Macaulay Land Use Research Institute (now James Hutton Institute), near Kelso, southern Scotland. Grid reference NT8545019630.
- Site characteristics: mid‑altitude temperate upland grassland, base-poor damp soils; stock excluded since April 1998.
- Experimental design: 5 blocks, each with 6 main plots (total ~30 main plots, about one hectare). Sampling within 2 × 2 m subplots; three sub-samples collected per location (depth ~5 cm) with randomised sampling locations.
- Sampling timeline: six occasions between March 1999 and February 2000 (with at least one July 2000 sampling date noted in the datasets).
- Focus: enumeration and characterization of protozoan communities (live and dead tests, direct and indirect counts) and size-class distributions.

## Materials & methods highlights

- Protozoan groups studied: naked amoebae, testate amoebae, flagellates, ciliates.
- Sample processing: air-dried soil preparations, incubation and staining protocols for enumeration; extraction and counting performed in controlled lab settings (Centre for Ecology & Hydrology, Windermere).
- Quantification: abundances expressed as individuals per gram oven-dried soil; includes both direct and indirect enumeration methods and size-class based distributions.

## Data structure and formats

- Data format: Comma separated values (CSV) files.
- Datasets (described briefly):
  - Dataset 1050: All Protozoa Abundance July 2000
    - 25 plots, single sampling occasion (July 17, 2000) for sub-plot S of plot 4D.
    - Key variables: SUID; BLOCK; MAIN_PLOT; TREATMENT; SAMPLE_NUMBER; NAKED_AMOEB A; FLAGELLATES_DIRECT; FLAGELLATES_INDIRECT; FLAGELLATES_AVERAGE; TESTATE_AMOEB A_LIVE; TESTATE_AMOBA_EMPTY; CILIATES.
  - Dataset 1051: All Protozoa Abundance (March 1999 – February 2000, six occasions)
    - Re-wetted soil samples; six sampling occasions across 25 plots.
    - Key variables include SUID1, SUID2, SAMPLING_DATE, BLOCK, MAIN_PLOT, TREATMENT, and counts for NAKED_AMOEBA, FLAGELLATES_DIRECT/INDIRECT/AVERAGE, TESTATE_AMOEB A_LIVE/EMPTY, CILIATES.
  - Dataset 1052: Protozoa Species Size Distribution
    - Abundances by cell-size classes for naked amoebae, flagellates, testate amoebae, and ciliates.
    - Variables cover SIZE_RANGE; counts by group; plot/sample context (air-dried soil).
  - Dataset 1053: Protozoa Size Distribution
    - Protozoa enumeration by six sampling occasions, across size classes.
    - Variables include SAMPLING_DATE; SIZE_RANGE; abundances for NAKED_AMOBA, FLAGELLATES, TESTATE_AMOEB A, CILIATES, etc.
  - Dataset 1054: Protozoan species diversity by plot
    - Presence/absence of protozoan groups, genera, and species by plot across six occasions.
    - Variables include BLOCK; MAIN_PLOT; PROTOZOAN_GROUP; GENUS; SPECIES; SPECIES_OCCURRENCE; NUMBER_OF_PLOTS.
- Each dataset is designed to support spatial analyses at plot-level scale and temporal analyses over the six sampling occasions.

## Quality control and usage notice

- Quality control: numeric range checks, formatting checks, and logical integrity verifications are applied.
- Limitations: NERC provides no warranty on data accuracy or fitness for a particular use; no liability for use of the data.
- Data provenance: data were produced under the NERC Soil Biodiversity Programme with stated methodologies and sampling protocols; references for methods and data management are provided in the documentation.

## How this data can inform GIS-based analyses

- Spatial mapping: plot- and block-level distribution of protozoan abundances and diversity across the Sourhope site.
- Temporal analysis: six occasions allow time-series visualization of protozoan communities, including size-class dynamics.
- Taxonomic and functional insights: visualization of genus/species presence and diversity by plot, and potential relationships to soil properties or treatments.
- Data integration: CSV datasets can be joined with other soil datasets (e.g., carbon and nitrogen turnover measures) using shared keys such as BLOCK, MAIN_PLOT, SAMPLE_DATE, and SUID identifiers.

## Additional notes and references

- References for further methodological detail and data context are provided within the documentation (e.g., Scott et al., 2003; Finlay et al., 2000; Usher et al., 2006).
- The structure and metadata support metadata-driven GIS work, including traceability of sampling units and dates.