# Natural enemies of crop pests in oilseed rape fields in relation to local plant diversity and landscape characteristics

- Overview
  - Investigates natural enemies of crop pests in winter-sown oilseed rape (Brassica napus) in relation to local plant diversity (in-crop and field margins) and landscape characteristics.
  - Part of the Wessex BESS project; fieldwork conducted in 2014 and 2015 in the Wessex region, southern England (arable/grassland-dominated landscape with remnant calcareous grassland).
  - Data can be used with other Wessex BESS WP4 datasets to explore ecological relationships and drivers of pest control.

- Study scope and location
  - Surveys across the NW to SE extent of the Wessex region; arable-dominated with intensive grassland.
  - Twelve fields surveyed per year; transects and margins sampled to capture habitat structure and plant diversity.

- Landscape characteristics and habitat metrics
  - Derived from GIS-based integration of multiple datasets within 0.5–3 km buffers around sampling points.
  - Datasets and habitat types used:
    - CEH Land Cover Map 2007
    - Natural England Priority Habitats Inventory (PHI)
    - Local National Vegetation Community surveys (NVC)
  - Grassland classification included: species-rich grassland (CG2, CG3, CG6, MG5), intermediate grassland, restored grassland, and improved grassland.
  - Landscape metrics calculated within buffers included: area/amount of grassland (intensive, restored, species-rich), semi-natural habitat, arable area, hedges and margins, and various proximity/distance measures to patches.

- Local scale habitat and plant diversity
  - Field-edge and margin measurements:
    - Field edge length, proportion of hedge and field margin, width of field margin.
  - Margin plant diversity assessed with five 1 m^2 quadrats near the transect start.
  - In-crop plant diversity assessed at sampling points 8 m, 33 m, and 58 m into the crop.
  - Species identification following standard flora references; percent cover recorded.

- Natural enemies and pests sampling
  - Suction sampling (canopy parasitoids): 1 m^2 area sampled for 7 seconds at 8, 33, and 58 m along each transect.
  - Pitfall traps (ground-dwelling enemies): 6 cm diameter traps with ethylene glycol; two 4-day periods per year.
  - Water traps: used to assess pest larvae dropping from the canopy; contents frozen for lab analysis.
  - Key pests targeted: Meligethes spp. (Nitidulidae), Ceutorhynchus spp. (Curculionidae), Dasineura spp. (Cecidomyiidae).
  - Identification and counts:
    - From suction: Hymenoptera parasitica identified to species.
    - From pitfalls: Carabidae, Staphylinidae (excluding Aleocharinae), and adult Araneae identified to species.
    - Pest larvae identified and counted from water traps; parasitoid eggs/ectoparasites noted.
  - Temporal coverage: suction sampling in 2013 and 2014; pitfall and water traps in specified periods (crop growth stage alignment).

- Data structure and content
  - Field data and metadata collected in coordination with the Wessex BESS WP4 framework.
  - Core datasets and linking mechanism:
    - NERCPestNatEnSpeciesList.csv: taxonomic list with species, collection method (Pitfall or Suction), gender (where recorded for Hymenoptera), and a SpeciesCode to link to sample datasets.
    - NERCPitfall.csv: pitfall trap results (SampleCode, SurveyDate, PointCode, etc.) with species counts per trap (5th–312th columns for species counts).
    - NERCSuctionSample.csv: suction sample results (PointCode, SampleCode, etc.) with species counts (columns 2–33).
    - NERCWaterTrap.csv: pest larva counts per water trap (Meligethes, Dasineura, Ceutorhynchus, and parasitism indicators).
    - NERCNatEnLandscapeSurvey.csv: landscape and habitat variables linked to FieldID/FieldCode (e.g., transect data, FarmID, Year, habitat area metrics, plant richness, margins, hedges, and numerous radius-based landscape variables).
  - Variables include detailed habitat metrics (margin width, hedge height, field-edge length), plant richness (margin and in-crop), and extensive landscape buffers (grassland types, restored/restored grassland, semi-natural habitat, arable cover, SppRich, TotAra, SN, IG, Res metrics, and distance-based measures).

- Data quality, ethics, and accessibility
  - Data collection protocols standardized; data entry in MS Access; training provided to field and lab teams.
  - Data quality assurance steps documented; attempts to protect data integrity during capture and entry.
  - Ethics approval obtained from CLES Penryn Research Ethics Committee (application 2014/622).
  - Noted data caveats:
    - Some missing data in pitfall datasets due to field mishaps (e.g., pitfalls knocked over).
    - Field 3.1 had only two transects due to crop failure.
  - Data management emphasizes traceability and potential for public discoverability via metadata.

- Practical use and integration
  - The dataset enables analyses of correlations and potential causal links between natural enemy communities, pest pressure, local plant diversity, and landscape configuration.
  - Designed to be combined with other Wessex BESS WP4 datasets for broader ecosystem-services analyses and to support predictive modeling of natural pest control in agroecosystems.
  - Rich metadata and linking across species, traps, and landscape variables facilitate reproducible analysis and dataset discoverability.