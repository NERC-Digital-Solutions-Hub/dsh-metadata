# Data files: Chemistry_PorewaterLitterSoil.csv; LitterBagData.csv; TBI_Data.csv

## Overview
- Describes three CSV data files from a UK field experiment on acidity effects in organic soils.
- Data collected to assess how acidity influences carbon cycling, litter decomposition, and Tea Bag Index (TBI) metrics.
- Metadata and acronyms accompany each dataset to support reuse and interoperability.

## Datasets

### Chemistry_PorewaterLitterSoil.csv
- Sample types: pore water, decomposing surface litter, soil.
- Sampling timeline and locations: monthly pore water samples Sept 2015–Oct 2016; four locations per plot; plots at two sites (Migneint, Peaknaze) and two soil types (peat, podzol).
- Sample collection methods:
  - Pore water: depth 10 cm, Rhizon suction samplers; four locations per plot; bulked to one sample per plot.
  - Litter: collected from soil surface; 3 time points in 2016 (April, July, October); handled to minimize disturbance.
  - Soil: collected 10–20 cm depth; 30 g organic soil per sample.
- Laboratory analyses:
  - pH, electrical conductivity (EC), dissolved organic carbon (DOC), ultraviolet absorbance.
  - DOC concentration for pore water (mg L^-1); for litter/soil extracts, DOC per g dry material.
  - SUVA254 calculated as a proxy for DOC quality.
- Instruments and protocols:
  - UV-Vis spectra (240–600 nm) using a microplate reader; a correction factor applied for plastic vs quartz pathlength differences.
  - DOC quantified by Thermalox TC-TN analyser with TIC subtraction.
- Units:
  - pH (pH units), EC (μS), DOC (mg/L), SUVA254 (mg C^-1 m^-1).
- Acronyms:
  - M = Migneint, PN = Peaknaze, Pod = Podzol, PW = Pore water, DSL = Decomposing surface litter, EC = Electrical conductivity, DOC = Dissolved organic carbon.

### LitterBagData.csv
- Purpose: evaluate acidity effects on litter decomposition using buried litter bags.
- Litter types: Calluna vulgaris, Eriophorum vaginatum, Festuca ovina, Pleurozium schreberi, Sphagnum spp. (collected at respective sites).
- Procedure:
  - Litter prepared (species-specific masses) and placed in 10 x 10 cm, 0.5 mm mesh litter bags buried at 5 cm depth in Oct 2015.
  - Bags retrieved Oct 2016; processing included washing, drying, and weighing; cold-water extraction of litter with 1:20 litter:water ratio for 24 h.
  - Post-extraction mass measured; oven-dried mass for final mass loss calculations.
  - Additional incubations: 3, 6, 9 months in control plots to determine quarterly mass loss.
- Analyses on extracts:
  - pH, EC, DOC, SUVA254.
- Data outputs:
  - Percentage mass loss (%ML) and related metrics; DOC concentrations in extracts.
- Acronyms:
  - M = Migneint, PN = Peaknaze, Pod = Podzol, EC = Electrical conductivity, DOC = Dissolved organic carbon, TN = Total nitrogen, %ML = Percentage mass loss, S = Sphagnum, E = Eriophorum, CM/CP/ F/P = genus/site-specific litter identifications.

### TBI_Data.csv
- Purpose: apply Tea Bag Index (TBI) methodology to measure decomposition rates and stabilisation under acidity treatments.
- Tea types: Green tea and Rooibos tea bags (Lipton); three sets per plot.
- Field procedure:
  - Tea bags buried in July 2016 for 90 days; subjected to three pH treatment applications.
  - Retrieved Oct 2016; mass loss used to compute:
    - k_TBI (decomposition rate)
    - S (stabilisation factor; extent of organic matter stabilisation from labile to resistant forms)
- Acronyms:
  - M = Migneint, PN = Peaknaze, Pod = Podzol, S = Stabilisation factor, K = Decomposition rate.

## Field experiment design and data collection (context for data quality and governance)

- Locations and plots:
  - Two UK sites: Migneint (North Wales) and Peaknaze (Northern England).
  - At each site: two soil types (peat, peaty podzol); four experimental plots per site-type combination (Migneint Peat, Migneint Podzol, Peaknaze Peat, Peaknaze Podzol).
  - Each plot uses a randomized blocked design with four replicates for control, acid, and alkaline treatments.
- Treatments and timing:
  - Treatments applied Oct 2008–Dec 2012; re-established Jan 2015–Oct 2016 following the same design and allocations.
  - Acid treatment: H2SO4 in rainwater (50 kg S ha^-1 yr^-1 at podzol, 100 kg S ha^-1 yr^-1 at peat); alkaline treatment: NaOH/KOH with MgCl2/CaCl2 rinse to maintain base cation ratios.
  - Control: rainwater only; 20 L per application.
  - Aimed to mimic ambient sulphur deposition and balance soil chemistry changes via buffering considerations.
- Data collection and stewardship:
  - All data collection and interpretation conducted by Dr. Catharine Pschenyckyj (PhD work, University of Reading).
  - Metadata describes sampling depth, materials, extraction procedures, and instrumentation to support traceability and reuse.
- Data provenance and references:
  - Data linked to publications on soil acidity and DOC mobility, and Tea Bag Index methodology, with cited sources for methods and context.

## Data governance and reuse considerations for Data Stewards

- Standards and interoperability:
  - Clear metadata for each dataset including sampling methods, units, acronyms, and measurement techniques to facilitate cross-study reuse.
- Data availability and updates:
  - Documentation of treatment timelines and plot allocations aids reproducibility and future updates or re-analysis.
- Data quality and provenance:
  - Detailed lab methods (e.g., DOC via TIC subtraction, SUVA254 calculation, extraction ratios) support reproducibility and error tracing.
- Challenges to anticipate:
  - Heterogeneous data types and formats across datasets; bespoke methods may require careful documentation for interoperability.
  - Timeliness of data submission and alignment with existing governance policies for sharing and embargo management.

## References
- DUDDIGAN, S., SHAW, L. J., ALEXANDER, P. D. & COLLINS, C. D. 2020. Chemical Underpinning of the Tea Bag Index: An Examination of the Decomposition of Tea Leaves. Applied and Environmental Soil Science, 2020.
- EVANS, C. D., JONES, T. G., BURDEN, A., OSTLE, N., ZIELIŃSKI, P., COOPER, M. D. A., PEACOCK, M., CLARK, J. M., OULEHLE, F., COOPER, D. & FREEMAN, C. 2012. Acidity controls on dissolved organic carbon mobility in organic soils. Global Change Biology, 18, 3317-3331.
- KEUSKAMP, J. A., DINGEMANS, B. J. J., LEHTINEN, T., SARNEEL, J. M. & HEFTING, M. M. 2013. Tea Bag Index: a novel approach to collect uniform decomposition data across ecosystems. Methods in Ecology and Evolution, 4, 1070-1075.