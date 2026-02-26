# Overview

- A multi-component vegetation dataset from 49 plots across 18 sites in Eastern Sabah, Malaysian Borneo, collected July–November 2017.
- Study compares fragmented forest within RSPO-certified oil palm plantations (14 sites) with a large continuous forest tract (4 sites) to assess vegetation structure, biodiversity, and habitat context.
- Data cover living trees/palms, lianas, coarse woody debris (CWD), ground vegetation, soil characteristics, and site/landscape habitat metrics.
- Data are organized into six CSV files: CWD.csv, lianas.csv, seedlings_groundveg.csv, sites_habitat.csv, soil.csv, trees.csv.

## Data scope and structure

- Focus areas
  - Ground vegetation, tree seedlings, saplings, adult trees and palms
  - Lianas and coarse woody debris
  - Habitat, topography, and landscape context for each plot
- Data organization
  - Six CSV files containing mutually referable data:
    - CWD.csv: coarse woody debris measurements (size, decay, dimensions, type)
    - lianas.csv: liana measurements (dbh, associated tree, linkage to tree)
    - seedlings_groundveg.csv: morphospecies, counts, ground cover, native/exotic status
    - sites_habitat.csv: plot-level metadata, location, fragmentation status, forest type, disturbance, edge metrics, and landscape buffers
    - soil.csv: soil chemistry and moisture (pH, P, N, C, moisture)
    - trees.csv: individual tree stems, dbh, height (where measured), species or genus, lianas count, and subplot context
- Data units and measurement notes
  - Tree and liana dbh in cm; height by eye for most stems, with a subset measured by clinometer
  - CWD: diameter at ends or stump top, length/height, decay class (1–5)
  - Ground vegetation: morphospecies codes, native/exotic status, life form, voucher status
  - Soil: pH, TP, AvP, TN, TC, OC, C:N ratios, moisture (%)
  - Habitat metrics include leaf litter depth, forest cover by densiometer (to be converted to canopy cover as 100 – (Forest_cover readings × 1.04))
- Data links and keys
  - Site-level and plot-level linkage across files primarily via Site_name, Site_plot_code, Plot_no, and Date
  - Lianas are linked to trees via Tree_individual_no (Tree_ID and Tree_individual_no in trees.csv and lianas.csv)

## Study design and sampling design

- Sites and fragmentation
  - 18 study sites total: 14 fragmented forest set-asides within RSPO-certified oil palm plantations; 4 continuous forest sites for comparison
  - Fragmented sites represent a range of fragmentation, time since fragmentation, and forest structure
  - Continuous forest sites include fully protected primary forest and selectively logged variants
- Plot and transect design
  - 49 circular plots of 30 m radius (0.28 ha) across 18 sites
  - Fragmented sites: 2–3 plots per site, with edge-adjacent placement to capture edge effects
  - Continuous forest sites: plots arranged to capture interior forest structure
  - Plot spacing: 100 m apart (where feasible), with boundaries ≥25 m from forest edge
  - Five nested sampling radii:
    - Main plot: 30 m radius for mature trees ≥25 cm dbh and CWD ≥25 cm
    - 20 m radius subplot for trees 10–25 cm dbh and CWD 10–25 cm
    - 5 m radius subplot for trees 2–10 cm dbh
  - Ground vegetation sampled with eight 1x1 m quadrats per plot, located 25 m from plot center along random bearings
- Fragmentation context metrics
  - Landscape-scale metrics derived from UAV imagery and Google Earth data: forest area and edge index within 0.1–2 km buffers, distance to nearest forest–oil palm edge, and years since fragmentation
  - Parallel forest-area/edge metrics provided for continuous-forest plots for comparability

## Dataset-by-dataset highlights for governance and data use

- CWD.csv
  - Item-level records for coarse woody debris (≥10 cm diameter)
  - Fields include Site_name, Plot_no, Site_plot_code, Date, Dbh_1_cm, Dbh_2_cm, Type (F/S/H), Decay (1–5), Length_m, and Subplot_radius_m
  - Useful for carbon stock and wood decomposition analyses; note boundary-crossing items captured up to their boundary
- lianas.csv
  - Individual lianas entering the crown of recorded trees ≥10 cm dbh
  - Linked to tree by Tree_individual_no; includes Tree_ID, Tree_dbh_cm, Tree_height_m, and Liana_dbh_cm
  - Not identified to species; exclude from biodiversity analyses or treat as genus-level where appropriate
- seedlings_groundveg.csv
  - Ground vegetation morphospecies data across eight 1x1 m quadrats per plot
  - Includes morphospecies codes, N_individuals_present, Ground_cover_perc, exotic/native status, life form, and voucher/identification details
  - Taxonomic resolution varies (some to genus/family; some Unknown); identify which units are suitable for biodiversity analyses
