# Bird and Butterfly abundance data from consistently surveyed agri-environmental monitoring transects at Hillesden, UK (2006-2017)

## Overview
- Dataset of bird and butterfly abundance from field-surveyed transects at Hillesden, UK (2006-2017).
- Enables analysis of ten-year interannual population trends across two 5-year AES phases and comparison with equivalent national recording schemes (BBS for birds, WCBMS for butterflies).
- Focuses on transects recorded consistently (nine bird transects, seven butterfly transects) and on species present on the majority of transects.
- Data represent maximum annual counts per transect, across monthly visits within the scope of national schemes (April–August for birds; May–August for butterflies).

## Experimental design and AES context
- Hillesden Estate in southern lowland England used for a two-phase AES experiment (2006–2010; 2012–2017) to investigate effects on biodiversity.
- AES uptake: 1–5% of land converted to habitats delivering resources (grass margins, perennial wildflowers, nectar/pollen plants, and sown wild bird seed mixtures).
- AES management informed by expert agronomic and environmental advice; Hillesden chosen as representative of lowland England landscapes.

## Data collection and methods
- Birds:
  - Monthly breeding-season surveys on ~1 km transects along field boundaries.
  - Surveys within ~4 hours after sunrise; three transects surveyed per surveyor per day.
  - Record all birds detected in or near hedges and AES habitats on ~1:2000 maps; transects omitted in heavy rain or wind > Beaufort 4.
- Butterflies:
  - Monthly surveys May–August on 2 × 50 m transects within AES habitats, plus two 2-minute timed 2 × 2 m quadrats at ends of each transect.
  - Surveys 10:00–16:00 GMT; conditions: minimum 13°C in sunny conditions (or 17°C with more cloud), wind < Beaufort 4, no precipitation.
- Consistency filtering:
  - Only transects surveyed across all years in the respective phases (birds: 2006–2010 and 2012–2016; butterflies: 2007–2010 and 2014–2017).
  - Excluded transects without AES intervention or with changes in AES uptake.
  - Species chosen if present on >50% of selected transects.
  - Birds: counts limited to adults within 10 m of transects; individuals seen only in flight excluded.
- Data processing:
  - Raw counts converted to maximum counts per transect per year to assess interannual trends.

## Data structure and contents
- Data files:
  - Hillesden_Bird_Abundance_2006-2016.csv
  - Hillesden_Butterfly_Abundance_2007-2017.csv
- Columns (common to both files):
  - Species: vernacular name (butterflies) or BTO 5-letter code (birds)
  - SiteCode: transect identifier
  - Year: year of study
  - MaxCount: maximum annual count per transect
- Data provenance:
  - Collected by experienced surveyors; transect locations mapped; data digitised with error checking.
  - Key references documenting methods and AES context include Hinsley et al. 2010; Heard et al. 2012; Redhead et al. 2018; Bibby et al. 1992.

## Usage considerations and limitations
- Represents a subset of Hillesden’s broader biodiversity data, limited to consistently surveyed transects and species present on the majority of those transects.
- Enables cross-comparison with national schemes (BBS, WCBMS) but only for the consistently surveyed subset.
- Data are suitable for assessing interannual trends and AES effects within the two 5-year phases, with recognition of scale and AES uptake changes over time.

## Funding and references
- Project led by UK Centre for Ecology and Hydrology; Defra funded the Hillesden AES work.
- Analytical work funded by the Natural Environment Research Council (NERC) under ASSIST (NE/N018125/1).
- Foundational references include key methodological and AES impact studies (Hinsley et al. 2010; Heard et al. 2012; Redhead et al. 2018).