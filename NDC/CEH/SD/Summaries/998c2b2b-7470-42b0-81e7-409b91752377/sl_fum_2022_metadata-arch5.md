# Ammonia enhancement data from Queensberry experimental site in Sri Lanka (2022)

- Purpose and scope
  - Ammonia (NH3) enhancement experiment to study effects of high atmospheric NH3 on tropical forest vegetation, bryophytes, lichens, and soil.
  - Location: Queensberry Estate, central Sri Lanka; coordinates 6.9693° N, 80.5911° E; altitude 1645 m.
  - Timeframe: data collected from 13 March 2022 to 31 December 2022 (Sri Lanka Standard Time, SLST).

- Experimental design and data collection
  - NH3 release controlled by below-canopy wind conditions; releases occur only when wind direction is within 5–75° and 185–255° at threshold speeds (0.3–10 m s^-1).
  - Release system: three horizontally arranged 20 m tubes (110 mm OD) at 0.5, 1.35, and 2.2 m heights; six holes per tube at 20 cm intervals.
  - Gas delivery: pure anhydrous NH3 from a cylinder via a stainless steel manifold, pre-programmed mass flow controller (MFC) and solenoid valve; NH3 injected into fan airflow for dilution and release through tubes.
  - Control and monitoring: solenoid valve opens only under correct wind conditions; below-canopy wind data from a WXT536 weather station; NH3 release rate recorded by MFC every 20 seconds with 15-minute interval averaging.
  - Data format and timezone: all data provided in CSV with timestamps in SLST; dataset spans 13 March 2022 to 31 December 2022.

- Quality control and data curation
  - Visual quality checks performed; obvious instrument or programming errors removed.
  - Gaps noted due to replacement of faulty gas-control components and occasional power issues.

- Data structure and metadata
  - Total records: 28,257 measurements across 5 parameters.
  - Format: CSV file with structured columns and rich metadata for traceability.
  - Key columns and metadata fields (examples):
    - Timestamp (and 15-minute interval context)
    - NH3_status: status of NH3 release (OFF/ON) with instrument (Type 6027 solenoid valve), manufacturer (Bürkert), and description
    - NH3_flow_set: flow set point (slpm) with instrument (G series MFC), manufacturer (MKS Instruments), and description
    - NH3_flow: actual NH3 flow (slpm) with instrument and manufacturer details
    - Wind_speed: below-canopy wind speed (ms^-1) with instrument (WXT536), manufacturer (Vaisala), and description
    - Wind_direction: below-canopy wind direction (degrees) with instrument (WXT536), manufacturer (Vaisala), and description

- Data provenance and usage notes
  - Complete experimental design, methodology, analysis, and findings documented in Deshpande et al. (2024).
  - Funding: UKRI GCRF South Asian Nitrogen Hub.
  - Access and reuse: dataset is described for interoperability and reuse; metadata fields align with instrument origins and data lineage to support discovery and reproducibility.

- Reference
  - Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.