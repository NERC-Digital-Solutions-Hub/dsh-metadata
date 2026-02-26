# River Habitat Survey - spot-check data

- Welsh Glastir Monitoring & Evaluation Programme (GMEP) collects freshwater and river habitat data to monitor environment, biodiversity, and water quality outcomes, and to assess drivers of change such as land use, climate, and pollution.
- The dataset covers 2013–2016 within a 1 km squared sampling framework, employing a rolling 4-year survey cycle to maximize spatial coverage while tracking year-on-year changes.
- Two sampling components:
  - Wider Wales Component: baseline estimation and national trends.
  - Targeted Component: linked to Glastir priority areas.
- Sampling frame and site selection:
  - 300 1 km squares sampled over the cycle.
  - Squares split evenly between random Wider Wales strata (based on the Land Classification of GB) and Glastir-priority targeted squares.
  - Exclusions: squares with more than 75% urban land or more than 90% sea.
- Integration and comparability:
  - Common 1 km square unit adopted across components to enable data integration.
  - Sample design aligned with the Countryside Survey of Great Britain to facilitate future integration.
- Data collected and data products:
  - Multi-metric, ecosystem-based data captured in a single snapshot visit where possible.
  - Outputs include data tables and products to enable end users to self-serve (e.g., dashboards, pivot tables) and to support interpretation and decision-making.
  - Data underpin national reporting for Glastir and analysis of environmental drivers and outcomes.

## Survey design and sampling framework

- 4-year rolling cycle (2013–2016) to maximize site visits while capturing temporal and spatial variation cost-effectively.
- Two components:
  - Wider Wales: baseline estimation and national trends.
  - Targeted: links to Glastir priority areas.
- Sampling unit: 1 km squares; 300 squares in total over the cycle.
- Stratified random sampling within Land Classification strata to minimize environmental heterogeneity within strata and maximize differences between strata.
- Exclusion criteria: urban land >75% or sea >90% (based on LCM2007 and census data).
- Spatial layout and confidentiality: distribution shown at 10 km resolution; sampling ensures robust national/sub-national indicators.

## Field data collection and sample analysis

- Field methods are documented in the Field Handbook (O’Hare et al., 2013) and implemented consistently across sites.
- Diatoms (GMEP_STREAM_DIATOMS_2013_16.csv):
  - Up to 300 valves counted per slide; diatoms identified to species level with standard references.
  - Sample processing: peroxide digestion, mounting, microscopy; diatom counts presented as percentages of the total sample.
- Invertebrates (GMEP_STREAM_INVERTS_2013_16.csv):
  - Sorting and identification performed by specialists; taxa identified to species where possible; abundance recorded as counts; quality control through re-analysis of a random sample.
  - Lab analysis by APEM Ltd; QA procedures included.
- Water chemistry (GMEP_STREAM_WATER_CHEMISTRY_2013_16.csv):
  - Contains analyses for conductivity, pH, phosphate, total dissolved nitrogen (TDN), and alkalinity.
  - Analyses conducted by UKCEH laboratories; methods include colorimetry, chemiluminescence, and standardized titration.
  - Results include instrument details and detection notes (e.g., <LOD).
- Site and habitat data (GMEP_STREAM_SITE_INFO_INVERTS_2013_16.csv and GMEP_STREAM_RHS_MAIN_2013_16.csv):
  - River Habitat Survey (RHS) components A–M–N–O–P–Q captured for headwater streams; includes field survey details, habitat types, and structural features (riffles, pools, banks, weirs, embankments, vegetation, etc.).
  - RHS_BANK_2013_16.csv covers sections H and I (sweep-up) with banks, substrate, banktop and bankface features, vegetation, land-use within banks, and related channel attributes.
  - Numerous RHS fields document channel morphology, substrate composition, vegetation, obstructions, structure counts (bridges, culverts, fords, weirs, etc.), and hydromorphological indicators.
- Macrophytes (GMEP_STREAM_MACROPHYTES_MTR_2013.csv):
  - Macrophyte species and cover recorded for streams (Mean Trophic Rank system used in 2013); species codes, plant names, cover percentages, and year.
- Spot checks (GMEP_STREAM_RHS_SPOTCHECK_2013_16.csv):
  - RHS spot-check data (sections E, F, G) including nuisance plants, bank/face vegetation, and major/minor impacts; supports field verification and targeted habitat assessment.
- Additional RHS data coverage (GMEP_STREAM_RHS_BANK_2013_16.csv):
  - Detailed bank and channel features including substrates, banktop/bankface structures, land use within 5 m of banks, channel vegetation, and various RHS modification and habitat descriptors.
- Data coding and quality notes:
  - -9 denotes no data; -9999 or -9 indicates missing data in several tables.
  - Data tables are structured with consistent identifiers (e.g., SQ_ID) and geospatial references (EASTING_10km, NORTHING_10km).

## Data quality, assurance, and standards

- DEFRA Joint Codes of Practice (JCoPR) followed to ensure robust science quality, reproducibility, and auditable procedures.
- UKAS accreditation for UKCEH laboratories (Lancaster).
- Quality control:
  - Invertebrate samples: re-analysis of one randomly selected sample per twenty by a different analyst.
  - Diatom counts and phytobenthos data undergo standardized taxonomic references and quality checks as part of the GMEP protocol.

## Data structure and accessibility

- Data are provided in multiple CSV tables, each corresponding to a data type or RHS component:
  - Diatoms (GMEP_STREAM_DIATOMS_2013_16.csv)
  - Invertebrates (GMEP_STREAM_INVERTS_2013_16.csv)
  - Site information (GMEP_STREAM_SITE_INFO_INVERTS_2013_16.csv)
  - Water chemistry (GMEP_STREAM_WATER_CHEMISTRY_2013_16.csv)
  - RHS main (GMEP_STREAM_RHS_MAIN_2013_16.csv)
  - RHS spot-check (GMEP_STREAM_RHS_SPOTCHECK_2013_16.csv)
  - RHS bank (GMEP_STREAM_RHS_BANK_2013_16.csv)
  - Macrophytes (GMEP_STREAM_MACROPHYTES_MTR_2013.csv)
- Typical identifier and coordinate fields include SQ_ID, EASTING_10km, NORTHING_10km, LC (land classification), and YEAR (2013–2016).
- Data are designed for integration with national surveys (e.g., Countryside Survey GB) and for generation of indicators at national and sub-national levels.

## Purpose, usage, and outputs

- Primary purpose: monitor the Glastir scheme and assess environmental outcomes related to climate, biodiversity, soil, woodland expansion, and water quality, while quantifying status and trends in the Welsh environment.
- Outputs enable:
  - Baseline estimation, national trends, and targeted Glastir reporting.
  - Multi-taxa ecological assessments (diatoms, invertebrates, macrophytes) and hydromorphology indicators.
  - Self-serve data exploration via dashboards, pivot tables, and reports.
- Outputs support evidence-based policy, data sharing, and iterative product development (e.g., early prototypes and user feedback) and advocate for improved data creation where needed.

## References and context

- Bunce et al. (2007) ITE Land Classification of Great Britain.
- Field methods and field handbook: O’Hare et al. (2013) Glastir Monitoring & Evaluation Programme Field Handbook – Freshwater.
- Environment Agency River Habitat Survey guidance and related documentation (1999, 2003).
- Emmett et al. (2014–2017) Glastir Monitoring & Evaluation Programme: first-year annual report and subsequent updates.
- Supporting taxonomic references for diatoms and aquatic plants, and standard ecological literatures cited in the data descriptions.