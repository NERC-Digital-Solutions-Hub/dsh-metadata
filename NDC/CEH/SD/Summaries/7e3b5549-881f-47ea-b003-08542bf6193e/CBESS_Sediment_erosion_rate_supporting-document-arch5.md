# Coastal Biodiversity Ecosystem Service Sustainability (CBESS) the erosion rate of sediment cores from salt marsh sites at Morecambe Bay and Essex

- Purpose and scope: Dataset measuring erosion rate of sediment cores from salt marsh sites in Morecambe Bay and Essex, UK, using flume tank flow to quantify % mass loss per hour under three flow conditions.
- Staff responsible: Hilary Ford.
- Study context: Part of CBESS exploring coastal biodiversity and ecosystem service sustainability; site selection includes contrasting soil types (clay in Essex vs. sandy in Morecambe Bay) and differing grazing regimes and inundation characteristics.

## Dataset content and variables

- Core description: One large sediment core (16 cm diameter, 30 cm height) per 1 m x 1 m quadrat, with above-ground vegetation recorded.
- Measurements: Erosion rate calculated from mass loss over 30 minutes at three flow regimes (low, medium, high), with measurements taken at 0, 5, 10, 15, and 30 minutes.
- Variables/parameters observed:
  - 1 and 2 entries describe the same core sampling and erosion measurement procedure for each quadrat.
  - Calibration: stagnation pressures for low (61 Pa), medium (146 Pa), and high (351 Pa) flow.
  - Data treatment: None specified for statistical processing; data quality checks not explicitly defined.
  - File formats: Excel workbook.
- Data notes:
  - Mass loss per hour greater than 100% considered valid after conversion; some low-flow measurements may yield negative values due to initial water saturation.
  - High-flow results can destroy cores; medium-flow results are typically more reliable and recommended for overall erosion-rate modeling.
- Data fields (dataset structure):
  - Season (Winter/W) and (Summer/S)
  - Location (Essex E or Morecambe M)
  - Site (Essex: Abbotts Hall AH, Fingringhoe Wick FW, Tillingham TM; Morecambe: Cartmel Sands CS, Warton Sands WS, West Plain WP)
  - Habitat (Mudflat MF or Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A-D; ranges 1 m to upper limit)
  - L_%massloss (low velocity, % mass loss per hour)
  - M_%massloss (medium velocity, % mass loss per hour)
  - H_%massloss (high velocity, % mass loss per hour)

## Locations and sampling

- Essex observations: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM); coordinates provided for each site.
- Morecambe Bay observations: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP); coordinates and descriptions of grazing regimes (hare/geese grazing in Essex; sheep grazing in Morecambe Bay with variable intensity).

- Sampling window: Winter and Summer 2013, with Essex winter samples collected in an extended window (2–6 March 2013).

## Data quality, governance, and documentation

- Metadata and provenance: Includes site descriptions, habitat context, and grazing regimes to aid interpretation of erosion results.
- Data quality considerations:
  - Medium-flow measurements are more reliable for modeling erosion rates.
  - Negative low-flow values may occur due to initial saturation; high-flow experiments can destroy cores.
  - No explicit quality-control procedures documented; calibration details provided, but broader QA steps are not specified.
- Documentation gaps to address for stewardship:
  - Define and document QA/QC procedures clearly (data checks, outlier handling, replication).
  - Include a formal data dictionary and a metadata standard (units, coordinate reference system, timestamp formats).
  - Add data lineage: how raw measurements map to L/M/H values and final erosion rate calculations.
  - Provide licensing, access conditions, and versioning for repository storage.

## Format, structure, and readiness for discovery

- Primary format: Excel workbook.
- Structure notes: Data fields defined, with explicit columns for seasonal, spatial, and measurement metadata, plus per-flow erosion values (L, M, H).
- Enhancements recommended for discoverability:
  - Provide a machine-readable metadata file (e.g., JSON or CSV) describing fields, units, and data types.
  - Include a clear data dictionary with definitions for L_%massloss, M_%massloss, H_%massloss and the normalization to mass loss per hour.
  - Add coordinate reference system (e.g., WGS84) and precise geospatial coordinates for all sites.
  - Include data license and citation information.

## Challenges and considerations for data stewards

- Incomplete user need picture: Ensure metadata communicates intended downstream uses (erosion-rate modeling, habitat assessment, coastal management).
- Timely data transfer: The dataset spans multiple sites and campaigns; establish a standardized delivery schedule and persistent identifiers for quadrats and cores.
- Interoperability: Different sites use similar yet potentially non-interoperable formats; harmonize field naming (e.g., consistent Quadrant/Quadrat IDs, Site codes) and units.
- Handling large datasets: Cores across multiple quadrats and flows can generate substantial measurements; ensure scalable storage and indexing.
- Documentation of procedures: Duplicate or unclear entries (e.g., repeated “1”/“2” rows) should be cleaned and clearly documented to avoid confusion.

## Recommendations for Data Stewards

- Formalize metadata:
  - Create a complete data dictionary with definitions, units, and allowed values for all fields.
  - Specify coordinate systems and provide precise site coordinates with uncertainty.
  - Document sampling dates, times, and any field conditions affecting measurements.
- QA/QC enhancements:
  - Establish and publish QA procedures, including checks for measurement consistency, calibration validation, and outlier handling.
  - Record data checks and any corrections or exclusions with justification.
- Data lineage and reproducibility:
  - Provide a clear mapping from raw measurements (mass loss over time) to derived metrics (mass loss per hour) for each flow condition.
  - Include formulas or scripts used for converting to %mass loss and for selecting preferred flow (medium) in modeling.
- Access and governance:
  - Attach a data license, usage terms, and citation requirements.
  - Implement versioning and change logs; assign persistent identifiers to datasets, sites, and quadrats.
- Usability improvements:
  - Offer a machine-readable delivery format (CSV/JSON) alongside the Excel workbook.
  - Add a README with a high-level summary, data lineage, and example analyses to guide new users.

- Overall takeaway for Data Stewards: This CBESS dataset provides a structured measurement of sediment-core erosion under controlled flow regimes across multiple salt-marsh sites, with rich contextual metadata. To maximize discoverability, reuse, and governance, augment the dataset with comprehensive metadata, QA procedures, standardized field naming, and machine-readable documentation while preserving the underlying experimental context and provenance.