# The habitat association (phi coefficient of association) of ground beetles (Carabidae) in Great Britain

- Purpose and scope
  - Presents habitat association data (phi coefficient of association) for ground beetles (Carabidae) in Great Britain.
  - Based on 100 m carabid records from the NBN atlas and CEH Land Cover Map 2015 (LCM2015) habitats.
  - Habitats scored for each species from -1 to 1 with accompanying p-values to indicate significance.
  - Provides both weighted and unweighted correlation indices to assess habitat associations, with permutation-based p-values.
  - Aims to inform conservation planning, habitat loss impacts, connectivity, and landscape modelling.

- Outputs and data products
  - Primary outputs: habitat association results for each species, including weighted and unweighted indices.
  - Availability of multiple thresholded versions to gauge confidence:
    - Weighted: carabidae_habitat_associations_weighted14.csv
    - Unweighted: carabidae_habitat_associations_unweighted07.csv, carabidae_habitat_associations_unweighted14.csv, carabidae_habitat_associations_unweighted28.csv, carabidae_habitat_associations_weighted07.csv, carabidae_habitat_associations_weighted28.csv
  - Confidence recommendation: only for species with 50 or more presence records.
  - R package PhiCor (Chetcuti, 2018) available for reproducing similar analyses; related paper: A weighting method to improve habitat association analysis: tested on British carabids (Chetcuti et al., 2019).

- Data sources
  - Carabid presence records: National Biodiversity Network (NBN) atlas (2017), 100 m grid resolution.
  - Taxonomic harmonisation: NHM UK species inventory checklist (Raper 2014) and Luff (2007).
  - Land cover: Land Cover Map 2015 (LCM2015) with 21 habitat classes based on UK Biodiversity Action Plan Broad Habitats.

- Data preparation and habitat representation
  - Presence/absence per 100 m location: created a wide-format dataset with a binary presence indicator for each species at each location.
  - Absence determination: since NBN lacks true absences, absence locations are inferred using a survey effort proxy (presence of at least 14 other carabid species in a location, following a threshold analysis; 14 species chosen as a 5% threshold leading to 556 potential absence grid cells).
  - Habitat data: proportion of each of the 21 LCM2015 habitats within each 100 m location obtained by intersecting LCM2015 polygons with NBN grid cells.

- Correlation indices and methodological approaches (2.1)
  - Unweighted index: for locations with a single habitat only; discard multi-habitat squares to compute presence/absence associations (limitations include data loss).
  - Weighted index: addresses multiple habitats by weighting each location by the proportion of each habitat present; uses a weighted phi formula (Phi^w) that accounts for habitat proportions.
  - Group-equalised version: phi^g_w (group-equalised) to adjust for unequal habitat representation across locations.
  - Statistical inference: both original and uncertainty-weighted indices computed; p-values obtained via permutations (per De Cáceres & Legendre, 2009).

- Data (2.2) and land cover specifics
  - Carabid data (2.2.1)
    - Source: NBN atlas (2017); initial filtering to species with at least 10 records (268 species).
    - Spatial resolution: records mapped to 100 m grid cells.
    - Absence treatment: true absences inferred using the 14-species threshold method; sensitivity analysis performed with different thresholds (7, 14, 28 none).
  - Land cover (2.2.2)
    - LCM2015 provides 21 classes mapped to OS Master Map polygons (random forest classification using Landsat-8 and AWIFS; 30 m and 60 m resolutions).
    - Small polygons (<0.5 ha or <50 m wide) merged into neighbors.
    - Habitats intersected with 100 m NBN squares; calculated proportion of each habitat per location.
    - Preference for keeping the 21-class scheme without further grouping for this analysis.

- Analyses workflow (2.3)
  - Data restructuring: collapsed multiple records per location to a single presence/absence entry per species (wide format) using R.
  - Analysis execution: correlation indices and permutations performed for each species and each method/version; computations conducted on the JASMIN cluster.
  - Output interpretation: results include both original and weighted indices with associated p-values, facilitating assessment of habitat associations for each species.

- Practical considerations for GIS work
  - Texture of outputs: ready-to-use CSVs with habitat association scores and significance, aligned to habitat classes 1–21 from LCM2015.
  - Spatial scale: 100 m grid resolution; integrates species occurrence data with high-resolution land-cover proportions.
  - Data quality and confidence: use of 50+ records recommended; threshold analyses provide a means to gauge robustness across methods.
  - Accessibility: data and analysis framework enable replication via PhiCor and accompanying literature; outputs suitable for map-based visualization and policy-relevant storytelling.

- Context and references
  - Framework and methodology draw on established studies in habitat association analysis and spatial ecology (De Cáceres & Legendre 2009; Hickling et al. 2006; Lonsdorf et al. 2009; Pouzols & Moilanen 2014; Rowland et al. 2017a,b; Chetcuti 2018; Chetcuti, Kunin, & Bullock 2019).

- Summary for GIS workflow
  - Integrate NBN presence data (100 m) with LCM2015 habitat proportions per location.
  - Decide on unweighted vs weighted approach based on data complexity (multi-habitat squares).
  - Compute phi coefficients (Phi^w and phi^g_w) and permutation-based p-values for each species.
  - Use the provided CSVs (weighted/unweighted, with various thresholds) for map-based visualization and decision-support.
  - Leverage PhiCor for reproducibility and to apply similar analyses to other species.