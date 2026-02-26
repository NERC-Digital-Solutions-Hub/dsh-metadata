# Vegetation cover at 54 UK Butterfly Monitoring Scheme sites in southern England, 2008-9

## Overview
- Vegetation cover estimates collected as part of a PhD field study at 54 sites in southern England.
- All sites are semi-natural grasslands within the UK Butterfly Monitoring Scheme (UKBMS).
- Data intended to support understanding of vegetation structure and plant composition in butterfly monitoring context.

## Experimental Design & Data Collection
- Surveys conducted in summer 2008 and 2009, mainly in August.
- UKBMS transect framework used to determine quadrat locations and numbers.
- Transects divided into 1–15 sections (mean 7.5); four 1 m² quadrats per section (total 1,624 quadrats: 54 sites × 7.5 sections × 4 quadrats).
- Quadrat locations chosen at random from a 10 m wide polygon centered on the transect route.
- For each quadrat: record of plant species cover as a percentage, plus counts of flower heads and florets (and subset that are inflorescent).
- Average of 10.3 plant species per quadrat; 16,720 plant-abundance estimates across 165 species.
- Data aggregated to site level yield 2,934 plant:site combinations, averaging 54.3 plant species per site.
- Vegetation structure recorded as percentages in four categories: Bare ground, Grass, Herbaceous, Woody; plus %Dung.
- Background sources referenced: Carey et al. 2008; Shimwell 1972.

## The Dataset: Vegetation.csv
- Contains 16,720 vegetation-cover estimates.
- Key columns:
  - Taxon.name; Latin binomial; Common.name
  - Site.name; BMS.ID
  - Section; Date; QuadratNum
  - %Cover
  - FH (flower heads); FI (florets)
  - Fl_I (flower heads that are inflorescences); Fl (number of florets)
- Link to Quadrat data via Site.name, BMS.ID, Section, and QuadratNum.

## The Dataset: Quadrats.csv
- Contains additional site- and quadrat-level information for the 1,624 quadrats.
- Key columns:
  - Site.name; BMS.ID
  - GRIDREF; LATITUDE; LONGITUDE
  - Date; Section; QuadratNum
  - Aspect; Slope; Unevenness.cm
  - Distance (from ground to crown base)
  - Av.Turf.Height
  - %BareGround; %GrassLayer; %HerbLayer; %WoodyLayer; %Dung

## Data Metrics and Statistics
- Total quadrats: 1,624 across 54 sites.
- Plant species observations: 165 species; average 10.3 species per quadrat.
- Site-level aggregation: 2,934 plant:site combinations; mean ~54.3 species per site.
- Data granularity enables analyses of species composition, vegetation structure, and spatial patterns alongside UKBMS transects.

## Data Quality, Provenance, and Metadata
- Data collected in a structured, repeatable transect framework aligned with UKBMS protocols.
- Precise geolocation data provided (GRIDREF, LATITUDE, LONGITUDE) for each quadrat.
- Date stamps for quadrat sampling to enable temporal analyses within the 2008–2009 window.
- Metadata includes measurement definitions (e.g., %Cover, how flower counts and inflorescence status are recorded) and data relationships between Vegetation.csv and Quadrats.csv.

## References
- Carey, P. D., et al. (2008). Countryside Survey: UK Headline messages from 2007.
- Shimwell, D. W. (1972). The description and classification of vegetation.