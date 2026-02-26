# Amazon Fertilization Experiment (AFEX)

## Context and Study Area
- BDFFP area, KM41 reserve, ~100 km from Manaus, Brazil; location coordinates 02 24'S, 59 52'W.
- Soils: clay-rich Ferralsols (~30% of the Amazon Basin).
- Climate: 1900–2500 mm annual rainfall with a pronounced dry season (Jun–Oct).
- Forest metrics at KM41: above-ground biomass (AGB) ~322 ± 54 Mg ha-1 (≥10 cm DBH); mean wood density ~0.67 g cm-3; ~280 species (≥10 cm DBH) per ha.

## Experimental Design and Plot Layout
- Amazon Fertilization Experiment (AFEX) started in March 2017; full factorial with eight treatments.
- 32 plots total: 4 replicates per treatment, arranged in four independent blocks at least 200 m apart.
- Plot dimensions: 50 × 50 m; plots within blocks ≥50 m apart.
- Nutrient treatments: combinations of N (125 kg N ha-1 yr-1 as urea), P (50 kg P ha-1 yr-1 as triple superphosphate), and cations (K 50 kg K ha-1 yr-1 as KCl; Ca 160 kg Ca ha-1 yr-1; Mg 160 kg Mg ha-1 yr-1 as dolomitic limestone).
- AFEX 2.0: plot delineation with location maps showing blocks and plots inside KM41; fertilization occurs annually in three applications to mitigate nutrient loss.

## Data Collection Methods
- LAI measurements collected at 36 points per plot using LAI-2200 C.
- Sampling window: 06:00–17:00 (avoid 12:00–14:00); above-canopy reference reading required; sensor oriented consistently (west in morning, east in afternoon).
- Data collection procedure: system immersement with a 45° view cap; sensors matched before collection.
- LAI computation using FV2200 software with 5-, 4-, and 3-ring configurations.
- Sampling campaigns: Oct 2017, Mar 2018, Aug 2018, and Oct 2018 (Central Amazon, Amazonas, Manaus).

## Data Output and Structure
- LAI data produced per plot, per date, and per ring configuration (LAI_5_rings, LAI_4_rings, LAI_3_rings).
- Spatial sampling: 36 points per plot with intra-plot coordinates (coord x and coord y) at 0, 10, 20, 30, 40, 50 m.
- Spreadsheet schema (CSV-like) includes:
  - CENSO: PlotID; B_Obs: 36 sampling points; Time: collection time; LAI_5_rings; LAI_4_rings; LAI_3_rings; Date (YYYY_MM); coord x; coord y.
- Example data organization shows repeated campaigns and per-point records for each date and ring configuration (e.g., October_2017 data entries).

## Spatial, Temporal, and GIS Considerations
- Spatial enabling: point-level LAI data tied to precise plot coordinates within each 50×50 m plot, suitable for creating high-resolution LAI maps across AFEX plots.
- Temporal dimension: multiple campaigns allow time-series analysis of LAI responses to fertilization treatments.
- Linkages: LAI measurements can be joined with plot-level attributes (treatment, block) and environmental layers (soil type, rainfall) for GIS analyses and map-based data products.

## Data Quality, Standards, and Provenance
- Data collection required careful standardization across rings/time and post-collection cleaning/transformations.
- Data are stored in the EIDC system (as indicated by figure captions), implying a centralized data repository and need for metadata alignment.
- References provided for underlying site characterization and prior work.