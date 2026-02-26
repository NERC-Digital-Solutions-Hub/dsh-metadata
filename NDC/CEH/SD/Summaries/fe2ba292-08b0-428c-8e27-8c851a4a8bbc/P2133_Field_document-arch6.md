# Measurements of microarthropod community structure and diversity from an upland grassland experimental site [NERC Soil Biodiversity Programme]

## Overview and aims
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) studying soil biota diversity and their functional roles in ecological processes.
- Focus on relationships between soil microarthropod communities and soil fertility/manipulations in temperate grassland.
- Project 2133 led by Dr R. Bardgett; site at Sourhope, Scotland.

## Site description and experimental design
- Location: Sourhope field site, Cheviot Hills, south-east Scotland; semi-improved upland grassland, ~350 m altitude.
- Climate and soil: annual rainfall ~1117 mm; temperatures 3.8–12.2 C; humic brown Sourhope soil.
- Plant community: dominated by Agrostis capillaris, Festuca ovina, Poa pratensis, Anthoxanthum odoratum.
- Experimental layout: five replicate blocks downslope; each block has six 12×20 m plots.
- Treatments (randomised): Control, Lime (CaCO3), Nitrogen (NH4NO3), Nitrogen + Lime.
- Application schedule: N—May 1999, Sep 1999, Apr 2000, May 2000; Lime—May 1999 and Apr 2000.
- Management: site cut five times per year to 6 cm; plot sampling included 80 cores (Nov, Feb, May) and 120 cores (Aug) across blocks.

## Data collection and measurements
- Microarthropods
  - Core processing: soil cores extracted to 5 cm depth; Berlese-Tullgren funnel used for 96 h to extract microarthropods.
  - Taxonomy: mites and Collembola identified; dominant species used for analyses; some taxa grouped into relative taxonomic units (rtu).
  - Diversity metrics: Shannon-Wiener index (H), evenness (J), cumulative species richness (R); group-specific indices for mites and Collembola; functional diversity inferred from predatory vs non-predatory mites.
  - Biomass: estimated from group-specific conversion factors to yield microbial-corrected biomass estimates.
- Plant productivity and soil/roots
  - Above-ground productivity: ANPP estimates from dry weights of 0.25 m2 quadrats across five mowing events.
  - Root and soil chemistry: dry root biomass; total carbon (C) and nitrogen (N) content in roots and soil (via automated Dumas method).
  - Soil properties: soil moisture, pH (using deionised water), organic matter content (loss on ignition); microbial biomass carbon via fumigation-extraction (CHCl3 method); soil basal respiration (CO2 production).
- Datasets and structure
  - Dataset 1040: Plant species data per core, including sampling Unit ID, dates, block/plot/cell identifiers, treatment, and core details; species names and surface area per core.
  - Dataset 1041: Field microarthropod population density (mites and Collembola) counts per core, depth to 5 cm, with block/plot identifiers and sampling dates.
  - Dataset 1042: Field microarthropod species abundance (counts by species) per core in August 2000; includes depth and treatment metadata.
  - Dataset 1043: Field soils data, capturing microbial biomass carbon (BIOMASSC), respiration, pH, loss on ignition (LOI), root dry biomass (ROOT), soil/ root C and N (SOIL_C_N, ROOT_C_N), soil moisture, and related fields; includes depth, sampling dates, and treatment information.

## Data structure and variables (highlights)
- Core identifiers: SUID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y; TREATMENT; SAMPLE_TYPE; SURFACE_AREA.
- Biological data: SPECIES (for 1040/1042), Mites, COLLEMBOLA counts; COUNT (for 1042).
- Depth and sampling: consistent 5 cm depth for microarthropods; multiple cores per plot/time point for soil/root measures.
- Measurements: ANPP (above-ground biomass), biomass carbon (BIOMASSC), respiration (RESPIRATION), pH (PH), LOI (organic matter), ROOT (dry root biomass), SOIL_C_N, ROOT_C_N, PERCENT_MOISTURE.

## Data quality, limitations, and usage notes
- Quality control included numeric range checks, formatting checks, and logical integrity checks.
- Data are subject to QA procedures but no warranty of accuracy; no liability for fitness or use in decision-making.
- Some fields (notably in dataset descriptions) contain formatting inconsistencies in the provided text; users should verify against original data files and metadata when integrating.
- Datasets are designed to enable analyses linking microarthropod diversity/abundance with soil fertility manipulations and plant productivity, with potential for cross-variable analyses (e.g., diversity vs biomass, soil C/N dynamics vs respiration).

## References and related resources
- Core methodology and related literature cited, including: Hopkin (Collembola key), Jenkinson & Powlson (microbial biomass methods), Luxton & Petersen (arthropod biomass/calorific content), and foundational biodiversity ecology texts (Begon et al.).
- Related data handbook and prior publications describing Sourhope Field Experiment data and approaches (e.g., Sourhope Field Data Handbook 2003; related biodiversity studies).

## Practical implications for data use
- Enables exploration of how nutrient and lime amendments affect below-ground biodiversity and functional processes.
- Facilitates cross-dataset analyses: linking microarthropod community structure with soil microbial activity, soil carbon/nitrogen dynamics, and above-ground productivity.
- Supports meta-analyses on the relationship between soil biota diversity and ecosystem function in temperate grasslands.