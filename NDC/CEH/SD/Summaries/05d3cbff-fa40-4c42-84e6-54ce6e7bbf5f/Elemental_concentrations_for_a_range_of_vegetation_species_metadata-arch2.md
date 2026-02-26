# Elemental meta-data

- Purpose and scope
  - Defines metadata fields and elemental measurement data for environmental monitoring analyses, enabling consistent formatting to assess environmental health and policy performance over time.
  - Supports standardised data collection, verification, quality assurance, cleaning, transformation, and reporting (e.g., reports, maps, charts) with data stored/uploaded to appropriate portals.

- Sample context and identifiers
  - Laboratory_ID: CEH centralised chemistry laboratory unique sample identifier.
  - Sample_ID: CEH Radiochemistry laboratory unique sample identifier.
  - Collection_Site: Sampling site.
  - Sampling_date: Date of sampling (dd/mm/yyyy).
  - Species: Latin name of plant species (n/a for soil samples).
  - Common_name: Common name of species (n/a if not provided).
  - Taxonomy: Order, Family, Genus (n/a for soil samples).
  - Sample type: Indicates plant vs soil sample context.

- Data quality and representation
  - Data are verified, quality assured, cleaned, and transformed; datasets stored on appropriate portals.
  - Data may include n/a or not applicable for certain fields depending on sample type.
  - Below-detection flags: Columns with “<” (e.g., Be_<, Na_<, S_<, Cr_<, Se_<, etc.) indicate concentrations below the limit of detection (LOD).
  - Dual data points per element: Many elemental measurements have suffixes _1 and _2, representing two data points per sample (e.g., two measurement entries or two related metrics); some entries distinguish quantitative vs semi-quantitative or fresh weight contexts.
  - Units and measurement basis: Primarily mg/kg (per kg dry weight) for ICPMS and ICPOES measurements; some fields specify dry weight explicitly; a few mention fresh weight where relevant.
  - Data completeness: Some fields may be “n/a” or “not available” depending on measurement type or data availability.

- Elemental measurement details
  - Methods: ICPMS (inductively coupled plasma mass spectrometry) for quantitative/semi-quantitative data; ICPOES (inductively coupled plasma optical emission spectrometry) for quantitative data in some cases.
  - Concentration types: Quantitative (mg/kg dry weight) or semi-quantitative (mg/kg dry weight); some entries explicitly note fresh weight measurements.
  - Element coverage: Broad suite from Li, Be, Na, Mg, Al, Si, P, S, K, Ca, Ti, Cr, Mn, Fe, Co, Ni, Cu, Zn, Se, Rb, Sr, Y, Zr, Nb, Mo, Cd, Sn, Sb, Cs, Ba, La, Ce, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Tm, Yb, Lu, W, Hg, Tl, Pb, Th, U, and others; encompassing macro- and micronutrients as well as potential contaminants.
  - Special cases: Some elements have soil vs plant distinctions, and certain columns may be labeled as “not applicable” for specific sample types or measurement contexts.

- Practical implications for environmental analysts
  - Data integration: When merging datasets, account for the dual-field structure (_1 and _2) and interpret which measurement corresponds to which context (quantitative vs semi-quantitative, dry vs fresh weight).
  - Handling LOD: Treat "<" flagged values appropriately in analyses (decide on imputation or censoring strategy).
  - Contextual filtering: Soil samples may render plant-specific fields irrelevant; ensure consistent application of sample-type rules.
  - Reporting and visualization: Use the standardized metadata to generate consistent reports, maps, and charts across time for monitoring environmental health and policy performance.