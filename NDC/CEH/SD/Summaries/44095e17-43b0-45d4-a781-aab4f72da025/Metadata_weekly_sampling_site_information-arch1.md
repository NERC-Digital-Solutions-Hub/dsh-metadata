# DRAINAGE AREAS AND STREAM FLOW CONVERSION

- This document catalogs multiple monitoring sites within the Hafren, Hore, Tanllwyth, and related catchments around Plynlimon, mid-Wales, detailing site metadata, hydrological sampling points, forestry management history, and associated references. It includes stream channels, rainfall, cloud water, groundwater components, and borehole data, with published references spanning 1997–2010. Time coverage varies by site, with many records starting in the early to mid-1980s and continuing into the 1990s and 2000s.

## Data scope and site types

- Site metadata and descriptors
  - Location codes (e.g., A: Lower Hore, B: Lower Hafren, C: Rainfall, D: Upper Hore, E: Stemflow, F: Throughfall, G: Upper Hafren, H: South 2 Hore, J: Cloud, T: Quarry 1 Borehole, K: Tanllwyth, AD: Tanllwyth Bridge, M: South East 1, V: South East 3, P: Tan North, Q: Tan South, AA–Z: various Vyrnwy-related sites, VB1: Valley Bottom, BCL/CCL: chloride datasets, AG: Carreg Wen nitrogen, etc.)
- Measurement types and data streams
  - Stream discharge measurements (e.g., Tanllwyth flume readings)
  - Water chemistry and hydrochemistry data (chloride, total dissolved nitrogen, etc.)
  - Rainfall measurements (Rainfall site at Carreg Wen; Vyrnwy rainfall)
  - Cloud water and throughfall data
  - Groundwater-related data (Tanllwyth boreholes; various Upper/Lower slope and Hafren groundwater areas)
- Physical and environmental context
  - Main soil types (Podzol, Gley, Brown Earth, etc.)
  - Vegetation and land management (plantation Sitka spruce, moorland, standing crop, clearfelling events; 1985–1988, 1995, 1996, 1997, etc.)
  - Mining history (historic Pb/Zn near upper catchment)
- Temporal coverage and data treatment notes
  - Start and end dates per site; some datasets are ongoing
  - Tanllwyth time series notes: samples after 7 March 1995 affected by borehole; recommended long-term series use Tanllwyth through 7 Mar 1995 and Tanllwyth Bridge thereafter
  - References linked to site data (primary reference numbers 1–10) detailing methodological and hydrochemical findings
- Data provenance
  - Primary references provide published hydrology/hydrochemistry context for catchment-scale interpretation (e.g., effects of conifer harvesting on water quality, rainfall and cloud water chemistry, groundwater occurrences)

## Metadata quality and considerations

- Data granularity and locality
  - Many sites are local to specific sub-catchments and may be at different scales; local administrative boundaries and sampling points vary
- Data integration challenges
  - Some fields are repeated, split across multiple lines, or partially missing (e.g., some “END DATE” fields shown as “Cont..”)
  - Datasets are linked to a series of publications; cross-referencing is required to interpret methods and quality controls
- Time synchronization and borehole effects
  - Borehole introductions can affect long-term time series; awareness of borehole-related artifacts is necessary for trend analysis
- Legal and access considerations
  - Much of the data appear to be historical and derived from published references; raw data may require access through the referenced publications or data portals with metadata

## Reference framework and data provenance

- References (selected examples by site group)
  - Rainfall, Cloud, Throughfall, and related hydrochemistry series referenced in multiple works (e.g., Neal et al. 1997; Neal et al. 2003; Neal et al. 2004; Neal et al. 2010)
  - Specific site groups (Upper/Lower Hafren, Tanllwyth, Vyrnwy, etc.) associated with targeted hydrochemical studies and catchment responses to forestry activities
- Publication years and topics
  - 1997–2010 period with topics including: cloud water and rain chemistry, hydrochemistry of the River Severn headwaters, nitrogen in rainfall and streamwater, impact of conifer harvesting on stream water quality, and groundwater occurrence in upland Wales

## Drainage areas and stream flow conversion

- Catchment areas (sq. km)
  - Lower Hore (A): 3.172
  - Upper Hore (D): 1.62
  - Tanllwyth (K): 0.916
  - Lower Hafren (B): 3.58
  - Upper Hafren (G): 1.22
  - Note: Upper Hafren drainage area is 122 ha to the flow gauging structure and 117 ha to the chemistry sampling point
- Flow conversion formulas
  - To convert from Cumecs to mm/15 min (flow): mm/15min = cumecs × 0.9 ÷ (catchment area in km^2)
  - To convert from mm/15 min to Cumecs: cumecs = (mm/15min) × (catchment area in km^2) ÷ 0.9

## Analytical opportunities for an data-driven analyst

- Correlation and causation analyses
  - Investigate relationships between forestry management (clearfell events) and stream water chemistry, including chloride and nitrogen species
- Temporal trend analysis
  - Exploit start/end dates and borehole notes (e.g., Tanllwyth data pre- vs post-borehole introduction) to assess data consistency and long-term trends
- Spatial integration and scaling
  - Use the provided catchment areas to normalize flow and water quality data across sites for comparative analyses
- Hydrological modeling
  - Apply the provided conversion factors to harmonize discharge data (cumecs) with precipitation/flow metrics (mm/15min) for model calibration
- Multi-proxy hydrochemistry synthesis
  - Combine rainfall, cloud water, throughfall, stemflow, and groundwater datasets to understand atmospheric deposition and redistribution within the catchments
- Data provenance and reproducibility
  - Leverage the primary reference numbers and cited publications to document methodologies, QA steps, and data transformations for reproducible analyses

## Quick data pointers

- Start with the catchment areas and flow conversion section to align hydrological calculations
- Use site metadata (coordinates, soil types, vegetation, land management) to contextualize water quality signals
- Refer to the cited publications for methodological guidance and to interpret hydrochemical findings across sites
- Pay attention to borehole effects and sampling date cutoffs (Tanllwyth pre- vs post-1995) when constructing time series