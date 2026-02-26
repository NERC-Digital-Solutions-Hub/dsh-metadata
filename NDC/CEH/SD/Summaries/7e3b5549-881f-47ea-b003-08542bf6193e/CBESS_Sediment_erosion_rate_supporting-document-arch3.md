# Coastal Biodiversity Ecosystem Service Sustainability (CBESS) the erosion rate of sediment cores from salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset records erosion rate of sediment cores from salt marsh sites, using a re-circulation flume to apply three flow regimes (low, medium, high) and measure %mass loss per hour.
- Purpose aligns with monitoring for environmental health insights to support policy scrutiny and future decision-making.
- Field campaign conducted in Winter and Summer 2013, with additional Essex winter sampling window (2–6 March 2013).

## Study design and scope
- Core measurement: one large sediment core (16 cm diameter, 30 cm height) per 1 m x 1 m quadrat; above-ground vegetation noted.
- Flow regimes: measurements taken across three waterfall forces representing low (1.0 m/s), medium (1.6 m/s), and high (2.2 m/s) velocities.
- Time points: mass loss recorded at 0, 5, 10, 15, and 30 minutes to compute hourly rates.
- Outcome: erosion rate expressed as %mass loss per hour; higher flow typically yields higher erosion rates.

## Site locations and environmental context
- Essex sites (clay soils): Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites (sandy soils): Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Regional differences: Essex sites generally have higher inundation frequency, distinct creek structures, and are hare-grazed; Morecambe Bay sites are sandy with different grazing patterns (sheep grazing at CS/WS; Pink-footed geese grazing; West Plain lightly grazed).
- Geographical coordinates included for each site, aiding reproducibility and spatial analysis.

## Data collection and variables
- Variables per observation: 
  - Core location within quadrat; Season (Winter W or Summer S); Location (Essex E or Morecambe M); Site (AH, FW, TM, CS, WS, WP); Habitat (Mudflat MF or Saltmarsh SM); Quadrat Number; Scale coding (A/B/C/D with corresponding spatial ranges).
  - L_%massloss: %mass loss per hour at low velocity.
  - M_%massloss: %mass loss per hour at medium velocity.
  - H_%massloss: %mass loss per hour at high velocity.
- Data organization notes: dataset field descriptions and header/row number metadata included to aid interpretation and sorting.
- Data handling: vegetation cover recorded; cores returned to Bangor University for processing.

## Calibration and quality notes
- Calibration: stagnation pressures set to Low 61 Pa, Medium 146 Pa, High 351 Pa to control flow in the flume.
- Data quality observations: 
  - Some low-flow mass loss values can be negative due to initial water saturation.
  - Some high-flow cores were destroyed, reducing sample size at that regime.
  - Medium-flow results are deemed more reliable and should be preferred for model inputs.
- Quality control indicators (e.g., explicit QC procedures) are not specified; emphasis on data being usable with noted caveats.

## Data format and metadata
- File format: Excel workbook.
- Structure: includes detailed metadata fields, including dataset field descriptions, header information, and row numbering to maintain original input order.
- Metadata richness: site descriptions, habitat types, scale definitions, and seasonal/location coding enhance transparency and reusability.

## Governance, sharing, and applicability for monitoring frameworks
- Data availability is documented with explicit site, habitat, and methodological metadata, supporting governance and transparency.
- The dataset exemplifies a monitoring framework component: linking physical measurements (erosion rate) to environmental context (soil type, grazing, inundation) and hydrodynamic conditions.
- Potential policy relevance: provides standardized measures of sediment erosion under varying flows, useful for coastal management, habitat conservation, and erosion risk assessments.
- Important caveats for policymakers and analysts: data limitations under certain flow regimes, need to account for site-specific grazing and soil differences when aggregating results.