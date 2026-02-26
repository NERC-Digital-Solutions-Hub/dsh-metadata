# Supporting information for Pescott, O., Peyton, J., Mountford, J., Onete, M., Martinou, A. (2017). Non-native plant species GIS data from Cyprus Sovereign Base Areas, October 2015 and March 2017. NERC Environmental Information Data Centre. http://doi.org/10.5285/7c84e06d-bb1a-4aac-b1d7-33c11310d8a0

- Purpose and scope
  - Provides supporting information for GIS data on non-native plant species in the Cyprus Sovereign Base Areas (SBA), collected in October 2015 and March 2017.
  - Includes field methods, data structure, quality control, and project context; quadrat data to be archived separately on GBIF and linked to a Biodiversity Data Journal (BDJ) paper in prep.

- Field sampling and focus species
  - 2015 (Akrotiri, western SBA): mapping of woody non-natives and target notes; main species include Acacia saligna, Casuarina cunninghamiana, Eucalyptus camaldulensis, E. gomphocephala, and Symphyotrichum squamatum; quadrat data collected but stored separately.
  - 2017 (Akrotiri and Dhekelia, western and eastern SBA): emphasis on quadrat recording; additional Oxalis pes-caprae stands mapped in Dhekelia.
  - Field teams: OLP, JP, MO, JOM; AFM assisted with access and project management.

- Fieldwork instrumentation and data capture
  - Equipment: ruggedised Panasonic FZ-G1 Toughpad tablets with ArcPad v10.2.
  - Mapping approach: GPS tablet-based mapping with satellite photography base maps; typical positional accuracy ~10–15 m (variable with forest canopy).

- Data products and structure
  - Shapefiles created (temporal groups):
    - 2015: Acacia_saligna_EIDC.shp, Eucalyptus_spp_areas_EIDC.shp, Mixed_species_areas_EIDC.shp, Symphyotrichum_squamatum_EIDC.shp, Target_notes_EIDC.shp
    - 2017: Acacia_saligna_2017_EIDC.shp, Oxalis_pes-caprae_2017_EIDC.shp, Target_notes_2017_EIDC.shp
  - Attribute structure (Tables 1 and 2 descriptions):
    - IAS: Invasive Alien Species name (pre-set); notes that some species (e.g., Eucalyptus) may not be invasive in this context.
    - NOTES: Free-text field for field observations.
    - [SPECIES]_ID: Identifier for stand number.
    - TARGET_NOTES: Free-text notes; 2017 target notes prefixed with “17t” to separate from quadrat data.
  - Data integration note: Quadrat data will be archived on GBIF and linked to the BDJ paper; quadrat and stand data were recorded with pre-set forms that influenced the organization of categories (e.g., “mixed” stands).

- Temporal coverage and data creation dates
  - 2015 data: 10/10/2015 – 24/10/2015
  - 2017 data: 04/03/2017 – 18/03/2017
  - File naming reflects collection date and data type (e.g., …2017_EIDC.shp).

- Projection and coordinate reference
  - Data are in the ETRS89 / ETRS-LAEA European grid (EPSG:3035).
  - Proj4 string provided for reproduction: +proj=laea +lat_0=52 +lon_0=10 +x_0=4321000 +y_0=3210000 +ellps=GRS80 +units=m +no_defs

- Data quality control and validation
  - Species determinations cross-checked against standard floras (Meikle, etc.) and field specimens.
  - Collaborative verification across team members (OLP, JP, MO, JOM) to harmonize identifications.
  - Consultation with local experts (e.g., G. Hadjikyriakou) for confirmation of non-native species origins and classifications.

- Additional context and references
  - Related works and forthcoming publications (BDJ paper in prep; costs-action SSC missions; regional flora references).
  - Acknowledges funding and support from COST Action TD1209 Alien Challenge and NERC CEH. 

- Usage notes and future data access
  - The main dataset files are intended to be used alongside the quadrat data to enable broader analyses of non-native plant distributions in Cyprus SBA.
  - Quadrat data and broader context are planned to be published in BDJ and archived on GBIF for public access and reuse.