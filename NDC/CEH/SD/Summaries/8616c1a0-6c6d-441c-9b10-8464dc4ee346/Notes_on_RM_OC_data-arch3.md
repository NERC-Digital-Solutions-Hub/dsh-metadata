# Sediment collection

- Study site and period: Rostherne Mere, May 2010 to September 2016.
- Sampling method: Technicap PPS 4/3 automatic sequencing traps deployed at 10 m and 25 m water depths; each trap channels sediment into 12 individual 250 ml HDPE bottles representing a 2-week collection period (longer periods of up to 4 weeks in January–February).
- Trap handling: Traps reset every 6 months; trap sediment kept cool, dark, and sealed during transport; samples stored frozen prior to analysis.
- Sediment core: A 112 cm long sediment core collected at 26 m depth in September 2011 using a Livingstone piston corer; core stored vertically in a cold room and analyzed by sectioning (1 cm intervals for the upper 50 cm, then 0.5 cm intervals thereafter).

# Sediment analysis

- Pre-treatment: Freeze-drying of trap and core samples; homogenisation.
- Organic matter (OM): Determined by sequential loss-on-ignition (LOI) with weight loss after 3 hours at 550°C.
- Organic carbon (OC): Calculated from %OM using a lake-specific conversion factor (%OC = %OM × 0.56) derived from analysis of 20 samples with varying OM; total OC validated by mass spectrometry.
- Isotopes and calibration: d13C values obtained by mass spectrometry; calibration results provided for reference materials (e.g., SOIL B and BROC2) with associated C_cal, N_cal, C/N, etc.
- Chronology and accumulation: 210Pb activity measured by alpha spectrometry to determine sediment age and accumulation rates using the CRS (constant rate of supply) model; confidence intervals from counting uncertainty.
- Data notation: Records include water content (LOI), CaCO3 (calcium carbonate), and minerogenic fraction; sedimentation fluxes derived from LOI, OC, and sedimentation rates.
- Outputs: Focused organic carbon burial rate (Focussing corrected) in g C m^-2 yr^-1 where applicable; blank entries indicate samples not analysed.

# Nature and Units of Recorded Values

- Recorded variables include: water, LOI, CaCO3, minerogenic fraction; OC and C/N, C/LOI ratios; sedimentation rates and fluxes.
- Units:
  - LOI, CaCO3, water percentage values (weight-based percentages).
  - Sedimentation rates: g cm^-2 yr^-1 (core) and g m^-2 d^-1 (traps).
  - Fluxes: g m^-2 d^-1 for organic matter, organic carbon, CaCO3, and minerogenic material.
  - OC, C, N, C/N, C/LOI: percentage values or ratios as specified.

# Details of the Data Structure

- RMLOItoTOC (9 columns):
  - SampleNo., d13C, C, N, C/N, Trap/core, Depth, LOI, C/LOI
- RMSedCore2011LOI (7 columns):
  - AverageDepth(cm), Water, Calcium_Carbonate(CaCO3), LOI, EstimatedDate(AD), SedimentationRate(gcm2yr-1), FocussingCorrectedOrganicCarbon(gm2yr-1)
- RMTrapSed (14 columns):
  - SampleCode, DateIn, DateOut, ShallowTrap/DeepTrap, CaCO3, LossOnIgnition, MinerogenicFraction, DaysCollecting, TotalSampleDryWeight(g), TrapArea(m2), FluxOrganicMatter(gm2d-1), FluxOrganicCarbon(gm2d-1), FluxCaCO3(gm2d-1), MinerogenicFlux(gm2d-1)

- Data interpretation notes:
  - Sample coding identifies whether the sample came from shallow (10 m) or deep (25 m) traps or from the sediment core depth.
  - Flux calculations rely on trap area, total collection days, and captured sample mass.
  - Some fields may be blank if a sample was not analysed.

# References

- APPLEBY, P. G. 2001. Chronostratigraphic techniques in recent sediments. In: Last, W. M. & Smol, J. P. (eds.) Tracking Environmental Change Using Lake Sediments. Vol. 1.
- DEAN, W. E. 1974. Determination of Carbonate and Organic-Matter in Calcareous Sediments and Sedimentary-Rocks by Loss on Ignition.
- WRIGHT, H. E. 1967. A square-rod piston sampler for lake sediments.