# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) sediment stability by Cohesive Strength Meter (CSM) in salt marsh and mud flat habitats

## Overview
- Dataset measures surface sediment stability using a Cohesive Strength Meter (CSM) across salt marsh and mud flat habitats.
- Collected at CBESS sites in two UK regions (Essex in South East England and Morecambe Bay in North West England) during winter and summer 2013.
- Aims to support analysis of sediment stability and its drivers, enabling correlations, reporting, and predictive insights about ecosystem stability.

## Study design and sampling
- Sites and habitats
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) — saltmarsh and adjacent mudflats.
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP) — saltmarsh and mudflats.
- Replication and quadrats
  - At each CBESS site, 22 designated quadrats were sampled with 3–5 replicate measurements per quadrat.
- Locations and context
  - Three locations in Essex and three in Morecambe Bay.
  - Essex sites typically grazed by Brent geese (heavily at AH and FW) and are erosive; Morecambe Bay sites grazed by sheep pale and pink-footed geese, generally depositional.
- Temporal coverage
  - Morecambe Bay: winter and summer 2013.
  - Essex: winter, early spring, and summer 2013.
- Coordinates and site descriptors
  - Essex and Morecambe Bay sites provided with precise coordinates and habitat descriptions (saltmarsh vs mudflat), including differences in inundation frequency and creek structure.

## Instrumentation and measurement
- Instrument: Cohesive Strength Meter (CSM) designed to measure erosion threshold of sediments.
- Measurement principle
  - Vertical, pulsed seawater jet applied to sediment; resistance to erosion inferred from changes in light transmission within a test chamber.
  - Output logged as stagnation pressure at the sediment surface (Nm^-2).
- Procedure overview
  - Calibrated device using standard procedures; routine includes selecting appropriate substratum routine (sand or mud; stable/unstable).
  - Observations focus on sediment stability by determining the pressure required to initiate erosion.

## Calibration and data processing
- Inter-machine calibration
  - Different CSM units vary in efficiency; calibrate using jet volume rather than firing pressure to enable cross-machine comparability.
  - Calibration references: Vardy et al. (2007) for calibration of high-pressure CSM.
- Calibration workflow
  - Weigh jets, remove erroneous results, and plot average jet output against firing pressure to determine a calibration line for each CSM.
  - Establish erosion threshold at a 10% drop in light transmission; compute the corresponding pressure using the device-specific calibration.
  - Convert jet weight measurements to stagnation pressure using the derived calibration equation.
- Core equations and constants (summarised)
  - P (stagnation pressure) is derived from jet parameters and constants (density of water, orifice diameter, nozzle height, etc.).
  - A simplified, device-specific calibration equation relates measured jet weight (or jet volume) to stagnation pressure.
  - Final data are expressed as stagnation pressure on the sediment surface (Nm^-2).
- Data outputs
  - For each jet: original reading converted to stagnation pressure; multiple replicates per quadrat averaged; results stored as mean stagnation pressure with standard deviation.
  - Data can be linked to firing pressure to validate linear calibration relationships.

## Data structure, formats, and fields
- Data format
  - CSV files (comma-separated values) with detailed field descriptions.
- Key data content
  - Site, location, habitat (saltmarsh or mudflat), quadrat number, season (Winter/Summer), replicate information.
  - Measured values: stagnation pressure (Nm^-2) per jet, with mean and standard deviation across replicates.
  - Metadata on calibration status, device used, and QA checks.
- Data provenance and QA
  - QA procedures include checking for outliers, re-running random samples for validation, and ensuring replicates are consistent.
  - Documentation tracks datasets, calibration parameters, and data cleaning steps.

## Quality assurance, maintenance, and data stewardship
- Quality assurance
  - Systematic checks for outliers and inconsistencies; replication provides reliability estimates (mean and standard deviation).
  - Data are checked for mathematical integrity and cross-validated against calibration relationships.
- Maintenance and calibration schedule
  - Calibrate CSMs every six months to account for potential drift; perform calibration prior to important campaigns or when performance changes are detected.
  - If performance shifts significantly, inspect and potentially replace the CSM’s filter or components.
- Data accessibility and discoverability
  - Datasets are structured with clear metadata and are intended to be discoverable, enabling reuse and combination with other CBESS data.

## Context for analysis and interpretation
- Potential analytic uses
  - Explore correlations between sediment stability (stagnation pressure) and site-level factors such as habitat type, inundation frequency, grazing regime, and regional differences (Essex vs Morecambe Bay).
  - Develop predictive models of sediment stability under varying environmental conditions and management scenarios.
- Considerations and limitations
  - Spatial scale: local quadrat-level measurements; potential upscaling requires careful aggregation.
  - Temporal coverage: 2013 campaigns; consider year-to-year variability when extrapolating.
  - Habitat and management differences (grazing, inundation) may drive observed variability between sites.
- Related literature
  - Foundational methods and calibration references include Tolhurst et al. (1999) and Vardy et al. (2007).

## References
- Tolhurst, T. J., et al. Measuring the in situ erosion shear stress of intertidal sediments with the Cohesive Strength Meter (CSM). Estuarine, Coastal and Shelf Science, 1999.
- Vardy, S., et al. Calibration of the high-pressure cohesive strength meter (CSM). Continental Shelf Research, 2007.