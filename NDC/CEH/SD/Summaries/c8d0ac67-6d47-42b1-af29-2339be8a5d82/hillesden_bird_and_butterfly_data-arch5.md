# Bird and Butterfly abundance data from consistently surveyed agri-environmental monitoring transects at Hillesden, UK (2006-2017)

## Overview
- A dataset of bird and butterfly abundance from field-surveyed transects at Hillesden, England, spanning 2006–2017.
- Focuses on ten-year interannual trends across two 5-year AES phases and enables comparison with national schemes (Birds: BBS; Butterflies: WCBMS).
- Represents a subset of the Hillesden biological survey data: transects that were recorded consistently (nine bird transects, seven butterfly transects) and species present on the majority of these transects.
- Contains maximum annual counts per transect per year, derived from monthly visits (April–August for birds; May–August for butterflies) within the time frame compatible with national schemes.
- Data produced by UK Centre for Ecology and Hydrology (funded by Defra) with analytical work funded by NERC under ASSIST.

## Scope and Content
- Taxa: Birds and butterflies.
- Transects: Nine bird transects; seven butterfly transects (selected for consistency across AES phases 2006–2010 and 2012–2017 for birds; 2007–2010 and 2014–2017 for butterflies).
- Timeframe: Birds (2006–2010, 2012–2016); Butterflies (2007–2010, 2014–2017).
- Data columns: Species, SiteCode (transect), Year, MaxCount (maximum annual count per transect per year).
- Data files:
  - Hillesden_Bird_Abundance_2006-2016.csv
  - Hillesden_Butterfly_Abundance_2007-2017.csv

## Experimental Design and Data Collection
- Location: Hillesden Estate, southern lowland England.
- AES context: Two 5-year phases (2006–2010; 2012–2017) with 1–5% of land removed from production to create AES habitats (grass margins, perennial wildflowers, nectar-producing plants, wild bird seed mixtures).
- Bird surveys:
  - Monthly during breeding season (April–July).
  - ~1 km transects along field boundaries; three transects surveyed per surveyor per day; early morning surveys; avoidance of heavy rain or wind > Beaufort 4.
  - Recording included birds detected in/near AES habitats; data mapped on ~1:2000 scale.
- Butterfly surveys:
  - Monthly May–August; 2 × 50 m transects in AES habitats plus two 2-minute timed quadrats (2 × 2 m) at transect ends.
  - Survey window 10:00–16:00; conditions: minimum temperatures and wind < Beaufort 4; appropriate sunshine conditions.
- Data selection:
  - Included only transects consistently surveyed across both AES phases and with AES intervention.
  - Species selected if present on the majority (>50%) of selected transects.
  - Birds: adults within 10 m of transects; excludes those observed only in flight.
  - Data transformed from raw counts to maximum counts per transect per year to analyze interannual trends.

## Data Processing and Structure
- Data handling:
  - Field-identification and counts by experienced surveyors; transect IDs assigned for birds and mapped for butterflies; data digitised with quality checks during and after entry.
- Structure:
  - CSV format with columns:
    - Species: English vernacular name (butterflies) or BTO 5-letter bird code (birds).
    - SiteCode: transect identifier.
    - Year: year of observation.
    - MaxCount: maximum annual count across monthly visits.
- Provenance and references:
  - Core methodological references include Bird census techniques (Bibby et al., 1992) and Hillesden AES evaluation papers (Hinsley et al., 2010; Heard et al., 2012; Redhead et al., 2018).
  - Data collection led by UK CEH; Defra-funded AES project; analytical work funded by NERC under ASSIST (NE/N018125/1).

## Quality, Limitations, and Governance
- Quality:
  - Data collected by trained observers; locations mapped; subsequent digitisation allows error-checking.
- Limitations:
  - Subset of the full Hillesden survey; excludes transects not consistently surveyed or lacking continuous AES intervention data.
  - Maximum counts per transect/year capture peak annual abundance but may obscure within-year dynamics.
  - Comparability to national schemes is best within the specified consistent transect set and species.
- Governance considerations for reuse:
  - Documented provenance, survey protocols, and AES context support reproducibility and cross-study integration.
  - Metadata includes experimental design, sampling regime, and data processing steps; users should reference the included publications for methodological details.

## Usage and Citations
- Suitable for analyses of interannual trends and for cross-woc comparisons with BBS (birds) and WCBMS (butterflies) using the shared transect subset.
- Recommended citations include Redhead et al. (dataset context) and Hinsley et al. (AES methodologies), along with the primary dataset files:
  - Hillesden_Bird_Abundance_2006-2016.csv
  - Hillesden_Butterfly_Abundance_2007-2017.csv