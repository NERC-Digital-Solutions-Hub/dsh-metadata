# CEH-GEAR1hr: Gridded Estimates of hourly Areal Rainfall for Great Britain (1990-2014)

- Purpose and scope
  - Provides 1-km gridded hourly rainfall estimates for Great Britain from 1990 onwards, originally 1990–2014 with planned annual updates.
  - Designed for hydrological modeling and environmental monitoring; aims to support policy scrutiny and decision-making.

- Access, citation, and provenance
  - Data accessible via the Environmental Information Data Centre (EIDC) with a DOI provided.
  - Must cite the dataset and associated publications when used.
  - Primary data sources include 1,903 UK rain gauges from Met Office MIDAS and national agencies (EA, NRW, SEPA), plus CEH-GEAR daily data; a QC process ensures data quality.

- Dataset description and coverage
  - Spatial: gridded to 1 km, covering Great Britain; daily minimum distance to a used gauge is recorded per grid cell.
  - Temporal: hourly rainfall from 1990 onward; daily and monthly backbone data from CEH-GEAR.
  - Metadata includes the minimum distance to the nearest gauge for each grid cell and whether statistical disaggregation was used.

- Data derivation and methods
  - Hourly grids derived by temporal disaggregation of CEH-GEAR daily data using hourly gauge data; nearest-neighbour interpolation preserves storm shapes.
  - Daily totals from CEH-GEAR are preserved when generating hourly estimates.
  - The hourly value for a grid cell corresponds to the rainfall accumulated in the preceding hour.
  - If the nearest gauge is >50 km away or if there is inconsistency between daily and hourly records, a statistical disaggregation using average storm shapes is applied (Table 1 describes average storm shapes by daily total and season).

- Minimum distance and representativeness
  - The dataset records the distance to the closest gauge for each grid cell per day.
  - Mean distance across the period is 11.3 km; maximum distance reaches ~97.7 km (notably on Scotland’s west coast).
  - A 50 km minimum distance threshold is used to avoid unrepresentative estimates; grid calculations are not performed when this threshold is exceeded.

- Statistical disaggregation
  - Used for grid cells more than 50 km from a gauge or when hourly data are missing but daily totals exist.
  - Zero rainfall in hourly records and grid cells far from gauges are two common disaggregation scenarios.
  - Proportions: zero-rainfall disaggregation occurs on up to ~26% of daily grids; distance-based disaggregation occurs on up to ~3% of grid squares (1990–2014 period).
  - Impact on diurnal cycle: the use of average storm shapes can bias diurnal analyses (e.g., peak at 10:00) and should be accounted for in analyses.

- Quality control and data integrity
  - A three-step QC process:
    1) Compare gauge data to the gridded CEH-GEAR daily dataset to identify suspect gauges.
    2) Apply automated QC tests (flags QC1–QC15) to suspect hourly values.
    3) Apply a rule base (R1–R20) to determine which flagged data are erroneous and should be removed (replaced with -999).
  - The QC procedures, flags, and rules are detailed in the associated literature; the full methodology is documented in Lewis et al. (2018).

- Gauge and grid filtering
  - Spearman rank correlation (r_s) > 0.8 and P11 + P00 > 0.8 are required after QC for gauges to be used in constructing the dataset.
  - These quality thresholds ensure reliable gauge-to-grid representations for inclusion.

- Use guidelines and caveats
  - Intended for hydrological modeling; users should consider:
    - Diurnal and hourly pattern biases due to statistical disaggregation.
    - Spatial “blocky” patterns from nearest-neighbour interpolation without smoothing.
    - The dataset’s metadata and disaggregation flags when conducting analyses that rely on true hourly variability or extreme-value estimation.
  - Validate analyses with the accompanying metadata and, if possible, sensitivity analyses to disaggregation choices.

- Data format and access
  - File format: NetCDF4, following CEH conventions.
  - Structure: monthly files (e.g., CEH-GEAR-1hr_199001 for January 1990) containing three variables:
    - Rainfall_amount: hourly rainfall in kg/m2 (equivalent to mm depth).
    - Stat_disag: indicator of whether statistical disaggregation was used (1) or not (0).
    - Min_dist: minimum distance to the nearest gauge used for that day (in meters).

- References and documentation
  - Key sources: Keller et al. (2015) for CEH-GEAR daily/monthly data; Lewis et al. (2018) for the CEH-GEAR1hr QC workflow; Met Office MIDAS data catalog entry.
  - Additional methodological papers detailing validation and disaggregation approaches.

- Practical implications for monitoring frameworks
  - Provides transparent data provenance, rigorous QC, and explicit metadata to support governance and data-sharing needs.
  - Emphasizes the importance of metadata in evaluating data suitability, especially regarding disaggregation effects and representativeness.
  - Highlights data governance considerations: open data availability, citation requirements, and the need to interpret hourly unfolds with awareness of disaggregation and interpolation methods.