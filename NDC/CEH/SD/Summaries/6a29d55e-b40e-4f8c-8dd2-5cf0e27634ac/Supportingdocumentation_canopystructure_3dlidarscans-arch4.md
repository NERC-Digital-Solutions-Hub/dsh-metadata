# Supporting documentation

## Overview
- Dataset of 3D LiDAR scans representing Caatinga vegetation, built from 0.5 ha permanent sample plots.
- Locations: Serra das Almas Reserve (SDA) with two plots (SDA-01, SDA-02) and Petrolina (PET) with one plot (PET-01) in Brazil.
- Collected as part of the Nordeste project to understand plant, soil, and climate relationships in the Caatinga and to support conservation and ecosystem-function research.
- Scans collected between July 2017 and May 2019 using a TLS Faro Focus scanner; data processed with Faro Scene software and exported as point clouds in xyz format (and ply for some data).
- Dataset contains 32 files describing processed point clouds for individual trees and subplots, with both outdoor (OUT) and indoor (IN) scans.

## Data content and structure
- PET-01 (Petrolina) and SDA-01 / SDA-02 (Serra das Almas) plots with precise geographic coordinates (latitude, longitude, city, state, country).
- Species scanned include Manihot pseudoglaziovii, Commiphora leptophloeos, Sapium glandulosum, and Cnidoscolus quercifolius.
- Scanning scope includes:
  - Individual trees: xyz-format point clouds representing native Caatinga trees (OUT and IN scans with the same protocol).
  - Subplots: xyz-format point clouds for 10 m x 10 m subplots, scanned at multiple times for longitudinal coverage.
- Data formats:
  - xyz: six columns (X, Y, Z, and RGB intensities).
  - ply: used for some datasets, including the raw scans.
- Processing outcome: registered and cleaned 3D models with metric and radiometric capabilities; raw scans were consolidated and converted to ply where applicable.

## Context and purpose
- Nordeste project aims to rectify long-standing neglect of Caatinga biodiversity and ecosystem-function data, enabling better understanding of growth, carbon allocation, stocks, biodiversity, and remote sensing correlations.
- The dataset supports analysis at both tree and subplot levels to inform carbon dynamics, structural architecture, and ecosystem processes in seasonally dry biomes.

## Data collection and processing workflow
- Field collection protocol (summary):
  - Select representative tree or subplot; tag trees and record species/date.
  - Capture photos from multiple viewpoints (recommended ~4).
  - Record initial low-resolution 3D scans of whole trees/subplots to document original structure.
  - Conduct indoor scans of portions of the tree (detailed multi-angle scans).
- Data processing workflow (Faro Scene):
  - Load scans; remove dark points; smooth scans.
  - Filter stray points and edge artifacts.
  - Register scans manually; create a point cloud.
  - Clip to isolate the target tree/subplot; manually clean noise.
  - Export processed point cloud to xyz; wipe project history to free space.
- Data are organized with separate procedures for PET (outside/inside) and SDA plots, using a 10 m x 10 m subplots framework.

## Metadata and site details
- PET-01: Petrolina, latitude -9.04803, longitude -40.3198, city Petrolina, state Pernambuco, country Brazil.
- SDA-01: Serra das Almas, latitude -5.1468, longitude -40.9282, Crateus, Ceara, Brazil.
- SDA-02: Serra das Almas, latitude -5.1414, longitude -40.9149, Crateus, Ceara, Brazil.
- Data were acquired using a TLS 3D Faro Focus scanner; processed with Faro Scene software; outputs in xyz and ply formats.

## Data governance, reuse, and implications for data strategy
- Demonstrates end-to-end data lifecycle: from field collection and tagging to processing, registration, cleaning, and exporting standardized point clouds.
- Supports cross-site comparability (PET and SDA plots) and longitudinal analysis (repeated scans for subplots).
- Enables data discoverability through explicit site metadata, species, plot details, and standardized formats (xyz/ply) suitable for integration with other datasets and remote sensing analyses.
- Highlights best practices for data stewardship in 3D ecological datasets: detailed processing workflow, explicit documentation of steps, and clear provenance through project history management.

## Key considerations for data leadership
- Data quality and standardization: consistent scanning protocols, processing steps, and metadata are essential for interoperability across sites and projects.
- Discoverability and metadata completeness: ensure complete site coordinates, species, plotting scheme, and processing history are preserved for future reuse.
- Access and sharing: consider licensing, data access permissions, and how to balance openness with any sensitive or restricted aspects of field data.
- Scalability and reuse: the approach supports expansion to additional plots or regions, enabling broader analyses of Caatinga biodiversity and carbon dynamics.