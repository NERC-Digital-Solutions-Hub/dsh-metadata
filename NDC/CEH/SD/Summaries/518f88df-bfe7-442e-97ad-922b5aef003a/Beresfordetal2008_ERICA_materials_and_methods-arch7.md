# Materials and methods for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERCEnvironmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7442e-97ad-922b5aef003a

## Objective and scope
- Document the data collection and analytical methods used to assess radionuclide activity in soils and small mammals within the Chernobyl Exclusion Zone.
- Provide a methodology framework for estimating exposure in small mammals, with results enabling map-based representation of contamination and dose indicators.

## Study design and sites
- Three forest sites chosen to represent differing soil radionuclide activity: Low, Medium, and High.
- Each site defined a 100 m × 100 m study area using posts at 10 m intervals; trapping points located within this grid.
- Site distances from Chernobyl reactor complex: Low ~8.5 km SE; Medium ~8 km W; High ~5 km W.

## Field data collection
- Gamma-kerma (dose rate) measured at 5 cm above ground at trapping points using MKS-01R-01 with BDKB-01R detector; three 10 s readings per point.
- Trapping and sampling layout:
  - 14 trapping occasions (July–August 2005).
  - 100 Sherman humane traps per site, baited with rolled oats, placed at marker posts.
  - Traps revisited next day; captured animals transported to local lab.
  - Geographic position of trapping points recorded with handheld GPS.
- Soil sampling:
  - 23 samples per site, depth 10 cm, extended 50 m beyond trapping area to capture likely home ranges.
  - Samples dried, homogenised; small subsamples analysed for gamma-emitting radionuclides.
- Trapped species (processed): Apodemus flavicollis (yellow-necked mouse), Myodes glareolus (bank vole), Microtus spp. (vole).
- Live monitoring and tagging:
  - First capture of an animal resulted in a numbered collar with a LiF-100 thermoluminescent dosimeter (TLD) attached.
  - Live-weight recorded; whole-body 137Cs and 90Sr measured.
  - Animals released at their trap location; recapture rules applied for TLD handling (see below).
  - 230 TLD collars fitted; 85 recovered (6–36 days deployment).
  - Seven TLD collars shipped from the UK as controls.
- TLD deployment variants:
  - At four randomly selected points per site, place TLDs at 5 cm above ground, at ground level, and 10 cm deep in soil. One paired TLD was encapsulated in Perspex for each position. 25 of 36 paired TLDs recovered; rest lost.

## Laboratory analysis and radionuclide measurements
- Soil and animal measurements:
  - Whole-body 137Cs and 90Sr in small mammals measured via detector setup with lead shielding and dual detectors (germanium for 137Cs; thin-film NaI for 90Sr via its daughter 90Y).
  - 137Cs spectra analysed with Genie-2000 software.
  - 90Sr concentration derived from 90Y activity; calibration against phantoms and radiochemical analyses validated the method (Bondarkov et al. references).
- Specific methods:
  - 238,239,240Pu in soils determined in 10 g dry weight sub-samples using Lx-radiation method after α-decay; absorption correction based on Ba K x-radiation; reported detection limit ~3–5 Bq; accuracy ~10–15%.
  - 90Sr in soils determined in 10 g DW subsamples via 90Y measurement using a thin-film NaI detector; calibration described by Bondarkov et al.
- Count times:
  - For animal measurements, count times ranged from 150 to 1200 s depending on radioactivity levels.
  - Gamma- and radiochemical procedures previously validated against standard radiochemistry methods.

## Data processing, quality, and provenance
- Calibration and validation:
  - 40K estimates constrained to <20% error through appropriate count times.
  - Lx-method and 90Sr methods validated against radiochemical standards.
- Recapture and data integrity:
  - If recaptured >14 days after collar fitting, TLD removed and animals reweighed with follow-up Cs and Sr measurements.
  - If recaptured ≤14 days, only trapping location recorded; additional measurements where available.
  - In last two weeks, TLDs removed if recaptured within 6 days of fitting.
- Data scope and linking:
  - Temporal frame mainly July–August 2005; multiple recapture events captured for exposure dynamics.
  - Data linked to soil measurements, trapping locations, animal captures, and TLD readings for integrated exposure assessment.

## GIS-ready data considerations and outputs
- Spatial elements:
  - Trapping points with GPS coordinates; soil sampling locations within a 50 m extension beyond trapping area.
  - TLD deployment positions (5 cm, ground level, 10 cm depth) and control TLDs.
- Data layers suitable for mapping:
  - Site-level gamma-kerma/dose-rate surfaces.
  - Soil radionuclide activity concentrations (137Cs, 90Sr, Pu isotopes, 40K as applicable).
  - Animal-level whole-body radionuclide burdens (137Cs, 90Sr) and TLD-derived exposure indicators.
  - Temporal/duration aspects, including recapture events and TLD deployment durations.
- Metadata and data standards:
  - Experimental design rationale linked to exposure modelling (ERICA tool context).
  - References for methods and calibration (Bondarkov et al.; ERICA-related literature).

## Limitations and considerations for GIS
- Variability in sample masses and detection limits across sites (e.g., ~750 g DW per soil sample for Medium/Low vs ~130 g DW for High).
- Random sampling and potential losses of TLDs introduce gaps that must be documented in GIS datasets.
- Differences in field effort and recapture intervals influence temporal resolution of exposure estimates.

## References
- Bondarkov, M., Zheltonozhsky, V., Sadovnikov, L., Strilchuk, N., 2002a. Determining Plutonium isotopes content in Chornobyl samples based on Uranium characteristic Lx-radiation.
- Bondarkov, M.D., Maximenko, A.M., Zheltonozhsky, V.A., 2002b. Non radiochemical technique for 90Sr measurement.
- Bondarkov, M., Maximenko, A., Zheltonozhsky, V., Sadovnikov, L., et al., 2002c. Studying vertical migration of 90Sr by non radiochemical technique.
- Bondarkov, M.D., Gaschak, S.P., Goryanaya, Ju.A., et al., 2002d. Parameters of Bank vole decontamination from radiocesium and radiostrontium.
- Beresford, N.A., et al., 2008. Estimating the exposure of small mammals at three sites within the Chernobyl exclusion zone - a test application of the ERICA Tool.