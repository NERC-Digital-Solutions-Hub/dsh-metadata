# Elemental concentrations (Ca, Cs, K, Mg, Sr) in a range of crops and associated soils from the UK and Spain

- Purpose and scope
  - A dataset documenting concentrations of Ca, Cs, K, Mg, Sr, NH4-N and NPOC across crops, soils, soil pore waters and irrigation waters.
  - Derived from two UK plant growth studies (spring/summer 2018 and 2019) at CEH Lancaster and a 2018 study in Spain (Universidad de Extremadura) with seed exchange between sites.
  - Crops studied include radish, lettuce, grass, chard, courgette, strawberry, and potato grown in diverse soil types with varying pH (4.5–7.9) and organic matter (LOI 3.1–23.7%).

- Data content and structure
  - Elements and variables
    - Ca, Cs, K, Mg, Sr measured by ICPMS or ICPOES; NH4-N and NPOC measured (NPOC by TOC analyzer).
    - Pore waters and irrigation waters analyzed; some measurements provided as mg/kg dry mass (soil/crop) and mg/L (pore water).
  - Sample types and sources
    - Crops: multiple tissues (e.g., leaves, roots, fruits) at maturity.
    - Soils: several named soil types (e.g., Top, Heath, Allotment, Clay loam, Loamy sand, Spanish).
    - Pore water: collected at end of 2018 growth study; irrigation water from lab greenhouse taps and laboratory sources.
  - Experimental design
    - Cross-site plant growth experiments with UK-Spain collaboration; seeds/material shared; Spain-grown crops include radish, strawberry, radish grown in UK soil, etc.
  - Data tables and metadata
    - Large set of data tables (e.g., CONFIDENCE_PlantGrowthStudy_...) detailing:
      - Plant growth study crop/soil combinations and sample counts
      - Soil sample lists and crop-soil associations
      - Pore water sample descriptions and counts
      - pH and LOI values by sample
      - Detailed crop-specific datasets (radish, strawberry, potato, courgette, grass, chard, lettuce)
      - Elemental concentrations by crop and soil (K, Ca, Mg, Sr, Cs) and extraction methods
      - Elemental data for soils and AR/BaCl-extracted fractions
      - Pore water elemental concentrations (Ca, Cs, K, Mg, Sr, NPOC, Ti as contamination marker)
  - Data dictionaries
    - Includes descriptive fields for samples, crops, soils, sample IDs, years harvested, and notes
    - Several tables specify internal identifiers, extraction-method specifics (AR, BaCl2), and detection notes (e.g., <Cs for below detection)

- Analytical methods and QA/QC
  - Sample preparation and digestion
    - Freeze-drying of crop samples; grinding to <2 mm
    - Aqua regia digestion (3:1 HNO3:HCl, 175°C, 12 min) for AR extracts
    - BaCl2 extraction for soil extracts
    - Pore water and irrigation water acidified and measured directly
  - Instrumentation
    - ICPMS (Cs, Sr) and ICPOES (Ca, K, Mg) with external calibration
    - Internal standards: Ga, In, Re
  - Quality assurance
    - Measures to minimize contamination (non-metallic containers; agate tools; ceramic blades)
    - LOQ/LOD determined from blanks; dilution factors accounted for to compute total method LODs
    - TOC analyzer used for NPOC; sample acidification and purging steps described
  - Data handling
    - Data recorded in Excel from lab notebooks/instrument reports
    - Approximately 20% of data validated by a second person

- Provenance and accessibility
  - Good Laboratory Practice observed throughout
  - Data stored and prepared for upload to appropriate data portals
  - Acknowledgement of funding: CONFIDENCE project, part of CONCERT EJP; EU Horizon 2020 (grant No 662287)

- Key notes and caveats
  - K recovery via AR extraction is partial (51–63% recoveries for soils); clays may not dissolve completely in AR extraction
  - Cs measurements below detection indicated with special notation in BaCl and AR-extracted datasets
  - Some rows identify “Unused” soils (no crops grown); some datasets include notes about sample descriptions and replicates
  - Pore water/NPOC datasets contain markers for sample size issues (NES: not enough sample)

- Relevance for environmental monitoring and analysis
  - Provides a standardized, cross-site dataset of elemental concentrations across crops, soils and waters
  - Facilitates monitoring of environmental health and policy performance related to elemental transfer in the human food chain
  - Designed to be combined with other relevant data to enhance data value and support data sharing via portals
  - Detailed metadata and extraction methods enable reproducibility and cross-study comparisons

- References and acknowledgments
  - References cited for methodologies (Allen 1989; Lofts et al. 2001)
  - Project and funding details for the CONFIDENCE CONCERT EJP and Horizon 2020 support
  - Acknowledgements to individuals assisting during UK experiments and data preparation