# Bird and Butterfly abundance data from consistently surveyed agri-environmental monitoring transects at Hillesden, UK (2006-2017)

- Overview
  - Long-term dataset of bird and butterfly abundance from field-surveyed transects at Hillesden, England, spanning 2006–2017.
  - Supports analysis of interannual trends across two five-year agri-environmental schemes (AES) phases and comparison with national schemes (BBS for birds, WCBMS for butterflies).
  - Focuses on transects recorded consistently and on species present on the majority of transects; represents a subset of the Hillesden biological survey data.

- Experimental design and scope
  - Two five-year AES phases: 2006–2010 and 2012–2017.
  - AES areas: 1–5% of land taken out of production and replaced with habitat resources (grass margins, wildflowers, nectar/pollen sources, and wild bird seed mixes).
  - Hillesden chosen as representative of lowland England landscape and farming systems.
  - Data intended to evaluate the effects of AES on biodiversity and agronomic indicators; collaboration between UKCEH, Defra, NERC, and ASSIST.

- Data collection methods
  - Birds
    - Monthly breeding-season surveys (April–July) on ~1 km transects along field boundaries.
    - Three transects surveyed per surveyor per day; sunrise timing; maps indicating detections; activity recorded.
    - Surveys not conducted in heavy rain or winds above Beaufort 4.
  - Butterflies
    - Monthly surveys (May–August) on 2 × 50 m transects within AES habitats plus two-minute timed quadrats.
    - Conducted 10:00–16:00 with temperature and weather controls (≥13–17°C, wind < Beaufort 4, minimal precipitation).

- Data processing, scope, and filtering
  - Consistency filtering: only transects surveyed across all years in each phase (birds: 2006–2010 and 2012–2016; butterflies: 2007–2010 and 2014–2017).
  - Excluded transects without AES or with AES uptake changes.
  - Resulting in nine bird transects and seven butterfly transects for analysis.
  - Species selection: present on >50% of selected transects across surveys.
  - Data transformation: raw counts converted to maximum counts per transect per year to assess interannual trends.

- Nature, units, and data structure
  - Recorded values: maximum annual counts per species per transect per year.
  - Birds: Species coded (BTO 5-letter codes); transect locations mapped to transect IDs.
  - Butterflies: Species named by vernacular names; transects mapped similarly.
  - Data structure in CSV files with columns: Species, SiteCode, Year, MaxCount.

- Data quality, governance, and provenance
  - Field identifications conducted by experienced surveyors; data digitized and error-checked.
  - Transect locations recorded with detailed mapping (Ordnance Survey 1:2000 scale for birds).
  - Metadata considerations discussed; datasets designed to support openness, data sharing, and governance from source.
  - Data produced under a project led by UKCEH and funded by Defra, with analytical work by NERC/ASSIST (NE/N018125/1).

- Data availability and references
  - CSV data files: Hillesden_Bird_Abundance_2006-2016.csv and Hillesden_Butterfly_Abundance_2007-2017.csv.
  - Key references covering methods and AES evaluations (Bird census techniques; Hillesden AES studies; related ecology and impact assessments).

- Relevance for monitoring frameworks
  - Demonstrates practical workflow for environmental health monitoring: from long-term experimental design to consistent data collection, rigorous filtering for comparability, and transformation to trend-friendly metrics.
  - Provides a robust basis for policy evaluation of AES effects on biodiversity and for benchmarking against national schemes.
  - Highlights governance considerations: data standardization, metadata quality, data sharing, and transparency of underlying data linked to policy-relevant outputs.