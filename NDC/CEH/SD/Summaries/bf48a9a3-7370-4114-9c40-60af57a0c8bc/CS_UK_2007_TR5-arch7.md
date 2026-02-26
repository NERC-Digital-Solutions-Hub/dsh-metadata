# Countryside Survey 2007 Headwaters and Pond Condition Survey Manual

- Purpose and scope
  - National freshwater survey (CS2007) aiming to re-survey headwaters in 425 CS2000 squares and assess ponds in 629 CS squares.
  - Integrated data collection for macroinvertebrates (RIVPACS), aquatic plants (MTR/IRIS), water chemistry, and River Habitat Survey (RHS).

- GIS-relevant spatial framework
  - Sampling units and extents defined for mapping and GIS integration:
    - Headwaters: 500 m stream stretches per site; RHS focused 500 m length centered on macroinvertebrate site.
    - Ponds: survey pond identified within each square; 100 m macrophyte survey around macroinvertebrate site; pond boundary, area, drawdown, and inflows/outflows recorded.
  - Precise geolocations and site identifiers:
    - GPS/NGR coordinates; CS square numbers; pond and macroinvertebrate sampling points tracked for relocation.
  - Photographs and relocation aids:
    - Marker boards and site photos used to re-locate in future surveys.

- Data capture and workflow (GIS-centric)
  - Tablet-based field data entry systems:
    - RHS data entered in RAPID (River Habitat Survey) to minimize transcription errors; validation on site.
    - Aquatic plant data entered in IRIS (aquatic plant survey).
  - Standardized data models and drop-down menus to ensure consistent coding (reduces free text errors for GIS-ready databases).
  - Data flows:
    - Macroinvertebrate, plant, RHS, and water chemistry data compiled in central CEH databases; samples transported with traceable labeling (TREM cards) and stored for processing.

- Headwaters survey design and data components
  - Sampling design
    - 425 old squares re-surveyed; 25 new headwater sites within 425 squares for a more focused headwater coverage.
    - For each headwater square: macroinvertebrate sampling point, water chemistry, RHS site environmental data, 500 m sampling length; 50 m upstream/downstream plant survey embedded in the macroinvertebrate reach.
  - Data collected at each headwater site
    - Macroinvertebrate community (RIVPACS protocol) and environmental variables (RHS data integrated with RAPID).
    - Water chemistry: pH, conductivity; SRP, TON, alkalinity from filtered samples.
    - Photography for relocation and habitat context.

- River Habitat Survey (RHS) specifics (GIS-ready aspects)
  - 2003 RHS protocol adopted; data captured in RAPID with on-site validation.
  - 500 m RHS reach linked to the macroinvertebrate site; spot-checks (1, 6, and 10) with GPS checks.
  - Data capture sections cover field survey details, valley form, number of riffles/pools, artificial features, physical attributes, bank top vegetation, channel vegetation, substrate, shading, and water clarity.
  - Output-ready data includes spatially-referenced RHS attributes (habitat types, substrate composition, shading, etc.) for GIS analysis.

- Aquatic macrophyte survey (MTR) and plant data management
  - 100 m macrophyte survey length centered on macroinvertebrate site; walk/wade transect with grapnel sampling for submerged plants where needed.
  - Plant identification to species level where possible; representative samples collected for laboratory confirmation; rare species flagged for expert confirmation.
  - Data management via IRIS:
    - Species lists, abundance (dominant to rare) on a 9-point cover scale; total submerged/floating/emergent cover totals.
    - Specimens and vouchers managed with standardized labeling to link back to the MTR survey.
  - Output-ready plant data supports GIS layers of macrophyte presence/absence and cover by habitat type.

- Pond condition survey (Pond Mapping and Condition)
  - Mapping phase: ponds identified and boundary delineated; area estimated; outer boundary defined by maximum winter water level.
  - Condition survey steps (if water present):
    - Water turbidity estimate; water chemistry sample collected with SRP/TON/alkalinity filtered sample.
    - Environmental survey including amenity use; macrophyte survey (100 m reach) and RHS/Macrophyte data (where applicable).
  - Data capture forms:
    - CS2007 Pond Condition Survey Recording Sheets cover water quality, environmental survey, and macrophyte survey.
    - Spatial data (pond location, boundary, transects) integrated for GIS mapping.
  - Data products and storage:
    - Samples and fieldsheets dispatched to Pond Conservation; photographs captured with pond square identifiers.

- Quality control, safety, and data integrity
  - Certifications and training: RHS, macroinvertebrate sampling, MTR plant surveying; regular team rotation to maintain consistency.
  - On-site validation: RAPID and IRIS validations check for missing data, with stepwise error correction.
  - Audits: ~7% of headwater sites audited by CEH staff; field-safety guidance for ponds and headwaters.

- Practical GIS implications and data products
  - Rich geospatial dataset enabling mapping of:
    - 500 m RHS hydromorphology and habitat diversity along headwater reaches.
    - Macroinvertebrate richness and RIVPACS-derived site quality indicators.
    - Macrophyte assemblages (100 m MTR surveys) mapped by species and cover.
    - Pond boundaries, area, drawdown, sediment composition, inflows/outflows, and land-use context.
    - Water chemistry layers (pH, conductivity, SRP/TON/alkalinity) linked to sampling points.
  - Integrated data pipelines support spatial analyses, change detection across CS2000 to CS2007, habitat suitability mapping, and policy-relevant GIS products for freshwater management.

- References and supporting materials
  - References to Environment Agency RHS guidance (2003), MTR/Macrophyte manuals, and Murray-Bligh/Stewart protocols.
  - Field data entry tools (RAPID for RHS, IRIS for plants) and transport/logistics procedures for sample handling.

- End-user outcomes
  - GIS-ready, standardized, geo-referenced datasets across macroinvertebrates, hydromorphology, macrophytes, ponds, and water chemistry.
  - Robust documentation and relocation aids (maps, photographs, site boards) to enable reproducible, repeatable spatial analyses and policy-informed decision-making.