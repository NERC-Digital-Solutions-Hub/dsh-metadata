# Supporting information for Pescott, O., Peyton, J., Mountford, J., Onete, M., Martinou, A. (2017). Non-native plant species GIS data from Cyprus Sovereign Base Areas, October 2015 and March 2017. NERC Environmental Information Data Centre. http://doi.org/10.5285/7c84e06d-bb1a-4aac-b1d7-33c11310d8a0

## Overview
- Provides supporting information for the GIS dataset of non-native plant species in the Cyprus Sovereign Base Areas (SBA), covering October 2015 and March 2017 fieldwork.
- Data are compiled as shapefiles with associated field notes and target observations; quadrat data to be archived separately on GBIF and linked to a Biodiversity Data Journal paper in preparation.
- Fieldwork focused on mapped stands of woody non-natives (e.g., Acacia saligna, Casuarina cunninghamiana, Eucalyptus spp.) and certain forbs; some categories aggregate similar species for mapping purposes.

## Sampling and fieldwork description
- 2015 sampling (Akrotiri, western SBA): stands of woody non-natives mapped in October 2015 using GPS tablet-based mapping with satellite imagery for orientation.
  - Main study area bounded by Akrotiri-Kolossi road (west), Akrotiri forest (north), Mediterranean Sea (east), Akrotiri-Lady’s Mile Beach road (south).
  - Primary species: Acacia saligna, Casuarina cunninghamiana, Eucalyptus camaldulensis, E. gomphocephala; Symphyotrichum squamatum noted as a forb.
  - Quadrat recording accompanying mapping; some stands recorded as “mixed” due to indistinguishable composition at mapping scale.
- 2017 sampling (Akrotiri and Dhekelia, western and eastern SBA): March 2017 fieldwork focused on quadrat recording; limited stand maps and target notes archived.
  - Included Oxalis pes-caprae stands in Dhekelia.
- Fieldwork management and access facilitated by local teams; data collection employed portable GIS tools.

## Fieldwork instrumentation
- Data captured on ruggedised tablet computers (Panasonic FZ-G1 'Toughpad') using ArcPad v10.2.
- Base mapping relied on satellite imagery for orientation.
- Typical spatial accuracy: approximately 10–15 m, varying with forest canopy.
- Field notes and polygon attributes provide additional detail on composition.

## Temporal coverage and data files
- 2015 data files created between 10/10/2015 and 24/10/2015:
  - Acacia_saligna_EIDC.shp
  - Eucalyptus_spp_areas_EIDC.shp
  - Mixed_species_areas_EIDC.shp
  - Symphyotrichum_squamatum_EIDC.shp
  - Target_notes_EIDC.shp
- 2017 data files created between 04/03/2017 and 18/03/2017:
  - Acacia_saligna_2017_EIDC.shp
  - Oxalis_pes-caprae_2017_EIDC.shp
  - Target_notes_2017_EIDC.shp

## Data structure and formats
- Shapefiles archived in European grid projection (ETRS89 / ETRS-LAEA, EPSG:3035).
- Projection details:
  - Projection: ETRS89 / ETRS-LAEA (EPSG:3035)
  - Proj4 string: +proj=laea +lat_0=52 +lon_0=10 +x_0=4321000 +y_0=3210000 +ellps=GRS80 +units=m +no_defs
- Attribute table formats (Table 1 and Table 2 descriptions):
  - Table 1 (for Acacia_saligna_EIDC.shp, Eucalyptus_spp_areas_EIDC.shp, Mixed_species_areas_EIDC.shp, Symphyotrichum_squamatum_EIDC.shp, Acacia_saligna_2017_EIDC.shp, Oxalis_pes-caprae_2017_EIDC.shp):
    - IAS: pre-set invasive alien species name
    - NOTES: free text field for observations
    - [SPECIES]_ID: stand number identifier
  - Table 2 (Target_notes_EIDC.shp, Target_notes_2017_EIDC.shp):
    - NOTES: free text field for field observations
    - 2017 target notes prefixed with '17t' to facilitate separation from location data
- Quadrat data linkage: quadrat data linked to shapefiles and will be archived on GBIF and associated with the BDJ paper.

## Quality control and data validation
- Species determinations cross-checked against standard Floras and field guides; involved multiple researchers to unify determinations.
- Consultation with local experts (e.g., G. Hadjikyriakou) used to confirm identifications, particularly for forestry-planted species (e.g., Casuarina spp.).
- Some notes indicate that certain species were recorded in aggregate categories (e.g., mixed stands) due to mapping scale limitations.

## Data management, discoverability, and linking to outputs
- Data are archived within the NERC Environmental Information Data Centre (EIDC).
- The accompanying quadrat data will be deposited on GBIF and integrated with the BDJ paper in preparation, which will link to this resource.
- Metadata and field forms (ArcPad) support discoverability and reuse; data standards, formats, and field definitions are described to aid interoperability.
- References and supplementary material provide context for species identifications and historical context.

## Access, reuse, and limitations
- Primary data are accessible via the EIDC, with additional data (quadrat observations) planned for GBIF integration.
- Limitations include spatial accuracy variability due to canopy cover and the use of aggregated categories in some mapping scenarios.
- The data paper and accompanying BDJ publication (in prep) will provide further interpretation, impact, and contextual information.

## Acknowledgements and references
- Acknowledges COST Action TD1209 Alien Challenge support for field missions.
- Fieldwork and data collection contributions from multiple researchers; local access facilitated by AFM and others.
- References include regional flora sources and related projects on invasive species and Cyprus biodiversity.