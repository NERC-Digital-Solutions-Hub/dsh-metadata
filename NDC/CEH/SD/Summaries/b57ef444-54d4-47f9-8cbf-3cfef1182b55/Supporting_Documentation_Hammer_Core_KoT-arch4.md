# Supporting documentation for data resource Hammer_Cores_KoT.csv

## Overview
- Describes a sedimentological and organic carbon data resource from Kyle of Tongue Saltmarsh hammer cores.
- Contains 39 soil samples across 4 cores, with measurements of water content, bulk density (wet and dry), porosity, and organic carbon content.
- Collected as part of the Carbon Storage in Intertidal Environments (C-SIDE) project; linked to a published best-practice work on blue carbon stock estimations.

## Data resource details
- Data resource name: Sedimentological and organic carbon data from the Kyle of Tongue Saltmarsh (Hammer cores).
- Description: Bulk density, water content, porosity, and organic carbon content for 39 soil samples across 4 hammer cores.
- Locations: Kyle of Tongue, Scotland. Site coordinates provided in decimal degrees (WGS84), plus British National Grid (OSGB36) references and E/N coordinates.
- Observations: No planned repeat sampling.
- Variables observed: Water Content (%), Wet Bulk Density (g cm^-3), Dry Bulk Density (g cm^-3), Porosity (Φ, dimensionless), Organic Carbon Content (% by weight), plus core and sampling metadata.
- File format: CSV (.csv).
- Related publication: Smeaton et al. (2020) Geoderma on coring and best practices for blue carbon stock and burial estimations.
- Data resource description structure: Includes core metadata fields (Core ID, collection date, lat/long, grid reference, easting/northing, depth, sampling method) and detailed measurements (Troels-Smith description, water content, bulk densities, porosity, OC replicates and statistics).

## Data collection methods and quality assurance
- Core sampling: 150 cm PVC tubes, 6.16 cm inner diameter, beveled edge for root material, hammered into soil to 100 cm depth; top sealed to create a vacuum and cores extracted with a tractor jack.
- Sample processing: Cores split lengthways into working/archive sections; fixed volumetric samples (4 cm^3) taken at 10 cm intervals; GPS locations recorded with DGPS.
- Soil description: Troels-Smith (1955) classification used for dominant class; descriptions independently validated by two team members.
- Physical and chemical analyses: 
  - Wet/dry bulk density calculated from mass changes after drying at 60°C (72 hours).
  - Porosity derived from density and water content data.
  - Organic carbon measured with an Elemental Analyzer after acidifying to remove carbonates; three replicates per sample for accuracy; calibration with Acetanilide and standard reference material (B2178).
- Data quality control: Independent dual classification for soil descriptions; triplicate OC measurements to ensure accuracy.
- Documentation and provenance: Calculations and methods align with established literature (Athy 1930; Dadey et al. 1992; Verardo et al. 1990; Nieuwenhuize et al. 1994; Tröels-Smith 1955).

## Data structure and variables
- Core metadata: Core ID, collection date, latitude/longitude (decimal degrees, WGS84), grid reference, X/Easting, Y/Northing, Depth (cm), Mid-Point Depth (cm), Sampling Method, Simplified Troels-Smith classification.
- Measurements: Water Content (%), Wet Bulk Density (g cm^-3), Dry Bulk Density (g cm^-3), Porosity (Φ).
- Organic Carbon: OC Content (%) with three replicates (OC_perc_Rep1, Rep2, Rep3), Mean_OC_perc, Std_Dev.
- Data format: CSV with well-defined column descriptions and units.

## Data governance, access, and documentation
- Ownership and funding: Project "Carbon Storage in Intertidal Environments (C-SIDE)"; funded by NERC (NE/R010846/1); Staff Responsible: Craig Smeaton; Research team includes Craig Smeaton, Luis Rees-Hughes, Natasha L.M. Barlow, William E.N. Austin.
- Documentation: Linked to a peer-reviewed publication on best practices for blue carbon stock estimation; detailed methodologies and calibrations cited within the resource.
- Metadata completeness: Column-level descriptions and data formats provided; measurement replicates and derived statistics included for transparency and reusability.
- Reuse potential: Data designed to support carbon stock and burial estimations in intertidal environments; suitable for integration with broader datasets, given clear methodology, QA steps, and provenance.

## Relevance for Data Leaders
- Demonstrates end-to-end data lifecycle: clear data resource name, collection methods, QA, metadata, and linkage to scholarly work.
- Highlights importance of data discoverability, standardization, and metadata richness (coordinates, depth, sampling method, Troels-Smith classification, replicates, derived statistics).
- Shows how to balance field practicality (sampling strategy, replication) with analytical rigor (calibration, QA, independent validation).
- Provides a concrete example of governance and provenance when coordinating cross-institutional data assets for environmental data and policy-relevant research.