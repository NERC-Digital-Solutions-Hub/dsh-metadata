# River Habitat Survey - spot-check data

## Overview and Aim
- Welsh Government monitoring framework (Glastir Monitoring & Evaluation Programme, GMEP) to evaluate environmental outcomes and drivers of change (climate, land use, pollution) and quantify status/ trends.
- Four-year rolling survey designed to enable integration across multiple measures and scales (ecosystem-based approach).

## Data Scope, Architecture and Sampling Design
- Two components: Wider Wales (baseline estimation, national trends) and Targeted Component (Glastir priority areas); both integrated on a common 1 km square spatial unit.
- Sampling plan: 300 x 1 km squares over a four-year cycle; half randomly sampled within Land Classification strata (GB/Bunce et al., 2007), half targeted to Glastir priorities.
- Exclusion criteria: squares with >75% urban land or >90% sea excluded.
- Sampling unit and integration: alignment with Countryside Survey methodology to enable future GB-wide analyses; data designed for national and sub-national indicators.
- Field methods documented in Field Handbook (O’Hare et al., 2013).

## Data Collection and Analysis Methods
- Diatoms (GMEP_STREAM_DIATOMS_2013_16.csv): up to 300 valves per slide identified; diatom counts recorded as percentage of total sample; taxonomy aligned with standard references; analysis conducted by Bowburn Consultancy.
- Invertebrates: sorting and identification by accredited labs (APEM Ltd); QA through re-analysis of ~1 in 20 samples; abundance recorded as counts (free-living individuals; colonies counted as one).
- Water chemistry: analyses of phosphate (PO4-P), total dissolved nitrogen (TDN), alkalinity; conducted by UK Centre for Ecology & Hydrology labs using accredited methods; QA in line with DEFRA JCoPR; UKAS-accredited labs used.
- River Habitat Survey (RHS) components: main RHS data (GMEP_STREAM_RHS_MAIN_2013_16.csv) and RHS spot-check data (GMEP_STREAM_RHS_SPOTCHECK_2013_16.csv) covering sections E–G; detailed field attributes, habitat features, and spot-check annotations.
- Additional RHS datasets cover bank, substrate, vegetation, in-channel features, and various morpho-hydraulic descriptors (GMEP_STREAM_RHS_BANK_2013_16.csv).
- Data are organized with standardized identifiers (SQ_ID) and geographic coordinates (EASTING_NORTHING_10km), plus year and sampling metadata.

## Datasets and Data Model
- Diatoms: GMEP_STREAM_DIATOMS_2013_16.csv (1 km square, species, percent composition).
- DARES Diatoms: GMEP_STREAM_DARES_2013_16.csv (Diatoms for Assessing River Ecological Status).
- Invertebrates abundance: GMEP_STREAM_INVERTS_2013_16.csv.
- Invertebrate site info: GMEP_STREAM_SITE_INFO_INVERTS_2013_16.csv.
- Macrophytes: GMEP_STREAM_MACROPHYTES_MTR_2013.csv (Mean Trophic Rank approach; 2013 only).
- Water chemistry: GMEP_STREAM_WATER_CHEMISTRY_2013_16.csv.
- RHS main habitat data: GMEP_STREAM_RHS_MAIN_2013_16.csv.
- RHS spot-checks: GMEP_STREAM_RHS_SPOTCHECK_2013_16.csv.
- RHS bank and related fields: GMEP_STREAM_RHS_BANK_2013_16.csv.
- Spot-check narrative and nuisance species data: GMEP_STREAM_RHS_SPOTCHECK_2013_16.csv (notable plant species, etc.).
- All datasets are designed for integration across time (2013–2016) and space (1 km squares; 10 km coordinate references).

## Data Quality, Standards, and Assurance
- Field methods standardized in Field Handbook; data collected under formal protocols to ensure consistency across sites and years.
- Laboratory QA: UKCEH labs are UKAS-accredited; DEFRA Joint Codes of Practice followed to ensure scientific robustness, repeatability, and auditability.
- Data quality controls include systematic identification standards, QA sampling checks (e.g., re-analysis), and clear handling of non-detections and missing values (e.g., -9999 or -9 denoting no data).
- Documentation emphasizes robust metadata, including sampling date, location, land classification, and sampling method.

## Governance, Collaboration and Access
- Collaboration among Welsh Government, CEH, Bowburn Consultancy, and APEM Ltd; data management and QA led by UK CEH staff.
- The dataset compilation supports policy evaluation of Glastir AES schemes and broader environmental monitoring, with potential integration with GB Countryside Survey for national trend analyses.
- Data are described through comprehensive tables and field definitions, supporting discoverability and reuse.

## Implications for Data Leaders (Data Strategy Perspective)
- Demonstrates a multi-taxa, multi-m-scale data ecosystem designed for policy evaluation and landscape-scale analytics.
- Emphasizes a common spatial unit (1 km) to enable data fusion across disparate datasets and future integration with national surveys.
- Highlights end-to-end data governance: standardized field methods, QA regimes, accreditation, and detailed documentation to support trustworthy analytics.
- Provides a model for data discovery, metadata richness, and cross-domain linkage (biological indicators, chemistry, habitat metrics).

## Key Challenges and Considerations
- Coordinating integration across diverse data streams (diatoms, invertebrates, macrophytes, RHS, water chemistry) over multiple years.
- Maintaining consistency in taxonomy, measurement standards, and field protocols as methods evolve.
- Managing large, complex datasets with extensive metadata and ensuring discoverability for reuse in policy analytics.
- Data gaps and representativeness due to sampling design (stratified random and targeted squares) and exclusions.

## References and Further Reading
- Field Handbook: Glastir Monitoring & Evaluation Programme, Freshwater, 2013.
- Bunce et al. 2007: ITE Land Classification of Great Britain.
- DEFRA JCoPR and UKAS QA standards.
- O’Hare et al. 2013: Glastir GMEP Field Handbook Freshwater.
- Emmett et al. and CEH/UKCEH technical reports on GMEP.