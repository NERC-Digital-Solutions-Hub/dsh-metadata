# Sediment collection

## Overview
- Long-term sediment sampling at Rostherne Mere (May 2010–Sept 2016) using sequencing traps and a piston corer for a sediment core.
- Traps deployed at 10 m and 25 m water depth, with 12 individual 250 ml bottles representing 2-week collection periods (longer periods in Jan–Feb).
- Samples stored cold, dark, sealed during transport; core stored vertically at 5°C before sectioning for analysis.
- A 112 cm sediment core collected at 26 m depth (Sept 2011) with vertical sectioning for 1 cm intervals (top 50 cm) then 0.5 cm intervals.

## Sampling design
- Traps: automatic sequencing traps (Technicap PPS 4/3) with defined trapping ratio and area; trap contents split into 12 bottles per collection interval.
- Core: Livingstone piston corer used; core transported and stored vertically to preserve stratigraphy.

## Laboratory analysis and calibration
- All samples freeze-dried prior to analysis.
- Organic matter (OM) determined by loss-on-ignition (LOI) at 550°C for 3 hours; organic carbon (OC) calculated from LOI using a lake-specific factor (OC = OM × 0.56).
- Calibration records provided for OC/TOC relationships and elemental analyses (Cs for C, N, and C/N calibrations) with multiple sample references.
- 210Pb activity measured by alpha spectrometry to establish chronology using the CRS (constant rate of supply) model; confidence intervals derived from counting uncertainty.

## Data products and structure
- The dataset comprises three CSV files:
  - RMLOItoTOC
  - RMSedCore2011LOI
  - RMTrapSed

## Data fields and units
- RMLOItoTOC (9 columns)
  - SampleNo., d13C, C, N, C/N, Trap/core, Depth, LOI, C/LOI
- RMSedCore2011LOI (7 columns)
  - AverageDepth(cm), Water, Calcium_Carbonate(CaCO3), LOI, EstimatedDate(AD), SedimentationRate(g cm^-2 yr^-1), FocusingCorrectedOrganicCarbon(g m^-2 yr^-1)
- RMTrapSed (14 columns)
  - SampleCode, DateIn, DateOut, ShallowTrap/DeepTrap, Calcium_Carbonate(CaCO3), LossOnIgnition, MinerogenicFraction, DaysCollecting, TotalSampleDryWeight(g), TrapArea(m^2), FluxOrganicMatter(g m^-2 d^-1), FluxOrganicCarbon(g m^-2 d^-1), FluxCaCO3(g m^-2 d^-1), MinerogenicFlux(g m^-2 d^-1)

## Chronology and interpretation
- 210Pb dating used to determine sediment accumulation rates for the core samples via CRS model.
- Age interpretation linked to estimated dates and sedimentation rates, enabling historical context for OC, CaCO3, LOI, and other fractions.

## Data quality, standards, and access
- Data include calibration constants and lake-specific OC conversion factors; explicit metadata on sample depths, trap depths, and collection periods to support reproducibility.
- Quantities reported as percentages (water, LOI, CaCO3, minerogenic fraction) and fluxes in relevant units (g cm^-2 yr^-1 for core sedimentation and g m^-2 d^-1 for trap fluxes).
- Clear documentation of sample identification codes, depths, and dates to ensure traceability across the three data files.

## References
- APPLEBY, P. G. 2001. Chronostratigraphic techniques in recent sediments.
- DEAN, W. E. 1974. Determination of carbonate and organic matter by LOI.
- WRIGHT, H. E. 1967. A piston sampler for lake sediments.