# Sampling Regime

## Study Area and Temporal Coverage
- Western Amazonian basin, Tambopata National Reserve, Madre de Dios, Peru (lat 12°49' S, lon 69°16' W).
- Sampling of two small streams (MT Main Trail, NC New Colpita) and two rivers (LT La Torre, TP Tambopata).
- Campaigns: February 2011–May 2012; targeted wet and dry seasons.
- MT dries during the dry season; no MT samples Sept–Nov 2011.
- Upstream catchments: LT ~2000 km2, TP ~14000 km2.

## Data Collected
- Fluvial carbon and nutrients:
  - DIC (mg/L) and δ13C-DIC (‰)
  - DOC (mg/L)
  - POC (mg/L)
  - Nutrients: Ca, Mg, K, Na (mg/L); P (totP, μg/L); Si (mg/L)
- Rainfall fractions dataset includes DIC, δ13C-DIC, DOC, POC, Ca, Mg, K, Na, totP, Si for:
  - Rain water, Throughfall, Stemflow, Overland flow
- Rainfall sampling sites: throughfall collectors at TAM9 plot; stemflow collected from eight diverse-tree species; overland flow collected at stream banks.

## Sampling Campaigns and Coverage
- Three fluvial campaigns: Feb–Apr 2011; Sept–Dec 2011; Mar–May 2012.
- MT not sampled in Sept–Nov 2011 due to dry-season drying.
- Rainfall fractions collected Apr–May 2012.
- Data point counts are provided per site (NC, MT, LT, TP) for each variable in Tables 1 and 2; datasets include both streams/rivers and rainfall fractions.

## Sampling and Analytical Methods
- DIC: pre-acidified exetainers; headspace method with GasBench/Delta V Plus; triplicate exetainers; δ13C measured.
- DOC: filtered (0.7 μm GF/F), acidified to pH 3.9, degassed; measured by TOC combustion.
- POC: measured by loss on ignition after drying and combustion.
- Cations and nutrients: Ca and Mg by Atomic Absorption Spectrometry; K and Na by flame photometry; totP by colorimetric phosphomolybdate/ascorbic acid; Si by heteropoly blue method.
- QA/QC: drift correction standards every ~10 samples; randomised sample order; multiple replicates; calibration standards and drift checks for DOC and cations; standard repeats for instrument stability.

## Data Structure and Content
- File types: two CSV datasets (Amazon streams and nutrients; Amazon rainfall fractions and nutrients).
- Columns:
  - Streams/rivers: Time (hh:mm:ss), Date (dd/mm/yyyy), Type (stream/river), Site (MT, NC, LT, TP), CollectorID (for rainfall; or sampling identifier), DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, TotP, Si.
  - Rainfall fractions: Time, Date, Type (TF, SF, OF, RW), CollectorID (TF tree name or EI for rainwater), and corresponding DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, TotP, Si.
- NA values indicate data not analysed.
- Detection and unit details align with methods described.

## Data Quality, Access, and Usage
- Prior submissions exist for portions of the data (DOI references provided); this release consolidates additional campaigns (notably including last two campaigns for some variables).
- Data suitable for: assessing hydrological controls on carbon concentrations, seasonal and flow-variation analyses, cross-system comparisons (streams vs rivers), and multi-source data integration.
- Datasets enable correlation analyses between DIC/DOC/POC and inorganic nutrients, isotopic signatures, and rainfall inputs at varying scales (site-level to catchment).