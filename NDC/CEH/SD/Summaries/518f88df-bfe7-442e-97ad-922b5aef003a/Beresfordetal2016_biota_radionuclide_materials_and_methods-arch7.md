# Materials and Methods for: Radionuclide data for vertebrates in the Chernobyl Exclusion Zone, Gaschak, S.P., Beresford, N.A., Barnett, C.L., Wells, C., Maksimenko, A. and Chaplow, J.S. NERCEnvironmental Information Data Centre. doi: https://doi.org/10.5285/518f88df-bfe7442e-97ad-922b5aef003a, 2018.

## Overview
- Presents radionuclide data for vertebrates within the Chernobyl Exclusion Zone (CZ), including additional unreported bat data around CZ and data for ground-dwelling small mammals from Beresford et al. (2008) and Beresford et al. (2016).
- Provides context for data collection sites, sampling populations, and analytical methods used to quantify radionuclide concentrations.

## Data Content
- Biota_radionuclide_data.csv includes whole-body concentrations of 137Cs and 90Sr for birds, bats, and ground-dwelling small mammals, with additional data for Pu isotopes.
- Some data are from the main Beresford et al. (2016) site (approx. 8 km west of the Chernobyl plant) and extended data from other CZ sites (2004–2007 and 2005–2008 for different species).
- Soil activity concentrations (from Beresford et al. 2008) are provided for context, including 137Cs, Pu isotopes, and 90Sr, across multiple sampling sites.

## Spatial and Sampling Scope
- Primary study site: ~8 km west of the Chernobyl power plant; woodland types include Scots pine, oak, rowan, lime, with sparse understorey (bracken).
- Soil sampling area: 200 m x 200 m (40,000 m2), with soils collected up to 50 m beyond animal sampling area to reflect likely home ranges.
- Vertebrate sampling included:
  - Passerines captured by mist nets at the main site (June 2005), euthanised, and stored frozen.
  - Bats (May–June 2008) captured via mist nets; some additional bats collected 2004–2007 across CZ.
  - Ground-dwelling small mammals; samples collected from various CZ sites (and extended data for species not in 2008 Beresford paper).

## Data Collection and Analysis Methods
- Sample preparation:
  - Birds: GIT removed; general processing; samples weighed and washed.
  - Bats: GIT removed.
  - Ground-dwelling small mammals: pelt and GIT removed.
- Radiometric measurements:
  - 137Cs and 90Sr (whole-body) measured using a high-purity germanium detector (137Cs) and a thin-film NaI scintillation detector (90Sr via 90Y).
  - 137Cs spectra analyzed with Canberra Genie-2000 software.
  - 90Sr concentration derived from 90Y daughter nuclide.
  - Counting times ranged from 150 to 1200 seconds, depending on activity.
  - Counting errors typically <3% for 90Sr and <7% for 137Cs.
- Pu isotopes:
  - Samples dissolved in 65% HNO3; 242Pu added as a yield tracer.
  - Anion exchange (BioRad AG 1 x 8, 100–200 mesh) and co-precipitation used for purification.
  - Counts obtained with a planar ion-implanted silicon detector.
  - Counting errors typically <20% for Pu isotopes.
- Method validation:
  - Calibration against phantoms containing 137Cs and 90Sr.
  - Validation against traditional radiochemical methods (as per Bondarkov et al. 2011 reference).

## Soil Data
- Beresford et al. (2008) details for soils (n = 23) from the Medium site and two other sites:
  - Soil area represented at 200 m x 200 m around trapping areas.
  - Reported mean ± SD activity concentrations:
    - 137Cs: 43.3 ± 25.7 kBq kg−1 dry mass
    - Pu isotopes (238,239,240Pu): 0.83 ± 1.49 kBq kg−1 dry mass
    - 90Sr: 18.6 ± 14.9 kBq kg−1 dry mass
  - Spatial patterns: variable but no clear spatial pattern across the sampling site.
- Contextual soil data also described for other sampling sites in Beresford et al. (2008).

## Data Quality and Provenance
- Data collection and analysis procedures are documented with calibration and validation references (Bondarkov et al. 2011; Gaschak et al. 2010; Beresford et al. 2008; Beresford et al. 2016).
- Expanded datasets include species not originally reported in Beresford et al. (2008) and additional bat data from across CZ (2004–2007).

## GIS and Data Integration Considerations
- Spatially explicit data across multiple CZ sites with varying years necessitate careful temporal alignment when map-visualizing trends.
- Soil context data support correlation analyses between environmental radionuclide levels and vertebrate tissue concentrations.
- Data can be integrated with habitat and land-cover layers (e.g., woodland types, soil types) to assess spatial patterns of radionuclide transfer to vertebrates.
- Resolution considerations:
  - Site-level and area-based (200 m x 200 m) scales for soils; individual-level tissue concentrations for vertebrates.
  - Spatial extents suitable for regional CZ analyses and for examining habitat associations.

## References
- Beresford, N.A., Gaschak, S., Barnett, C.L., Howard, B.J., Chizhevsky, I., Strømman, G., Oughton, D.H., Wright, S.M., Maksimenko, A., Copplestone D. 2008. Estimating the exposure of small mammals at three sites within the Chernobyl exclusion zone - a test application of the ERICA Tool. J. Environ. Radioact. 99, 1496-1502.
- Beresford, N.A., Gaschak, S., Maksimenko, A., Wood, M.D. 2016. The transfer of 137 Cs, Pu isotopes and 90 Sr to bird, bat and ground dwelling small mammal species within the Chernobyl exclusion zone. J. Environ. Radioact. 153, 231-236.
- Bondarkov, M.D., Maksimenko, A.M., Gaschak, S., Zheltonozhsky, V.A., Jannik, G.T., Farfán, E.B., 2011. Method for simultaneous 90 Sr and 137 Cs in-vivo measurements of small animals and other environmental media developed for the conditions of the Chernobyl exclusion zone. Health Phys. 101, 383-392.
- Gaschak, S., Beresford N.A., Maksimenko A., Vlaschenko A.S. 2010. Strontium-90 and caesium-137 activity concentrations in bats in the Chernobyl exclusion zone. Radiation Environ Biophys. 49, 635-644.