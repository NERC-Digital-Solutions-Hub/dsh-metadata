# Plant and soil animal diversity measurements from a disturbance and nitrogen addition experiment in an upland grassland site [NERC Soil Biodiversity Programme]

## Overview
- Describes data from the NERC Soil Biodiversity Thematic Programme (established 1999) at Sourhope, Scotland, investigating soil biodiversity and functional roles in key ecological processes.
- Focuses on plant and soil microarthropod diversity in a disturbance and nitrogen (N) addition experiment.
- Data products include abundance measures for mites, Collembola, and plant biomass across treatments; multiple related datasets and sampling periods.

## Site and experimental design
- Location: Sourhope, Cheviot Hills, Southeast Scotland (55°28'30''N, 2°14'W), upland semi-improved grassland at ~350 m altitude.
- Climate/soils: ~1117 mm annual rainfall; humic brown Sourhope soil.
- Experimental layout: five replicate blocks; within each block, five experimental areas (3 m x 3 m sub-plots within control context) with a crossed gradient of fertilizer (0, 60, 120, 180, 240 kg N ha-1) and disturbance (0%, 25%, 50%, 75%, 100% ground cover disturbed).
- Edge-effect mitigation: 0.5 m buffer zones between sub-plots; random assignment of nitrogen and disturbance treatments.
- Treatments applied: annual N fertilization in Feb 2000 and Apr 2001; disturbance induced Dec 1999 and Dec 2000 using a metal pipe with a cross blade to simulate trampling.

## Data collection and measurements
- Plant diversity: assessed on 1–18 Aug 2000 and 20–23 Aug 2001 using point quadrat techniques; metrics include Shannon Wiener diversity index (H), evenness (J), and cumulative species richness (R).
- Functional diversity (belowground): indices for predatory vs. non-predatory mites; overall diversity for Microarthropods (mites + Collembola) and separate groupings.
- Aboveground productivity: plots mown to 6 cm on 17–18 Aug 2000 and 28–29 Aug 2001; aboveground biomass weighed after oven-drying at 70°C for 1 week.
- Soil sampling: three cores per 0.5 m² plot (3 cm diameter, 5 cm depth) collected on 17 Aug 2000 and 10 Jul 2001 for biomass and microarthropod extraction.
- Microarthropod processing: roots/soil incubated in Tullgren funnels for 96 h; specimens stored in 70% ethanol with 5% glycerol.
- Taxonomy and counts: total counts of mites and Collembola; species abundance recorded in 2001; Collembola identified per Hopkin (2000); mites identified per Krantz (1978) and related descriptions.
- Datasets include matrix plots (5 blocks x 25 sub-plots per area) with associated treatment metadata.

## Data structure and contents
- Datasets (four CSV files) capturing plant and microarthropod data across 2000 and 2001:
  - Dataset 1047: Matrix plant species abundance data 2000 (P2133_MATRIX_SURVEY2000.csv)
    - Variables: SAMPLING_DATE, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES, COUNT
  - Dataset 1048: Matrix plant species abundance data 2001 (P2133_MATRIX_SURVEY2001.csv)
    - Variables: SAMPLING_DATE, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES, COUNT
  - Dataset 1045: Microarthropod species abundance, 2001 (P2133_MATRIX_MPOD_SPECIES.csv)
    - Variables: YEAR, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES, COUNT
  - Dataset 1045: Microarthropod counts and aboveground biomass per matrix plot (P2133_MATRIX_PLANT_MPOD.csv)
    - Variables: YEAR, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, PLANT_BIOMASS (g m-2), MITES (counts m-2), COLLEMBOLA (counts m-2)
- Common structure: linked to Burke and Grime (1996) grid across 25 sub-plots per experimental area; treatment metadata (DISTURBANCE, NITROGEN) tied to each observation; standard zoogeographic and botanical identifiers and measurement units.

## Quality control and data management
- Quality assurance: numeric range checks, formatting conformity, and logical integrity checks applied to datasets.
- Limitations: while QA procedures are performed, data accuracy is not guaranteed by NERC; no liability for fitness of use or outcomes from data analyses.
- Data availability and references: data may be accompanied by a data handbook and related literature; suggested materials include SOURHOPE FIELD DATA HANDBOOK (2003) and Usher et al. (2006) on soil biodiversity methods.

## Context and references
- Key project references and reading:
  - Begon, Harper, Townsend (1996); Burke & Grime (1996) foundational design references.
  - Cole et al. (2008) on disturbance and nitrogen effects in Sourhope.
  - Hopkin (2000) and Krantz (1978) taxonomic references for Collembola and mites.
- Additional data documentation:
  - SOURHOPE FIELD DATA HANDBOOK 2003 (Scott et al., 2003) and related materials via EIDC catalogue; Usher et al. (2006) on soil biodiversity methodology.

## Access and usage notes for analysts
- Data designed for standardized monitoring outputs: enable verification, quality assurance, and transformation processes; outputs commonly presented as reports, maps, and charts.
- Data storage and portal practices: datasets are prepared for storage and upload to appropriate data portals; compatible with cross-study analyses and integration with other environmental datasets.