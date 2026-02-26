# Benthic organic matter of Welsh upland rivers in response to organic matter addition

## Overview
- A BACI (before-after-control-impact) study comparing upstream reference and downstream experimental stream zones to assess how added leaf litter influences benthic organic matter (BOM).
- Data collected across multiple months in 2013, with detailed field and laboratory processing to quantify coarse (CPOM) and fine (FPOM) particulate organic matter.

## Experimental design and dataset scope
- Each stream includes an upstream reference zone and a downstream experimental zone, separated by 20–50 meters to ensure independence.
- Before period (T1): 61–65 days (Nov 2012–Jan 2013); after period (T2): 57–62 days (Jan–Mar 2013).
- In T2, the experimental zone received leaf litter additions, using 1-tonne bags of deciduous leaves (oak, birch, alder) proportionally to zone area, plus maintaining minimum wet weight in vegetable net bags; additional leaf litter (630 kg wet weight) added mid-February and early March after storm events.
- Data were collected from five reaches (across multiple streams) with six random BOM samples per reach, on five sampling occasions (Jan–May 2013).

## Data collection and structure
- Collection method: Surber net sampling (0.1 m2 area, 330 µm mesh, 10 cm depth); six random samples per reach per sampling occasion.
- On-site preservation: 70% IMS; lab processing included separation of macroinvertebrates, drying to constant weight, and ash-free conversion for inorganic content correction.
- Analytical outputs: BOM stocks weighted to nearest 0.01 g; units reported as grams for CPOM and FPOM.
- Data files: flatbed CSV format with 10 primary columns:
  - site_code: sampling site identifier
  - landuse: basin land-use
  - region: stream basin
  - time: Before/After manipulation
  - month: sampling month
  - reach: Experimental or Control site
  - replicate: replicate code
  - surber_area: area of the Surber sampler (m2)
  - cpom: coarse particulate organic matter (g)
  - fpom: fine particulate organic matter (g)

## Metadata and provenance
- Supporting site descriptions provided in DURESS_CU_site_description.csv, containing:
  - site_code, name, Eastings, Northings, Grid, Latitude, Longitude, Elevation
  - Survey, Catchment, and related contextual fields
- Field equipment and procedures (Surber net specs, preservation, lab processing) documented within the data products.

## Quality control and data governance
- Calibration steps: None reported.
- Quality control: No explicit QC procedures described beyond standard laboratory preparation and ash-free corrections.
- Data provenance: Clear linkage between BOM measurements (cpom/fpom) and site metadata, with explicit before/after and experimental/control design identifiers.
- Data format: CSV files suitable for interoperability, with standardized column definitions; paired with site description metadata to support data discovery and reuse.

## Data availability and considerations for reuse
- Data are organized for discoverability and reuse, including:
  - Time-based (Before/After) and treatment-based (Experimental/Control) design variables
  - Quantitative BOM metrics (CPOM, FPOM) across multiple months
  - Spatial metadata (site coordinates and catchment context)
- Potential considerations for data stewards and users:
  - Ensure consistent interpretation of time, month, and reach fields across datasets
  - Confirm unit consistency and handling of ash-free conversion factors for inorganic content
  - Assess need for additional quality assurance metadata or documentation to support broader reuse (e.g., raw vs. processed BOM values, sample handling notes)

## Practical notes for data stewards
- Align metadata with standard data governance practices (clear definitions for time periods, zones, and replication).
- Consider facilitating data discovery by indexing fields such as site_code, region, landuse, and reach in a data catalogue.
- If future updates or related datasets exist, maintain linkage to the site description file for coherent provenance trails.