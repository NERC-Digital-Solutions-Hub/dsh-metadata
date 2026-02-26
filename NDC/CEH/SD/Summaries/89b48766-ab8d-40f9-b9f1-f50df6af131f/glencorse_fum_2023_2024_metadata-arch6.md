# Ammonia enhancement data from Glencorse experimental site near UKCEH, Edinburgh (2023-2024)

## Purpose and scope
- Ammonia (NH3) enhancement experiment to study effects of high atmospheric NH3 on forest vegetation, bryophytes, lichens, and soil in Glencorse woodland near Edinburgh.
- Established in 2021; extension dataset covers 2023-2024 (extension of 2021-22 data).

## Data collection and experimental setup
- Location: Glencorse woodland (Birch plantation), near Edinburgh (coordinates provided in the study).
- Control system: NH3 release triggered only under specific wind conditions (wind direction 275–345° and threshold speeds 0.3–10 m/s).
- Release hardware: three horizontal PVC tubes (20 m each, 110 mm OD) at ground levels 0.5, 1.35, and 2.2 m; six holes per tube at 20 cm intervals; NH3 delivered via a central manifold and a mass flow controller (MFC) with a solenoid valve.
- Gas handling: pure anhydrous NH3 from a cylinder; injections diluted by the airflow to release NH3 through tubes.
- Sensing and logging: WXT536 weather station for wind data; MFC logs NH3 volume released every 20 seconds; 15-minute averages computed.
- Data timeframe: 1 January 2023 – 31 December 2024, all in GMT.

## Dataset details
- Structure: CSV dataset with 6 columns (Timestamp + 5 measured parameters).
- Measurements: 68,396 records at 15-minute intervals.
- Parameters (with units and descriptions):
  - Timestamp (formatted dd/mm/yyyy hh:mm)
  - NH3_status (Minutes): time NH3 is released; instrument: Type 6027 solenoid valve; manufacturer: Bürkert.
  - NH3_flow_set (slpm): NH3 flow set point for prevailing wind conditions; instrument: G series MFC; manufacturer: MKS Instruments.
  - NH3_flow (slpm): NH3 flow into the release manifold; instrument: G series MFC; manufacturer: MKS Instruments.
  - Wind_speed (ms^-1): below-canopy wind speed; instrument: WXT536; manufacturer: Vaisala.
  - Wind_direction (degrees): below-canopy wind direction; instrument: WXT536; manufacturer: Vaisala.

## Quality control and limitations
- Visual data checks performed; obvious instrument/recording issues removed.
- Gaps present due to replacement of faulty gas-control components.

## Temporal and data provenance
- Data cover 2023-01-01 to 2024-12-31.
- Extends and complements earlier 2021-22 dataset from the same site.

## Data usage and related publications
- Related work includes estimation of ammonia deposition to forest ecosystems and meteorological/concentration/deposition data from the Glencorse site (Deshpande et al., 2024a, 2024b).
- Data useful for modeling NH3 enhancement effects, deposition estimates, and cross-site comparisons.

## Funding
- UKRI GCRF South Asian Nitrogen Hub.
- UKCEH National Capability for UK Challenges Programme NE/Y006208/1.