- sites_habitat.csv
  - Plot-level spatial and ecological metadata
  - Coordinates (Latitude/Longitude), Elevation, First_plants_nearest_OP, Replanting_nearest_OP, Years_since_frag, Forest_type, Fragment status, Survey_date
  - Extensive landscape-context fields: ForeArea_buffer_X m, ForEdge_buffer_X m_ncells, ForEdge_buffer_X m_index, Nearest_edge_m
  - Leaf litter depth and forest cover readings (x-direction) are included for canopy estimates
  - Slopes in four directions (N, E, S, W)
- soil.csv
  - Plot-level soil chemistry and moisture: pH, TP_ppm, AvP_ppm, TN_perc, TC_perc, OC_perc, CtoN_totC, moisture_perc, CtoN_orgC
- trees.csv
  - Individual tree stems with site/plot identifiers, Date, Individual_code, ID (species/genus; Palm or UNKNOWN), Dbh_cm, Height_m, N_lianas
  - Subplot_radius_m indicates the sampling context for each stem
  - Includes notes on tree attributes and liana associations; distance/degrees not universally available

## Data quality, processing, and usage notes

- Height estimation and modeling
  - Height data include both eye estimates and a subset measured with clinometer; recommended approach is to build a height–dbh model using stems with reliable height data and exclude irregular stems (e.g., multi-stemmed or leaning trees) when fitting the model
  - For stems without Degrees_to_base, height is computed as eye-level height to crown top plus 1.5 m
- Canopy/forest cover calculation
  - Canopy cover: canopy (%) = 100 − (Forest_cover_readings × 1.04)
- Biodiversity analyses caveats
  - Palms and lianas are not identified to species and should be excluded from biodiversity or community analyses that require species-level data
  - Ground vegetation morphospecies may be unidentified (Unknown or Genus x), which affects species-level biodiversity metrics
- Data fidelity and provenance
  - Field data collected by a single observer for certain variables to ensure consistency
  - Some measurements were taken on multiple dates per plot; use the precise dates in the corresponding vegetation datasets for temporal alignment
- Data interoperability and governance considerations
  - Relationships across files rely on consistent site/plot codes (Site_name, Site_plot_code, Plot_no)
  - Several derived metrics (e.g., forest-edge indices, buffer-area metrics) require careful replication to ensure comparability across studies
  - The dataset integrates ecological measurements with landscape context, enabling cross-scale analysis but requiring careful handling of differing spatial resolutions

## Governance, sharing, and stewardship considerations

- Data standards and interoperability
  - Six CSV files with clear field definitions; ensure consistent data typing and key fields (Site_name, Site_plot_code, Plot_no)
  - Maintain links between trees, lianas, and CWD via identifiers (Individual_code, Tree_individual_no)
- Metadata and documentation
  - Field methods, measurement protocols, and decays are documented; reference provided sources for height estimation, CWD decay classes, and ground vegetation identification
  - Document any deviations or data quality issues (missing values, unidentified taxa) when sharing or integrating with other datasets
- Data quality assurance
  - Preserve original field coding and units; provide translation maps if integrating with other datasets
  - Include notes on which datasets exclude certain taxa (palms, lianas) for biodiversity analyses
- Access, citation, and reuse
  - Data are organized for reuse in carbon stock assessments, fragmentation studies, and biodiversity analyses, with explicit caveats
  - Proper attribution to the study and the cited references is required
- Update and maintenance
  - The data reflect fieldwork from 2017; consider versioning if updates or corrections are made or if additional datasets are added

## Practical guidance for data stewards and analysts

- How to join datasets
  - Use Site_name, Site_plot_code, and Plot_no to link site-level metadata (sites_habitat.csv) with plot-level measurements (soil.csv, trees.csv, CWD.csv, lianas.csv, seedlings_groundveg.csv)
  - Use Date fields to align measurements across datasets or to filter by sampling date
- Recommended analyses
  - Compare structural attributes and species diversity between fragmented vs continuous forests, accounting for edge distance and fragmentation metrics
  - Analyze relationships between soil properties and aboveground biomass or CWD accumulation
  - Assess liana load in relation to tree dbh and the associated tree health; use Tree_individual_no to connect lianas to their host trees
  - Use canopy estimates derived from densiometer readings for habitat structure analyses
- Cautions
  - Treat lianas and palms as non-identifiable for species-level biodiversity metrics
  - Be mindful of NA values and date discrepancies when merging across datasets
  - Validate height models if used for biomass estimations, omitting irregular stems as recommended

This summary highlights the data's scope, structure, and governance implications from a Data Steward perspective, emphasizing interoperability, metadata clarity, data quality, and appropriate use.