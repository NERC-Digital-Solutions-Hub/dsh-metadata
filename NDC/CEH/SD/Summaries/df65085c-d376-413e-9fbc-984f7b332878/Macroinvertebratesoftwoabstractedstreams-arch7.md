# Macroinvertebrates of two abstracted streams - taxon data.csv

- Purpose and scope
  - A GIS-relevant data package containing species-level macroinvertebrate data from two Lowther catchment streams (Howes Beck and Heltondale Beck), collected upstream and downstream of water abstraction points.
  - Includes supporting habitat and geographic data to enable spatial analysis and mapping.

- Spatial and geographic data
  - Sampling sites located on two tributaries of the Lowther: Howes Beck (Cawdale Beck) and Heltondale Beck.
  - Spatial references and coordinates
    - Provided as OS grid references with corresponding Northings and Eastings for each site.
    - Includes altitude, slope, distance from source, and source height.
  - Habitat and environmental layers
    - Supporting environmental data tables include BGS solid and drift geology codes, NCC geology codes, wetted width, water depth, and habitat assessments.
    - Habitat Quality Assessment (HQA) and Habitat Modification Score (from River Habitat Survey, RHS) and RHS class.
  - Sampling geometry
    - 100 m reaches around abstraction points (50 m upstream and 50 m downstream) within which five riffles were sampled.

- Data structure and key fields
  - Taxon dataset (macroinvertebrates)
    - Columns include: sample identifier, taxon name, taxon code, life stage (L, P, A, U), and abundance per sample (0.0625 m^2 Surber area).
    - Taxa identified to the lowest possible taxonomic level; validated against the Davies & Edwards (2011) code list.
  - Supporting information (environmental)
    - Table entries for each stream/reach with fields such as grid reference, northings/eastings, altitude, slope, distance from source, geology codes (BGS and NCC), width, depth, HQA, HMS, and HMS class.
    - Entries differentiate Howes Beck (DS/US) and Heltondale Beck (DS/US) with corresponding coordinates and environmental attributes.
  - Sample coding
    - Sample codes combine waterbody (HB = Howes Beck, HDB = Heltondale Beck), position relative to abstraction (US, DS), and replicate number (1–5).

- Methods and data quality
  - Field collection
    - Date: 23–24 September 2010.
    - Sampling: five riffles per 100 m reach; Surber sampler (250 μm mesh, 0.0625 m^2) across ~5 cm of substrate, with samples preserved in 4% formaldehyde.
  - Laboratory processing
    - Samples washed and macroinvertebrates identified to species level where possible; taxon names and unique codes sourced from Davies & Edwards (2011).
  - Data validation and provenance
    - Data entry validated by cross-checking printouts with laboratory sheets.
    - Map variables and geography derived using Intelligent River Network (IRN) Version 17 (Dawson et al., 2002).
    - RHS habitat assessments guided by Environment Agency River Habitat Survey manual (2003).

- Usage and GIS applications
  - Integrate the taxon data with spatial attributes (grid references, coordinates, altitude) and habitat/geology attributes for mapping and spatial analysis.
  - Analyze spatial patterns of macroinvertebrate communities in relation to abstraction points, habitat quality, and geological context.
  - Link sample codes to map locations and RHS/HQA classifications for targeted habitat management and policy discussions.

- Accessory information and references
  - Related files: macroinvertebrate taxon data CSV; supporting environmental information table.
  - Foundational references: Davies & Edwards (2011) taxon code list; Dawson et al. (2002) IRN methodology; Environment Agency (2003) RHS manual.
  - Version history: Version 1.0 (21/06/2016) by F. Edwards; 2.0 (22/06/2016) to support information; contributors include sample collection and laboratory analysis teams.