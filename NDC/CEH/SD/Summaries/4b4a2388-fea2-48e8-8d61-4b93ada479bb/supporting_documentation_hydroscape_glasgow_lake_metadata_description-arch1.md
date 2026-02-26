# Project: Historical lake sediment metal concentrations from Greater Glasgow File Uploaded to EIDC: hydroscape_glasgow_core_metadata.csv

## Overview
- Metadata file uploaded to EIDC for the Greater Glasgow hydroscape study, documenting lake sediment core metadata.
- File name: hydroscape_glasgow_core_metadata.csv.
- Source organization: UK Centre for Ecology & Hydrology (CEH).
- Purpose: support linkage between core metadata and historical lake sediment metal concentrations; includes spatial, sampling, and core characteristics.

## Key Data Fields
- WBID (Waterbody Identification): unique ID for each waterbody, linked to lakes index.
- Hydroscape: named Hydroscape region hosting the lake cores.
- Name: lake name.
- General location of core: categorical descriptor of core sampling zone (deep, littoral, intermediate).
- OSGB36_E / OSGB36_N: Easting and Northing coordinates in OSGB36 datum.
- Water depth at core site (m): distance from water surface to sediment at core site.
- Secchi disc depth (m): water clarity prior to coring.
- Core length and type: core length (m) and descriptive type.
- Corer types: specifies coring equipment used (e.g., Tapper, Chambers).
- Date core collected: field collection date (dd/mm/yyyy).
- UCL_Code: internal UCL code used on bags/database.
- UCL Sample ID: internal Amphora code for the entire core (unique ID).
- 210 Pb-dated (Y/N) for Hydroscape: indicates whether the core was radiometrically dated using 210Pb.

## Data Provenance and Scope
- Source: CEH Hydroscape region data for Greater Glasgow.
- Spatial data: coordinates provided (OSGB36), enabling mapping within the region.
- Temporal and methodological scope: includes collection date and corer type; 210Pb dating status indicates availability of age dating for cores.

## Use for Analysis
- Facilitates integration of core metadata with historical metal concentration data for analyses by site, depth category, or sampling method.
- Enables spatial analyses (lake-level and core location) and cross-referencing by corer type and dating status.
- Supports data governance and reproducibility via internal IDs (UCL_Code, UCL Sample ID) and documented metadata fields.

## Data Quality and Limitations
- Potential coordinate system considerations: OSGB36 may require transformation for other mapping systems.
- Depth, clarity, and core characteristics are single-point descriptors; variability within a lake is not captured.
- 210Pb dating status (Y/N) indicates presence/absence of age information; actual dating details not included in this metadata file.
- Some fields rely on consistent labeling (e.g., deep vs littoral vs intermediate) which may require standardization across cores.

## Practical Considerations for Analysts
- Prepare for data integration by aligning OSGB36 coordinates with other spatial datasets and consider reprojecting if needed.
- Use 210Pb-dated flag to filter cores with age information for time-series or age-model analyses.
- Pay attention to internal UCL identifiers for data traceability and dataset provenance when merging with metal concentration data.

## Access and Metadata
- Data organized under the EIDC repository; metadata supports discoverability and linking with related data on metal concentrations.