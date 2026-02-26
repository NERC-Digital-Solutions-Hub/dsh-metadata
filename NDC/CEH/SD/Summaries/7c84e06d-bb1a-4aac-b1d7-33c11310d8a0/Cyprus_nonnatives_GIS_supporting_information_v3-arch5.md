# Supporting information for Pescott, O., Peyton, J., Mountford, J., Onete, M., Martinou, A. (2017). Non-native plant species GIS data from Cyprus Sovereign Base Areas, October 2015 and March 2017. NERC Environmental Information Data Centre. http://doi.org/10.5285/7c84e06d-bb1a-4aac-b1d7-33c11310d8a0

## Purpose and scope
- Provides supporting information for GIS data on non-native plant species in the Cyprus Sovereign Base Areas (SBA), covering October 2015 and March 2017 fieldwork.
- Data paper in preparation (BDJ) to accompany quadrat data; forthcoming-related publication will link to this resource.

## Data collection and methods
- 2015: mapping of woody non-natives in Akrotiri SBA using GPS tablet-based mapping with satellite base mapping; focus species included Acacia saligna, Casuarina cunninghamiana, Eucalyptus camaldulensis, E. gomphocephala, and Symphyotrichum squamatum; quadrat recording also undertaken.
- 2017: similar approach in Akrotiri and Dhekelia SBA; emphasis on quadrat recording; additional Oxalis pes-caprae mapped in Dhekelia.

## Fieldwork instrumentation and data capture
- Field data captured on Panasonic FZ-G1 Toughpad tablets using ArcPad v10.2.
- Typical spatial accuracy: ~10–15 m (canopy effects may increase uncertainty).

## Temporal coverage and files
- 2015 data files created 10/10/2015–24/10/2015:
  - Acacia_saligna_EIDC.shp
  - Eucalyptus_spp_areas_EIDC.shp
  - Mixed_species_areas_EIDC.shp
  - Symphyotrichum_squamatum_EIDC.shp
  - Target_notes_EIDC.shp
- 2017 data files created 04/03/2017–18/03/2017:
  - Acacia_saligna_2017_EIDC.shp
  - Oxalis_pes-caprae_2017_EIDC.shp
  - Target_notes_2017_EIDC.shp

## Projection and spatial reference
- Shapefiles use the European grid: ETRS89 / ETRS-LAEA (EPSG:3035).
- Proj4 string provided for reproducibility.

## Data structure and schema
- Table 1: Shapefile attribute formats for Acacia_saligna_EIDC.shp, Eucalyptus_spp_areas_EIDC.shp, Mixed_species_areas_EIDC.shp, Symphyotrichum_squamatum_EIDC.shp, Acacia_saligna_2017_EIDC.shp, Oxalis_pes-caprae_2017_EIDC.shp.
- Table 2: Attribute formats for Target_notes_EIDC.shp and Target_notes_2017_EIDC.shp.
- Key fields include:
  - IAS: pre-set invasive alien species name (species identifications cross-checked against floras and field guides).
  - NOTES: free-text field for field observations.
  - [SPECIES]_ID: stand number identifier.
- Field recording categories include dedicated target notes and mixed-species classifications due to ArcPad recording forms.

## Quality control and taxonomic validation
- Species determinations cross-validated against standard floras (e.g., Meikle) and field specimens.
- Collaborative cross-checks among project team members; consultation with local experts (e.g., G. Hadjikyriakou) to confirm identifications, particularly for forestry-derived planted species.

## Data management, sharing, and reuse
- Data archived at the NERC Environmental Information Data Centre (EIDC).
- Quadrat data to be linked with the BDJ paper and GBIF records in due course.
- Notes on taxonomy updates and post-2015 revisions to determinations.
- Acknowledges funding and collaboration from COST Action TD1209 Alien Challenge and CEH/NERC support.

## Limitations and notes for users
- ArcPad category structure necessitated grouping some species (e.g., Casuarina and mixed stands; Eucalyptus spp. combined) due to field form constraints.
- Eucalyptus species noted as not observed to be spreading in Cyprus at the time; “invasive” designation may not apply uniformly.
- Spatial accuracy may vary with canopy cover and small-scale heterogeneity; field notes provide contextual detail.

## References and acknowledgements
- Lists supporting literature for species identifications and regional flora.
- Acknowledges project participants, funders, and institutional support.