# Amazon Fertilization Experiment (AFEX)

## Context and Study Area
- Conducted within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, Brazil.
- Location details: 41-km vicinal road ZF-3 of BR-174 (02°24'S, 59°52'W).
- Environment baseline:
  - Soils: clay-rich Ferralsols (~30% of the Amazon Basin).
  - Climate: annual rainfall 1900–2500 mm with a pronounced dry season (June–October).
  - Forest structure: above-ground biomass (AGB) 322 ± 54 Mg ha^-1 (ind. ≥10 cm DBH); mean wood density 0.67 g cm^-3.
  - Species richness: ~280 species (≥10 cm DBH) per hectare.

## Experimental Design: Amazon Fertilization Experiment (AFEX)
- Full factorial design with eight treatments and four replicates per treatment (32 plots total), arranged in four independent blocks at least 200 m apart.
- Treatments: combinations of Nitrogen (N, 125 kg N ha^-1 yr^-1 as urea), Phosphorus (P, 50 kg P ha^-1 yr^-1 as triple superphosphate), and Cations (K, Ca, Mg):
  - Control; N; P; cations; N+P; N+cations; P+cations; N+P+cations.
- Plot layout: 50 m x 50 m plots, with at least 50 m separation between plots.
- Fertilization protocol: annual, delivered in three applications to mitigate nutrient leaching and runoff.

## Data Collection: Leaf Area Index (LAI) Measurements
- LAI measured at 36 points per plot using LAI-2200 C.
- Measurement window: 6:00–17:00 (avoiding 12:00–14:00 to reduce sun impact).
- Sensor setup: above-canopy reference read by the instrument; sensor placed in clearings; field orientation maintained (west in morning, east in afternoon); view cap used to keep operator out of sensor view; sensors matched before data collection.
- Data processing: FV2200 software to compute LAI with 5 rings, 4 rings, and 3 rings (LAI_5_rings, LAI_4_rings, LAI_3_rings).
- Sampling dates: October 2017, March 2018, August 2018, October 2018 (Central Amazon, Manaus region).

## Data Management and Dataset Structure
- Data collection spreadsheet (Figure 4) captures:
  - CENSO: PlotID (block and plot codes)
  - B_Obs: observed metric
  - Time: sampling time (hours:minutes:seconds)
  - LAI_5_rings, LAI_4_rings, LAI_3_rings: LAI values
  - Date: campaign date (year_month)
  - coord x and coord y: plot sampling coordinates (0–50 m grid)
- Example columns and descriptors:
  - Column D/E/G/H: time and LAI values for 5/4/3 rings
  - Column J: Date (e.g., October_2017)
  - Columns K-L: coordinate positions (x, y) in plot
- Data deposited in EIDC system (Figure 4 caption indicates deposition of the leaf area index dataset).

## Site Context and References
- References provide context on regional forest structure and soil properties (e.g., DUQUE et al. 2017; De Oliveira & Mori 1999; Quesada et al. 2011; Rankin de Merona et al. 1992).

## Relevance to Environmental Monitoring
- Standardized, repeatable LAI measurements across a factorial fertilization experiment enable assessment of canopy responses to nutrient additions over time.
- Data are stored and accessible via an established data portal (EIDC), supporting transparency, reuse, and cross-study integration.
- The documented methodology supports reproducibility and comparability with other environmental monitoring datasets, aligning with the goal of tracking environmental health and policy-relevant outcomes over time.
- Key challenges addressed include increasing dataset value through integration with other data sources and ensuring access to underlying data used to generate outputs.