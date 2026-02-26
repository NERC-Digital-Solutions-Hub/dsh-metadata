# Vegetation cover at 54 UK Butterfly Monitoring Scheme sites in southern England, 2008-9

## Overview
- Vegetation cover estimates from 54 sites in southern England, conducted as part of Robin Curtis’s PhD fieldwork; all sites are part of the UK Butterfly Monitoring Scheme (UKBMS).
- Focused on semi-natural grassland vegetation; site-level data linked to UKBMS transects.
- Provides baseline measures of plant community composition and vegetation structure that can inform habitat quality assessments for butterflies and broader environmental monitoring.

## Methods (Experimental Design & Collection Methods)
- Surveys conducted in summer 2008 and 2009, predominantly August.
- UKBMS transect structure used to determine quadrat locations: transects divided into 1–15 sections (mean 7.5).
- Four 1 m² quadrats placed in each section, totaling 1,624 quadrats (54 sites × ~7.5 sections × 4 quadrats).
- Quadrat positions chosen at random within a 10 m wide polygon centered on the transect route.
- For each quadrat: recorded plant species percent cover; counts of flower heads, florets, and inflorescences; average of ~10.3 plant species per quadrat.
- Data aggregated to site level: 2,934 plant:site combinations; mean ~54.3 plant species per site.
- Vegetation structure recorded as percent cover in four categories (Bare ground, Grass, Herbaceous, Woody) and included dung cover.

## The dataset
- Consists of two files: Vegetation.csv and Quadrats.csv.

### Vegetation.csv
- Contains 16,720 vegetation cover estimates.
- Key columns:
  - Taxon.name, Latin binomial, Common.name
  - Site.name, BMS.ID, Section, Date, QuadratNum
  - %Cover (plant cover)
  - FH (flower heads), FI (florets), Fl_I (inflorescent heads), Fl (florets)

### Quadrats.csv
- Contains 1,624 quadrat-level metadata.
- Key columns:
  - Site.name, BMS.ID
  - GRIDREF, LATITUDE, LONGITUDE
  - Date, Section, QuadratNum
  - Aspect, Slope, Unevenness.cm
  - Distance, Av.Turf.Height
  - %BareGround, %GrassLayer, %HerbLayer, %WoodyLayer, %Dung

## Data fields and structure (highlights)
- Site identifiers link Vegetation.csv and Quadrats.csv (Site.name, BMS.ID).
- Spatial data provided (GRIDREF, LATITUDE, LONGITUDE) for mapping and spatial analyses.
- Temporal data provided (Date) for trend assessment across 2008–2009.
- Detailed vegetation metrics include species-level cover, reproductive structures (flower heads, florets), and broad vegetation structure categories.

## Data quality and references
- Methods anchored to standardized UKBMS transect methodology for comparability across sites and time.
- References for methodology:
  - Carey et al. (2008) UK Headline messages from 2007, Countryside Survey.
  - Shimwell (1972) Vegetation description and classification.

## Relevance for environmental monitoring and policy
- Provides quantitative measures of plant community composition and vegetation structure across multiple habitat sites, enabling:
  - Assessment of habitat suitability and quality for target species (e.g., butterflies) within UKBMS contexts.
  - Baselines for detecting changes in vegetation communities over time.
  - Integration with butterfly monitoring data to explore habitat–population relationships.
  - Spatial analysis and mapping of vegetation characteristics using precise location data.

## Considerations for data governance and use
- Dataset comprises publicly structured CSV files with explicit field definitions, enhancing transparency and reusability.
- Rich metadata supports data verification and integration with other monitoring datasets.
- Temporal scope limited to two summers (2008–2009) and to August surveys, which should be considered in trend analyses.
- Consistent data collection protocols (quadrats per section, standardized cover measures) support comparability across sites.