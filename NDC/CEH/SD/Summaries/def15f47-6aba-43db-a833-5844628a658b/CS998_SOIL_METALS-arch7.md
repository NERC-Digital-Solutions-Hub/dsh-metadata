# Soil metals data 1998 [Countryside Survey], Great Britain Version: 1: 02-6-2016

## Overview
- A dataset of soil metal concentrations from soil samples across up to 256 1km squares in Great Britain, surveyed in 1998/1999.
- Source: Countryside Survey, CEH; intended for map-based data products and GIS analyses.
- Includes both metal concentrations and geographic/land classification attributes to support spatial analysis.

## Data structure and content
- File: CS1998_SOIL_METALS.csv
- Columns of interest:
  - SQUARE: 1km square sampling site code (text)
  - PLOT: Plot identifier within each 1km square (text)
  - YEAR: Year of survey (numeric)
  - CD, CR, CU, NI, PB, ZN: Cadmium, Chromium, Copper, Nickel, Lead, Zinc concentrations (ppm)
  - LC07: ITE Land Classification 2007 (text)
  - LC07_NUM: Numeric code for LC07
  - COUNTRY: Country location (England ENG, Scotland SCO, Wales WAL)
  - COUNTY07: County or Council area
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Spatial context: data are tied to 1km grid cells with additional land classification and environmental descriptors.

## Spatial and GIS integration
- Resolution: 1km grid; suitable for joining to 1km square shapefiles and aggregating by area.
- Rich attribute set for mapping: land classification (LC07), environmental zones (EZ_DESC_07), and location identifiers (COUNTRY, COUNTY07).

## Laboratory methods and quality assurance
- Sample preparation: air-dried and sieved (<2 mm); coning and quartering; ball milling.
- Digestion: aqua regia; 3 g soil digested to 100 ml.
- Measurement: ICP-OES; some measurements below detection limit confirmed via ICP-MS at a secondary lab.
- Quality control: batches include certified reference materials, internal QC samples, blanks, and duplicates; traceability to CRM standards (NBS 1646, BCR 280).
- Data handling: analytical batches typically 20 samples plus 2 QC and 2 blanks; some samples re-measured if below detection.

## Usage notes and acknowledgments
- Acknowledgment required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; data rights apply.
- Data usage should include the provided attribution language in all outputs.

## Context and references
- Key references and related publications include:
  - MASQ: Monitoring and Assessing Soil Quality in Great Britain (2002)
  - ITE Merlewood Land Classification (1996, 1981) and 2007 update
  - Countryside Survey: UK Results from 2007 (2008)
- Countryside Survey project information and methodologies are available via the Countryside Survey website.

## Practical guidance for GIS analysts
- Data limitations: some elements may have measurements below detection limits; missing values may occur.
- Temporal context: data pertain to the 1998/1999 survey period; year field documents survey year.
- Potential analyses: map spatial distributions of Cd, Cr, Cu, Ni, Pb, Zn; overlay with LC07 land classes and environmental zones; analyze spatial patterns by country or county; integrate with other soil or environmental layers.

## Data provenance
- Source and methodology documented in Countryside Survey technical materials and related publications cited above.
- Data produced following CS2000 Field Survey Handbook and QA procedures described in the dataset notes.