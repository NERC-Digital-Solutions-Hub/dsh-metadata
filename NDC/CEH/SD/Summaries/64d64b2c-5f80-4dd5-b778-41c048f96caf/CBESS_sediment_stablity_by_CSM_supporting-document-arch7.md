# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) sediment stability by Cohesive Strength Meter (CSM) in salt marsh and mud flat habitats

## Overview
- Purpose: Dataset of surface sediment stability measured with a Cohesive Strength Meter (CSM) to assess erosion resistance in salt marsh and mud flat habitats within CBESS.
- Scope: 22 designated CBESS quadrats across multiple coastal sites; measurements taken at salt marsh and adjacent mudflat habitats.
- Primary variable: Sediment stability expressed as stagnation pressure at the sediment surface, derived from CSM measurements and calibration.

## Spatial and temporal coverage
- Regions and sites:
  - Essex, South East England: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay, North West England: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Habitats: Saltmarsh and mudflat
- Coordinates (selected observation locations):
  - Essex: AH 51°47'N, 0°52'E; FW 51°49'N, 0°58'E; TM 51°41'N, 0°56'E
  - Morecambe Bay: CS 54°10'N, 3°0'W; WS 54°8'N, 2°48'W; WP 54°9'N, 2°58'W
- Sampling: Field campaign during Winter and Summer 2013 (Essex and Morecambe Bay variations in season timing)

## Sampling design and data collected
- Experimental design: 3 locations per site in each region; 22 quadrats per CBESS site; 3 to 5 replicate measurements per quadrat
- Measurements: Sediment stability using the Cohesive Strength Meter (CSM)
- Site characteristics: Saltmarsh and adjacent mudflats; region-specific differences in inundation frequency, creek structure, and grazing intensity (Essex vs. Morecambe Bay)

## Methods: Cohesive Strength Meter (CSM) and calibration
- Instrument: CSM designed to quantify erosion threshold via a vertical water jet pulsed against the sediment surface; data logged as jet-induced transmission changes
- Calibration and comparability:
  - Calibrations account for machine-to-machine differences in efficiency; calibrate using jet volume rather than firing pressure
  - Calibration yields a relationship to stagnation pressure (Nm-2) at the sediment surface
  - Routine QA: calibration every six months; more frequent if campaigns are critical; if performance changes, inspect/replace filters
- Data processing workflow:
  - Weigh individual jets and convert to jet volume/flow
  - Remove anomalous jets (timing errors manifest as peaks/dips) before calibration
  - Derive stagnation pressure P from calibrated equations; express erosion threshold as the pressure corresponding to a 10% drop in light transmission
  - Use per-machine calibration equations to convert observed jet data to stagnation pressure
- Replicate handling: Typically 4 replicates per measurement, occasionally 5; missing replicates noted in data

## Data formats and structure
- File formats: Comma-separated values (.csv)
- Data fields include (examples):
  - Season (Winter or Summer)
  - Location (Morecambe or Essex)
  - Site (CS, WS, WP, AH, FW, TM)
  - Habitat (Mudflat or Saltmarsh)
  - Quadrat Number (1–22)
  - Replicate identifiers and results
  - Original jet weights, volume flux (Q), and calibrated stagnation pressure (Nm-2)
  - Mean and standard deviation across replicates
  - Quality control indicators (outliers/NA entries)

## Data quality, QA, and maintenance
- Quality assurance:
  - Calibration of CSMs (semi-annual minimum; more frequent if campaigns demand)
  - Data checks for mathematical validity; re-run and reassess any outliers
  - Documentation of data provenance, calibration parameters, and per-machine specifics
- Maintenance: Calibration recommended every six months; check for clogged filters or mechanical changes affecting performance

## Usage considerations for GIS applications
- Cross-site comparability: Calibration per machine/time is essential for comparing stagnation pressures across sites
- Data integration: Can be joined with site metadata, habitat maps, and other CBESS datasets to produce map-based representations of sediment stability
- Interpretation: Stagnation pressure provides a proxy for erosion resistance; combine with environmental layers (grazer presence, inundation patterns) for spatial analyses

## Key references
- Foundational CSM methodologies and calibration approaches cited (e.g., Paterson, Tolhurst et al., Vardy et al.)
- Data and QA procedures documented in related CBESS methodological sources

## Additional notes
- Staff responsible for dataset: David M. Paterson
- Observational context: Coastal sites in Essex (eastern Atlantic UK) and Morecambe Bay (western UK) with differing sediment dynamics and grazing regimes, contributing to regional variability in sediment stability measurements