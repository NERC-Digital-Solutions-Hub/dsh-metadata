Repeat electrical resistivity tomography (ERT) measurements to capture changing soil resistivity throughout the agricultural growing season

## Aim and scope
- Conduct repeat ERT measurements across four sites to monitor how soil resistivity changes with the agricultural growing season.
- Capture transitions between construction, production, and post-harvest stages (Spring/Summer/Autumn).
- Support the LAND MANAGEMENT in Lowland Catchments for Integrated Flood Risk Reduction (LANDWISE) NFM research project.
- Data collection points: April/May (initial), June/July (summer), September 2021 (final).

## Sites and deployment
- Four survey locations:
  - Lower Hampen Farm – Barn Ground
  - Lower Hampen Farm – Flat Ground
  - Manor Farm – Whittington Hill
  - Hendred Farm – Lockinge (Untraffic) and East Hendred (Traffic A/B)
- Each site had defined start and end coordinates to ensure repeatability.
- Fieldwork dates aligned with seasonal phases and site conditions.

## Methods and hardware
- 19 m ERT transects with 96 electrodes spaced 20 cm apart (Campus Tigre system).
- Data collection using a Wenner Array to obtain subsurface resistivity at both vertical and horizontal resolutions.
- Each traverse yielded approximately 660 apparent resistivity readings down to about 1 m below ground level (bgl).
- Field data collected with ImagerPro2006; processed with Geotomo’s Res2DInv.
- GNSS positioning (Leica) with ~0.01 m accuracy to ensure precise repeat surveys.

## Data specifics and measurement units
- Physical basis: Resistivity measurements reflect soil structure, interstitial water, and salts; Wenner Array geometry defines depth sensitivity (approximately a-spacing/2).
- Recorded values: Apparent Resistivity (Ohm·m).
- Data formats and organization:
  - Res2DInv format (example file: BarnGround_April.dat).
  - Key fields include: file name, electrode spacing (0.2 m), Wenner indicator, number of data points (660), mid-point x-location, and data point values.
  - Data points structured as: x-location, a-spacing, apparent resistivity, followed by 659 additional data points per traverse.
  - End-of-survey indicated by specific flags in the data file.

## Quality control and processing
- Pre-survey checks for electrode-ground contact to minimize noisy data.
- Re-establish poor electrode contact as needed in the field.
- Data cleaning and inversion performed in Res2DInv to remove noisy points before interpretation.

## Data governance, metadata, and openness
- Provenance and workflow are documented (field collection, equipment, and processing software) to support reproducibility.
- Data are stored in a standardized format (Res2DInv) with explicit metadata embedded in the file structure.
- The document does not specify public data sharing or broader data governance steps; adherence to metadata standards and data-sharing policies would influence accessibility for wider monitoring use.
- Outputs aim to support transparent reporting and stakeholder consultation within the LANDWISE project framework.

## Relevance for monitoring frameworks and policy
- Demonstrates a structured approach to temporal and spatial environmental health monitoring through repeat geophysical measurements.
- Provides high-resolution, site-specific soil resistivity data across multiple seasons to inform land management and flood risk reduction strategies.
- Emphasizes the importance of data quality, traceability, and standardized data formats in informing policy decisions and future monitoring plans.