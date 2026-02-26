# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) sediment stability by Cohesive Strength Meter (CSM) in salt marsh and mud flat habitats

## Overview
- Dataset measures surface stability of sediments using a Cohesive Strength Meter (CSM) across salt marsh and adjacent mudflat habitats.
- Part of the CBESS field campaign in winter and summer 2013.
- Sites include Morecambe Bay (west UK) and Essex (southeast Atlantic UK), with three locations per site and two habitat types per CBESS site.
- Replicates per quadrat: typically 3–5 measurements across 22 designated quadrats.

## Data collection and scope
- Observations focus on sediment stability (erosion threshold) using the CSM device.
- Sites: Morecambe Bay (Cartmel Sands, Warton Sands, West Plain) and Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes).
- Habitat types: saltmarsh and mudflat; in Essex areas, grazing and inundation characteristics differ from Morecambe Bay.
- Seasonal sampling: winter and summer campaigns in 2013; some Essex samples collected in winter, early spring, and summer 2013.

## Metadata and locations
- Staff: David M. Paterson.
- Geographic coordinates and location descriptions provided for each site (Essex and Morecambe Bay).
- Habitat and site-specific descriptions include grazing regimes and hydrodynamic differences (e.g., Morecambe Bay tends to be more depositional; Essex coast more erosive).

## Methods and processing
- Instrument: Cohesive Strength Meter (CSM), used to quantify erosion threshold with a vertical pulsed water jet.
- Calibration:
  - Inter-machine variation exists; calibrations account for differing efficiencies between devices.
  - Calibration ties jet weight/volume to stagnation pressure (Nm^-2) rather than firing pressure.
  - Calibration procedure includes measuring multiple jets, removing erroneous readings, and deriving a device-specific calibration equation.
  - Final emission metric: stagnation pressure at sediment surface corresponding to a 10% drop in light transmission (erosion threshold).
- Procedure details:
  - Weigh jet outputs, convert to stagnation pressure using a defined formula, and derive calibration curves in spreadsheet software.
  - Calibration performed for each CSM at time of use; maintenance recommended every six months.
- Data processing:
  - Data exported to CSV; QA procedures described (outlier checks, replication checks, data re-runs).
  - Replicate measurements (typically 4 per setting; up to 5) are averaged for final values.
  - Data fields include: Season, Location, Site, Habitat, Quadrat Number, Replicate, Mean stagnation pressure, Standard deviation, etc.

## Data structure and formats
- Primary data format: comma-separated values (.csv).
- Dataset fields cover: site, location, habitat type, quadrat number, season, replicate identifiers, original jet readings, calibrated stagnation pressure, mean values, and standard deviations.
- Data lineage and documentation include dataset field descriptions, header/tables, and replication metadata.

## Quality assurance and governance
- Quality control includes:
  - Data entered into spreadsheets with mathematical checks.
  - Random data re-runs for QA; outlier and unusual measurements reassessed.
  - Documentation of replicates and any missing data (ND indicators).
- Reproducibility supported by:
  - Detailed calibration methodology per device and per campaign.
  - Clear units and transformation steps (from jet weight to stagnation pressure).
- Versioning and maintenance:
  - Calibration should occur every six months or before important campaigns; potential filter replacement if performance changes.
  - Data sharing and updates facilitated via uploading to relevant portals and catalogues.

## Data sharing and stewardship considerations
- Dataset is intended for discovery and reuse through CBESS portals and catalogue data holdings.
- Metadata integrates site, habitat, sampling regime, and device calibration specifics to support interoperability.
- Key governance considerations for data stewards:
  - Maintain consistent metadata standards across sites and campaigns.
  - Ensure calibration history is attached to each device and dataset version.
  - Document any data gaps due to missing replicates or equipment issues.
  - Monitor and communicate any methodological changes (e.g., calibration equation adjustments) that affect comparability over time.

## References and provenance
- Foundational references informing methods and calibration:
  - Tolhurst et al. (1999) measuring in situ erosion shear stress with CSM.
  - Vardy et al. (2007) calibration of high-pressure CSM; data checking and file formats guidance.
  - Paterson (1989) device description and subsequent applications (e.g., Tolhurst et al., Defew et al., etc.).
- Data documentation notes include CSV data structure and replication metadata as part of the calibration and QA framework.