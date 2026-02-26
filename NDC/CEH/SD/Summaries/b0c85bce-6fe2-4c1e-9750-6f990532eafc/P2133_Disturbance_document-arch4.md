# Plant and soil animal diversity measurements from a disturbance and nitrogen addition experiment in an upland grassland site [NERC Soil Biodiversity Programme]

## Overview
- Describes a long-running field experiment (NERC Soil Biodiversity Programme) at Sourhope, Scotland, to understand soil biodiversity and its functional roles, alongside aboveground productivity and plant diversity.
- Focuses on how disturbance and nitrogen addition affect plant communities and soil microarthropods (mites and Collembola) across multiple taxonomic levels and functional indices.
- Data derived from two years of plant surveys (2000 and 2001) and associated microarthropod measurements; includes detailed metadata and data-quality checks.

## Study site and experimental design
- Location: Sourhope field, Cheviot Hills, Southeast Scotland, UK (approx. 55°28'30"N, 2°14'W); upland semi-improved grassland at ~350 m elevation; annual rainfall ~1117 mm; soils are humic brown (Sourhope series).
- Plant community: dominated by Agrostis capillaris, Festuca ovina, Poa pratensis, Anthoxanthum odoratum.
- Experimental setup: five blocks; within blocks, five replicated experimental areas forming a crossed gradient in a 3 m x 3 m sub-plot matrix (0.5 m2 sub-plots) totaling 25 sub-plots per area.
- Treatments: gradient of nitrogen fertilization (0, 60, 120, 180, 240 kg N ha-1) and disturbance (0%, 25%, 50%, 75%, 100%), randomly oriented following Burke and Grime (1996).
- Edge effects mitigated by a 0.5 m buffer zone around sub-plots.
- Fertilization occurred in February 2000 and April 2001; disturbance applied December 1999 and again December 2000 (simulated trampling with a metal pipe and cross blade).
- Sampling timepoints: August 2000 and August 2001.

## Data collected and what they measure
- Plant diversity and composition:
  - Assessed via point quadrats; diversity indices include Shannon-Wiener (H), evenness (J), and species richness (R).
  - Relative abundances reported for plants and microarthropods; functional diversity indices for predatory vs. non-predatory mites.
- Aboveground productivity:
  - Vegetation harvested to a 6 cm sward height, dried (70°C, 1 week) for biomass.
- Belowground biodiversity and microarthropods:
  - Soil cores (3 cm diameter, 5 cm depth) collected per plot; cores combined for analysis.
  - Microarthropods extracted using a Tullgren funnel (96 h); counts for mites and Collembola; species-level identifications for some taxa.
- Taxa and metrics:
  - Plants and microarthropods tracked by taxon, with abundance counts and, for plants, percent cover per sub-plot.
  - Indices and measures include total microarthropod counts, as well as group- and species-level data for mites and Collembola.

## Data structure and files
- Four CSV datasets underpin the data structure:
  - Dataset 1047: Matrix plant species abundance data, 2000
    - Fields include SAMPLING_DATE, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES, COUNT (percent area cover), among others.
  - Dataset 1048: Matrix plant species abundance data, 2001
    - Similar fields as 2000; includes YEAR/temporal context for 2001 sampling.
  - Dataset 1045: Microarthropod species abundance, 2001
    - Fields include YEAR, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES (microarthropod species), COUNT (per sample).
  - P2133_MATRIX_PLANT_MPOD.csv and P2133_MATRIX_MPOD_SPECIES.csv (within the MPOD data group)
    - Provide above-ground plant biomass (PLANT_BIOMASS), and microarthropod totals (MITES, COLLEMBOLA) per sample, plus species-level counts for MPOD in 2001.
- Data collection methods and unit conventions are described in detail within the dataset metadata, including sampling dates, plot identifiers, treatment levels, and measurement units.

## Methods, quality control, and metadata
- Sampling methods are described for plants (point quadrats), aboveground biomass (sward height harvest and drying), and microarthropods (3 cm cores, 5 cm depth, 96 h Tullgren extraction).
- Taxonomic identification references include Hopkin (2000) for Collembola and Krantz (1978) for mites; plant identifications aligned with Begon et al. (1996) and Burke & Grime (1996).
- Quality control: numeric range checks, data formatting checks, and logical integrity tests performed to ensure dataset consistency; data providers offer no warranty on accuracy or fitness for a particular use.
- References and additional reading include Scott et al. (2003) and Usher et al. (2006); supporting information and a field data handbook are available via the EIDC catalogue.

## Usage, access, and provenance
- Data originated from the NERC Soil Biodiversity Thematic Programme (1999 onward) at Sourhope; primary outputs relate to the relationship between diversity, biomass, and function in soil microarthropod communities.
- Supporting literature and data handbooks provide context, methodologies, and guidance for reuse.
- The dataset is accompanied by acknowledgments of limitations and disclaimers regarding data accuracy and liability.