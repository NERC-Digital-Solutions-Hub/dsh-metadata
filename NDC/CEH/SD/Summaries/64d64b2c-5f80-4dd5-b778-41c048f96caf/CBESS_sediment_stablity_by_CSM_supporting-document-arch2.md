# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) sediment stability by Cohesive Strength Meter (CSM) in salt marsh and mud flat habitats

## Overview and aim
- Dataset describing surface sediment stability measured with a Cohesive Strength Meter (CSM) across salt marsh and adjacent mudflat habitats.
- Sampling design: 22 designated CBESS quadrats per site with 3–5 replicates each.
- Sites: salt marsh and mudflat pairs in Essex (SE England) and Morecambe Bay (NW England).
- Temporal coverage: Morecambe Bay samples in winter and summer 2013; Essex samples in winter, early spring, and summer 2013.
- Purpose aligned with CBESS monitoring to assess environmental health and ecosystem service sustainability.

## Contents and variables
- Primary variable: sediment stability expressed as stagnation pressure on the sediment surface (Nm^-2).
- Data structure includes: replicate measurements per quadrat, site, habitat type (saltmarsh or mudflat), season, and location identifiers.
- Metadata includes staff responsible, observation locations (with coordinates), site descriptions, and habitat characteristics.

## Sites, habitats, and context
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) – saltmarsh/mudflat contexts with grazing pressures (heavy Brent geese grazing at Abbotts Hall and Fingringhoe Wick; hare grazing in some areas).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP) – different grazing dynamics (pink-footed geese and sheep) and sediment dynamics; saltmarsh regions contrasted with depositional mudflat areas.
- Habitat contrasts influence inundation frequency, creek structure, and mudflat morphology (Morecambe generally sandier; Essex more erosive in some areas).

## Methods: data collection and device operation
- Instrument: Cohesive Strength Meter (CSM) designed to measure erosion threshold via a pulsed vertical water jet.
- Procedure: jets fired at sediment surface; eroded sediment reduces light transmission in a test chamber, with data logged per pulse.
- Calibration and standardization: calibration accounts for machine-to-machine variability due to component differences and aging; conversion from jet-weight measurements to stagnation pressure using a calibrated equation.
- Output: for each measurement, results are converted to stagnation pressure (Nm^-2) to reflect energy required to counter the jet at the sediment surface.
- Replicates: typically 4 replicates per measurement, with some measurements having up to 5 replicates; data include mean and standard deviation across replicates.

## Calibration and data processing specifics
- Calibration approach: use volume of water jets and a regression-based calibration equation to normalize across different CSM units (addressing differences in jet velocity between machines).
- Core formula concept: relates jet volume (or weight) and firing pressure to stagnation pressure at the sediment surface; key constants include water density, nozzle diameter, and geometry terms.
- Data handling: identify and remove erroneous results (timing glitches) before calibration; plot versus firing pressure to obtain a linear calibration line; use the line equation to convert observed outputs to stagnation pressure.
- Data products: final outputs expressed as stagnation pressure (Nm^-2) corresponding to a 10% drop in light transmission as the erosion threshold.

## Quality assurance, maintenance, and data formats
- Quality control: data checked for mathematical validity, outliers reassessed, and random rechecks of entries (5 per 100 readings).
- Maintenance: CSM calibration recommended every six months, with heightened calibration if the instrument is key for campaigns; possible maintenance if filters clog.
- Data formats: CSV (comma-separated values) used for dataset storage.
- Dataset metadata: includes dataset field descriptions, headers, replication details, site codes, habitat types, seasons, and location descriptors.

## Data storage, dissemination, and use
- Proper storage and uploading to designated portals/servers are part of the data management workflow.
- Outputs (stagnation pressure) facilitate standardized comparisons of sediment stability across sites, times, and habitats.
- The dataset supports environmental health monitoring and evaluation of policy performance over time, enabling cross-site data integration with other CBESS datasets.

## Limitations and considerations for analysts
- Inter-machine variability requires consistent calibration and documentation of the specific CSM used for each batch of measurements.
- Site-specific factors (grazing regime, inundation frequency, sediment type) influence stability readings and should be considered when comparing across sites or seasons.
- Data interpretation should account for seasonal and spatial context, particularly when aggregating Essex versus Morecambe Bay results.

## References and related methodology
- Tolhurst, J. et al. (1999). Measuring in situ erosion shear stress with the Cohesive Strength Meter (CSM).
- Vardy, S. et al. (2007). Calibration of the high-pressure Cohesive Strength Meter (CSM).