# Bird and Butterfly abundance data from consistently surveyed agri-environmental monitoring transects at Hillesden, UK (2006-2017)

## Purpose and scope
- Provides bird and butterfly abundance data from field-surveyed transects at Hillesden, UK, spanning 2006–2017.
- Enables analysis of ten-year interannual population trends across two five-year AES phases and comparison with national schemes (BBS for birds, WCBMS for butterflies).
- Focuses on transects recorded consistently (nine for birds, seven for butterflies) and on species present on the majority of selected transects.
- Data represent a subset of the Hillesden biological survey, with maximum annual counts per transect across monthly visits in the April–August window (birds) and May–August window (butterflies).

## Data content
- Files:
  - Hillesden_Bird_Abundance_2006-2016.csv
  - Hillesden_Butterfly_Abundance_2007-2017.csv
- Columns: Species, SiteCode, Year, MaxCount
  - Birds: Species is a BTO five-letter code; Butterflies: vernacular names
- Time coverage and transects:
  - Birds: 2006–2010 and 2012–2016; nine transects used for analyses
  - Butterflies: 2007–2010 and 2014–2017; seven transects used for analyses
- Measurements: maximum annual counts per transect per year
- Coverage: data filtered to species present on the majority (>50%) of selected transects

## Experimental design
- Hillesden Estate in southern lowland England; baseline AES experiment started in 2006 to assess biodiversity responses to environmental stewardship.
- Two five-year phases: 2006–2010 and 2012–2017 (AES management varied to reflect policy changes).
- AES interventions included 1–5% land area converted to habitats (grass margins, perennial wildflowers, nectar/pollen sources, and wild bird seed mixtures).
- AES options chosen to reflect typical lowland England farming systems; high-quality AES habitat delivery guided by expert advice.

## Data collection methods
- Birds:
  - Monthly breeding-season surveys on ~1 km transects along field boundaries.
  - Surveys within ~4 hours after sunrise; three transects per surveyor per day; transect order rotated monthly.
  - All birds detected in/near AES habitats mapped on ~1:2000 scale; standard methods used; not conducted in heavy rain or winds > Beaufort 4.
- Butterflies:
  - Surveys on series of 2 × 50 m transects within AES habitats plus two-minute timed observations of 2 × 2 m quadrats at transect ends.
  - Monthly surveys May–August; 10:00–16:00 GMT; minimum temperatures 13°C (sunny) or 17°C (cloudy) with wind < Beaufort 4 and no precipitation.

## Data processing and quality control
- Transects filtered to those surveyed consistently across all years; excluded transects without AES or with changes in AES uptake.
- Species selection based on presence on >50% of selected transects.
- Birds: adults recorded within 10 m of transects; birds seen only in flight excluded.
- Data digitised and cross-checked; locations mapped using transect IDs (butterflies) or Ordnance Survey maps (birds).

## Data structure and units
- Recorded values: maximum annual counts of birds/butterflies per species per transect per year.
- Columns:
  - Species: vernacular (butterflies) or BTO 5-letter codes (birds)
  - SiteCode: transect identifier
  - Year: study year
  - MaxCount: maximum count per transect per year

## Provenance and references
- Project led by UK Centre for Ecology and Hydrology; Defra funded; analytical work funded by NERC under ASSIST (NE/N018125/1).
- Key references for methods and context:
  - Bibby et al. 1992; Hinsley et al. 2010; Heard et al. 2012; Redhead et al. 2018.

## Potential uses and considerations
- Analyze long-term, interannual trends in bird and butterfly abundance.
- Compare Hillesden trends with national schemes (BBS for birds, WCBMS for butterflies) for benchmarking.
- Enable data-driven, self-service exploration and support AES impact assessments.
- Limitations: dataset covers a subset of the Hillesden survey (consistent transects and species only); not a full biodiversity census; monthly windows restrict temporal scope.