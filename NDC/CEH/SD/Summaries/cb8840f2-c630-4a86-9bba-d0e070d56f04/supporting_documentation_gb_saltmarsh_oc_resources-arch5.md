# Supporting document for: GB_saltmarsh_OC_resources.zip

- A dataset describing spatially explicit surficial soil organic carbon (OC) storage and stocks across Great Britain saltmarshes (top 10 cm), produced from multiple national datasets and vegetation maps.
- Project: Carbon Storage in Intertidal Environments (C-SIDE); funded by NERC; staff Responsible: Craig Smeaton; multidisciplinary team across universities and UK ecological centers.
- Dataset scope: Mapping OC density (kg OC m^-2) and OC stocks (tonnes OC) for 438 saltmarshes over 451.65 km^2 of Great Britain (Scotland, England, Wales); includes locations, marsh areas, and per-NVC class/zone statistics.

- Data resource overview
  - Data Resource ID: not specified here; Description centers on the spatial mapping dataset.
  - Description: Surficial OC storage and stocks across Great British saltmarshes derived from surficial soil OC density data and dry bulk density, combined with existing saltmarsh vegetation maps.
  - Locations: Great Britain (Scotland, England, Wales); coordinates provided as decimal lat/long (WGS84) and as OSGB 1936 X/Y.
  - Coverage: 451.65 km^2; 438 marshes with individual OC stock estimates.
  - Variables observed: 
    - Saltmarsh surficial soil OC stock (tonnes OC)
    - Sample Location (Latitude/Longitude; X/Y)
    - Marsh Area (km^2)
    - Organic Carbon Storage (kg OC m^-2) for top 10 cm soil
  - Data structure: Bespoke GIS layers mapping OC storage by NVC class/marsh zone; includes per-marsh statistics.

- Data sources and relationships
  - Primary data inputs: 
    - NERC C-Side project data (dry bulk density, OC content)
    - Marine Scotland data
  - Supporting vegetation maps: Environment Agency (England, 2021), Haynes (Scotland, 2016), Natural Resources Wales (2016)
  - Calibration and methods are built on these sources to produce the final OCI storage maps.

- Methods and processing
  - Calculation approach: OC stock and storage calculated for each saltmarsh class/zone using OC content (%) and dry bulk density (kg m^-3).
  - Statistical treatment: Monte Carlo Markov Chain (MCMC) framework; 1,000,000 samples drawn from a larger pool (up to 100,000,000) for input variables to populate stock calculations.
  - Data quality checks: QC fields reported as NA in this document; indicates potential gaps in quality control metadata within the summary.
  - Spatial and software specifics: 
    - Spatial projection: OSGB 1936
    - Software: ESRI ArcGIS
    - File formats: .cpg, .dbf, .prj, .sbn, .sbx, .shp, .shp, .shx (standard shapefile suite)

- Data governance and provenance
  - Ownership and responsibility: Staff Responsible—Craig Smeaton; project team includes researchers from University of St Andrews, UK Centre of Ecology and Hydrology, University of Glasgow, University of York, Bangor University.
  - File organization: Datasets embedded in GB_saltmarsh_OC_resources.zip; dataset-specific metadata described in this supporting document.
  - Licensing and access: The document does not specify licensing or access restrictions; Data Stewards should confirm data reuse rights and any embargoes before sharing or redistribution.

- Relevance for Data Stewards
  - Governance fit: The dataset aligns with standards for large, multi-source datasets requiring consistent metadata, provenance tracking, and update mechanisms.
  - Key stewardship actions:
    - Ensure complete metadata: units, methods, data origins, spatial extent, temporal coverage, and licensing.
    - Confirm update cadence and data ingestion processes for future OC updates and new marsh extents.
    - Standardize fields and documentation across shapefiles to support interoperability.
    - Verify data sharing rights, licensing, and repository placement (portal formats, DOIs, or accession IDs).
    - Maintain traceability of data lineage from raw inputs (OC content, density data, DB densities) through to final OC storage maps.
    - Address potential data transfer constraints for large datasets and oversee compatibility across multiple national datasets.

- Challenges to anticipate
  - Incomplete understanding of user needs and priorities.
  - Timeliness of data delivery from contributing sources.
  - Encouraging data creators to provide complete metadata and adhere to standards.
  - Heterogeneous systems and formats across contributing datasets.
  - Handling large, complex datasets and potentially non-interoperable legacy databases.
  - Ensuring updates remain compatible with existing GIS layers and projections.

- References and supporting documentation
  - Environment Agency (England) 2021: Saltmarsh extent and zonation
  - Haynes, T.A. 2016: Scottish saltmarsh survey national report
  - Natural Resources Wales 2016: Saltmarsh extent
  - Ruranska et al. 2020/2022: NERC C-Side surficial soil OC data for English/Welsh and Scottish saltmarshes
  - Miller et al. 2022: Scottish saltmarsh soils physical and geochemical properties

- Project and team credits
  - Project: Carbon Storage in Intertidal Environments (C-SIDE)
  - Funding: NERC (NE/R010846/1)
  - Institutions: University of St Andrews; UK Centre for Ecology and Hydrology; University of Glasgow; Bangor University; University of York
  - Team members include Annette Burden, Paulina Ruranska, Cai J.T. Ladd, Angus Garbutt, Laurence Jones, Lucy McMahon, Lucy C. Miller, David A. Norris, Martin W. Skov, and William E.N. Austin, among others.