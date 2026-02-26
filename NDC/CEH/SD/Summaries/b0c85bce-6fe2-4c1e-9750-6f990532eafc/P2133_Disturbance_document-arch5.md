# Plant and soil animal diversity measurements from a disturbance and nitrogen addition experiment in an upland grassland site [NERC Soil Biodiversity Programme]

- Purpose and scope: Datasets documenting plant and soil microarthropod diversity responses to a crossed gradient of nitrogen addition and disturbance in upland grassland, part of the NERC Soil Biodiversity Thematic Programme (1999 onwards). Aimed at understanding how soil biota and plant communities respond to nutrient enrichment and physical disturbance.

- Project and stewardship context:
  - Project: 2133, Title: The relationship between diversity, biomass and function of soil microarthropod communities.
  - Project Leader: Dr. R. Bardgett.
  - Site custodianship: Sourhope site, Cheviot Hills, Southeast Scotland (55°28'30"N, 2°14'W; ~350 m altitude).
  - Site characteristics: Semi-improved upland grassland; mean annual rainfall ~1117 mm; dominated plant species listed; humic brown Sourhope soil.
  - Data governance: Data produced with associated references; data handling and documentation align with Sourhope Field Data Handbook and related technical literature.

- Experimental design and sampling framework:
  - Experimental layout: Five replicate blocks; within each block, five replicated experimental areas (3 m x 3 m) with a crossed grid of treatments.
  - Treatments: Continuous gradient of fertilizer nitrogen addition (0, 60, 120, 180, 240 kg N ha-1) and disturbance (0%, 25%, 50%, 75%, 100% ground cover disturbed).
  - Plot structure: Sub-plots (0.5 m^2) arranged in a 25-cell matrix per experimental area with buffer zones to minimize edge effects.
  - Timeline: Fertilizer applied February 2000 and April 2001; initial plot disturbance December 1999; secondary disturbance December 2000.
  - Sampling windows: Plant and soil arthropod sampling in August 2000 and August 2001.
  - Measurement focus:
    - Aboveground plant biomass via clipping to 6 cm height, drying, and weighing.
    - Plant diversity metrics using point quadrats: Shannon-Wiener index (H), evenness (J), and species richness (R).
    - Microarthropod diversity and abundance (mites and Collembola) from soil cores (3 cm diameter, 5 cm depth) using a 96-hour Tullgren funnel extraction; storage in 70% ethanol with glycerol.
    - Belowground functional diversity indicators for mite groups (predatory vs non-predatory).
    - Aboveground biomass and soil microarthropod counts aggregated to plot/sub-plot level; taxonomic identification following standard references.

- Data structure and contents:
  - Dataset 1047: Matrix plant species abundance data 2000 (P2133_MATRIX_SURVEY2000.csv)
    - Key fields: SAMPLING_DATE, BLOCK, MAIN_PLOT, MATRIX_POSITION (1-25), DISTURBANCE (0-100%), NITROGEN (kg N ha-1), SPECIES, COUNT (percentage cover).
    - Describes plant species counts/abundance on matrix plots for Aug 2000.
  - Dataset 1048: Matrix plant species abundance data 2001 (P2133_MATRIX_SURVEY2001.csv)
    - Similar structure to 2000 with sampling in Aug 2001.
  - Dataset 1045: Microarthropod species abundance, 2001 (P2133_MATRIX_MPOD_SPECIES.csv)
    - Records: YEAR, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN; SPECIES (microarthropod taxa), COUNT (per sample).
    - Focus on microarthropod species counts from 2001 sampling.
  - Dataset: P2133_MATRIX_PLANT_MPOD.csv
    - Combines microarthropod counts (mites and Collembola) and above-ground plant biomass per subplot; variables include YEAR, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, PLANT_BIOMASS (g m-2), MITES (counts per m-2), COLLEMBOLA (counts per m-2).
    - Provides integrated below- and above-ground response data for each plot.
  - Data documentation and quality notes:
    - Quality control included numeric range checks, formatting conformity, and logical integrity checks.
    - Metadata and data dictionaries accompany the datasets, describing each field, data type, units, and sampling context.

- Metadata, standards, and provenance:
  - Data provenance: Collected as part of the Sourhope Field experiments under the NERC Soil Biodiversity Programme; references and data handbook links provided (e.g., Scott et al. 2003; Usher et al. 2006).
  - Metadata references: Begon et al. 1996; Burke & Grime 1996; Cole et al. 2008; Hopkin 2000; Krantz 1978; related supporting information via EIDC; Sourhope Field Data Handbook 2003.
  - Data format and accessibility: Data stored as CSV files with described column headers and units; dataset outputs documented for reuse and reproducibility.

- Usage notes and limitations:
  - Data are subject to quality assurance checks but not guaranteed by NERC; no liability for fitness or accuracy for a user’s intended use.
  - Handling and transformation steps (e.g., calculation of diversity indices) are described or derivable from the metadata.
  - Temporal scope limited to 2000–2001 with specific treatment gradients; cross-study comparisons should account for site- and year-specific conditions.

- Practical considerations for Data Stewards:
  - Ensure consistent metadata across all datasets (variable definitions, units, sampling dates, block and plot identifiers).
  - Maintain clear mapping between MATRIX_POSITION and Burke & Grime grid references for interoperability.
  - Preserve provenance links to associated publications and the Sourhope Field Data Handbook.
  - Facilitate discoverability by indexing by project (2133), site (Sourhope), treatment types (DISTURBANCE, NITROGEN), and organisms (plants, mites, Collembola).
  - Retain quality control notes and disclaimers to inform data consumers about limitations and liability.