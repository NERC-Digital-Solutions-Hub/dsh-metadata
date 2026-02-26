# Supporting information for Pescott, O., Peyton, J., Mountford, J., Onete, M., Martinou, A. (2017). Non-native plant species GIS data from Cyprus Sovereign Base Areas, October 2015 and March 2017

## Overview
- Describes GIS data for non-native plant species in Cyprus Sovereign Base Areas (SBA), collected in October 2015 and March 2017.
- Aims to support environmental health monitoring, policy scrutiny, and informing future decisions; data intended to be linked with a forthcoming Biodiversity Data Journal paper and with GBIF for quadrat data.

## Study areas and sampling periods
- 2015 sampling in Akrotiri part of the western SBA, covering area bounded by Akrotiri-Kolossi road (west), Akrotiri salt lake boundary (north), Mediterranean Sea (east), and Akrotiri-Lady’s Mile Beach road (south).
- 2017 sampling in Akrotiri and Dhekelia (western and eastern SBA) to extend mapping with a primary focus on quadrats and associated notes.
- Target woody non-native species: Acacia saligna, Casuarina cunninghamiana, Eucalyptus camaldulensis, E. gomphocephala; also Symphyotrichum squamatum (Aster squamatum) and later Oxalis pes-caprae (in Dhekelia in 2017).

## Field methods and instrumentation
- Data collection method: GPS tablet-based mapping with satellite photography basemaps for orientation.
- 2015 field team: OLP, JP, MO, JOM; led by AFM for access and project management.
- 2017 field team: OLP, JP, MO, JOM; quadrat-focused, with AFM project management.
- Field devices: Panasonic FZ-G1 Ruggedpad tablets using ArcPad 10.2; typical spatial accuracy around 10–15 m (varying with canopy).

## Data products and structure
- 2015 shapefiles:
  - Acacia_saligna_EIDC.shp
  - Eucalyptus_spp_areas_EIDC.shp
  - Mixed_species_areas_EIDC.shp
  - Symphyotrichum_squamatum_EIDC.shp
  - Target_notes_EIDC.shp
- 2017 shapefiles:
  - Acacia_saligna_2017_EIDC.shp
  - Oxalis_pes-caprae_2017_EIDC.shp
  - Target_notes_2017_EIDC.shp
- Spatial data reserved in ETRS89 / ETRS-LAEA European grid (EPSG:3035); Proj4 string provided in documentation.
- Attribute data structure (Tables 1 and 2 in the supporting information) describe:
  - IAS column with pre-set invasive species names (note: some species not necessarily invasive in Cyprus context).
  - Free-text NOTES fields for field observations.
  - [SPECIES]_ID identifiers for stand numbers.
  - Target_notes fields with prefixes (e.g., 17t) for year-specific notes.

## Temporal coverage
- 2015 files created between 10/10/2015 and 24/10/2015.
- 2017 files created between 04/03/2017 and 18/03/2017.
- 2017 dataset adds Oxalis pes-caprae observations not present in 2015.

## Data quality and validation
- Species determinations cross-checked against standard floras (Meikle 1976, 1985) and additional guides; field and specimen verification conducted by the team.
- Consultation with local experts (e.g., G. Hadjikyriakou) to confirm identifications of forestry-planted non-natives (e.g., Casuarina spp.).
- Field notes and polygon attributes provide additional context on composition when species could not be separated at mapping scale.

## Data governance, sharing, and integration
- Data will be archived in the NERC Environmental Information Data Centre (EIDC).
- Quadrat data to be archived on GBIF and integrated with the BDJ paper (in prep) linking to this resource.
- Acknowledges broader data-sharing considerations and aims to share underlying data appropriately, with governance in place to manage data quality and accessibility.

## Supporting materials and references
- Supporting information references include broader context on invasive species and Cyprus flora, plus related COST Action missions and other field guides.
- A forthcoming data paper and BDJ publication are expected to provide additional context and linking data products.

## Acknowledgements
- Funding support from COST Action TD1209 Alien Challenge and related organizations; participants acknowledge multiple funding and support sources.