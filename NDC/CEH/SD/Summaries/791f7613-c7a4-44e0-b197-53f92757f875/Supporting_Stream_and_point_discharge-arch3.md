# Supporting information

- Objective and study scope
  - Blelham Tarn hydrological monitoring to derive discharge for four streams (three inflows: Wray Beck, Fish Pond Beck, Ford Wood Beck; one outflow: Blelham Beck) and to understand water levels, temperatures, and related dynamics.
  - Data collected to support understanding of inflow–outflow relationships and to inform environmental monitoring decisions.

- Data collection and instrumentation
  - Water level, depth, and water temperature recorded every 15 minutes at the Blelham Beck outflow using an In-Situ Level TROLL logger.
  - A logger on the bank of Wray Beck recorded air temperature and atmospheric pressure to adjust water level pressure readings.
  - Monthly quality checks of downloaded logger data.
  - Detailed stream surveys at inflows/outflow to determine stream geometry; bank-full depth measured every 10 cm.
  - Flow velocities measured with a SonTek handheld Acoustic Doppler Velocimeter (ADV) at 3–4 evenly spaced locations per inflow/outflow; measurement locations adjusted to avoid bedload obstructions.

- Data processing and discharge calculations
  - Mean-Section Method (Qseg) used: Qseg = 0.5(v1+v2) × 0.5(d1+d2) × b, where v is velocity, d is depth, and b is the number of segments.
  - Mean discharge per stream (Q) calculated by summing Qseg across segments and dividing by the number of segments.
  - A rating curve (discharge vs. water level) developed for the outflow; relationship fitted with a polynomial (R^2 = 0.8162).
  - Daily discharge for the outflow converted to inflow discharges using the rating curve; remaining inflows related to the outflow discharge via linear relationships (Table 1) with corresponding R^2 values.
  - An alternative approach for inflow discharges used a proportional split of the outflow: Wray Beck 26.35%, Fish Pond Beck 49.22%, Ford Wood Beck 24.43%.

- Data products and structure
  - BLEL_Stream_Discharge.csv: Date; discharge (m3/s) for Blelham Beck (outflow) and the three inflows (Wray Beck, Fish Pond Beck, Ford Wood Beck).
  - BLEL_water_level_temp.csv: DateTime; water level pressure (kPa); temperature (°C); depth (cm); barometric pressure (kPa); stream label (outflow or inflow).
  - BLEL_point_discharge.csv: Date; Stream name; discharge (m3/s) at specific points.
  - Instruments: Level Troll data logger at the outflow; SonTek ADV handheld flow meter.

- Figures and tables
  - Fig. 1: Map of Blelham Tarn and inflows/outflow.
  - Fig. 2: Rating curve for Blelham Beck.
  - Table 1: Linear regression equations relating outflow discharge to inflow discharges (S1–S4) with R² values.

- References and methodological basis
  - Shaw, E. M., Beven, K. J., Chappell, N. A., and Lamb, R. (2011). Hydrology in Practice. Chapter 7: River Flow.