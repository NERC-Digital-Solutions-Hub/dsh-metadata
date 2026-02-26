# Experimental location and source site

## Overview
- Documents collection of seeds from six sites on Lord Howe Island for two palm species (Howea belmoreana and Howea forsteriana) and the subsequent greenhouse/nursery experiment.
- Examines effects of seed source, soil type, soil sterilisation, and drought treatment on seedling survival and growth.
- Experiment conducted at the Lord Howe Island Nursery with controlled soil conditions and structured phenotyping over time.

## Seed sources and sites (geospatial details)
- Seed sources (H. forsteriana): Bowker Avenue, Far Flats, Grey Face, Middle Beach, Plantation; coordinates provided for each site.
  - Bowker Avenue: latitude -31.528, longitude 159.071
  - Far Flats: latitude -31.566, longitude 159.076
  - Grey Face: latitude -31.562, longitude 159.083
  - Middle Beach: latitude -31.528, longitude 159.076
  - Plantation: latitude -31.548, longitude 159.077
- Seed sources (H. belmoreana): Far Flats (as above) and Golf Course; Golf Course coordinates: latitude -31.546, longitude 159.081
- Experimental location: Lord Howe Island Nursery; coordinates: latitude -31.525, longitude 159.067

## Experimental design
- For each seed source and species combination, 1000 seeds planted.
- Planting boxes: 60 cm x 30 cm x 30 cm, lined with sealable bags filled to 15 cm depth.
- Soil conditions: four combinations
  - Calcareous sterilised
  - Calcareous unsterilised
  - Volcanic sterilised
  - Volcanic unsterilised
- Replication: five boxes per soil condition per seed source/species, 50 seeds per box.
- Planting date: September 2015.
- Post-germination: November 2016, germinated seedlings potted individually in the same soil type (unsterilised) outside under shade, watering every three days.

## Treatments and timeline
- March 2018: drought treatment applied to randomly designated half of the plants from each condition (species, seed site, soil condition) by withholding water for two weeks; the other half remained watered.
- Drought and non-drought groups organized in boxes of 40 plants each and placed in a checkerboard arrangement.

## Phenotyping and measurements
- Survival recorded at three time points:
  - November 2016 (14 months)
  - March 2018 (30 months, before drought)
  - May 2018 (32 months, after drought)
- Growth measurements:
  - Height measured at November 2016 and May 2018 (in cm, to 5 mm accuracy)
  - Leaf number counted at November 2016 and May 2018 (including scars)
- Death definition: plant considered dead if the growing shoot was completely desiccated

## Data fields and schema (variables)
- Box_code: arbitrary box identifier
- Seedling_code: arbitrary seedling identifier (survived to November 2016)
- alive_Nov2016 / alive_Mar2018 / alive_May2018: survival status at the three time points (TRUE = alive, FALSE = dead)
- height_Nov2016 / height_May2018: plant height in cm at November 2016 and May 2018
- N_leaves_Nov2016 / N_leaves_May2018: number of leaves at November 2016 and May 2018
- drought_treatment: N = non-drought, D = drought
- soil_sterilisation: N = no (unsterilised), Y = yes (sterilised)

## GIS considerations and potential uses
- Spatial association: map seed sources, soil types, and experimental plots to analyze spatial patterns in survival and growth.
- Multivariate analyses: relate survival, height, and leaf counts to seed site, species, soil type, sterilisation, and drought treatment.
- Data integration: combine site coordinates with experimental plot layouts (boxes and randomization) for repeatable GIS workflows.
- Data quality and preparation: addresses challenges common to GIS data (multiple sources, varying resolutions, data cleaning, and standardization) to enable robust map-based data visualisations.