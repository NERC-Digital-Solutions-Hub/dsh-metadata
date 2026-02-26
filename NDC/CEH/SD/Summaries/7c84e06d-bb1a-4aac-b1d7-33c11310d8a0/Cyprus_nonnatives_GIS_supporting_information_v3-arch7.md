# Supporting information for 'Non-native plant species GIS data from Cyprus Sovereign Base Areas, October 2015 and March 2017'

- Purpose and scope
  - Supporting information for the GIS data on non-native plant species in the Cyprus Sovereign Base Areas (SBAs), covering October 2015 and March 2017 fieldwork.
  - Focuses on woody non-natives Acacia saligna, Casuarina cunninghamiana, Eucalyptus camaldulensis, E. gomphocephala, and the forb Symphyotrichum squamatum; additional species notes and quadrat data are referenced for linking with broader datasets (GBIF and a Biodiversity Data Journal paper in preparation).

- Field sampling and methodology
  - 2015 (Akrotiri, western SBA): stands mapped and stood as polygons using GPS tablet-based mapping with ArcPad; orientation aided by satellite imagery; project managed by AFM.
  - 2017 (Akrotiri, Dhekelia, western and eastern SBA): quadrat-focused fieldwork; small number of stand maps and target notes archived; Oxalis pes-caprae mapped in Dhekelia during this visit.
  - Instruments: ruggedised tablets (Panasonic FZ-G1 Toughpad) with ArcPad v10.2; typical positional accuracy ~10–15 m (decreases under forest canopy).
  - Documentation: field notes accompany polygons; target notes recorded and archived; quadrat data to be archived on GBIF and linked with a BDJ paper.

- Data products and formats
  - Shapefiles created:
    - Acacia_saligna_EIDC.shp
    - Eucalyptus_spp_areas_EIDC.shp
    - Mixed_species_areas_EIDC.shp
    - Symphyotrichum_squamatum_EIDC.shp
    - Acacia_saligna_2017_EIDC.shp
    - Oxalis_pes-caprae_2017_EIDC.shp
    - Target_notes_EIDC.shp
    - Target_notes_2017_EIDC.shp
  - Data structure details (Tables 1 and 2):
    - Table 1: Attribute fields include IAS (invasive alien species name), NOTES (free-text observations), and [SPECIES]_ID (stand identifier).
    - Table 2: NOTES field for free-text observations; 2017 target notes prefixed with “17t” to separate from quadrat data.
  - Data categorization nuances:
    - Casuarina cunninghamiana included under a “mixed species” category due to field-recorded mixtures.
    - Eucalyptus spp. grouped together in some mappings because young individuals and mixtures make species-level separation difficult at mapping scale.
    - Field notes within polygon attributes provide additional composition details.

- Spatial reference and data provenance
  - Projection: ETRS89 / ETRS-LAEA Europe (EPSG:3035).
  - Proj4 string: +proj=laea +lat_0=52 +lon_0=10 +x_0=4321000 +y_0=3210000 +ellps=GRS80 +units=m +no_defs
  - Data collected in two periods: 2015 and 2017, with files dated accordingly.

- Temporal coverage
  - 2015 data collection: 10/10/2015 – 24/10/2015
  - 2017 data collection: 04/03/2017 – 18/03/2017
  - 2017 notes include a small set of Oxalis pes-caprae stands mapped in the Dhekelia base.

- Quality control and validation
  - Species determinations cross-checked against floras (e.g., Meikle references) and corroborated in the field with specimens.
  - Collaborative verification among researchers; consultation with local experts (e.g., G. Hadjikyriakou) to confirm identifications of non-native species planted for forestry (e.g., Casuarina).
  - Some updates to determinations in the archived shapefiles following additional study and fieldwork.

- Related information and references
  - A forthcoming Biodiversity Data Journal data paper will accompany quadrat data and link to the BDJ discussion.
  - References include Hadjikyriakou & Hadjisterkotis (2002), Meikle (1977, 1985), and related COST Action and RIS-Ký project materials.
  - Acknowledged funding from COST Action TD1209 Alien Challenge and NERC CEH support.

- Access and acknowledgments
  - Data are archived in the NERC Environmental Information Data Centre.
  - Acknowledgements note STSM funding and participation by project team members.