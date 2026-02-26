# Data overview

## Study purpose and scope
- Records of insect visitations to flowers in a wildflower seed mix trial.
- Conducted across two farms (Church Farm, Oxfordshire; Lee Farm, West Sussex) in a single field context.
- Seed mixes sown in 20 x 5 m contiguous plots; four seed mixes plus a control fallow.

## Study sites and design
- Locations with coordinates:
  - Church Farm, Oxfordshire: 51° 38' 14.4348'' N, 1° 11' 5.4528'' W
  - Lee Farm, West Sussex: 50° 53' 0.2112'' N, 0° 28' 24.1464'' W
- Plot layout: 20 x 5 m plots, arranged contiguously.
- Treatments: four wildflower seed mixes plus a control.
- Sampling cadence: April–August in 2019, 2020, 2021; eight survey periods per year.
- Data collection days: farms were surveyed on two separate days close to one another for each survey period.

## Data collection methods
- Insects observed visiting flowers were identified on the wing or captured for lab identification.
- Survey approach: each plot walked centrally lengthways; insects within 2 m either side identified.

## Taxonomy and data granularity
- Insect groups recorded at the 'group' level: hoverfly, other fly, solitary wasp, solitary bee, bumblebee, honeybee, beetle, butterfly.
- Bees, hoverflies, and butterflies identified to species where possible.
- Flower data captured at family and species level.
- For insects: taxon group (Insect.taxa), genus (Insect.genus), species (Insect.species), and Sex recorded where available.

## Data quality and verification
- Specimens not identifiable by initial identifiers were sent to experts (Steven Falk for wild bees; Ellen Rotheray for hoverflies) with sub-samples to ensure accuracy.

## Data structure and format
- Data stored in InsectData.csv with 14 columns:
  - Year
  - Date
  - Month
  - Period
  - Farm
  - PlotID
  - Mix
  - Replicate
  - Flower.family
  - Flower.species
  - Insect.taxa
  - Insect.genus
  - Insect.species
  - Sex

## Temporal and spatial scope
- Temporal coverage: April–August across years 2019–2021.
- Spatial scope: two farms with plot-level data; farm coordinates provided; PlotID identifies each surveyed plot within the field context.

## Data use and GIS considerations
- Suitable for map-based visualization of insect visitation patterns across plots, seed mixes, and time.
- Can be integrated with additional GIS layers for spatial analyses.
- Considerations: plot-level resolution, consistency of species identifications over years, and metadata completeness for precise geolocation at the plot level.

## Limitations and considerations
- Limited to two farms in different regions; may limit broader generalizability.
- Data complexity and resolution require careful data cleaning and standardization for cross-dataset GIS integration.

## Access and data details
- Primary data format: InsectData.csv containing 14 descriptive fields as listed above.