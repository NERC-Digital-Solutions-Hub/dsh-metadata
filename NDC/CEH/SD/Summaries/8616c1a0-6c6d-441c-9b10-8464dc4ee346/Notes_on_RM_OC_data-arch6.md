# Sediment collection

## Overview
- Study period: May 2010 to September 2016.
- Methods: Sediment trapping using Technicap PPS 4/3 automatic sequencing traps deployed at 10 m and 25 m depths; each trap feeds into 12 individual 250 ml HDPE bottles representing a 2-week collection period (longer periods of up to 4 weeks used in January–February).
- Sampling cadence: Traps reset every 6 months; trap sediment kept cool, dark, sealed during transport and stored frozen prior to analysis.
- Sediment core: A 112 cm core collected at 26 m depth in September 2011 using a Livingstone piston corer; stored vertically in a dark cold room at 5°C, extruded at 1 cm intervals for the top 50 cm and 0.5 cm intervals thereafter.
- Objective: Characterise sediment composition and accumulation to support later data analysis and interpretation.

## Sediment analysis methods
- Sample preparation: All trap and core samples freeze-dried before analysis.
- Organic matter (OM) and organic carbon (OC):
  - OM determined by loss-on-ignition (LOI) at 550°C for 3 hours.
  - %OC calculated from %OM using a lake-specific conversion factor %OC = %OM × 0.56.
  - Calibration data provided for converting LOI to OC (examples include d13C_cal and C_cal/N_cal values for specific samples such as SOIL B and BROC2).
- Chronology:
  - 210Pb activity measured by alpha spectrometry to determine sediment age and accumulation rates using the CRS (constant rate of supply) model; confidence intervals via first-order error analysis.
- Recorded variables (general focus):
  - Water content, LOI, CaCO3, minerogenic fraction, sedimentation rates, and fluxes.
  - Organic carbon burial rates with focussing correction.

## Data structure and files
- The dataset comprises three CSV files:
  - RMLOItoTOC
    - Columns: SampleNo, d13C, C, N, C/N, Trap/core, Depth, LOI, C/LOI.
  - RMSedCore2011LOI
    - Columns: AverageDepth(cm), Water, Calcium_Carbonate(CaCO3), LOI, EstimatedDate(AD), SedimentationRate(gcm2yr-1), FocusingCorrectedOrganicCarbon(gm2yr-1).
  - RMTrapSed
    - Columns: SampleCode, DateIn, DateOut, ShallowTrap/DeepTrap, Calcium_Carbonate(CaCO3), LossOnIgnition, MinerogenicFraction, DaysCollecting, TotalSampleDryWeight(g), TrapArea(m2), FluxOrganicMatter(gm2d-1), FluxOrganicCarbon(gm2d-1), FluxCaCO3(gm2d-1), MinerogenicFlux(gm2d-1).
- Data types and units:
  - Water content, LOI, CaCO3, and minerogenic fraction are percent values.
  - Sedimentation rates and various fluxes are given in g cm^-2 yr^-1, g m^-2 d^-1, or related per-surface-area units.
  - Depth references include trap depths (10 m and 25 m) and core depths (cm into the sediment).

## Provenance and references
- Datasets and methods align with established chronostratigraphic techniques in recent sediments.
- Key references cited for methods and calibration:
  - Appleby, P. G. 2001. Chronostratigraphic techniques in recent sediments.
  - Dean, W. E. 1974. Determination of Carbonate and Organic-Matter in Calcareous Sediments.
  - Wright, H. E. 1967. Piston sampler for lake sediments.

## Considerations for use
- Data cover multiple years with periodic collection gaps; some samples are not analyzed (blanks present in some fields).
- Data integrate trap-based flux measurements with core-based accumulation rates and organic carbon burial, suitable for self-serve exploration and comparative analysis with other lake sediment datasets.
- Calibration details (e.g., OC % conversion factor) are provided to support reproducibility and cross-dataset comparisons.