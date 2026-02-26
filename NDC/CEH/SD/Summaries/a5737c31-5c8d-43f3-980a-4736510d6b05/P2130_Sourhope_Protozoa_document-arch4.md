# Soil protozoan diversity data from Sourhope field experiment site, Scotland, 1999-2000 [NERC Soil Biodiversity Programme]

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999–2000) focused on understanding soil biodiversity and the functional roles of soil organisms.
- This dataset describes protozoan abundance and diversity at the Sourhope field experiment site, with links to soil carbon and nitrogen turnover processes.
- Data are organized into multiple datasets (1050–1054) with detailed metadata and methods; lab work conducted at the Centre for Ecology & Hydrology, Windermere.

## Site and study design
- Location: Sourhope field experiment site, Macaulay Land Use Research Institute (now James Hutton Institute), near Kelso, Scotland.
- Site characteristics: mid-altitude temperate upland grassland, base-poor mineral soils, approx. 950 mm annual rainfall; vegetation dominated by Agrostis capillaris.
- Experimental design: 5 replicate blocks arranged downslope; each block contains 6 main plots (30 plots total); sampling occurred across 1999–2000.
- Treatments (as indicated in the datasets): Nitrogen & Lime, Lime, Nitrogen, Biocide, Control.
- Soil sampling: cores to 5 cm depth, within 2 x 2 m sub-plots, randomized locations; 3 sub-samples per occasion; samples stored cool; testate sampling from 0–60 mm depth.

## Data collection and methods
- Protozoan groups measured: naked amoebae, flagellates, ciliates, and testate amoebae (live and empty tests); size distribution data included in some datasets.
- Protocol highlights:
  - Testate amoebae: soil slurry incubation, fixation with phenolated aniline blue, counting live and empty tests.
  - Naked amoebae and flagellates: incubation and both direct/indirect enumeration; wells scored for presence of organisms.
  - Ciliates and flagellates: enumeration from runoff samples; enrichment cultures used for identification.
- Reporting units: abundances are expressed as numbers per gram of oven-dried soil (with some datasets indicating “thousands per gram dry weight” for certain groups).
- Lab facilities: analyses conducted at the Centre for Ecology & Hydrology, Windermere.
- Growth potential protocol in the background references: Finlay et al. 2000.

## Datasets and data structure
- Datasets provided as comma-separated values:
  - 1050: All Protozoa Abundance July 2000
    - 25 re-wetted soil samples from sub-plot S of plot 4D; sampling date: 17 July 2000.
    - Key fields: SUID, BLOCK, MAIN_PLOT, TREATMENT, SAMPLE_NUMBER, NAKED_AMOEBA, FLAGELLATES_DIRECT/INDIRECT, TESTATE_AMOEBA_LIVE/EMPTY, CILIATES, etc.
  - 1051: All Protozoa Abundance (March 1999 – February 2000)
    - Six sampling occasions; includes SUID1, SUID2, SAMPLING_DATE, BLOCK, MAIN_PLOT, TREATMENT; multiple taxa descriptors.
  - 1052: Protozoa Species Size Distribution
    - Size-class based abundances and species counts (e.g., naked amoebae, flagellates, testate amoebae, ciliates) across six occasions and 25 plots.
  - 1053: Protozoa Size Distribution
    - Abundances by size class across six sampling occasions.
  - 1054: Protozoan species diversity by plot
    - Presence/absence and diversity per plot for protozoan groups, with fields for PROTOZOAN_GROUP, GENUS, SPECIES, SPECIES_OCCURRENCE, NUMBER_OF_PLOTS.
- Common metadata fields across datasets:
  - Temporal and spatial identifiers: SAMPLING_DATE, BLOCK, MAIN_PLOT, TREATMENT, SAMPLE_NUMBER (or SUID), etc.
  - Biological descriptors: NAKED_AMOBA, FLAGELLATES_DIRECT/INDIRECT, FLAGELLATES_AVERAGE, TESTATE_AMOEB_A_LIVE/EMPTY, CILIATES, etc.
  - Size-related data: SIZE_RANGE, NAKED_AMOEBA_ABUNDANCE, FLAGELLATE_ABUNDANCE, TESTATE_ABOUNDA NCE, CILIATE_ABUNDANCE, etc.
- Data status and units: some measurements are in thousands per gram dry weight; some samples are air-dried or flooded; data types include Number, Text, and Date.
- Documentation and references: Scott et al., 2003 (Sourhope Field Data Handbook); Finlay et al., 2000; Usher et al., 2006; related data handbooks and publications provide additional methodological context.

## Quality control, provenance, and limitations
- Quality assurance: numeric range checks, formatting validation, and logical integrity checks performed.
- Limitations and liabilities: data providers (NERC) do not warrant accuracy or fitness for a particular use; no liability for inaccuracies or misuse.
- Scope considerations: data come from a single experimental site; interpretation should consider site-specific conditions and methodological complexity.

## Governance, access, and reuse notes for Data Leaders
- Asset characteristics: large, multi-dataset soil protozoa data resource with detailed sampling design, site metadata, and laboratory methods.
- Reusability: supports longitudinal analyses of protozoan communities, size-structured diversity, and links to soil carbon and nitrogen turnover; enables cross-dataset analyses (abundance, size distribution, and species diversity) across plots and treatments.
- Metadata value: includes block/plot identifiers, treatments, sampling dates, and explicit enumeration methods and units, aiding data discoverability and proper interpretation.
- Documentation and references: related publications and data handbooks provide provenance and methodological context; some materials accessible via EIDC catalogue records.