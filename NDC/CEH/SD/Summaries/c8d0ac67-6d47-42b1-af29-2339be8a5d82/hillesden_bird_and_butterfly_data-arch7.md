# Bird and Butterfly abundance data from consistently surveyed agri-environmental monitoring transects at Hillesden, UK (2006-2017)

## Overview
- Dataset of bird and butterfly abundance from field-surveyed transects at Hillesden, UK, covering 2006-2017.
- Focuses on data suitable for analyzing ten-year interannual population trends across two AES (agri-environmental) habitat phases and comparing with national schemes (BBS for birds, WCBMS for butterflies).
- Represents a subset of the Hillesden biological survey, restricted to transects recorded consistently and species present on the majority of transects.

## Content and scope
- Bird data: 9 transects, monthly surveys (April–August) with maximum annual counts per transect per species per year.
- Butterfly data: 7 transects, monthly May–August surveys with maximum annual counts per transect per species per year.
- Only transects surveyed consistently across both experimental phases (2006–2010 and 2012–2016 for birds; 2007–2010 and 2014–2017 for butterflies) and species present on >50% of selected transects are included.
- Data transformation: raw counts converted to maximum counts per transect per year.
- Spatial framing: transects are field boundary-based; bird data mapped to Ordnance Survey maps (~1:2000) and butterfly transects mapped to unique transect IDs.

## Experimental design and data collection
- Location: Hillesden Estate, southern lowland England (51°57′ N, 1°00′ W).
- AES experiment periods: 2006–2010 and 2012–2017; 1–5% of land under AES per phase, with habitats such as grass margins, perennial wildflowers, pollen/nectar sources, and sown wild bird seed.
- Data collection methods:
  - Birds: monthly breeding-season surveys on ~1 km transects following field boundaries; surveys within ~4 hours after sunrise; three transects per surveyor per day; recordings mapped on ~1:2000 scale; no surveys during heavy rain or winds > Beaufort 4.
  - Butterflies: monthly surveys on 2 x 50 m transects within AES habitats plus 2-minute timed observations of 2 x 2 m quadrats at transect ends; surveys 10:00–16:00 in May–August under suitable temperature/conditions.
- Data filtering: excluded transects with no AES intervention or with AES uptake changes.

## Data structure and formats
- Source files:
  - Hillesden_Bird_Abundance_2006-2016.csv
  - Hillesden_Butterfly_Abundance_2007-2017.csv
- Columns:
  - Species: Bird data uses BTO five-letter codes; Butterflies use vernacular species names.
  - SiteCode: transect identifier.
  - Year: year of study.
  - MaxCount: maximum annual count across monthly visits.
- Data quality: collected by experienced surveyors; locations mapped; digitised with error checks during and after data entry.
- References for methods and context provided (e.g., Bibby et al. 1992; Hinsley et al. 2010; Redhead et al. 2018).

## Relevance to GIS applications
- Enables time-series and spatial analyses of biodiversity responses to AES at transect-level resolution.
- Suitable for comparing local Hillesden trends with national schemes (BBS for birds, WCBMS for butterflies).
- GIS-ready attributes include SiteCode, Year, and MaxCount per species per transect, facilitating join operations with spatial shapefiles of transects.

## Data provenance and acknowledgments
- Project led by UK Centre for Ecology and Hydrology (UKCEH); funded by Defra.
- Analytical work funded by the Natural Environment Research Council (NERC) under ASSIST (NE/N018125/1), jointly supported by NERC and BBSRC.
- Key references: Hinsley et al. 2010; Heard et al. 2012; Redhead et al. 2018.