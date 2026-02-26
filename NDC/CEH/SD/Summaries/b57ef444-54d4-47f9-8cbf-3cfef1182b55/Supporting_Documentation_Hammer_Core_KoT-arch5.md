# Supporting documentation for data resource Hammer_Cores_KoT.csv

- Project and team
  - Project: Carbon Storage in Intertidal Environments (C-SIDE)
  - Funding: NERC (NE/R010846/1)
  - Staff Responsible: Craig Smeaton
  - Research Team: Craig Smeaton (U. of St Andrews), Luis Rees-Hughes (U. of Leeds), Natasha L.M. Barlow (U. of Leeds), William E.N. Austin (U. of St Andrews/Scottish Association of Marine Science)

- Data resource overview
  - Name: Sedimentological and organic carbon data from the Kyle of Tongue Saltmarsh (Hammer cores)
  - Description: Measurements of bulk density, water content, porosity, and organic carbon content for 39 soil samples across 4 hammer cores
  - Location: Kyle of Tongue, Scotland
  - Geographic references: Site coordinates in decimal degrees (WGS84); OSGB 1936 grid references; X/Easting and Y/Northing
  - Sampling status: No repeat sampling planned
  - Related publication: Smeaton, Barlow, & Austin (2020) Geoderma; other references listed

- Data collection and methodology
  - Core sampling: Hammer cores; 150 cm PVC tubes with 6.16 cm ID and 0.24 cm walls; inserted to 100 cm depth; vacuum seal and extraction with tractor jack
  - Core processing: Split lengthways into working/archive sections; fixed-volume samples (4 cm3) collected at 10 cm intervals
  - Soil description: Troels-Smith (1955) classification applied (simplified to dominant class)
  - Physical properties: Wet bulk density, dry bulk density, water content derived from mass differences; porosity estimated from densities
  - Elemental analysis: 10 mg milled samples acidified with 10% HCl to remove CaCO3; dried and analyzed with Elemental Analyzer (carried out per Verardo et al., 1990; Nieuwenhuize et al., 1994)
  - Replicates and accuracy: Three replicates per sample for organic carbon; calibration with Acetanilide; repeated analysis of standard (B2178)
  - Data quality checks: Independent Troels-Smith classifications by two team members; combined result used

- Data resources and structure
  - Primary data resource: Hammer_CoRES_KoT.csv
  - Core and observations: 4 cores, 39 samples total
  - Key variables and units (from the Hammer_Core_KoT.csv file description)
    - Core (text): Core ID
    - Collection_date (numeric): Date of sample collection
    - Lat_dec_deg, Long_dec_deg (numbers): Decimal degrees (WGS84)
    - Grid_Reference (text): OS National Grid reference (OSGB36)
    - X_easting, Y_northing (numbers): OSGB36 coordinates
    - Depth_cm, Mid_Point_Depth_cm (numbers): Depth of sample, mid-point depth
    - Sampling_Method (text): Hammer Core
    - Simplified_Troels_Smith (text): Dominant Troels-Smith soil description
    - Water_Content_perc (number): Water content (%)
    - Wet_Bulk_Density_g_cm_3, Dry_Bulk_Density_g_cm_3 (numbers): Densities
    - Porosity (number): Porosity (Φ)
    - OC_perc_Rep1, OC_perc_Rep2, OC_perc_Rep3 (numbers): Organic carbon content (% w/w) for three replicates
    - Mean_OC_perc (number): Mean OC content across replicates
    - Std_Dev (number): Standard deviation across replicates
  - File formats: CSV for data and metadata files
  - Documentation linkage: Data resource description refers to the accompanying publication and methodological references

- Provenance, quality, and governance
  - Data provenance: Detailed recording of sampling methods, core processing, and analytical procedures
  - Calibration and QA: Elemental analyzer calibrated with Acetanilide; use of standard B2178; independent QC by two team members for Troels-Smith classifications
  - Documentation and metadata: Comprehensive descriptions of sampling, analysis, and data fields; explicit definitions of each variable and replicate treatment
  - Reproducibility: Derived fields (Mean_OC_perc, Std_Dev) computed from three replicates; clear calculation basis documented in literature references
  - Data linkage: Dataset linked to a peer-reviewed publication (Geoderma, 2020) for context and methodological grounding

- Notes for data stewards
  - Interoperability: Multiple coordinate representations (decimal degrees, OSGB grid, easting/northing) support GIS use but require consistent metadata mapping
  - Metadata completeness: Ensure metadata includes method details (Troels-Smith simplification, 10 cm sampling interval, core depth, replication scheme) and QA notes
  - Derived data: Document formulas or tooling used to compute Mean_OC_perc and Std_Dev to ensure reproducibility
  - Licensing and access: While not stated, reference to published work suggests a data-sharing expectation; confirm licensing, access rights, and any embargoes
  - Data updating: Current status indicates no planned repeats; if future updates occur, ensure versioning and changelog are maintained

- Summary for use
  - This resource provides a well-documented set of intertidal soil core measurements with standardized descriptions, geospatial context, and quality-controlled organic carbon analyses
  - Suitable for meta-analyses on soil carbon dynamics in saltmarsh environments, GIS mapping, and cross-study comparisons, provided metadata mappings are aligned and replicates are properly tracked