# Fieldwork Sampling - Experimental Design and Collection Methods

## Overview
- Seasonal field experiments conducted in July 2016, October 2016, February 2017, and March 2017 at Wood Brook, Staffordshire.
- Four fluorometers deployed at sites 1–4, creating three sub-reaches: 1-2, 2-3, and 3-4.
- Reaches 1-2 and 2-3 are sand-dominated; reach 3-4 is gravel-dominated.
- Reach lengths: 1-2 = 239.3 m, 2-3 = 289.2 m, 3-4 = 165.1 m.

## Experimental Design
- Instantaneous tracer injections using both conservative (fluorescein) and reactive (resazurin) tracers dissolved in stream water.
- Injections: 1.2 g fluorescein and 8 g resazurin for Oct/Feb/Mar; 2 g fluorescein and 8 g resazurin for July.
- Injection site located 180 m upstream of site 1 in July; 250 m upstream of site 1 in other seasons.
- Injection times: July at 18:47; October at 14:10; February at 14:09; March at 14:29.
- Breakthrough curves (BTCs) measured at all four sites.

## Equipment and Calibration
- Four field fluorometers calibrated in the field immediately prior to tracer injections.
- Calibration setup used a connected loop with identical flow through all fluorometers.
- Calibration solutions diluted with stream water; two-point calibration: zero (stream water) and reference concentrations (70 ppb fluorescein, 100 ppb resazurin, 100 ppb resorufin).
- readings stabilized over 2–3 minutes per calibration solution.

## Data Collection and Measurements
- BTCs recorded in units of parts per billion (ppb) with in-situ measurements.
- Data corrected for temperature and turbidity (as per Blaen et al., 2017) and tail baseline adjustments; drift corrections applied between start and end of BTC.
- Background concentrations adjusted to zero where needed (fluorescein, resazurin, resorufin are not naturally present in streams).

## Analytical Methods
- On-line fluorometers (GGUN-FL30, Albillia Sàrl) configured to excite/measure fluorescein, resazurin, and resorufin at 470, 570, and 525 nm respectively.
- Field calibration performed with stream water immediately before tracer injection.
- Fluorometers configured to measure every 10 seconds during the study.

## Data Structure
- One CSV file: Fluorescein_resazurin_resorufin_breakthrough_curves_Wood_Brook_UK_2016_2017 (64 columns).
- Columns are repeated for each sampling season and site: Date-Time (GMT), Fluorescein Concentration (ppb), Resazurin Concentration (ppb), Resorufin Concentration (ppb).
- Season and site identifiers are placed above the corresponding Date-Time columns.

## Geospatial Context and Visualization Opportunities for GIS
- Spatial layout includes four sampling sites across three reaches with distinct channel morphologies (sand vs gravel).
- Data supports mapping tracer concentrations over time by site and season, and linking to reach geometry and length.
- Calibration, correction steps and measurement cadence documented, enabling quality-assured GIS-based visualizations and analyses.
- Potential for integrating with other spatial datasets (e.g., stream network, reach delineations, site coordinates) to produce map-based data products and exploratory visualizations.

## References
- Blaen, P. J., et al. 2017. Multitracer Field Fluorometry: Accounting for Temperature and Turbidity Variability During Stream Tracer Tests. Water Resources Research.
- Lemke, D., et al. 2013. On-line fluorometry of multiple reactive and conservative tracers in streams. Environmental Earth Sciences.