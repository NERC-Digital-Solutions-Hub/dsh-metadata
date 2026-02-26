# Materials and methods for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, 2018, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERCEnvironmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7442e-97ad-922b5aef003a

## Aim
- Document the collection and analysis methods for radionuclide data in vertebrates and soils within the Chernobyl Exclusion Zone to support exposure assessment and data reuse.

## Study design and data collected
- Site layout and sampling
  - Three forest sites (Low, Medium, High) with anticipated differing soil radionuclide activity.
  - 100 m × 100 m study area at each site; 10 m interval posts used to place small mammal traps.
  - GPS used to record trapping point locations; soil sampling extended 50 m beyond trapping area to cover likely animal home ranges.
- Soil measurements
  - Gamma-kerma rates measured at 5 cm above ground at each trapping point (MKS-01R-01 dose rate meter with BDKB-01R detector); three 10 s measurements per point; mean used.
  - 23 soil samples per site (depth 10 cm); dry and homogenised; samples split for radionuclide analysis.
  - Sample mass: ~750 g dry weight per sample (Medium/Low sites) and ~130 g DW per sample (High site).
  - Radionuclide analyses:
    - Gamma-emitting nuclides: analysed by high-purity germanium detectors; Genie-2000 software; count times chosen to achieve <20% error on 40K.
    - Plutonium isotopes (238,239,240Pu): Lx-radiation method (13–23 keV) on 10 g DW sub-samples; absorption correction via Ba K X-ray method; detection limit 3–5 Bq; accuracy 10–15%.
    - Strontium-90 (90Sr): measured via 90Y decay using 1 mm NaI detector; calibration described in Bondarkov et al. (2002c).
- Small mammal trapping and radionuclide analysis
  - Trapping conducted on 14 occasions (early July to mid-August 2005) with 100 Sherman humane traps per site.
  - Species targeted: Apodemus flavicollis, Myodes glareolus, Microtus spp.
  - Each first capture fitted with a LiF-100 thermoluminescent dosimeter (TLD) collar; collar data logged and related to whole-body 137Cs and 90Sr.
  - Whole-body radionuclide analysis:
    - 137Cs and 90Sr measured after live monitoring using a lead-shielded counting container with Ge detector (137Cs) and NaI detector (90Sr via 90Y).
    - Count duration: 150–1200 s (depending on activity level).
  - Post-release monitoring:
    - If recaptured >14 days after collar fitting, TLD removed and reweighed; re-measured for 137Cs and 90Sr.
    - If recaptured ≤14 days, capture location recorded and released (additional Cs measurements where available).
    - In last two weeks, TLDs removed if recaptured within 6 days.
  - Collar deployment scale:
    - 230 TLD collars fitted; 85 recovered (durations 6–36 days).
    - Seven TLDs were shipped from the UK to the Chernobyl lab as controls.
- TLD deployment experiments at four random points per site
  - TLDs positioned at three vertical levels: 5 cm above ground, ground level, and 10 cm deep in soil.
  - At each position, one TLD prepared as standard and a second encapsulated in a Perspex cube (2 × 2 × 2 cm).
  - 25 of 36 paired TLDs recovered; remainder lost.
  - Recovered TLDs returned to supplier for analysis with site TLDs.

## Data processing and software
- Gamma spectra analyzed with Genie-2000 software; 40K estimates with <20% error target.
- Geospatial data collected via handheld GPS; trap locations and soil sampling points tied to site maps.
- TLD data linked to individual animals (collar IDs) and trapping events; recapture intervals tracked.

## Data quality, uncertainty, and provenance
- Uncertainty/limits:
  - 40K activity uncertainty targeted to be <20%.
  - Pu isotope measurements: accuracy 10–15%; detection limits 3–5 Bq (via Lx method).
  - Calibration and validation referenced to Bondarkov et al. (2002a–d).
- Quality controls:
  - Use of UK-based control TLDs for methodological consistency.
  - Standardization across sites for trap density and sampling geometry.

## Data products and potential reuse
- Datasets likely produced:
  - Site-level soil radionuclide activity concentrations (238,239,240Pu; 90Sr; 40K; other gamma emitters).
  - Gamma dose-rates at multiple trapping points per site.
  - Small mammal data: species, capture date, trap location, collar ID, body weight, and whole-body 137Cs and 90Sr concentrations.
  - TLD-derived exposure records for tracked animals, including duration on animals and reading results.
  - Spatially explicit maps of radionuclide distributions and exposure indices by site and time point.
- These data support exposure assessment for vertebrates in the Chernobyl Exclusion Zone and can be reused for cross-study comparisons, meta-analyses, and correlation with habitat or soil radionuclide profiles.

## Limitations and challenges
- Patchy or variable data due to field conditions (e.g., some TLDs not recovered; differences in soil mass per sample and site conditions).
- Recapture rates and collar retention influenced long-term data continuity.
- Some TLDs were lost or delayed, affecting complete time-series coverage at all points.

## References and methodology context
- Primary methods drawn from Bondarkov et al. (2002a–d) for Pu and Sr determinations and QA context.
- Related methodological background drawn from Estimating the exposure of small mammals at three sites within the Chernobyl exclusion zone (Beresford et al., 2008).