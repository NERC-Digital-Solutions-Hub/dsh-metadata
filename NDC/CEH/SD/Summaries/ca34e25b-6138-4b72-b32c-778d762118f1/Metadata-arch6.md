# Vegetation cover at 54 UK Butterfly Monitoring Scheme sites in southern England, 2008-9

## Overview
- Study of vegetation cover estimates from 54 sites in southern England, all primarily semi-natural grassland.
- Part of the UK Butterfly Monitoring Scheme (UKBMS); data gathered by Robin Curtis during his PhD fieldwork.

## Experimental design & data collection
- Surveys conducted in summer 2008 and 2009, mostly in August.
- UKBMS transect structure used to determine quadrat count and locations.
- Transects divided into sections (1–15 per site; mean 7.5).
- Four 1 m² quadrats per section -> total of 1,624 quadrats (54 sites × ~7.5 sections × 4 quadrats).
- Quadrat locations determined by random points within a 10 m wide polygon centered on the transect route.
- For each quadrat:
  - Recorded plant species as percentage cover.
  - For flowering plants: counted flower heads and florets; subset that were inflorescent.
  - On average, 10.3 plant species per quadrat; 16,720 species-quantity estimates across 165 species.
- Site-level aggregation: 2,934 plant:site combinations; mean ~54.3 plant species per site.
- Vegetation structure captured as percentage cover in four categories: bare ground, grass, herbaceous, woody.
- Also recorded percentage cover of dung.

## The dataset
- Two CSV files: Vegetation.csv and Quadrats.csv.

### Vegetation.csv
- Contains 16,720 vegetation cover estimates.
- Key columns:
  - Taxon.name: Latin binomial
  - Common.name: English common name
  - Site.name: UKBMS transect route name (matches Quadrats.csv)
  - BMS.ID: UKBMS transect unique identifier (matches Quadrats.csv)
  - Section: transect section number
  - Date: quadrat survey date (matches Quadrats.csv)
  - QuadratNum: quadrat replicate number within the section
  - %Cover: plant cover percentage
  - FH: number of flower heads
  - FI: number of florets
  - Fl_I: number of flower heads that are inflorescences
  - Fl: number of florets on inflorescences

### Quadrats.csv
- Contains 1,624 quadrat-level details (linked to Vegetation.csv via Site.name and BMS.ID, etc.).
- Key columns:
  - Site.name, BMS.ID: identifiers matching Vegetation.csv
  - GRIDREF: centroid grid reference
  - LATITUDE, LONGITUDE: geographic coordinates
  - Date: quadrat date (matches Vegetation.csv)
  - Section, QuadratNum: transect section and quadrat within section
  - Aspect: slope direction (rounded to 5 degrees)
  - Slope: slope angle (nearest 5 degrees)
  - Unevenness.cm: vertical unevenness within quadrat
  - Distance: distance from ground to crown base of vegetation
  - Av.Turf.Height: average turf height
  - %BareGround, %GrassLayer, %HerbLayer, %WoodyLayer, %Dung: structural/cover metrics

### Scope and scale
- 54 sites, 1,624 quadrats, 165 plant species represented.
- 16,720 vegetation cover estimates; approximately 54.3 plant species per site on average.

## Data quality & considerations
- Field-collected data through standardized UKBMS transect framework.
- Random quadrat placement within a defined polygon enhances sampling representativeness.
- Detailed metadata enables robust joining across files (Site.name, BMS.ID, Date, Section, QuadratNum).
- Measurements include both quantitative cover and counts related to flowering structure (FH, FI, Fl_I, Fl).

## Potential data products and use cases (Data Support perspective)
- Self-serve exploration of plant species composition and vegetation structure by site, section, or quadrat.
- Dashboards or pivot-style summaries showing:
  - Species richness per site
  - Most abundant species by transect
  - Proportions of bare ground, grasses, herbs, and woody vegetation
  - Spatial patterns using LATITUDE/LONGITUDE and GRIDREF
  - Temporal comparisons between 2008 and 2009 (where dates align)
- Data integration with UKBMS butterfly monitoring data to explore plant-butterfly habitat associations.
- Data cleaning/quality checks workflows:
  - Join Vegetation.csv and Quadrats.csv on Site.name/BMS.ID/Date/Section/QuadratNum
  - Validate percent cover sums and consistency of structural categories
  - Geospatial validation using LAT/LONG and GRIDREF
- Reproducible data products for policy or conservation reporting, including site-level species lists and habitat structure summaries.

## References
- Carey, P. D., et al. (2008). Countryside Survey: UK Headline messages from 2007.
- Shimwell, D. W. (1972). The description and classification of vegetation.