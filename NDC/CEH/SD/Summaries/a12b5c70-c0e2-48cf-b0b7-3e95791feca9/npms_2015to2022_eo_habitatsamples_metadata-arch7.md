# Habitat samples dataset

## Purpose and Context
- Part of the National Plant Monitoring Scheme (NPMS), a habitat-based plant monitoring program across the UK and nearby territories.
- Aims to support training and validation of Earth Observation–based data products by pre-joining NPMS samples with their recorded habitat and providing habitat-change information.
- Provides data to detect habitat change, understand drivers, and contribute to biodiversity indicators.

## Dataset Contents
- File: npmsHabitatSamples_2015to2022.csv (Size: 4287 kb).
- It documents plant-community samples taken at fixed plots over time, with fields including:
  - sample_id: unique NPMS fixed-plot sample identifier.
  - survey_id: NPMS survey code (e.g., 87, 154, 155) indicating survey level.
  - entered_sref / entered_sref_system: spatial reference and system used for the sample entry.
  - LATITUDE / LONGITUDE: precise sample location coordinates.
  - monad / monadCRS: 1 km grid cell and its CRS (OSGB, OSIE, UTM).
  - country: Britain, Channel Islands, or Northern Ireland context.
  - surveyorHabitat / NPMS_hab_type / NPMS_broad_habitat: habitat classification (fine or broad scale; mapped to NPMS broad habitat).
  - multipleHabs: flag indicating whether habitat changed between samples for a fixed plot (Y/N); note potential non-true-change causes (data entry issues, plot relocation).

## Spatial Details and Compatibility
- Spatial reference systems used: OSGB (EPSG:27700), OSIE (EPSG:29902), and WGS84 (EPSG:4326).
- Monads denote 1 km grid cells aligned with the chosen CRS.
- Data are pre-joined with habitat classifications to ease GIS integration and model training.

## Use in GIS and Data Product Development
- Enables mapping of plant-community samples and their habitat classifications over time.
- Supports analysis of habitat change across habitats and regions, with the ability to link to EO-derived datasets.
- Useful for validating habitat-change signals and informing conservation planning and policy.

## Evidence Quality Assurance (EQA) and Governance
- EQA framework supported by published research and NPMS documentation; primary sources include field guidance notes and multiple peer-reviewed papers.
- Data and outputs are publicly available for independent review.
- Governance:
  - Project Steering Group oversees NPMS activities.
  - External peer review invoked for high-risk outputs or design issues (e.g., survey design workshop).
- Uncertainty, assumptions, and limitations:
  - Outputs are checked by scientists to ensure evidence-based claims.
  - Uncertainty is addressed via robust statistical design and modeling.
  - Plans to quantify and report uncertainty alongside results.
- Data handling, versioning, and documentation:
  - Design work, outputs, and versions archived and backed up off-site per a Data Management Plan.
  - Follow PRINCE2 project management standards.
- Data input, verification, and publishing:
  - Online data capture with standardized dictionaries, date calendars, map-based locations, and controlled habitat terms.
  - Automated geographic range checks; exceptions reviewed via the IRecord system (for expert verification).
  - Data and results to be disseminated through NPMS newsletters and peer-reviewed publications.

## Notes on Data Quality and Limitations for GIS
- Habitat-change flag (multipleHabs) may reflect non-biological issues (data entry errors, plot relocation) rather than true ecological change.
- Variability in surveyor expertise and habitat classification scale (fine vs broad) can introduce classification differences.
- Formal on-field QA of recording currently not implemented but planned for future consideration.

## Access and Documentation
- Primary dataset and NPMS resources available via the NPMS website and the CEH data repository (EIDC dataset).
- Supplementary publications and reports provide methodological context and QA guidance for users.