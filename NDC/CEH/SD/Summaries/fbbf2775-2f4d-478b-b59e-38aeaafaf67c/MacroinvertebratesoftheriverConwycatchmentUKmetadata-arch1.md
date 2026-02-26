# Macroinvertebrates of the Conwy catchment

- Purpose and scope
  - Species-level descriptions of macroinvertebrate communities from the Conwy catchment, Wales, UK
  - Data collected over three years (2008–2010) with supporting habitat and geographic data

- Data files
  - Macroinvertebrates of the Conwy catchment - taxon data.csv
  - Macroinvertebrates of the Conwy catchment - environmental variables.csv
  - Macroinvertebrates of the Conwy catchment - supporting information.csv

- Sampling design and methods
  - Study area: tributary streams of the Conwy, Wales, UK
  - Sampling periods: November 2008, 2009, 2010
  - Collection method: 1 mm kick net following RIvPACS field protocol
  - Site variables collected: depth, width, velocity, substrate cover, macrophyte cover
  - Sample processing: field preservation in 4% formaldehyde; lab processing included washing through 500 μm sieve and identifying macroinvertebrates to lowest possible taxonomic level (usually species)
  - Taxonomic reference: Davies, Edwards (2011) code list for macroinvertebrates in the British Isles
  - Data validation: crosscheck between laboratory sheets and data printouts
  - Spatial variables: map variables derived using Intelligent River Network (v17)

- Data structure and key variables
  - Taxon dataset:
    - Site code, Year, Sample date
    - Taxon code and Taxon name (per Davies & Edwards 2011)
    - Life stage (L, N/A; Pupa, A, U as applicable)
    - Abundance in sample
  - Environmental variables dataset:
    - Site code, Year
    - Wetted width (m), Depth (cm), Velocity (m/s)
    - % cover of rock pavement; % cover of boulders/cobbles, pebble/gravel, sand/clay (sums to 100%)
    - % cover by macrophytes
  - Supporting information dataset:
    - Site-level metadata: Site name, Easting, Northing, Grid reference
    - Distance from source (km), Altitude (m), Slope (m/km)
    - Stream Strahler order, Upstream catchment area
  - Sample identifiers: unique combination of site code and project year; site codes accompanied by a key in the supporting information

- Site metadata and geography
  - Detailed site-level coordinates and grid references
  - Hydrological context: distance from source, catchment area, Strahler order
  - Physical characteristics: altitude and slope, aiding geographic and environmental analyses

- Taxonomy and data standards
  - Taxon codes/names aligned with Davies & Edwards (2011)
  - Consistent life-stage coding (L, P, A, U)
  - Map variables derived from established river classification methods

- Data quality and provenance
  - Version 1.0 released 28/06/2016
  - Clear attribution of sampling, laboratory analysis, and data management roles
  - Data entry validated against laboratory records

- Analytical potential and applications
  - Multivariate analyses of macroinvertebrate community composition relative to environmental variables
  - Correlation and regression analyses to identify drivers of taxa abundance and diversity
  - Development of predictive models for river condition indicators or habitat quality
  - Data can be shared or published with metadata to improve discoverability and reuse

- Access, reuse, and provenance notes
  - Dataset organized for reuse in ecological and environmental analyses
  - Metadata supports traceability of samples, methods, and site characteristics
  - Grounded in RIvPACS-based sampling with standardized processing and taxonomic references