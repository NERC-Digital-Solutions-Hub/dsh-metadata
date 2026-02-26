# Vegetation cover at 54 UK Butterfly Monitoring Scheme sites in southern England, 2008-9

## Overview
- Study of vegetation cover estimates across 54 sites in southern England, part of the UK Butterfly Monitoring Scheme (UKBMS); vegetation dominated by semi-natural grassland.
- Data gathered as part of a PhD fieldwork by Curtis; intended to support environmental monitoring within UKBMS.

## Methods: Experimental Design & Collection
- Surveys conducted in summer 2008 and 2009, predominantly August.
- UKBMS transect structure used to define quadrats: transects divided into 1–15 sections (mean 7.5).
- Four 1 m² quadrats per section → total 1,624 quadrats (54 sites × ~7.5 sections × 4 quadrats).
- Quadrat positions chosen randomly from a 10 m wide polygon centered on the transect route.
- For each quadrat, record:
  - Plant species percent cover (area occupied by foliage/stems).
  - Flower counts: number of flower heads, number of florets, and subset that are inflorescent.
- Outputs include an average of 10.3 plant species per quadrat; total of 16,720 plant abundance estimates across 165 species.
- Site-level aggregation yields 2,934 plant:site combinations, average 54.3 plant species per site.
- Structure categories recorded: percent cover of bare ground, grass, herbaceous, and woody vegetation; percent dung.

## The Dataset: Structure and Contents
- Two files: Vegetation.csv and Quadrats.csv.

- Vegetation.csv (16,720 vegetation-cover estimates) includes:
  - Taxon.name, Latin binomial, Common.name
  - Site.name, BMS.ID, Section, Date, QuadratNum
  - %Cover, FH (flower heads), FI (florets), Fl_I (flower heads that are inflorescences), Fl (florets on inflorescences)

- Quadrats.csv (1,624 quadrat records) includes:
  - Site.name, BMS.ID, GRIDREF, LATITUDE, LONGITUDE
  - Date, Section, QuadratNum
  - Aspect, Slope, Unevenness.cm, Distance (cm from ground to crown base)
  - Av.Turf.Height, %BareGround, %GrassLayer, %HerbLayer, %WoodyLayer, %Dung

- Both files share keys for linkage: Site.name, BMS.ID, Section, QuadratNum, Date (i.e., quadrats align across the two datasets).

- References for methodology:
  - Carey, P. D. et al. 2008. Countryside Survey: UK Headline messages from 2007.
  - Shimwell, D. W. 1972. The description and classification of vegetation.

## Outputs and Monitoring Utility
- Provides a standardised dataset compatible with UKBMS structures, enabling monitoring of environmental health and policy performance over time.
- Outputs suitable for reports, maps, and charts; supports site- and species-level analyses across the transects.

## Data Management and Access
- Emphasises storing and uploading created datasets to appropriate data portals for accessibility.
- Highlights ongoing challenges:
  - Increasing the value of datasets by integrating with other relevant data.
  - Enabling broad access to the underlying data used to produce final outputs.