# Plant and soil animal diversity measurements from a disturbance and nitrogen addition experiment in an upland grassland site [NERC Soil Biodiversity Programme]

## Scope and purpose
- Data from the NERC Soil Biodiversity Thematic Programme (1999–2001) examining how plant and soil microarthropod diversity respond to disturbance and nitrogen addition in upland grassland.
- Aimed to link aboveground productivity and plant diversity with belowground soil animal diversity and function.

## Site, design, and treatments
- Location: Sourhope, Cheviot Hills, Southeast Scotland (55°28'30"N, 2°14'W); semi-improved upland grassland, ~350 m altitude.
- Climate/Soil: Annual rainfall ~1117 mm; average temperatures 3.8–12.2°C; humic brown Sourhope soil.
- Plant community: Dominated by Agrostis capillaris, Festuca ovina, Poa pratensis, Anthoxanthum odoratum.
- Experimental layout: Five blocks; within each block a crossed, continuous gradient of:
  - Nitrogen addition: 0, 60, 120, 180, 240 kg N ha-1
  - Disturbance: 0%, 25%, 50%, 75%, 100% ground cover disturbed
- Plot structure: A matrix of 25 sub-plots per experimental area (0.5 m2 each) arranged within five replicated and randomly positioned experimental areas (3 m x 3 m) per block, with buffer zones to minimise edge effects.
- Treatments applied: Annual N fertiliser applications in February 2000 and April 2001; disturbance applied December 1999 and December 2000.
- Sampling windows: Plant and soil measurements collected in August 2000 and August 2001.

## Data collected and key variables
- Plant diversity and productivity:
  - Plant species abundance on matrix plots (2000 and 2001)
  - Diversity metrics: Shannon-Wiener index (H), evenness (J), species richness (R)
  - Aboveground biomass: harvested, dried (70°C) biomass per sub-plot
- Microarthropod communities (soil fauna):
  - Total counts of mites and Collembola per sample (2000 and 2001)
  - Microarthropod species abundance (recorded in 2001)
  - Belowground functional diversity: indices distinguishing predatory vs non-predatory mites
- Sampling and processing methods:
  - Plant diversity sampled via point quadrats, 1–18 Aug 2000 and 20–23 Aug 2001
  - Vegetation clipped to 6 cm and biomass weighed after drying
  - Soil cores (three per 0.5 m2 subplot) taken at 0–5 cm depth; microarthropods extracted using a 96 h Tullgren funnel
  - Species identifications for Collembola and mites followed standard taxonomic references
- Outputs include a matrix of plots linked to treatment levels, with corresponding plant and microarthropod measurements.

## Data structure and files
- Four comma-separated data files are provided:
  - Dataset 1047: Matrix plant species abundance data 2000 (P2133_MATRIX_SURVEY2000.csv)
    - Variables include SAMPLING_DATE, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES, COUNT (percent area)
  - Dataset 1048: Matrix plant species abundance data 2001 (P2133_MATRIX_SURVEY2001.csv)
    - Similar structure to 2000 dataset
  - P2133_MATRIX_PLANT_MPOD.csv
    - Microarthropod counts linked to plant plots, includes YEAR, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, PLANT_BIOMASS, MITES, COLLEMBOLA
  - Dataset 1045: Microarthropod species abundance, 2001 (P2133_MATRIX_MPOD_SPECIES.csv)
    - YEAR, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES, COUNT
- Note: Each file includes detailed field descriptions, units, and data types; data are organized by block, main plot, matrix position, and treatment along with sample-specific measurements.

## Quality control and limitations
- Quality checks performed: numeric range validation, formatting checks, and logical integrity tests.
- NERC provides no warranty on data accuracy or fitness for a particular use; liability for use is disclaimed.
- Data reflect local-scale experimental conditions; users should consider potential edge effects (mitigated by buffer zones) and temporal gaps (sampling dates confined to specific August periods).
- Some analyses (e.g., species-level data) are present only for certain years (notably 2001 for detailed microarthropod species counts).

## How analysts can use the data
- Explore correlations and potential causal links between disturbance and nitrogen treatments and diversity metrics for both plants and soil microarthropods.
- Build models predicting aboveground biomass or plant diversity responses from soil fauna metrics, or vice versa.
- Compare community composition shifts across years (2000 vs 2001) under identical or differing treatment combinations.
- Assess scale and methodological limitations (e.g., spatial grid design, sampling depth, and timing) when applying findings to broader upland grassland contexts.
- Integrate with additional climate or soil chemistry data to refine understanding of drivers behind observed patterns.

## References and access notes
- Foundational references: Burke & Grime (1996); Begon, Harper & Townsend (1996); Hopkin (2000); Krantz (1978); Usher et al. (2006); Scott et al. (2003); and related Sourhope Field Data Handbook (2003).
- Data availability and context: Detailed project documentation and supporting information are available via the EIDC catalogue and related publications; data are provided with metadata to facilitate reuse and discovery.