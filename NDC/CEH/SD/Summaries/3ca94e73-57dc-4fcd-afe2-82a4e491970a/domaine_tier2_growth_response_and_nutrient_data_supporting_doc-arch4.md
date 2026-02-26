# DOMAINE_Tier2_growthresponse_nutrients.csv

- Purpose and scope
  - Dataset from river phytoplankton bioassays assessing growth responses to inorganic and organic nutrient additions, and comparing against in situ nutrient concentrations.
  - Includes calculated growth responses (natural log response ratios) for multiple nutrient treatments and corresponding background water chemistry data.

- Data content and key variables
  - Growth response variables (natural log response ratio) per treatment:
    - RP, RN, RNP, RON1, RON2, RON3, RON4, ROP1, ROP2, ROP3, ROP4
    - RONav (average growth response for all dissolved organic N compounds)
    - ROPav (average growth response for all dissolved organic P compounds)
    - Datasets use log response ratios to quantify growth relative to controls.
  - Water chemistry variables (mg N L-1 or mg P L-1, and ratios):
    - TON..mg.N.l.1., Ammonia..mg.N.l.1., DON..mg.N.l.1., TN..mg.N.l.1.
    - SRP..mg.P.l.1., DOP..mg.P.l.1., TP..mg.P.l.1., DOC..mg.C.l.1.
    - DIN.mg.N.L.1, DONTNratio (0-1), DOPTPratio (0-1)
  - Additional derived/applied metrics:
    - RONav and ROPav (average growth responses for organic N and P compounds)
  - Metadata per observation:
    - siteinfo (sampling site name)
    - rep (replicate number)
    - date (incubation start date, dd/mm/yyyy)

- Data structure and format
  - File format: CSV
  - File naming convention: DOMAINE_Tier2_growthresponse_nutrients.csv
  - Units and descriptions provided for each variable (e.g., TON..mg.N.l.1. = mg N L-1; RP, RN, etc. = natural log response ratio)
  - Includes 12 nutrient treatments (control, inorganic N, inorganic P, inorganic N+P, four organic N additions, four organic P additions) across triplicate setups

- Spatial coverage
  - Multiple sampling sites listed (e.g., Ashop, Black Burn, Brocky Burn, Coln, Cottage Hill, Deepford Brook, Dickler, Dove, East Dart, Enbourne, Frome, Goredale Beck, Lambourne, N. Teign, Newby Beck, Piddle, Pow Beck, Sherbourne, Tarn Beck, Taw, Tippets Brook, Upper Chew, Windrush, Yeo)
  - Locations provided with coordinates in OSGB 1936 (Northings, Eastings, and National Grid references)

- Temporal coverage
  - Collection period: 01 September 2017 to 31 October 2017
  - One sampling date per site

- Collection, processing, and methods
  - Raw samples collected at each site; transported to lab at 4°C within 48 hours
  - Acclimatisation and controlled incubation (20°C, 18 h light/6 h dark) for 14 days
  - Nutrient treatments applied at or near Redfield ratio
  - Growth quantified via chlorophyll a concentration (measured spectrophotometrically) after incubation
  - Growth response calculated as change relative to control using natural log response ratio
  - Water chemistry analyzed using Skalar autoanalyzer after persulfate digestion; DIN, SRP, DON, DOP determined by standard methods
  - DON and DOP derived by difference from total vs dissolved inorganic nutrients

- Quality control and data quality
  - Missing values indicated as NA
  - Method references provided for chemical analyses and growth calculations (Elser et al. 2007; Maberly et al. 2002; Mackay et al. 2020; Ritchie 2008; Talling 1974; Yates et al. 2019, 2022)

- Provenance and references
  - Methods align with Mackay et al. (unpublished) and established nutrient-growth protocols
  - Chlorophyll-based growth assessment following Ritchie (2008)
  - Supporting methodological references listed (Elser et al. 2007; Maberly et al. 2002; Mackay et al. 2020; Talling 1974; Yates et al. 2019, 2022)

- Implications for data management and reuse
  - Rich, multi-dimensional dataset integrating in situ chemistry with experimental growth responses across numerous sites
  - Well-defined variables and units support cross-site comparisons and meta-analyses
  - Spatial and temporal resolution suitable for regional nutrient limitation and phytoplankton growth studies
  - Emphasizes need for clear metadata, standard units, and accessible coordinate references to enable discoverability and reuse by other researchers and data platforms