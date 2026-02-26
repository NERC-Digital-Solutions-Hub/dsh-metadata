# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

## Overview
- Field experiment at Sourhope, Scottish Borders, under the NERC Soil Biodiversity Thematic Programme.
- Aimed at providing a broad context for detailed studies via regular monitoring of site conditions, treatments, and yields to enable cross-project comparisons.
- Key management events in 2001 included restrictions due to Foot and Mouth Disease (FMD) and a change of site officer.

## Data types and collection timeline
- Automatic Weather Station data (2001 headline measures; 1999–2001 data context): rainfall, radiation, soil moisture, and temperatures at multiple depths; data downloaded regularly to the MLURI/CEH data manager.
- Above-ground biomass (1999–2001): five summer mowing events per year (May–September); biomass per 0.5 m^2 cell, later aggregated per plot; 2001 saw an apparent biomass increase linked to personnel changes and switch from manual cutting to mechanical shears.
- Soil pH (upper 5 cm): baseline in 1998; October 2001 pH measurements show lime and N/L treatment effects (limed plots ~6.19; N&L ~6.38; nitrogen alone uplift, less than lime).
- Botanical composition (point quadrat surveys): July 2000 and July 2001 inventories using a 100-cell frame with 25 random pins per quadrat; agreements between two surveyors demonstrated no significant cross-surveyor bias in 2001; 24 species observed in unimproved plots vs 18 in improved plots; shifts in dominance across treatments.
- Site heterogeneity indicators: spatial variation in pH and biomass across site columns (E/F vs. others) and a strong pH–biomass relationship.

## Data structure and provenance
- Experimental design: multiple sub-plots within blocks and six main treatments (Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime, Biocide) with data linked to specific plots; year-to-year comparisons used normalization (e.g., against C1) to interpret treatment effects.
- Data collection schedule (Table 1 reference in the report) includes:
  - Above-ground biomass measurements at five summer occasions.
  - Full botanical survey around mid-summer.
  - Minirhizotron-related vegetation surveys and disturbance/nutrient matrices on designated sub-plots.
  - Weather and related measurements continuously recorded and archived.
- Data handling and analysis: biomass data were ln-transformed for ANOVA; separate analyses addressed year-to-year inter-year effects; Genstat 5 used for statistical tests; PCA applied to point-quadrat data.

## Data quality and governance
- QA checks: two surveyors contributed to point quadrat surveys (~50% each) with no significant difference in results (NS).
- Methodological note: 2001 switch from manual cutting to mechanical shears; this coincided with higher biomass estimates, necessitating normalization to discern true treatment effects.
- Documentation and provenance: detailed logging of site management events (FMD restrictions, officer change) and measurement dates to aid reproducibility and cross-study comparisons.
- Metadata considerations: explicit species codes and their mappings (e.g., Ac = Agrostis capillaris, Fr = Festuca rubra, etc.); clear table and figure references for reproducibility.

## Key findings relevant to data usage
- Biomass responses: nitrogen and lime inputs increased above-ground biomass; the combination of nitrogen and lime yielded the strongest effect; 2001 biomass rise largely attributable to measurement method change and staffing rather than a biological anomaly.
- Soil chemistry: lime consistently raised soil pH; nitrogen alone also raised pH but to a lesser extent; untreated controls showed little pH change since baseline (1998).
- Plant community shifts: fertilized plots showed increased presence of species associated with improved pastures (Festuca rubra, Poa pratensis); Agrostis capillaris declined across treatments; diversity (number of different species) tended to be higher in unimproved plots than in improved plots.
- Vegetation–productivity linkage: PCA effectively separated plots treated with nitrogen and/or lime from control/biocide plots; biomass positively correlated with Festuca rubra and Poa pratensis abundance and negatively with certain grasses and bryophyte-associated species as biomass increased.
- Site heterogeneity: spatial patterning across columns indicated underlying heterogeneity in pH and biomass, with a strong positive pH–biomass relationship across plots.

## Metadata and interoperability considerations
- Units, measurement intervals, and data processing steps (e.g., ln-transformation of biomass, normalization to C1) should be captured in metadata to ensure cross-year comparability.
- Species codes and survey methodologies (Point Quadrat protocol) require clear mapping dictionaries for reuse in other datasets.
- Spatial layout (blocks, columns, plots, sub-plots) and the effect of site heterogeneity should be documented for accurate spatial analyses and data integration with other studies.

## Data access and preservation (context)
- Weather data management was handled by the CEH Merlewood Data Manager; other data (biomass, soil pH, botanical surveys) were organized within the MLURI/Sourhope experimental framework.
- The report provides detailed tables, figures, and appendices (e.g., Appendix 1: annualised biomass per plot) to support data reuse and verification.

## End-to-end considerations
- The dataset captures multi-year, multi-variable measurements with a robust QA framework, but care is needed when combining years due to equipment/methodology changes (notably in 2001).
- Spatial heterogeneity should be incorporated into analyses to avoid confounding treatment effects with site layout.