# DOMAINE_Tier2_growthresponse_nutrients.csv

- Aim and scope
  - Data from bioassay experiments to investigate growth responses of river phytoplankton to inorganic and organic nutrient additions.
  - Compare growth responses to nutrient additions with in situ nutrient concentrations.
  - Purpose: assess water chemistry drivers of organic nutrient growth responses.
  - Includes calculated growth responses from incubations and background nutrient data collected concurrently with sampling.

- File format and naming
  - File format: .csv
  - File name: DOMAINE_Tier2_growthresponse_nutrients.csv
  - Metadata describes variables (Table 1) and spatial sites (Table 2).

- Content and structure
  - Growth response variables (natural log response ratio):
    - RP, RN, RNP: responses to inorganic phosphate/nitrate combinations and their nutrient mixes.
    - RON1–RON4: responses to organic N compounds (e.g., urea, glycine, glutamic acid, acetyl glucosamine).
    - ROP1–ROP4: responses to organic P compounds (e.g., glucose-6-phosphate, phytic acid, methylumbelliferyl-phosphate, methylphosphonate).
    - RONav and ROPav: average growth responses for all dissolved organic N and P compounds.
  - Water chemistry data (concentrations, units):
    - TON..mg.N.l.1., Ammonia..mg.N.l.1., DON..mg.N.l.1., TN..mg.N.l.1.
    - SRP..mg.P.l.1., DOP..mg.P.l.1., TP..mg.P.l.1., DIN.mg.N.L.1, DONTNratio, DOPTPratio.
    - TON, Ammonia, DON, TN, SRP, DOP, TP, DOC..mg.C.l.1., DIN, etc.
    - DONTNratio and DOPTPratio: ratios of dissolved organic nitrogen/phosphorus to total concentrations (0 to 1).
  - Units and descriptions for each variable are provided in Table 1 of the dataset documentation.
  - Spatial coverage (Table 2): multiple sampling sites with coordinates, NGR codes, and OSGB 1936 coordinate system.
  - Temporal coverage: 01 September 2017 to 31 October 2017, one sampling date per site.
  - Data structure notes: missing values denoted NA.

- Spatial and temporal coverage
  - Spatial: numerous river sites (examples include Ashop, Black Burn, Brocky Burn, Coln, Cottage Hill, Deepford Brook, etc.) with precise northings/eastings and National Grid References.
  - Coordinate reference system: OSGB 1936.
  - Temporal: single sampling date per site within 01 Sep 2017 – 31 Oct 2017.

- Collection, generation, and transformation methods
  - Bioassay design and incubation:
    - Raw river water collected, stored at 4 C, transported to lab within 48 hours.
    - Acclimated at 20 C; filtered to remove zooplankton/large detritus.
    - 12 nutrient treatments applied in triplicate around Redfield-like N:P ratio (N ~ 90 µmol L-1; P ~ 6 µmol L-1).
    - Treatments: control, inorganic N only, inorganic P only, inorganic N and P, plus four organic N additions and four organic P additions.
    - Incubation: 14 days at 20 C, 80–120 µmol m-2 s-1 PAR, 18h light/6h dark.
    - Growth response measured via chlorophyll a after incubation (acid extraction and spectrophotometry).
    - Growth response quantified as natural log response ratio relative to the relevant control.
  - Water chemistry data:
    - Inorganic nutrients measured with Skalar autoanalyzer after persulphate digestion (unfiltered samples) and pre-leached 0.45 µm filtered samples (for total vs dissolved fractions).
    - DIN, NH4/NH3, SRP for dissolved inorganic P/N; DON and DOP by difference (TDN - DIN, TDP - SRP).
  - References for methods include Mackay et al. (unpublished; bioassay framework), Maberly et al. (2002), Elser et al. (2007), Ritchie (2008), Talling (1974), Yates et al. (2019, 2022).

- Quality control and data quality
  - Missing values are denoted NA.
  - Methods and quality control are documented via citations to established procedures; provenance includes both experimental growth assays and water chemistry analyses.

- Metadata, provenance, and governance
  - Detailed variable descriptions (Table 1) and sampling site locations (Table 2) are provided to support discoverability and reuse.
  - Provenance anchored in published or pre-published methodological references (e.g., Mackay et al., Maberly et al., Elser et al., Ritchie, Talling, Yates et al.).
  - Enables traceability from bioassay outcomes to specific nutrients and corresponding water chemistry contexts.
  - Potential data governance considerations:
    - Interoperability: numerous variables with long names and sometimes unusual formatting (e.g., TON..mg.N.l.1.) that should be harmonized with common naming conventions when integrating with other datasets.
    - Unit consistency: ensure uniform units (mg N L-1, mg P L-1, mg C L-1) when merging with other datasets.
    - Temporal scope limited to 2017 and specific UK sites; consider versioning and update plans if expanded datasets become available.
    - Documentation completeness supports reuse but may require careful alignment with other DOMAINE Tier-2 datasets for cross-study comparisons.

- References
  - Elser et al. 2007; Maberly et al. 2002; Mackay et al. 2020; Ritchie 2008; Talling 1974; Yates et al. 2019, 2022.

- Practical implications for Data Stewards
  - The dataset presents a well-documented combination of experimental growth responses and matching nutrient/chemistry data, enhancing discoverability and reuse.
  - Ensure continued adherence to metadata standards, maintain the explicit data provenance, and consider adding a machine-readable data dictionary to harmonize with other datasets.
  - Where feasible, implement a data update workflow and versioning plan, and align variable naming with standard ontologies or controlled vocabularies to ease interoperability.