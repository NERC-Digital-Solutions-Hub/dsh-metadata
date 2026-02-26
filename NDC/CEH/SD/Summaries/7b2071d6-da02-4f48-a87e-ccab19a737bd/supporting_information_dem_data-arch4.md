# Digital elevation model of the Evoflood experiments, elevation data of the experimental river: supporting information

## Overview
- A data repository for Evoflood experiments studying morphological evolution of an experimental alluvial river under discharge variations.
- Two data types: XYZ elevation files (XYZ_i.csv) and the experimental parameters file.
- Location and setup: 10 m long x 2.5 m wide flume at The Total Environment Simulator, University of Hull, UK; data collected Sep–Dec 2021.
- Data were generated using a fixed-position 3D terrestrial laser scanner (Faro Focus X330) with seven targets for re-orientation and quality control.

## Data structure and content
- XYZ_i.csv (i = 0 to 137): elevation data with X and Y as pixel coordinates and Z as elevation in meters; Z = 999999 indicates no data for that pixel.
- DEM processing: scans reoriented with target locations; pre-processed in CloudCompare to isolate the experimental area; converted to TIFF for Python analysis.
- Grid: down-sampled to a regular grid (0.5 x 0.5 cm cells), resulting in a grid of 2100 rows x 477 columns.
- experimental_parameters.csv: linked to XYZ_i.csv; includes time (seconds), water discharge (L/min), and morphological characteristics extracted from the DEM (units noted in description).
- DEM-linked metadata: each DEM_i.csv has metadata fields including DEM_name, Slope (m/m) with dS (error), Width (pixels) with D_w (error), Depth (m) with D_d (error), Conveyance (pixel.m) with D_cc (error).
- Data interpretation: active floodplain defined as areas below zero elevation after slope detrending; conveyance capacity calculated as the product of floodplain width and depth (CC = W * D).

## Data collection and processing workflow
- Data collection cadence varies by discharge: base flow (1 hour), medium flow (45 minutes), high flow (30 minutes); exact timings in experimental_parameters file.
- Dry-surface requirement exists because the laser cannot capture submerged surfaces; non-dry surfaces yield -999999 values.
- Re-orientation quality control: scans accepted only if re-orientation error < 0.5 mm; otherwise rescanned.
- Pre-processing steps: isolate experimental area (remove walls/instruments) in CloudCompare, convert to TIFF, then analyze with Python.
- Point cloud handling: CloudCompare used to sub-sample to a regular grid; typical vertical/horizontal errors are about ±1 mm.
- Data conversion: XYZ files produced from processed DEMs for downstream analysis.

## Variables and metadata
- Time and discharge: time in minutes since experiment start; Qw in L/min.
- DEM metadata: DEM_name links to the corresponding XYZ_i.csv file.
- Morphological metrics and uncertainties: Slope (dS), Width (D_w), Depth (D_d), Conveyance (D_cc); all accompanied by their respective errors.
- Floodplain interpretation: active floodplain below zero elevation; areas above zero are inundated only when conveyance capacity exceeds threshold.

## Data quality and governance
- Quality controls embedded in workflow: strict re-orientation accuracy, dry-surface requirement, and explicit handling of missing data (-999999).
- Documentation of uncertainties: each morphological metric provides associated error (e.g., dS, D_w, D_d, D_cc).
- Consistent units and naming conventions across DEMs and parameters to support reproducibility and comparability.
- Data packaged as raw DEMs (XYZ_i.csv) and derived metrics (experimental_parameters.csv) with explicit indices for traceability.

## Access, usage, and reuse
- Designed to enable analysis of floodplain evolution under varying discharges and to evaluate river conveyance capacity from geometry.
- Clear linkage between raw elevation data and derived morphological descriptors facilitates reproducibility and cross-study integration.
- Formats described (CSV for XYZ, CSV for parameters; TIFF intermediate format; potential Python-based analyses) support multi-tool reuse.

## Limitations and considerations
- Underwater surfaces not captured; reliance on dry-surface scans may limit some observations.
- Data gaps may exist (indicated by -999999); temporal sampling governed by scan cadence.
- Some units are described in the metadata; users should confirm interpretation when integrating with external datasets.

## Potential use cases for Data Leaders
- Data system stewardship: maintain raw DEMs and derived metrics with robust metadata for discoverability.
- Provenance and lineage tracking: document the end-to-end workflow from TLS data to DEMs to morphological metrics.
- Cross-project collaboration: reuse the dataset structure (index-based DEMs with linked parameter file) to harmonize data across flood or geomorphology projects.
- System-level analysis: leverage the conveyance capacity metric (CC) alongside morphology to study floodplain performance under different discharges.