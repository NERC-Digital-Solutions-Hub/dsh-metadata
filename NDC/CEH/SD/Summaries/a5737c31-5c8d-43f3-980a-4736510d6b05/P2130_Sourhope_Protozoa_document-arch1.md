# Soil protozoan diversity data from Sourhope field experiment site, Scotland, 1999-2000 [NERC Soil Biodiversity Programme]

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999–2000) focusing on soil biodiversity and its functional roles in key ecological processes.
- Describes protozoan abundance and diversity in samples from Sourhope field site, Supplementing broader studies of soil structure and processes.

## Study site and aims
- Location: Sourhope field experiment site, Macaulay Land Use Research Institute (now James Hutton Institute), near Kelso, Southern Scotland (grid reference NT8545019630).
- Site characteristics: mid-altitude temperate upland grasslands on base-poor, damp soils; soils are shallow brown forest soils with local gleying; average annual rainfall ~950 mm; pH 4.54–4.81; mean soil carbon ~7.61% and nitrogen ~0.56%.
- Experimental design: 5 replicate blocks; 6 main plots per block (30 main plots total). Stock excluded from April 1998. Vegetation resembles NVC U4d with Agrostis capillaris dominant.
- Primary goal: understand the biological diversity of soil biota and the functional roles of soil organisms in carbon and nitrogen turnover, through protozoan (and other microfauna) study.

## Data collection and methods
- Soil sampling: taken from the Sourhope site; samples collected within 2 x 2 m sub-plots, depth ~5 cm, on multiple dates (1999: March 2, May 4, July 7, September 7; 2000: July 17). Location within each sampling unit randomized prior to sampling.
- Sub-sampling: three sub-samples per designated location; samples kept cool for transport; samples from 5 cm depth represent upper soil organic layer.
- Testate amoebae, naked amoebae, flagellates, ciliates: soil processed via specific incubation and enumeration protocols to estimate abundances per gram oven-dried soil weight. Protocols involve air-drying, rewetting, incubation at 15 °C, staining (phenolated aniline blue), and microscopic scoring at various stages (live and empty tests, direct/indirect enumerations, enrichment cultures).
- Lab work: conducted at the Centre for Ecology & Hydrology, Ferry House, Windermere, UK.
- Metadata and protocols: detailed methodological steps for each organism group, including slurry preparation, incubation times, counting chambers, staining, and data recording. Ancillary information references related publications and data handbooks (e.g., Scott et al., 2003).

## Datasets included (protozoan data)
- Dataset 1050: All Protozoa Abundance July 2000 (P2130_PROTOZOA_ABUND_JULY2000.csv)
  - Variables include: SUID, BLOCK, MAIN_PLOT, TREATMENT, SAMPLE_NUMBER; NAKED_AMOBA, FLAGELLATES_DIRECT, FLAGELLATES_INDIRECT, FLAGELLATES_AVERAGE, TESTATE_AMOEBA_LIVE, TESTATE_AMOEBA_EMPTY, CILIATES; units in thousands per gram or per gram dry weight; sample status mostly Air Dried.
  - Describes enumeration from 25 re-wetted soil samples from a single occasion (Sourhope sub-plot S of plot 4D).
- Dataset 1051: All Protozoa Abundance (P2130_PROTOZOA_ABUNDANCE.csv)
  - Enumeration across six occasions (1999–2000) for 25 plots; contains SUID1, SUID2, SAMPLING_DATE, BLOCK, MAIN_PLOT, TREATMENT; measures similar organism groups as 1050 (naked amoebae, flagellates direct/indirect/average, testate amoebae live/empty, ciliates).
- Dataset 1052: Protozoa Species Size Distribution (P2130_PROTOZOA_SPECIES_SIZE.csv)
  - Size-class distribution (12 size classes) for naked amoebae, flagellates, testate amoebae, and ciliates; includes average numbers per gram dry weight and species counts per size class.
- Dataset 1053: Protozoa Size Distribution (P2130_PROTOZOA_SIZE_DIST.csv)
  - Enumeration by sampling date across six occasions; records size-class distributions for naked amoeba, flagellates, testate amoeba, and ciliates; values are average numbers per gram dry weight.
- Dataset 1054: Protozoan species diversity by plot (130_PROTOZOAN_SPEC_DIVERSITY.csv)
  - Species detected per plot and occasion; fields include PROTOZOAN_GROUP, GENUS, SPECIES, SPECIES_OCCURRENCE (detected/not detected), and NUMBER_OF_PLOTS where detected.

## Data structure and fields (highlights)
- Data are provided as comma-separated values (CSV) with detailed field descriptors and data-type hints.
- Common dimensions include BLOCK, MAIN_PLOT, TREATMENT, SAMPLING_DATE, and SUID identifiers that map to plot/sub-plot configurations.
- Abundance metrics are per gram dry weight (or thousands per gram for some direct counts), with statuses typically “Air Dried” or related.
- Size-distribution datasets categorize protozoa by cell length into multiple size classes, enabling community structure analyses.

## Quality control and caveats
- Verification steps include numeric range checks, formatting checks, and logical integrity checks.
- Despite quality assurance, the data provider (NERC) does not warrant the accuracy for a given use; no liability for outcomes arising from data use.
- Users should consider experimental design (block effects, treatments, and temporal replication) when conducting analyses.

## Potential analytic uses for data
- Correlate protozoan abundance and diversity with soil chemical properties (carbon, nitrogen, pH) and moisture across time and treatments.
- Assess treatment effects (Nitrogen & Lime, Lime, Nitrogen, Biocide, Control) on protozoan communities and size-structure.
- Explore temporal dynamics across six sampling occasions and spatial variation across plots (block, main plot, and sub-plot levels).
- Examine size-class distributions and species diversity to understand functional roles in carbon and nitrogen turnover.
- Integrate datasets (1050–1054) to model relationships between abundance, community composition, and environmental factors.
- Use the SUID and plot metadata to merge protozoan data with other soil-biodiversity or productivity datasets from Sourhope for broader ecological inferences.