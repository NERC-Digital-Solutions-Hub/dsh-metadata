# Supporting documentation for data resource Hammer_Cores_KoT.csv

- Project context and leadership
  - Project: Carbon Storage in Intertidal Environments (C-SIDE)
  - Funding: NERC (NE/R010846/1)
  - Staff Responsible: Craig Smeaton
  - Research team: 1) Craig Smeaton (University of St Andrews), 2) Luis Rees-Hughes (University of Leeds), 3) Natasha L.M. Barlow (University of Leeds), 4) William E.N. Austin (University of St Andrews/Scottish Association of Marine Science)

- Data resource at a glance
  - Name: Sedimentological and organic carbon data from the Kyle of Tongue Saltmarsh (Hammer cores)
  - Coverage: 39 soil samples across 4 hammer cores from Kyle of Tongue, Scotland
  - Observations: Bulk density, water content, porosity, and organic carbon content
  - Depths: Samples collected to 100 cm; measurements at 10 cm intervals
  - Output format: .csv data resource
  - Related publication: Smeaton et al. (2020) on coring and blue carbon stock estimation (Geoderma)

- Variables and measurements
  - Core sampling variables: Core ID, depth (Depth_cm), mid-point depth (Mid_Point_Depth_cm)
  - Physical properties: Water Content (%), Wet Bulk Density (g cm^-3), Dry Bulk Density (g cm^-3), Porosity (Φ)
  - Organic carbon: OC content (% wt) with three replicates per sample; Mean_OC_perc and Std_Dev
  - Descriptors: Simplified Troels-Smith soil description; Lat/Long coordinates; multiple coordinate representations (Lat_dec_deg, Long_dec_deg, Grid_Reference, X_easting, Y_northing)

- Sampling and laboratory methods
  - Core collection: PVC core tubes (150 cm length, 6.16 cm ID) driven to 100 cm depth; top sealed to create vacuum; cores extracted manually
  - Core handling: Cores split lengthways into working/archive sections; fixed-volume (4 cm^3) samples taken at 10 cm intervals
  - In-field measurements: GPS positioning (DGPS) for core locations
  - Soil description: Troels-Smith (1955) classification; simplified to dominant class; two independent assessments for QA
  - Physical properties: Wet bulk density from weighed samples; drying at 60°C for 72 hours to derive dry bulk density and water content; porosity calculated from density values
  - Organic carbon analysis: 10 mg milled samples acidified with 10% HCl to remove carbonates; dried and sealed; organic carbon measured with Elemental Analyser (Elementar Vario EL Cube); three replicates per sample; calibration with Acetanilide; repeated analysis of standard (B2178)
  - Data processing: Mean OC% computed from replicates; standard deviation reported

- Quality control and data provenance
  - Independent land-descriptions/classifications by two team members; combined result used for data reported
  - Calibration and analytical accuracy supported by standard references and replicates
  - Data quality notes: Documentation cites established procedures (Athy 1930; Dadey et al. 1992; Verardo et al. 1990; Nieuwenhuize et al. 1994; Troels-Smith 1955)

- Data structure and metadata
  - Data resource description file (Hammer_Core_KoT.csv) defines fields and formats, including:
    - Core (text)
    - Collection_date (numeric)
    - Lat_dec_deg (numeric)
    - Long_dec_deg (numeric)
    - Grid_Reference (text)
    - X_easting, Y_northing (numeric)
    - Depth_cm, Mid_Point_Depth_cm (numeric)
    - Sampling_Method (text)
    - Simplified_Troels_Smith (text)
    - Water_Content_perc (numeric)
    - Wet_Bulk_Density_g_cm_3 (numeric)
    - Dry_Bulk_Density_g_cm_3 (numeric)
    - Porosity (numeric)
    - OC_perc_Rep1/Rep2/Rep3 (numeric)
    - Mean_OC_perc (numeric)
    - Std_Dev (numeric)

- Data accessibility and linkage
  - File format: .csv for data resource; metadata and method details also documented
  - Geographic coordinates provided in multiple systems (WGS84 and OSGB 1936) to facilitate mapping and integration with other datasets
  - References and context: Data linked to best-practice work on blue carbon stock estimation; numerous historical methodological references for density, porosity, and organic carbon analyses

- Potential data products and use cases (Data Support perspective)
  - Self-serve data exploration: per-core and depth-profile visualizations of OC%, water content, and densities
  - Cross-core comparisons: identify spatial or depth-related trends in porosity and OC content
  - Geographic integration: map-based views using Lat/Long, Grid Reference, and Easting/Northing
  - Quality-aware dashboards: show replicates, mean OC, and associated standard deviations with data provenance notes
  - Data reuse in policy or coastal carbon assessments: integrate with broader datasets on blue carbon stocks and intertidal sediment properties

- Limitations and considerations
  - Sampling plan: No repeat sampling is planned; data represents a single time point per core
  - Coverage: 39 samples across 4 cores; suitable for regional-scale insights but not exhaustive temporal trend analysis
  - Documentation: Comprehensive methodological detail supports reproducibility and re-use, with explicit QA steps and references

- Related materials
  - Smeaton, C., Barlow, N. L., & Austin, W. E. (2020). Coring and compaction: Best practice in blue carbon stock and burial estimations. Geoderma, 364, 114180
  - Foundational methodological references for density, porosity, and organic carbon analysis (Athy 1930; Dadey et al. 1992; Verardo et al. 1990; Nieuwenhuize et al. 1994; Troels-Smith 1955)