# Coastal Biodiversity Ecosystem Service Sustainability (CBESS) the erosion rate of sediment cores from salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset describing erosion rate of sediment cores from salt marsh sites in Morecambe Bay and Essex.
- Measurements: % mass loss per hour for three flume flow regimes (low, medium, high).

## Locations and Sites
- Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Coordinates provided for each site; site descriptions note contrasting soil types (clay in Essex; sandy in Morecambe Bay) and differences in inundation, creek structure, and vegetation.
- Grazing context: Essex sites heavily grazed by geese; Morecambe Bay sites heavily to moderately grazed by sheep with geese in winter; West Plain lightly grazed.

## Field and Laboratory Methods
- Sediment cores: 16 cm diameter, 30 cm height; collected from 1 m x 1 m quadrats; each core’s above-ground vegetation noted.
- Testing: cores placed in a re-circulation flume (“waterfall” flow) for 1.5 hours (0.5 h per low, medium, high flow segments); mass loss measured at 0, 5, 10, 15, 30 minutes and converted to mass loss per hour.
- Flow specifics: low (1.0 m/s), medium (1.6 m/s), high (2.2 m/s), with stagnation pressures of 61 Pa, 146 Pa, 351 Pa respectively.
- Monitoring period: Winter and Summer 2013, with Essex winter samples collected 2–6 March 2013.
- Staff: Hilary Ford.

## Dataset Structure and Variables
- Primary variables:
  - L_%massloss: % mass loss per hour at low velocity
  - M_%massloss: % mass loss per hour at medium velocity
  - H_%massloss: % mass loss per hour at high velocity
- Spatial and attribute fields:
  - Site (Morecambe: CS, WS, WP; Essex: AH, FW, TM)
  - Location (Essex or Morecambe)
  - Habitat (Saltmarsh; adjacent mudflat data)
  - Quadrat Number (1–22)
  - Scale categories (A-D: 1 m, 1–10 m, 10–100 m, >100 m)
- Data format: Excel workbook; dataset and field descriptions included as metadata.

## Data Quality and Considerations
- Some low-flow measurements may yield negative mass loss due to initial saturation with water.
- High-flow tests occasionally destroyed cores; medium-flow results are the most reliable for overall erosion-rate modeling.
- Mass loss values >100% are considered valid after conversion to hourly rates.
- No statistical treatments or data quality control procedures detailed in the dataset metadata.

## Implications for GIS and Data Use
- Enables mapping of erosion rates by site, habitat type, and quadrat, with flow-condition context.
- Can be linked to soil type, grazing regime, inundation frequency, and vegetation to model spatial patterns of erosion risk.
- Useful for integrating with other CBESS datasets to analyze coastal biodiversity and ecosystem-service implications.