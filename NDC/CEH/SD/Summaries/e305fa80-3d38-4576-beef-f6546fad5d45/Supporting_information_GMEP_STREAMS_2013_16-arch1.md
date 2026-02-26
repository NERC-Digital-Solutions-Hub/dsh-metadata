# Glastir Monitoring & Evaluation Programme

## Overview
- Wales-wide initiative to evaluate the environmental effects of agri-environment schemes (AES), including Glastir, since the early 1990s.
- GMEP aims to collect evidence on the effectiveness of bundles of management interventions for climate, biodiversity, soil, water quality, and woodland expansion; also to quantify status and trends in the environment in general.
- Data are designed for analysis of drivers of change (land use, climate, pollution) and for informing policy and delivery decisions.

## Survey design and sampling framework
- 4-year rolling survey cycle: 2013–2016 (first cycle).
- Two components: Wider Wales (baseline estimation and national reporting) and Targeted (linking to Glastir priority areas).
- Common spatial unit: 1 km² squares; 300 squares sampled over the cycle.
- Sampling strategy mirrors Countryside Survey of Great Britain to enable future data integration.
- Stratified random sampling within Land Classification strata; half of squares are Wider Wales, half targeted at Glastir priorities.
- Exclusions: squares with >75% urban land or >90% sea were excluded.

## Field data collection and laboratory analysis
- Data collected in up to 300 1 km² squares using standardized field methods (Field Handbook).
- Data types include diatoms, macroinvertebrates, macrophytes, and water chemistry, collected across multiple scales to enable ecosystem-level analysis.
- Laboratory analyses:
  - Diatoms: sample digestion with hydrogen peroxide; slides prepared and at least 300 valves counted; identified to highest resolution; Bowburn Consultancy conducted analyses.
  - Invertebrates: sorted, identified to species where possible; QA via re-analysis of a random sample (1 in 20).
  - Water chemistry: phosphate, total dissolved nitrogen, alkalinity measured by UK Centre for Ecology & Hydrology (UKCEH); QA per DEFRA Joint Codes of Practice; UKAS-accredited labs.
- Data are structured to support integration across metrics and scales.

## Datasets and key variables (examples)
- GMEP_STREAM_DIATOMS_2013_16.csv: diatom species counts per 1 km²; includes species names, counts (% of sample), coordinates (E/N 10 km), year.
- GMEP_STREAM_DARES_2013_16.csv: Diatoms for Assessing River Ecological Status; substratum, shading, habitat variables, etc.
- GMEP_STREAM_INVERTS_2013_16.csv: stream invertebrate abundance by species.
- GMEP_STREAM_SITE_INFO_INVERTS_2013_16.csv: headwater site information (RIVPACS); sampling date, method, habitat proportions, etc.
- GMEP_STREAM_MACROPHYTES_MTR_2013.csv: macrophyte species and mean trophic rank-based cover (recorded in 2013 only).
- GMEP_STREAM_WATER_CHEMISTRY_2013_16.csv: water chemistry data (phosphate, TDN, alkalinity) with site/year details.
- GMEP_STREAM_RHS_MAIN_2013_16.csv: River Habitat Survey (RHS) site details across multiple sections (A, B, C, L, etc.); extensive habitat metrics.
- GMEP_STREAM_RHS_SPOTCHECK_2013_16.csv: spot-check data for nuisance plants and RHS-related observations.
- GMEP_STREAM_RHS_BANK_2013_16.csv: RHS sections H and I (bank features) including substrates, vegetation, banktop/bankface structures, hydraulic features, and man-made structures.
- GMEP_STREAM_RHS_SPOTCHECK_2013_16.csv and related RHS tables provide additional habitat and biota context.
- Brief Description: River Habitat Survey spot-check data (Sections E, F, G).

## Data quality, standards and provenance
- Quality assurance follows DEFRA Joint Codes of Practice (JCoPR); aims for robust, repeatable, auditable research processes.
- UKCEH laboratories are UKAS-accredited.
- Field and lab procedures are documented (Field Handbook; O’Hare et al., 2013; related references for diatoms, invertebrates, and macrophytes).
- Data are linked to standardized coordinate systems (OSGB 1936; 10 km grid references) and use clearly defined data codes (-9 or -9999 for missing data).

## Temporal coverage and limitations
- Temporal window: 2013–2016 (4-year rolling cycle).
- Some components are only available for 2013 (e.g., macrophyte data under Mean Trophic Rank system); other components are collected across 2013–2016.
- Data are designed for integration with wider GB datasets (e.g., Countryside Survey) to support national-scale analyses.

## Access, provenance and metadata
- Data are accompanied by extensive metadata and methodological documentation (Field Handbook; lineage to Bowburn Consultancy, APEM Ltd, UKCEH).
- Datasets are described with explicit field definitions, data types, units, and data provenance.
- Data management practices emphasize traceability and the potential to upload datasets to portals with metadata for discoverability.

## Implications for analysts
- Enables investigation of how Glastir interventions and external drivers affect riverine biodiversity, habitat condition, and water chemistry.
- Facilitates multi-taxa, multi-menchmark analyses across spatial scales (1 km² grids) and temporal scales (2013–2016).
- Supports integration with Countryside Survey GB and other national datasets for broader trend analyses and predictive modelling.
- Variants and richness of datasets allow assessment of drivers of change, links to land use, and policy impact evaluation.

## Limitations and considerations for modelling
- Multi-source, multi-year data require careful harmonization of variables and units; some datasets have year-specific availability.
- Spatial resolution and sampling design (1 km², targeted vs. Wider Wales) influence representativeness and require appropriate weighting.
- Data gaps in certain taxa (e.g., 2013-only macrophyte data) limit temporal analyses for those variables.
- Data access depends on portal availability and metadata completeness; adherence to QA standards is essential for robust analyses.

## References and further reading
- Bunce et al. (2007) ITE Land Classification of Great Britain.
- Emmett et al. (2014, 2017) Glastir Monitoring & Evaluation Programme; Annual Reports.
- Field Handbook: O’Hare et al. (2013) Glastir Monitoring & Evaluation Programme FIELD HANDBOOK Freshwater.
- Environment Agency (1999, 2003) River Habitat Survey guidance and QA procedures.
- Diatom and macroinvertebrate taxonomy references (Krammer & Lange-Bertalot; Hartley et al.; Fourtanier & Kociolek; Whitton et al.).
- CEH and UKAS QA and accreditation materials.