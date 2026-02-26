# Dataset: Zinc tolerance scores for Silene uniflora populations

- scope: Deep water culture experiments conducted 03/2021–09/2021 across 50 Silene uniflora populations to assess zinc tolerance.

- collection/generation methods:
  - cuttings from 50 populations propagated in common conditions
  - growth in diluted Hoagland's solution (pH 5.5) via deep water culture for 4 weeks
  - roots stained with activated charcoal, then transferred to fresh Hoagland's with 1000 μM ZnSO4
  - root growth scored after 48 hours using a 0–2 scale (0 = no growth, 1 = visible growth, 2 = growth with new root length >30% of original)
  - population tolerance levels estimated as the mean score per population

- nature and units of recorded values:
  - for each population: mean zinc tolerance score, standard deviation, and the number of cuttings scored
  - geographic positions of scored populations are recorded and linked to a separate site dataset

- data structure:
  - dataset contains 50 rows (one per population)
  - columns (in order): 
    1) population code (named after local areas/landmarks)
    2) number of cuttings assessed
    3) zinc tolerance score (mean)
    4) standard deviation of the score
  - full names and geolocations are provided in a connected dataset titled "Site records for Silene uniflora"

- quality control:
  - scoring performed by a single author; 10% of scores verified by two other authors

- geospatial context and usability for GIS:
  - populations have geographic positions; to map, join this dataset to the site records dataset for geolocations
  - suitable for creating map-based visualisations of zinc tolerance across geographic distribution (points representing populations)

- considerations for use:
  - data are aggregated at the population level (mean and SD per population) with a single scorer (potential observer bias)
  - sample size per population varies (as indicated by the number of cuttings assessed)
  - ensure proper linkage to the external site records dataset for coordinates and names before GIS analysis