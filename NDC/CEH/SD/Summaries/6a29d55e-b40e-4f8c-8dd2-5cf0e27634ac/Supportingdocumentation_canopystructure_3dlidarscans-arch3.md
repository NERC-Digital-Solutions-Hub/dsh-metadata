# Supporting documentation

## Overview
- Dataset comprises 3D LiDAR (TLS) scans representing 0.5 ha permanent sample plots in the Caatinga, Brazil.
- Plots: two at Serra das Almas Reserve (SDA) and one at Petrolina (PET); part of the Nordeste project.
- Scans collected between July 2017 and May 2019 to study plant, soil, and climate relationships and to support biodiversity, carbon allocation/stocks, and ecosystem-function research in this seasonally dry biome.

## Purpose and Context
- Nordeste project aims to address decades of neglect in Caatinga biodiversity and policy-relevant ecosystem research.
- Goals include understanding growth preferences, carbon stocks, biodiversity, and ecosystem functioning; integration of plant, soil, and climate data to improve conservation and future climate-related decision-making.

## Data Content and Structure
- Total of 32 files describing TLS data:
  - PET site: 20 processed point-cloud files for 10 individual trees representing native Caatinga species; includes species such as Manihot pseudoglaziovii, Commiphora leptophloeos, Sapium glandulosum, and Cnidoscolus quercifolius.
  - Subplots: data described for 3D scans of representative PET subplots with multiple scans across dates; data formats include xyz (with X, Y, Z coordinates and RGB intensities) and ply in some cases.
  - SDA site: multiple scans for subplots within 10 m × 10 m plots, scanned on several occasions to enable model integration.
- Plot metadata includes coordinates:
  - PET-01 (Petrolina): latitude and longitude provided; city, state, and country listed.
  - SDA-01 and SDA-02 (Serra das Almas): coordinates and locale details provided.

## Data Acquisition and Processing
- Acquisition:
  - Equipment: Faro Focus TLS scanner; Faro Scene software used for registering scans and exporting point clouds in xyz format.
  - Protocol steps include selecting representative trees/subplots, photographing from multiple viewpoints, acquiring initial low-resolution scans, performing indoor scans, and documenting the process.
- Processing workflow (PET as described in detail):
  - Load scans, remove dark scan points, smooth, and apply stray point and edge-artifact filters.
  - Manual registration (cloud-to-cloud alignment), create consolidated point cloud.
  - Cleaning: use clipping box to isolate target tree/subplot; manual noise removal.
  - Export: project history wiped to free disk space; export as xyz in a dedicated workflow.
- Similar processing approach for outside/subplot data and 10 m × 10 m subplot scans; aim is to homogenize scans to generate a single, analyzable 3D model with metric and radiometric capabilities.

## Temporal Coverage and Reproducibility
- Primary data collection window: 2017–2019.
- Repeated scans for some targets:
  - PET subplot scanned on multiple dates (dates include 2017-10-27, 2018-02-21, 2018-09-25 for some subplots), enabling temporal comparisons of structure.

## Accessibility and Data Governance (implicit)
- Raw scans originally stored in .fls formats, later converted to ply/xyz for broader use.
- The documented workflow emphasizes transparency and reproducibility, including explicit processing steps and registration procedures, which supports data verification and reuse.

## Relevance for Environmental Health Monitoring Frameworks
- High-resolution structural data on Caatinga trees and plots supports monitoring of vegetation structure, carbon stocks, and biodiversity under variable climate conditions.
- Data can be used to calibrate remote sensing, model growth and carbon allocation, and inform conservation and policy decisions in semiarid ecosystems.

## Key Considerations and Limitations
- The processing workflow is intensive and involves multiple manual steps (registration, cleaning, and parameter choices), which may affect reproducibility across different teams or times without strict adherence to the documented protocol.
- Metadata richness includes precise plot locations and species, but users may need to consult accompanying documentation for full context and data formats (xyz/ply) and to understand the exact composition of tree vs. subplot files.