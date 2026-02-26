# Non-native plant species GIS data from Cyprus Sovereign Base Areas, October 2015 and March 2017

- This document describes GIS shapefiles and supporting information for non-native plant species in the Cyprus Sovereign Base Areas (SBA), collected in October 2015 (Akrotiri) and March 2017 (Akrotiri and Dhekelia).
- Primary focus: woody non-natives Acacia saligna, Casuarina cunninghamiana, Eucalyptus camaldulensis, E. gomphocephala, and the forb Symphyotrichum squamatum; additional notes include Oxalis pes-caprae observed in 2017.

Sampling and fieldwork
- 2015 (Akrotiri, western SBA): stands mapped using GPS tablet-based mapping with ArcPad; target notes recorded; quadrat recording also conducted; main study area bounded by Akrotiri-Kolossi road, Akrotiri forest, Mediterranean Sea, and Akrotiri-Lady’s Mile Beach road.
- 2017 (Akrotiri and Dhekelia): quadrat-focused fieldwork; continued mapping with GPS tablets; Oxalis pes-caprae included in Dhekelia.
- Field personnel included OLP, JP, MO, JOM; AFM facilitated access and project management.
- Instrumentation: ruggedised tablets (Panasonic FZ-G1 Toughpad) with ArcPad v10.2; typical data capture accuracy ~10–15 m depending on canopy.

Data structure and files
- Shapefiles created (temporal coverage 2015 and 2017):
  - Acacia_saligna_EIDC.shp
  - Eucalyptus_spp_areas_EIDC.shp
  - Mixed_species_areas_EIDC.shp
  - Symphyotrichum_squamatum_EIDC.shp
  - Acacia_saligna_2017_EIDC.shp
  - Oxalis_pes-caprae_2017_EIDC.shp
  - Target_notes_EIDC.shp
  - Target_notes_2017_EIDC.shp
- Attribute structure (Tables 1 and 2 in the document):
  - IAS: Invasive alien species name (pre-set in ArcPad form)
  - NOTES: Free text field for observations
  - [SPECIES]_ID: stand identifier
  - Target_notes: free text notes (2017 notes prefixed with 17t to separate from location data)
- 2015 data: main categories include Acacia saligna, Eucalyptus spp., Casuarina cunninghamiana (recorded within “mixed species” when mixed with other taxa); 2017 data added Oxalis pes-caprae observations and continued target notes.
- Data quality and species determinations:
  - Cross-checked against standard floras (Meikle, etc.) and specimens.
  - Consultations with local experts (e.g., G. Hadjikyriakou) to confirm identifications, particularly forestry-planted Casuarina stands.

Spatial, temporal, and projection details
- Temporal coverage:
  - 10–24 October 2015 ( Acacia_saligna_EIDC.shp, Eucalyptus_spp_areas_EIDC.shp, Mixed_species_areas_EIDC.shp, Symphyotrichum_squamatum_EIDC.shp, Target_notes_EIDC.shp)
  - 4–18 March 2017 (Acacia_saligna_2017_EIDC.shp, Oxalis_pes-caprae_2017_EIDC.shp, Target_notes_2017_EIDC.shp)
- Projection: Shapefiles use ETRS89 / ETRS-LAEA European grid (EPSG:3035); Proj4 string provided in the documentation.
- Data scope: mapping areas defined around Akrotiri and Dhekelia within the western and eastern SBA boundaries; 2015 mapping focused on stands and broad composition, 2017 emphasized quadrats and targeted notes.

Quality control and provenance
- Species identifications validated against floras and specimen checks; collaboration with local experts to confirm planted forestry species identifications (e.g., Casuarina).
- Notes acknowledge some taxonomic simplifications (e.g., grouping Eucalyptus spp. in a single category due to difficulty distinguishing young plants).

Access, related resources, and acknowledgements
- Supporting information linked to the NERC Environmental Information Data Centre (EIDC) with a DOI.
- Quadrats and related data to be archived on GBIF and linked to a Biodiversity Data Journal (BDJ) paper in preparation.
- Acknowledgements include COST Action TD1209 Alien Challenge funding and support from CEH Wallingford.

Potential uses for analysts
- Combine these GIS layers with land-use, biodiversity, or invasion risk datasets to assess spread patterns, habitat associations, or management priorities.
- Use the 2015 vs. 2017 datasets to analyze temporal changes in non-native woody invasions and the distribution of Oxalis pes-caprae.
- Leverage the clearly defined projection and metadata to enable reproducible spatial analyses and integration with other regional datasets.

Limitations and cautions
- Mixed-species stands were sometimes recorded as combined categories, which may obscure species-specific dynamics at finer scales.
- Field accuracy is ~10–15 m, influenced by canopy and GPS conditions; use with appropriate spatial resolution considerations.
- Eucalyptus species were not observed as invasive in Cyprus within these datasets, so labeling as invasive may not apply in all contexts.

References and acknowledgements
- Key references include Hadjikyriakou & Hadjisterkotis (2002), Meikle (1977, 1985), and related BDJ and COST Action materials cited in the document.
- Acknowledges support from COST Action TD1209 Alien Challenge and NERC CEH for fieldwork and data collection.