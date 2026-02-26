# Vegetation cover at 54 UK Butterfly Monitoring Scheme sites in southern England, 2008-9

## Overview
- Vegetation cover estimates from 54 sites in southern England, part of the UK Butterfly Monitoring Scheme (UKBMS).
- Surveys conducted in summer 2008 and 2009 (majority in August) to align with UKBMS transect structure.
- Each site mapped to UKBMS transects, divided into 1–15 sections (mean 7.5).
- Across all sites: 1,624 quadrats (54 sites × ~7.5 sections × 4 quadrats per section).
- For each quadrat, plant species cover is recorded, yielding 16,720 vegetation-cover estimates across 165 plant species.
- When aggregated to the site level: 2,934 plant:site combinations, with an average of 54.3 plant species per site.
- Data are provided in two CSV files: Vegetation.csv (16,720 species-cover estimates) and Quadrats.csv (per-quadrat metadata).
- Includes measurements of plant cover, floral production (flower heads and florets), and inflorescence status, as well as vegetation-structure categories and dung.

## Experimental design & data collection
- Fieldwork conducted using the UKBMS transect structure to determine quadrat counts and locations.
- Transects are sectioned to reflect landscape discontinuities; sites contain 1–15 sections.
- Four 1 m² quadrats placed in each section, totaling 1,624 quadrats.
- Quadrat locations determined by random points within a 10 m wide polygon centered on the transect route.
- For each quadrat, recorded:
  - Percentage cover (plant species) and, for flowering plants, counts of flower heads, florets, and how many heads are inflorescences.
  - Average plant species per quadrat: 10.3 (used to derive overall species totals).
- Vegetation structure recorded as percentages of bare ground, grass, herbaceous, and woody vegetation, plus dung.

## The dataset
- Vegetation.csv: 16,720 estimates with the following columns:
  - Taxon.name (Latin binomial)
  - Common.name (English common name)
  - Site.name (UKBMS transect route name; matches Quadrats.csv)
  - BMS.ID (transect route ID; matches Quadrats.csv)
  - Section (transect section number)
  - Date (sampling date)
  - QuadratNum (quadrant replicate within the section)
  - %Cover (percent cover of the plant)
  - FH (number of flower heads)
  - FI (number of florets)
  - Fl_I (flower heads that are inflorescences)
  - Fl (number of florets on inflorescences)
- Quadrats.csv: per-quadrat metadata for the 1,624 quadrats with columns:
  - Site.name, BMS.ID (matching Vegetation.csv)
  - GRIDREF (site centroid location in OS grid)
  - LATITUDE, LONGITUDE (GPS coordinates)
  - Date (sampling date)
  - Section, QuadratNum (section and quadrat identifiers)
  - Aspect (slope direction, 5° increments; 180 = south)
  - Slope (slope angle, 5° increments)
  - Unevenness.cm (vertical variation within quadrat)
  - Distance (cm from ground to base of crown)
  - Av.Turf.Height (average turf height)
  - %BareGround, %GrassLayer, %HerbLayer, %WoodyLayer, %Dung (percentage cover for each category)
- References for methods:
  - Carey et al. 2008 for countryside survey methodology
  - Shimwell 1972 for vegetation description and classification

## Data quality, provenance & metadata
- Collected by Robin Curtis as part of his PhD fieldwork; dates 2008–2009.
- Data aligned with UKBMS transects, enabling integration with existing datasets and temporal monitoring.
- Standardized measurement definitions provided (e.g., %Cover, plant counts, and vegetation-structure categories) to support comparability and reuse.
- Documentation includes explicit field methods, variable descriptions, and references to established vegetation methodology.

## Access, licensing & reuse
- Data are provided as two CSV files (Vegetation.csv and Quadrats.csv), with detailed field descriptions included in the document.
- Data are associated with UKBMS and can be accessed via the UK Butterfly Monitoring Scheme platform (ukbms.org) for integration with related datasets.
- Licensing details are not stated in the document; users should refer to UKBMS data-use policies for reuse terms.

## Implications for Data Stewards
- Highlights the importance of clearly defined, standardized metadata to enable data discovery, interoperability, and reuse across systems and formats.
- Demonstrates the need to document:
  - Sampling design (transects, sectioning, quadrat placement)
  - Measurement protocols (cover definitions, floral counts, structure categories)
  - Geographic context (grid references and coordinates)
  - Data provenance (collector, dates, linking keys like Site.name and BMS.ID)
- Emphasizes the value of providing both per-quadrat measurements and site-level aggregates to facilitate downstream analyses (e.g., community composition, habitat structure, and ecological associations with butterfly monitoring data).
- Suggests maintaining alignment with broader networks (UKBMS) to support data sharing, updates, and cross-study comparability.