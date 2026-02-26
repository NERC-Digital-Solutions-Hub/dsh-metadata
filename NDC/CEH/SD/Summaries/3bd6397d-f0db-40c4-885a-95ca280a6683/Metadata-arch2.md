Data files: Chemistry_PorewaterLitterSoil.csv; LitterBagData.csv; TBI_Data.csv

## Aim
- Use standardized data to demonstrate environmental condition and track health and policy performance over time.
- Provide clear, comparable datasets for monitoring organic soils and litter decomposition, enabling scrutiny and secondary analyses.

## Study context and design
- Field locations: Migneint, North Wales and Peaknaze, Northern England.
- Sites and soils: four experimental categories (Migneint Peat, Migneint Podzol, Peaknaze Peat, Peaknaze Podzol).
- Experimental design: randomised blocked design with four replicates per plot; treatments include control, acid, and alkaline.
- Treatments and dosing: acids (H2SO4) dosed monthly with rainwater; 50 kg S ha-1 yr-1 for podzol, 100 kg S ha-1 yr-1 for peat; alkaline treatments use NaOH/KOH with MgCl2/CaCl2 rinses to balance base cation ratios.
- Timeframe: initial treatment 2008–2012; re-established with same methods and allocations 2015–2016.
- Data collection and interpretation: led by Dr. Catharine Pschenyckyj as part of a PhD project.

## Data files and sampling overview

### Chemistry_PorewaterLitterSoil.csv
- Sample types: pore water, decomposing surface litter, soil.
- Sampling timeline: monthly pore water samples Sep 2015–Oct 2016 (about one week after treatments).
- Sampling locations and depth: 10 cm depth; four locations per plot; samples bulked to one per plot.
- Litter and soil sampling: four litter/peat samples per plot; leaf litter collected 10–15 cm from plot edge; depth 10–20 cm soil sample.
- Extraction and processing: cold water extraction (soil 1:10; litter 1:20); shaker, centrifugation, filtration.
- Analyses: pH, electrical conductivity (EC), total organic carbon (TOC), ultraviolet absorbance; DOC quantified by Thermalox TC-TN analyzer (TIC subtracted from TC); DOC units: mg/L for pore water; mg DOC per g dry material for litter/soil extracts.
- Spectroscopic proxies: SUVA254 calculated from UV absorbance (240–600 nm) with pathlength correction.
- Data format: CSV; acronyms and units provided (M/Migneint, PN/Peaknaze, Pod/Podzol, PW, DSL, EC, DOC, SUVA254).

### LitterBagData.csv
- Litter types: Calluna vulgaris, Eriophorum vaginatum, Festuca ovina, Pleurozium schreberi, Sphagnum spp.; sourced from respective sites.
- Burial and materials: litter dried and weighed; 3 g Calluna/Eriophorum/Festuca; 1 g Sphagnum/Pleurozium per bag; 5 cm depth burial in 10 x 10 cm bags with 0.5 mm mesh.
- Timeline and retrieval: buried Oct 2015; retrieved Oct 2016; mass loss measured quarterly over 12 months.
- Processing: removing ingrown material; cold-water extraction (1:20 litter:water) for 24 h; centrifugation, filtration; reweighing and oven-drying (70°C, 48 h) to obtain post-extraction mass.
- Analyses: litter mass loss (%ML) and chemical extracts for pH, EC, DOC, SUVA254; includes total nitrogen (TN) and species-specific identifiers.
- Data format: CSV; acronyms and units provided (M/Migneint, PN/Peaknaze, Pod/Podzol, EC, DOC, SUVA254, TN, %ML, species codes).

### TBI_Data.csv
- Method: Tea Bag Index (TBI) to estimate decomposition rate (k_TBI) and stabilisation factor (S) as proxies for litter decomposition and stabilisation.
- Tea types and placement: Green and Rooibos tea bags (Lipton); three sets per plot; buried July 2016 for 90 days.
- Retrieval and metrics: bags retrieved Oct 2016; mass loss used to calculate k_TBI and S following Keuskamp et al. (2013).
- Data format: CSV; acronyms provided (M/Migneint, PN/Peaknaze, Pod/Podzol; S stabilisation factor; K decomposition rate).

## Data processing and quality
- All data collection and interpretation conducted by project lead (Dr. Catharine Pschenyckyj); aligned with a PhD study.
- Standardized protocols for sampling, extraction, and analysis to enable cross-site comparability.
- Data and metadata are provided in CSV formats with explicit acronyms and units to facilitate integration.

## Data management and access
- Datasets are stored as standardized CSV files with accompanying metadata (acronyms, units, sampling details).
- Outputs are designed for inclusion in monitoring portals and for reuse by others, consistent with environmental monitoring standards.
- Challenges highlighted include increasing dataset value through data integration and improving access to underlying data.

## Key challenges and opportunities for analysts
- Increasing value by integrating these datasets with other relevant environmental datasets (e.g., climate, hydrology, vegetation).
- Ensuring broad access to underlying data to support transparency, reproducibility, and secondary analyses.

## References and related work
- Cited methodological and contextual references for acidity, DOC mobility, and Tea Bag Index approaches (Evans et al. 2012; Duddigan et al. 2020; Keuskamp et al. 2013).