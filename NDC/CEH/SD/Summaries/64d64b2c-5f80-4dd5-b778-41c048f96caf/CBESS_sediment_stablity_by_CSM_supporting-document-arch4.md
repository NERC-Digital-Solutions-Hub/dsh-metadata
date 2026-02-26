# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) sediment stability by Cohesive Strength Meter (CSM) in salt marsh and mud flat habitats

## Purpose and content
- Datasets measure surface sediment stability using a Cohesive Strength Meter (CSM) across CBESS sites.
- 22 designated quadrats per site; across salt marsh and adjacent mudflats.
- Two regions: Essex (south-east Atlantic UK) and Morecambe Bay (west UK).
- Winter and summer 2013 sampling in Morecambe Bay; winter, early spring, and summer 2013 in Essex.
- Primary variable: sediment stability; stored as stagnation pressure (Nm^-2) after calibration.

## Study design and locations
- Staff: David M. Paterson.
- Sites in Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Sites in Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Coordinates provided for each location; habitat descriptions include saltmarsh and mudflat characteristics.
- Habitat context: Essex coast more erosive; Morecambe Bay more depositional; differences in inundation frequency, creek structure, and grazing pressures (e.g., Brent geese in Essex; pink-footed geese and sheep in Morecambe Bay).

## Data collection and instrumentation
- Field campaign timing: Winter and Summer 2013 (CBESS).
- Replication: typically 4 replicates per measurement, sometimes up to 5; 3–5 replicates per quadrat.
- Instrument: Cohesive Strength Meter (CSM) measuring erosion threshold via a vertical water jet pulsed at sediment.
- Procedure: test chamber inserted into sediment; jets fired with increasing force; resuspended sediment changes light transmission recorded; data logged per jet.
- Calibration needs: inter-machine variability due to nozzle length, maintenance, and tubing elasticity; calibration based on jet volume rather than firing pressure.

## Calibration, equations, and data processing
- Calibration approach (per machine): relate stagnation pressure to jet volume using a calibration equation; accounts for machine-specific efficiency differences.
- Core calculation: P = stagnation pressure at sediment surface (Nm^-2); derived from jet parameters with a standardized equation and constants (density of water, orifice diameter, distances, etc.).
- Data processing steps:
  - Weigh CSM jets to derive jet volume; convert to Q (volume per second) or jet weight per second.
  - Plot stagnation pressure vs firing pressure; derive a calibration line and its equation for that CSM at the time of testing.
  - Determine erosion threshold as the point where a 10% drop in light transmission occurs.
  - Report results as stagnation pressure on the sediment surface using the time-specific calibration equation.

## Data formats, metadata, and quality control
- Data format: CSV files for raw and calibrated data.
- Key dataset fields include: Season, Location, Site, Habitat, Quadrat Number, Replicate(s), CSM used, calibration details, mean and standard deviation of replicates, and QA checks.
- QA and data quality: data checked for mathematical integrity; multiple recalculations and random checks (5 per 100 readings); outliers reassessed; some replicates may be NA if not collected.
- Metadata aspects emphasize reproducibility and traceability to specific CSM units and calibration time.

## Maintenance and best practices
- Calibration recommended every six months; more frequent if a campaign is imminent or if performance changes are detected.
- Potential maintenance issue: clogged filters may require replacement; ongoing calibration helps ensure consistent results across time.

## Related references and context
- Tolhurst et al. (1999) and Tolhurst et al. (2003) on measuring in situ erosion shear stress with CSM.
- Vardy et al. (2007) on calibration of high-pressure CSM against jet volume rather than firing pressure.
- Data handling and quality assurance methodologies described in the 2007 calibration study (data checking, file formats, and metadata fields).

## Implications for data governance and reuse (Data Leaders perspective)
- The dataset exemplifies end-to-end data management: well-defined scope, site-level metadata, instrument-specific calibration, QA/QA documentation, and clear data formats.
- Offers a framework for managing sensor-based environmental data: instrument calibration history, unit consistency, and provenance tied to specific sites and campaign timings.
- Highlights challenges relevant to data ecosystems: inter-machine comparability, need for consistent metadata on instruments and calibration status, and documentation of sampling context (season, grazing, inundation regime).
- Supports co-ownership and stakeholder alignment by providing detailed site descriptions, habitat contexts, and data processing workflows, enabling integration with broader CBESS data and regional datasets.