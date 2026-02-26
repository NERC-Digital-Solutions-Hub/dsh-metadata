# Plant cover in foredunes following hurricane Irma: large scale surveys

## Overview
- Dataset of plant cover by species sampled in foredune areas after hurricane Irma (Oct 2017).
- Conducted as large-scale field surveys across Florida and Georgia, USA, at up to 28 sites.
- Observations collected on three occasions: Feb 2018, Jul 2018, and Jan 2019.
- Staff: John Griffin and Matthew Joyce.

## Study locations and context
- Field surveys conducted along the foredune area of sites distributed between Cape Canaveral (Florida) and Tybee Island (Georgia).
- Hurricane Irma impacted the coastline in 2017, providing a post-disturbance context for recovery.

## Experimental design and site selection
- In February 2018, sites were chosen based on accessibility, permitting, and a mix of coastal development levels.
- Sites undergoing active restoration (e.g., transplantation) were re-surveyed.
- For logical consistency, transects at each site were positioned in approximately the same areas across survey rounds (within ~10 m where possible).

## Methods and data collection
- At each site, transects perpendicular to the shoreline were placed at ~50 m intervals.
- Along each transect, at 1 m intervals from the dune crest to the upper beach, the percentage cover of each plant species was visually estimated within 0.5 x 0.5 m quadrats.
- Total plant cover per quadrat is the sum of all species' covers; species richness is the number of species recorded along a transect.
- For repeated surveys, transects 1–3 at each site were repositioned within ~10 m to maintain representativeness.

## Variables observed
- Plant percentage cover by species.
- Average plant cover.
- Species richness.
- Uniola paniculata mean cover (and other species represented across numerous columns).

## Data management and quality control
- Data checked by screening distributions for unusual values and cross-checking against field notebooks.
- Data conventions:
  - NA = not applicable (sampling not conducted for that site-variable combination).
  - 0 = zero (absence of a species or zero species richness in a sample).

## Data formats and field descriptors
- File formats: Excel, CSV.
- Key dataset fields:
  - Sampling_date: Month and year of sampling.
  - Site: Name of study site.
  - Lat, Long: Latitude and longitude of the study site.
  - Transect: Transect number.
  - Development: Category of development around the site.
    - A: Low development (no development within ~1 km of foredune toe; mainly parks).
    - B: Moderate development (no direct foredune or first swale development; boardwalks or low-density housing nearby).
    - C: High development (buildings directly on the beach behind small dune margins).
  - Number_of_species: Number of species recorded along the transect.
  - Species.richness: (Duplicate naming convention for richness per transect).
  - Total.cover: Total plant cover along the transect.
  - Uniola_paniculata: Mean cover of Uniola paniculata along the transect.
  - Additional columns: Represent other species (up to 67 subsequent species columns).

## Notes on interpretation and limitations
- The dataset emphasizes post-Irma recovery, with development context included to explore associations with cover and richness.
- Re-surveys targeted representativeness and accessibility, but exact areas re-sampled may shift slightly (~10 m), potentially influencing comparability across rounds.
- Observational estimates rely on visual cover assessments within small quadrats, which may introduce observer bias without calibration.