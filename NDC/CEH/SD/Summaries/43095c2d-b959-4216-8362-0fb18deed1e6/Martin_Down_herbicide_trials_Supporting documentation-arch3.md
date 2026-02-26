# Vegetation survey data for Martin Down Brachypodium pinnatum herbicide control trials

- A botanical field survey dataset from herbicide trials aimed at controlling Brachypodium pinnatum s.l. on calcareous grassland at Martin Down NNR, England.
- Timeframe: baseline survey in 2012 followed by post-treatment surveys in 2013, 2014, and 2015.
- Scope of data: percent cover for plant species, bare ground, and plant groups (total grasses, total forbs); indicator status; Ellenberg N fertility values.
- Study aims include assessing herbicide impacts on target species (B. pinnatum) and non-target groups, as well as community-level responses.

## Experimental design and treatments

- Study site: Martin Down calcareous grassland with two initial B. pinnatum cover levels — “dense” (mean baseline cover ~78%) and “sparse” (mean baseline cover ~26%).
- Structure: three experimental blocks per cover level; each block contains seven plots (3 m wide x 10 m long).
- Treatments: random assignment of different herbicides or management approaches across plots. Five herbicides plus glyphosate (six products in total were considered; glyphosate applied only in dense areas).
- Management conditions:
  - Dense areas: one plot per block treated with glyphosate; other plots left as controls or subjected to standard mowing regimes.
  - Sparse areas: one plot per block cut and grazed after mowing; remaining plots left ungrazed to avoid livestock exposure to residues.
- Application details:
  - Herbicides driven by efficacy for perennial grasses; administered with a 3 m boom sprayer, on days with favorable wind/ground conditions.
  - Timing aligned with product labels and operational constraints (autumn foliar applications for regrowth, with residual herbicides applied in winter for root uptake). In the third year, late-spring applications targeted regrowth after winter senescence due to some delays.
  - Administrative Trials Permit obtained for outside-label use.

## Data collection methods and structure

- Field sampling:
  - Each plot surveyed with five 50 cm x 50 cm quadrats placed along a W-shaped transect, avoiding outer plot edges to reduce drift risk.
  - In quadrats 1, 3, and 4, all plants recorded to species level; in quadrats 2 and 5, data recorded at group level (grasses/forbs).
  - For each quadrat, recorded: percentage cover of B. pinnatum, all vascular plants, bare ground.
- Data columns (single CSV dataset):
  - Brachypodium_initial_cover (dense/sparse), Block, Plot_number, Quadrat_Number, Treatment, Survey_Date, Survey_Year, Abbreviated_name, Species, PC_Cover (percent cover), Grass_v_Forb (G/F), Ellenberg_N, Indicator (P/N/A).
  - - entries indicate non-applicable columns for a given row.
- Data scope and outputs:
  - Analyses targeted at: B. pinnatum cover (target species) and non-target groups (other grasses, forbs), positive/negative indicators, arable indicators; plus community-level metrics such as Ellenberg-N weighted cover and DCA.
- Data structure notes:
  - Dataset is a single CSV file.
  - Some limitations due to budget/time: species-level recording was limited to three of the five quadrats per plot; other quadrats recorded at group level.

## Data quality, metadata, and governance considerations

- Metadata and data quality:
  - Some columns have non-applicable values (represented by '-'), requiring careful interpretation during analysis.
  - Limited species-level data in some quadrats; potential implications for fine-grained biodiversity analyses.
- Data provenance and sharing:
  - Data derived from field surveys and herbicide trials with clear experimental design and treatment mappings.
  - Suitability for inclusion in monitoring outputs (reports, charts, dashboards) and for informing governance decisions on management of calcareous grasslands.
- Governance implications:
  - The dataset demonstrates the need for transparent treatment metadata, clear documentation of sampling design, and consistent data collection protocols to support replication and policy evaluation.
  - Highlights the importance of assigning or clarifying data ownership, access permissions, and the ethical considerations around sharing underlying data, especially given treatment plots and potentially sensitive site information.

## Relevance for monitoring frameworks and policy decisions

- Key measures captured:
  - Target species response: B. pinnatum cover before and after herbicide applications.
  - Non-target vegetation responses: grasses, forbs, and indicator groups relevant to calcareous grassland condition.
  - Community structure indicators: Ellenberg N values and ordination metrics (e.g., DCA) to assess fertility and community shifts.
  - Management outcomes: differential responses under dense vs. sparse initial B. pinnatum cover and various management regimes (mowing, grazing, or herbicide application).
- Temporal design:
  - Baseline (2012) plus three follow-up surveys (2013–2015) enable assessment of short- to mid-term effects and the persistence of treatment impacts.
- Policy and management implications:
  - This framework supports evaluating herbicide efficacy and collateral impacts on biodiversity, informing decisions about herbicide use in nature conservation sites and the balance between target suppression and restoration of calcareous grassland communities.
  - The approach illustrates how to structure monitoring to detect both species-level changes and broader community responses, aiding adaptive management and governance of grassland restoration programs.

## References (selected background)

- Bobbink et al. 1989; English Nature 2003; Green 1972; Hill et al. 2004 (PLANTATT); Hurst 1997; Hurst & John 1999; Natural England 1999; Robertson & Jefferson 2000.