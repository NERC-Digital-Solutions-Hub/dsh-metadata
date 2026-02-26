# UrineComposition.csv

## Overview
- Dataset of Welsh Mountain ewe urine chemical composition and associated metadata from a grant project (Uplands-N2O, NE/M015351/1).
- Contains detailed laboratory methods and per-sample measurements across seasons, sites, and individual sheep replicates.
- Aims to support analyses of urinary chemistry in livestock and related environmental nitrogen processes.

## Data content and structure
- Data headers define variables: Season, Site, Sheep, Date, Time, Vol, TOC, TN, pH, EC, Urea, Nitrate, Ammonium, AA, Allantoin, Creatinine, Uric, Hippuric, Benzoic, Ca, Na, K.
- Season: spring, summer, or autumn; Site: semi-improved or improved pasture; Sheep: replicate identifiers.
- Laboratory measurements cover a broad suite of urinary constituents (organic carbon, nitrogen forms, amino acids, several metabolites, and ions).

## Methods and data processing
- Sample handling: urine filtered on ice through Whatman No.1 (11 μm) to remove particulates; samples frozen at -20 °C before analysis.
- In-field measurements: pH and electrical conductivity (EC) using standard electrodes.
- Quantification techniques:
  - TOC and TN: Multi N/C 2100S analyzer.
  - Urea: enzymatic method (Orsenneau et al., 1992).
  - Nitrate: colorimetric (Mulvaney, 1996).
  - Ammonium: colorimetric (Miranda et al., 2001).
  - Free amino acids: fluorometric method (Jones et al., 2002).
  - Allantoin, creatinine, uric acid, hippuric acid, benzoic acid: HPLC (Varian Pro Star 310) with C18 column; detection at 218 nm; specific mobile phases described.
  - K+, Na+, Ca2+: flame photometry (Sherwood Model 410).
- Sample preparation details include dilution in mobile phase A as needed for analysis.

## Metadata and provenance
- Data authors: Marsden, Lush, Holmberg, Whelan, King, Wilson, Charteris, Cardenas, Jones, Chadwick.
- Project context: Uplands-N2O; grant NE/M015351/1.
- Reuse guidance: if data are reused, ensure full citation of the dataset.
- References for analytical methods provided (four cited sources).

## Data quality, limitations, and governance
- Comprehensive method documentation supports reproducibility and audit trails.
- Metadata captures season, site, replicate, and precise sampling details for traceability.
- Potential concerns for data leaders: ensuring consistent units and documenting any data transformations; data may require harmonization if integrated with other datasets.

## Reuse, citation, and dissemination
- Clear citation requirements for data reuse embedded in the dataset description.
- Rich methodological detail facilitates cross-study comparisons and meta-analyses of urinary biomarkers.

## Practical implications for data strategy (Data Leaders)
- Demonstrates the value of well-documented lab data with rich metadata for discoverability and reuse.
- Highlights the importance of including provenance, measurement methods, and units to enable reliable downstream analyses.
- Provides a model for combining biological metadata with comprehensive chemical measurements across multiple sites and seasons.
- Encourages data governance practices: explicit reuse citations, standardized headers, and accessible methodological references to support broader data ecosystems.