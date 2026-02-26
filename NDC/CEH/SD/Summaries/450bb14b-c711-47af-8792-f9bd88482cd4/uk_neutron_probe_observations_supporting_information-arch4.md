# Collated neutron probe measurements and derived soil moisture data, UK, 1966-2013: Supporting Information

- Overview
  - UK Soil Moisture Databank (UKSMD) collects neutron probe soil moisture observations for 428 locations across 45 study areas in England, Wales, and Scotland from 1966 to 2013 (1–20 years per site).
  - Data types include neutron probe readings (R), volumetric soil moisture (θ, m3 water/m3 soil), depth-integrated profile moisture content (PMC), plus metadata and associated publications.
  - Locations are linked to British National Grid references and latitude/longitude to support discoverability and integration with other datasets.

- Dataset structure
  - Four CSV files:
    - Volumetric_soil_moisture_UKSMD.csv: Time-series of NP count rate R and volumetric soil moisture θ at various depths.
    - Profile_moisture_content_UKSMD.csv: Time-series of depth-integrated PMC in two formats (PMC1: m water per soil depth; PMC2: m3 water per m3 soil).
    - Tube_metadata_UKSMD.csv: Tube identifiers, locations, dates, depths, vegetation, land-use, soil type, geology, coordinates, and start/end dates.
    - Site_publications_UKSMD.csv: Published references, DOIs/URLs, and comments per site.
  - Data in SI units; CSV format to ease import into spreadsheet, R, Python, etc.
  - Metadata include area IDs, site IDs, tube depths, vegetation categories, and calibration details.

- Data production methods
  - Data recovered from long-deteriorated magnetic tapes and dispersed spreadsheets/databases dating from 1966–2013.
  - Older SMDB data (1960s–1980s) recovered from Univac tapes; additional data recovered from LOCAR-related datasets and other sources (1970s–2013).
  - All data quality controlled and converted to standard SI units; aimed to create a consistent, open dataset spanning 1966–2013.
  - Final dataset covers 441 tube locations in 45 study areas; 428 locations with soil moisture observations; some older values were recalculated when needed.

- Data representations and processing
  - Neutron probe readings (3.2.1): NP measurements obtained by lowering probes into access tubes; readings apply to surrounding soil within a sphere around the probe.
  - Volumetric soil moisture (3.2.2): θ derived from R using a calibration equation; Rw is the water-count reference; site-specific calibrations or Wallingford calibration used when site calibrations are unavailable. Shallow-depth readings (<15–20 cm) are often excluded due to neutron loss.
  - Depth-integrated PMC (3.2.3): PMC is derived by integrating θ over depth using layer factors; PMC values provided from surface to specified depths or to maximum measurement depth. When PMC values are missing, PMC down to the maximum depth may be reconstructed using the described approach.
  - Availability notes: approximately 73% of θ and 78% of R/Rw values recovered; some sites have only depth-integrated PMC.

- Dataset contents and coverage
  - Data types available: raw NP readings (R) and water counts (Rw), θ values at multiple depths, and PMC values to various depths.
  - Geographic distribution shown in a map; no observations for Northern Ireland.
  - Notable datasets include multi-year records in the Tern catchment and long-running sites such as Hodnet Heath and Lincolnshire.

- Quality control, uncertainties, and flags
  - Data quality: missing data marked as -1; recalculated values labeled with a 'c' in the COMMENT column when necessary.
  - θ quality: θ values normally 0–1; some areas show θ > 1 (likely peat-rich, high rainfall regions); QUALITY1 flags such values as suspect.
  - Time-series reliability: NP-derived soil moisture is reliable for detecting changes; absolute θ values can be uncertain due to calibration variability and soil properties.
  - Quality flags:
    - q1: values >1.0 or otherwise suspect absolute θ/PMC values.
    - q2: unrealistic jumps in PMC time series; retained if they agree with original observer data and study context.
  - Calibration uncertainty: choice of calibration equation can cause notable differences in θ (potentially >20% in wet soils); where θ is not available, authors may calculate θ using generic equations with higher uncertainty (labeled with 'c').

- How to use the data
  - Acknowledge original studies; references and URLs are provided in Site_publications_UKSMD.csv.
  - Choose data form based on need:
    - For depth-specific analyses: Volumetric_soil_moisture_UKSMD.csv (R, Rw, θ across depths).
    - For cross-site comparisons: PMC data (PMC1, PMC2) from surface to depth, suitable for aggregated moisture content.
  - Consider data quality flags (q1, q2) and compare analyses with and without suspect values to assess sensitivity.
  - Potential applications:
    - Hydrological, agricultural, and land-surface model validation or data assimilation.
    - Cross-dataset comparisons with ISMN, COSMOS-UK, and Global Soil Moisture Databank for regional or national studies.
    - Historical drought analysis and soil moisture variability (spanning 1966–2013, including the 1976 drought).
    - Studies on soil moisture drivers, vegetation effects, and impact on processes like greenhouse gas emissions.
  - Limitations:
    - NP-derived θ values are more robust for detecting change than for precise absolute moisture content; calibration and soil properties add uncertainty.
    - Topsoil (first 10 cm) measurements can be unreliable for satellite-based comparisons; caution when integrating with EO products.

- Acknowledgements and references
  - Data recovery and analysis supported by NERC-CEH Water Programme and FP7 MELODIES; dataset preparation supported by NERC ASSIST program.
  - Authors acknowledge contributions from several colleagues and related studies referenced within the dataset, including CALIBRATION, LOCAR, and other foundational hydrology research.

- Practical notes for data leaders
  - Emphasize provenance: multiple recovery sources, calibration methods, and documented uncertainties to inform data governance and reuse.
  - Ensure metadata richness: tube metadata, area/site IDs, coordinates, vegetation, soil type, start/end dates, and publications to enable discoverability and cross-domain reuse.
  - Plan for data integration: design with interoperability in mind (SI units, common depth conventions, and cross-referencing with ISMN/COSMOS-UK).
  - Establish data stewardship practices: flag management, versioning, and guidance on handling suspect data (q1/q2) to support robust analyses and reproducibility.