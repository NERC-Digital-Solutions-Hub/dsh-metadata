# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment colloidal carbohydrate concentration in saltmarsh and mudflat habitats.

## Overview
- Dataset measuring the concentration of colloidal carbohydrates in surface sediments, expressed as glucose equivalents in micrograms per gram (µg g⁻¹).
- Focuses on saltmarsh and mudflat habitats across two UK regions (Essex and Morecambe Bay) during winter and summer 2013.

## Data scope and authorship
- Staff responsible: Jack Maunder.
- Observations collected at six sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Habitat types: mudflat and saltmarsh; saltmarsh sites represent contrasting soil types (clay in Essex, sandy in Morecambe Bay) with differing inundation and vegetation.
- Sampling campaign: CBESS field campaign conducted in winter and summer 2013; no planned repeat sampling.

## Sampling design and methods
- Replicates: five replicates in each 1 x 1 m quadrat for both mudflat and saltmarsh.
- Quadrat layout: 22 quadrats per site, randomly allocated; scales A-D defined to vary spatial separation (A: 1 quadrat; B: 3 quadrats 1–10 m apart; C: 6 quadrats 10–100 m apart; D: 12 quadrats 100 m to site maximum).
- Location determination: random quadrat placement using R.
- Core collection and processing: collection of contact cores; freezing top 2 mm with liquid nitrogen; storage below -80°C; weigh wet weight; freeze-dry.
- Carbohydrate analysis: Dubois Phenol-Sulphuric assay on sub-samples (50–500 mg) with known water added; color development (35 minutes) and absorbance read at 486.5 nm; concentration calculated against standard regression to express as µg g⁻¹.
- Quality controls: spectrophotometer calibration via glucose standards; scale and weight measurements recorded; species/season coding for data.

## Variables and data structure
- Primary variable: Colloidal carbohydrate concentration (µg g⁻¹) as glucose equivalents.
- Associated fields and metadata: Season (Winter W, Summer S); Location (Essex E, Morecambe M); Site (AH, FW, TM for Essex; CS, WS, WP for Morecambe); Habitat (Mudflat MF, Saltmarsh SM); Quadrat Number (1–22); Scale (A–D with defined spatial extents); Standard deviation (StDev) per measurement; Row Number and data type descriptions.
- Data format: Comma-separated values (.csv).
- Data quality notes: Zero values indicate colloidal carbohydrate concentration below detectable level; NA indicates missing data due to inaccessibility of a quadrat.

## Data management and provenance
- Location and site descriptions chosen to represent contrasting sediment types and habitat conditions.
- Procedures and calibration steps documented (lab/field workflow, spectrophotometer readings, standard dilutions).
- Clear data dictionary and field formats provided to support discoverability and reuse.

## Access, use, and potential applications
- Suitable for studies on coastal sediment biogeochemistry, ecosystem services, and biodiversity modeling within CBESS.
- Enables cross-site comparisons of seasonal and spatial variability in colloidal carbohydrate content across saltmarsh and mudflat habitats.
- Can inform analyses of data quality, measurement uncertainty, and the influence of sediment type on carbohydrate concentrations.

## Limitations and considerations for data leaders
- No planned repeat sampling beyond 2013 CBESS campaign; temporal replication is limited to two seasons within a single year.
- Data are site- and method-specific; careful alignment with other datasets required for broader syntheses.
- Metadata is comprehensive but users should verify exact procedural details (e.g., site coordinates and scale definitions) when integrating with external data sources.