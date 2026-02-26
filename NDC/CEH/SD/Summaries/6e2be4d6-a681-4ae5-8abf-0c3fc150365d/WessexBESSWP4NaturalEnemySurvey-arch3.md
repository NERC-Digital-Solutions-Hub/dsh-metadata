# Natural enemies of crop pests in oilseed rape fields in relation to local plant diversity and landscape characteristics

## Overview
- A dataset examining how natural enemies of crop pests in winter-sown oilseed rape relate to local plant diversity in fields and margins, plus surrounding landscape characteristics.
- Part of the Wessex BESS project, funded by NERC; designed to inform monitoring of biocontrol and biodiversity in agricultural landscapes.

## Study area and time frame
- Location: Wessex region, southern England (arable and intensive grassland with remnant calcareous grassland).
- Field surveys conducted in 2013 and 2014 across 12 fields per year.
- Field and landscape context derived from GIS and national/local vegetation datasets.

## Data collected and measures
- Natural enemies and pests
  - Parasitoids and predatory beetles collected via suction sampling (area ~1 m^2, 7 seconds) and pitfall traps (6 cm diameter, 50% ethylene glycol).
  - Key pest larvae counted from water traps (Meligethes spp., Ceutorhynchus spp., Dasineura spp.).
  - Specimens identified to species for key groups; parasitoids and pest counts recorded.
- Local plant diversity
  - Field margins and crop edges surveyed with quadrats (1 m^2) for plant species richness and percent cover.
  - Margin structure metrics: hedge proportion, field margin width, margin length.
- Landscape characteristics
  - Ground-truth and GIS-derived metrics within buffers of 0.5–3 km around sampling points, including:
    - Grassland area and type (species-rich, restoring, semi-natural, semi-improved, improved).
    - Proportions of arable land and semi-natural habitats.
    - Distances and areas for intensive grassland, restored grassland, and species-rich grassland patches.
  - Specific metrics include IG (intensive grassland), Res (restored grassland), SppRich (species-rich grassland) and related area/distance measures at multiple radii.

## Sampling design and protocols
- Field layout
  - Three 58 m transects per field, including hedged and non-hedged edges; margins sampled near transects.
  - Plant diversity and habitat features measured along transects and in margins.
- Temporal window
  - Suction sampling conducted June–July in 2013 and May–June in 2014.
  - Pitfall traps deployed during two 4-day periods in each year.
  - Water traps deployed concurrently to assess pest larvae drop from the canopy.
- Data handling
  - Specimens frozen prior to lab analysis; identification followed taxonomic references.
  - Data entered in MS Access with procedures to check for anomalies.

## Taxonomic and data linking
- Species-level identifications for key parasitoids and predatory groups; multiple CSVs linked via:
  - SpeciesCode in NERCPestNatEnSpeciesList.csv to NERCPitfall.csv and NERCSuctionSample.csv.
  - SampleCode and PointCode for linking pitfall, suction, water trap, and landscape data (NERCNatEnLandscapeSurvey.csv).

## Data quality assurance
- Standardized collection and lab protocols; trained personnel; data validation and cleaning procedures documented.
- Ethics approval obtained from the University of Exeter Penryn Research Ethics Committee.

## Data files and structure
- NERCPestNatEnSpeciesList.csv
  - Taxonomic details, species codes, collection method, gender data (limited to Hymenoptera).
- NERCPitfall.csv
  - Pitfall sample metadata and counts by species; notes on missing data due to field losses.
- NERCSuctionSample.csv
  - Suction sample metadata and counts by species; notes on missing transects.
- NERCWaterTrap.csv
  - Water trap data with counts for targeted pest larvae and parasitized instances; linked to species list.
- NERCNatEnLandscapeSurvey.csv
  - Landscape context data per field/point, including transect, farm, field IDs, year, and numerous habitat/land-use metrics.

## Data quality notes and limitations
- Some missing data in pitfall (knocked over traps) and field 3.1 transects due to crop failure.
- Gender data only recorded for Hymenoptera; other groups lack gender metadata.
- Some fields and columns contain missing or categorical data that require careful handling during analysis.

## Relevance for monitoring frameworks
- Provides standardized, multi-scale indicators linking natural enemy assemblages and pest pressures to local plant diversity and landscape context.
- Enables evaluation of habitat features (hedges, field margins, grassland patches) on biological control services.
- Supports policy-relevant monitoring of biodiversity-friendly farming practices and landscape-scale pest management.
- Data governance considerations include linking datasets, metadata completeness, and transparency about missing data and collection limitations.

## References
- Ferguson et al. 2010; Joy 1932; Lott 2009; Lott & Anderson 2011; Luff 2007; Morton et al. 2011; Roberts 1993; Rodwell 1992; Stace 1997; Toynton & Ash 2002; Walker & Pywell 2000.