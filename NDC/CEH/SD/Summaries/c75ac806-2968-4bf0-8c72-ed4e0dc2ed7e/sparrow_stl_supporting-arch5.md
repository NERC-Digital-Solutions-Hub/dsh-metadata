# MicroCT 3D scans from Passer sparrows - house ( Passer domesticus) , Spanish ( Passer hispaniolensis) , and Italian ( Passer italiae) sparrows and F1 hybrids generated during a crossing experiment at the University of Oslo, Norway in 2014/2015.

## Overview
- A dataset of MicroCT 3D skull scans from multiple Passer sparrows (house, Spanish, Italian) and F1 hybrids, produced during a crossing experiment (2014/2015) at University of Oslo.
- Data collected and processed to enable morphometric analysis of skull shape and size, with a clear provenance and metadata structure to support discovery and reuse.

## Collection and origin
- Samples originate from the Natural History Museum of Oslo under a material transfer agreement.
- Scanned at the Hounsfield Facility, Sutton Bonington Campus, University of Nottingham, UK, using Waygate Technologies v|tome|x M 240kV CT system (26 μA).
- Skulls were mounted on polystyrene and rotated during imaging, creating ring artefacts mainly dorsally around the braincase; artefacts deemed non-significant for analyses and not minimized.

## Data generation and processing
- Raw outputs include .TIF projections that are reconstructed into 3D skull models; .VOL files created for visualization and analysis in Avizo 9.1.0.
- Landmarking:
  - 20 anatomical landmarks placed in 3D space on each skull, repeated three times per individual; the mean coordinates used for analysis.
  - Landmarks mirrored to the right side only (sagittal plane) to avoid redundancy and simplify analyses, given general skull symmetry and study focus.
- Alignment and shape analysis:
  - Landmark coordinates organized in 3D arrays in R.
  - Partial Generalized Procrustes Analysis (Gower 1975) performed with geomorph (gpapgen).
  - Steps: translate to a common centroid, scale to centroid size = 1, rotate to minimize Procrustes distance; configurations are superimposed in tangent space.
  - Shape defined by geometric features of landmarks excluding scale, location, and rotation; size defined by centroid size (square root of sum of squared distances of landmarks from centroid).

## Data format, structure, and units
- Data format: STL files describing triangulated 3D surfaces (wireframes) with recorded landmark coordinates.
- Structure: each STL file corresponds to a single individual skull.
- Units: 3D Cartesian coordinates embedded in STL representations; centroid size used for size measurement.

## Metadata and provenance
- Metadata table accompanies the dataset, capturing for each individual:
  - Species and subspecies (e.g., P. domesticus, P. hispaniolensis, P. italiae) and F1 hybrids.
  - Sex and capture/location information (e.g., badajoz, Spain; oslo, Norway).
- Filenames reflect metadata (example: 2019-1.stl, 2019-26.stl, HYB-10.stl, etc.), with entries detailing species, sex, and location.
- The dataset includes a wide range of individuals across multiple populations and hybrids, with explicit provenance from museum collections and cross-lab imaging facilities.

## Quality control and data quality
- Manual placement of landmarks checked by examining average coordinates; any issues corrected on the scans.
- Ring artefacts acknowledged but not corrected due to negligible impact on analyses.

## Practical governance and reuse considerations for Data Stewards
- Data governance: provenance clearly documented (museum transfer, imaging facility, instrument, and processing pipeline).
- Data formats and interoperability: STL for 3D surfaces with standardized landmark metadata; use of widely accepted morphometric methods (Procrustes alignment) and tools (geomorph in R, Avizo).
- Accessibility and discoverability: explicit metadata and consistent file naming to support dataset discovery and interpretation.
- Updating and versioning: notes on data processing steps (landmark averages, QC corrections) imply a transparent processing trail suitable for updates if new analyses or repairs are needed.
- Potential challenges to plan for:
  - Managing large 3D STL files and associated TIFF projections; ensuring storage, cataloging, and access controls align with governance standards.
  - Maintaining metadata completeness across all individuals and ensuring consistency with file naming conventions.