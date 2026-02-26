# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment water content in saltmarsh and mudflat habitats

## Overview
- Datasets measure percentage water content in surface sediment (top 2 mm) from saltmarsh and mudflat habitats.
- Sampling during CBESS field campaign in winter and summer 2013; no planned repeats.
- Five replicates per quadrat; data collected across two UK regions (Essex and Morecambe Bay).

## Responsibility and Context
- Staff responsible: Jack Maunder.
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) with coordinates provided.
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP) with coordinates provided.
- Site descriptions emphasize contrasts in sediment types and soils:
  - Saltmarsh: two soil types (clay in Essex; sandy in Morecambe Bay) and differing inundation, creek structure, and vegetation.
  - Mudflat: Essex (cohesive clays, mud, silt) vs Morecambe Bay (coarse, mobile sediments).

## Sampling Design and Methods
- Grid and replication:
  - 22 quadrats sampled per mudflat and per saltmarsh site.
  - Random quadrat allocation using R to define four spatial scales (A–D).
- Seasonality:
  - Winter and Summer 2013 sampling; no planned repeat sampling.
- Measurement approach:
  - Wet/dry weights used to calculate percentage water content.
  - Sample handling: surface 2 mm of sediment collected with a contact corer, flash-frozen in liquid nitrogen, stored below -80°C, then freeze-dried.
- Data collection scope:
  - Variables recorded include average water content per quadrat and its standard deviation (StDev).
  - File format for data: CSV.

## Data Structure and Content
- Core variables:
  - Season (Winter or Summer)
  - Location (Morecambe or Essex)
  - Site (CS, WS, WP; AH, FW, TM)
  - Habitat (Mudflat or Saltmarsh)
  - Quadrat Number (1–22)
  - Scale (A–D; related spatial extent)
  - Percentage Water Content (average per quadrat)
  - StDev (standard deviation across quadrats within a Quadrat)
  - Other information (NA when data are missing due to inaccessibility)
- Data quality checks:
  - Readings from scales entered into spreadsheets as part of QA.
- Additional metadata:
  - Dataset field descriptions, headers, and row numbers are included to facilitate sorting and reuse.
- Data management and sharing:
  - Dataset prepared in a portable format (CSV) and intended for upload to relevant data portals/catalogues.

## Data Quality, Limitations, and Governance
- Quality control:
  - QA conducted via straightforward checks (e.g., spreadsheet entry of wet/dry weights, scale readings).
- Limitations:
  - Some quadrats are inaccessible, resulting in NA entries.
  - No repeat measurements planned beyond the winter/summer 2013 campaigns.
- Governance considerations for Data Stewards:
  - Ensure metadata completeness (fields like Season, Location, Site, Habitat, Quadrat Number, Scale, and Percentage Water Content).
  - Maintain consistency of site coordinates and habitat classifications across portals.
  - Monitor data availability constraints (access issues causing missing values) and document reasons.
  - Update stakeholders if sampling plans or accessibility change; otherwise maintain the published 2013 time frame.