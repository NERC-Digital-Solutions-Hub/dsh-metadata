# GR6J model estimates of daily river flows at 95 river catchments in Great Britain - EC-Earth large ensemble (climate model) driving data

- Purpose and scope: A dataset of GR6J-modeled daily river flows for 95 Great Britain catchments, driven by precipitation and PET from the EC-Earth SMILE large ensemble, spanning present-day and warming scenarios (2°C and 3°C above pre-industrial).
- Ensemble and time coverage: EC-Earth GCM v2.3 with large ensemble approach; for each ensemble member, 25 realizations across 5 years, pooled to 2000 years per warming level (PD, 2C, 3C). The best-performing GR6J parameter set for each catchment drives the flows.
- Catchment selection: 100 catchments from the Low Flow Benchmark Network (LFBN) within GB plus 10 additional key public water supply catchments in East Anglia.
- Model calibration and evaluation: GR6J calibrated with Latin Hypercube Sampling (10,000 parameter sets) across six performance metrics (NSE high, NSE range, logNSE low, PBIAS, MAPE, Q95 APE, MAM30 APE). The top parameter set is selected per catchment based on a total rank score, using observed precipitation (CEH-GEAR) and observed temperature (CEH-CHESS); PET computed with UK calibration.
- Climate data and bias adjustment: Precipitation bias-adjusted multiplicatively to match monthly observed means; temperature bias-adjusted additively; a power transformation applied to preserve CV; PET derived from bias-adjusted temperature. Fidelity testing (Thompson et al. 2017) confirms 95 of 100 catchments pass the criterion that model statistics are statistically indistinguishable from observations (via bootstrapped samples).
- Data products and formats: 
  - 95 catchment-specific CSV files for each warming level, organized in PD (present-day), 2C, and 3C directories.
  - Two file types per catchment: 
    - LE_Flow_<NRFA catchment ID>.csv containing simulated river flows (Qsim) and metadata (Catch_id, Ens_member, Realisation).
    - LE_Input_<NRFA catchment ID>.csv containing driving data (Precip, PET, Temp) plus identifiers (Catch_id, Ens_member, Realisation).
  - Each file contains 730,400 rows (2000 years of daily data) across corresponding columns; one file per catchment per warming level, totaling 285 files across all levels.
  - File naming and structure: 
    - Qsim files located in LE_Flow_<NRFA catchment ID>.csv
    - Driving data files located in LE_Input_<NRFA catchment ID>.csv
- Data organization and accessibility: Data are organized by warming level in separate folders; driving data and simulated flows are stored in parallel directories (Qsim and Driving_data) with consistent Catch_id and ensemble metadata (Ens_member, Realisation). Each catchment has a unique NRFA ID, enabling straightforward joins to GIS attributes or spatial layers.
- Provenance and acknowledgments: Produced as part of a PhD project supported by the Natural Environment Research Council via the SCENARIO Doctoral Training Partnership (grant NE/S007261/1).
- References and methodological context: Methods and datasets underpinning model calibration, bias adjustment, and fidelity testing are drawn from multiple UK hydrology and climate literature, including eFLaG, UKCP18-based studies, and associated validation techniques (citations provided in the document).