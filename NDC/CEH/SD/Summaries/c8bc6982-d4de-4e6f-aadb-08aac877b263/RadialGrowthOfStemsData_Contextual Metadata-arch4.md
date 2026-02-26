# Radial growth in stems in human-modified forests of Eastern Amazonia

- Dataset: RadialGrowthOfStemsData.csv
- Purpose: Measurements of radial growth of stems (via dendrometers) across 20 Amazonian forest plots along a disturbance gradient prior to and during El Niño, collected Dec 2014–Sep 2018.
- Context: Part of the NERC Human-modified Tropical Forests Programme (HMTF).

## Data scope and disturbance gradient

- 20 plots divided into five plots per disturbance class:
  - undisturbed primary forests
  - logged primary forests
  - logged-and-burned primary forests
  - secondary forests
- Disturbance classification combines:
  - canopy disturbance analysis from a 1988–2010 satellite chronosequence
  - field assessments of fire scars, charcoal, and logging debris
- Includes El Niño impact data: Fire_ElNino flag indicates whether each plot burned during the 2015–16 El Niño.

## Data collection methods

- Per plot:
  - Trees and palms stratified into five DBH size classes (1019.99 cm, 20–29.99 cm, 30–39.99 cm, 40–49.99 cm, ≥50 cm)
  - At least 50 dendrometer bands per plot, distributed evenly across size classes (10 bands per class)
  - Dendrometer bands installed 10 cm above DBH measurement point; also installed on all lianas ≥10 cm DBH
- Procedure:
  - After installation, wait one month to mark the zero-growth line
  - First measurement 5 months after marking; measurements then monthly
  - If a band is damaged, it is replaced and reinstalled following the same procedure
  - If a stem dies, its band is removed and a new band is installed on another stem in the same size class
- Growth observations:
  - Some stems show negative growth due to water loss; no correction applied (positive growth includes water accumulation)

## Data structure and variables

- CSV: RadialGrowthOfStems.csv
- Key fields:
  - Catchment, Transect, Plot: plot identifiers
  - Rainfor: plot code in the ForestPlots database
  - Forest: disturbance class before the 2015–16 El Niño
  - Fire_ElNino: whether the plot burned during El Niño
  - Tree_tag, Tree_code: individual identifiers and codes
  - DBH: diameter at breast height (2014)
  - Life form: A (tree), C (liana), P (palm)
  - Re-installed: whether the dendrometer was re-installed during the collection
  - Data-Dec14, mm-Dec14, OBS-Dec14, etc.: monthly data columns for December 2014 onward
- Monthly coverage: radial growth measurements in millimeters (mm) with corresponding observational notes (OBS-YYYYMM)

## Spatial and temporal coverage

- Plot coordinates provided for all 20 plots (latitude and longitude for each plot)
- Temporal span: December 2014 to September 2018
- Spatial scope: Eastern Amazonia, across multiple microcatchments and forest categories

## Data quality, notes, and governance

- Data collection details allow assessment of methodological consistency across plots and time
- Handling of anomalies:
  - Negative growth permitted as a natural consequence of bark water dynamics; not corrected
  - Reinstallation events and missing bands are recorded to maintain data lineage
- Metadata richness supports transparency and reproducibility, including disturbance classification criteria, El Niño context, and measurement procedures

## Practical implications for use

- Enables analysis of radial growth responses to disturbance type (primary, logged, logged-and-burned, secondary) and El Niño events
- Facilitates exploration of how growth relates to initial DBH, life form (tree, liana, palm), and reinstallation history
- Suitable for cross-plot comparisons and integration with canopy disturbance and fire history data
- Useful for data governance teams to audit data provenance, measurement cadence, and metadata completeness across long-term ecological datasets