# Plants, carabid beetles and birds in native reforestation sites in the Scottish Highlands

- Context and aim
  - Investigates biodiversity value of fenced native reforestation sites in the central Scottish Highlands (Glen Affric and Glen Moriston) compared with unforested grazed and ungrazed areas, and with mature Caledonian pineforest.
  - Focuses on plants, carabid beetles (ground beetles), and birds to assess habitat restoration progress and biodiversity value relative to target habitat and prior land use.
  - Context: high historical deforestation and deer grazing pressure impede natural forest regeneration; restoring priority habitats like Caledonian Pineforest is a priority.

- Study area and design
  - Location: fourteen fenced reforestation sites established between 1990 and 2012 in Glen Affric and Glen Moriston; sites include adjacent unforested areas and, at three sites, associated mature forest.
  - Grazing treatment: fenced to exclude grazing (mainly deer); some sites have residual grazing; mature forest plots included where present.
  - Experimental structure: hierarchical design with treatments representing forest status (reforestation, unforested, mature) and grazing status (grazed, ungrazed) across plots; reforestation × grazed combination not present due to deer pressure.
  - Plot structure:
    - Plants and carabids surveyed in 10 × 10 m plots.
    - Birds surveyed in 50 m radius plots.
    - Bird surveys conducted on a subset of 10 of the 14 reforestation sites; mature forest plots included at two sites (in two grazed/ungrazed pairs per site, totaling five mature forest plots).
  - Sampling cadence:
    - Plant and carabid data collected in summer 2018.
    - Bird data collected in summer 2019.

- Data collection methods
  - Plant surveys
    - Timing: 22 June – 5 July 2018.
    - Method: three randomly placed 1 × 1 m quadrats per plot; percent cover using the DOMIN scale; full plot-level species list recorded.
    - Identification: vascular plants to species; non-vascular to genus or morphospecies; some mosses identified to morphospecies.
  - Carabid beetle surveys
    - Timing: 7 June – 18 August 2018.
    - Method: six pitfall traps per plot (two traps per plant quadrat); traps filled with propylene glycol/water; monitored and emptied at regular intervals; specimens identified to species level.
    - Voucher specimens deposited in Oxford University Museum of Natural History.
  - Bird surveys
    - Timing: two surveys per plot during late May to mid-June 2019.
    - Method: 15-minute surveys conducted by two observers (covering ~50% of the plot each); birds identified visually or by song/call; weather conditions noted.
    - Distance from plot center recorded for each sighting; some plots not surveyed due to logistical constraints.

- Data structure and contents
  - plot_locations files
    - plant_carabid_plot_locations.csv: locations and metadata for the 10 × 10 m plant/carabid plots; includes site, plot type, forest and grazing status, year established, grid references, and pitfall dates.
    - bird_plot_locations.csv: locations and metadata for the 50 m radius bird plots; includes site, plot type, forest and grazing status, year, grid references, and weather notes for each survey.
  - species data files
    - plants.csv: plant species presence/cover data per plot and per 1 × 1 m quadrat; includes DOMIN percentage, presence of additional species, and seedling frequency.
    - carabids.csv: carabid species frequencies per plot across sampling times.
    - birds.csv: bird species frequencies per plot; each row represents a sighting with date, time, distance from plot center, how recorded, and species name.
  - Data quality and provenance
    - Identifications aligned with standard references cited in the study.
    - Weather notes collected for bird surveys; dates and sampling times recorded for plants and carabids.
    - Data files include unique identifiers, site/plot mappings, and sampling dates to enable reproducibility and cross-site comparisons.

- Site details and context
  - The study spans multiple fenced reforestation sites in two Glenes of the Scottish Highlands; detailed site information includes years established, number of trees planted, planting methods, and whether mature forest is present at each site.
  - Table 2 (referenced) provides site-specific data such as size, planting method, and mature forest status; a mix of sites with natural regeneration and varied tree species (including Scots Pine, broadleaf species, aspen, birch, willow, alder) are represented.
  - Notable sites include Coille Ruigh and Ghubhais (with mature forest present), and several other sites established in the 1990s and early 2000s.

- Data use, purpose, and potential
  - Enables evaluation of biodiversity responses across habitat statuses (reforestation, unforested, mature) and grazing regimes (grazed vs ungrazed).
  - Facilitates comparisons with the nearby target habitat (Caledonian Pineforest) and prior land uses, helping to assess restoration value and guide future management decisions.
  - Provides a structured, queryable data framework for meta-analyses and cross-network collaboration within the wider data community studying forest regeneration and biodiversity restoration.

- Access, governance, and provenance notes
  - Data collected 2018–2019; plant and carabid data from 2018, bird data from 2019.
  - Voucher specimens for carabids deposited in the Oxford University Museum of Natural History.
  - Appendix details roles of authors responsible for experimental design, field data collection, and background information.