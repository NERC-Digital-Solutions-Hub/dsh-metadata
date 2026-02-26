# Background exposure rates of terrestrial wildlife in England and Wales

- Aim
  - Categorise available data for naturally occurring radionuclides in England and Wales based on the ICRP-recommended reference animals and plants (RAPs) to assess potential radiation exposure of terrestrial wildlife.

- ICRP Reference Animal and Plant (RAPs) considered
  - Reference Deer; Reference Rat; Reference Duck; Reference Frog; Reference Bee; Reference Earthworm; Reference Pine Tree; Reference Wild Grass.
  - Two mammalian RAPs are highlighted by ICRP; data were collated for “any wild mammalian species” and separately for Deer and Rat.

- Data sources and availability
  - Reviewed data from: grey literature, refereed journal papers, and in-house databases.
  - Key data sources:
    - RIFE (Radioactivity in Food and the Environment) reports (UK-wide data 1995–2004), largely for edible components of wildlife or foods related to humans.
    - CEH (Centre for Ecology & Hydrology) analyses related to Chernobyl-derived radiocaesium and Sellafield discharges; gamma analyses included 40K data.
  - Rationale: many data were not specifically tied to the RAPs, so data were attributed to RAPs with defined mapping rules.

- RAP attribution rules
  - Duck → any wild bird
  - Frog → any amphibian
  - Bee → any flying insect
  - Earthworm → any earthworm
  - Pine Tree → any tree
  - Wild Grass → any wild grass or herb (and any data labeled as grass)
  - Deer → any wild deer
  - Rat → data for wild rat
  - Any wild mammal → broader “any wild mammal” category

- Targeted sampling and analyses (addressing data gaps)
  - Due to limited data for several RAPs, a targeted sampling campaign was conducted for:
    - Duck, Bee, Earthworm, Pine Tree, Frog
  - Samples relied on existing CEH archives when possible, supplemented by new sampling.
  - Collected samples included:
    - Flying insects (mostly moths) from Environmental Change Network sites
    - Lodgepole pine trunks
    - Grey heron liver (CEH Predatory Birds Monitoring Scheme)
    - Earthworms
    - Rabbits; toad; mallards
  - Wales representation: increased sampling of rabbits, mallards, lodgepole pine, and earthworms to improve coverage where data were sparse.

- Sample preparation and analyses
  - Preparation and homogenisation:
    - Lodgepole pine trunks washed and ashed at 450°C.
    - Earthworms evacuated of gut contents, freeze-dried and homogenised.
    - Insects supplied dry and homogenised.
    - Mallards plucked, gastrointestinal tract removed; liver analysed separately.
    - Rabbits skinned; carcasses washed and ashed; bones, claws, and GI tract removed.
    - Heron and mallard liver samples freeze-dried and homogenised.
  - Gamma spectrometry:
    - Samples sealed and stored for ~25 days to reach secular equilibrium before gamma counting.
    - Analyzed by gamma spectrometry using hyperpure germanium detectors; typical 2-day counting.
    - Spectra analysed with Canberra Genie-VMS; energy range 59.5–1836 keV; detectors calibrated with certified reference solutions.
  - U and Th analyses:
    - When size allowed, ~0.5 g digested in 10 ml concentrated HNO3 and HF, digested in microwave, and brought to 10 ml in 10% HNO3.
    - Analysed by ICP-MS for U and Th (detection limits ~10^-2 mg/kg for Th and ~10^-3 mg/kg for U).
    - Total U and Th activity concentrations derived from measured total concentrations, assuming secular equilibrium for U-series with 238U and 234U; equilibrium among Th-series members not assumed due to differing behaviours.
  - Special cases:
    - Toad analysed fresh due to handling constraints, then ashed for total U/Th determinations.

- Derivation of soil activity concentrations (G-BASE data)
  - Source: British Geological Survey (BGS) Geochemical Baseline Survey of the Environment (G-BASE) data for K, U, and Th in soils.
  - Sampling density and coverage:
    - Soils: ~one sample per 2 km2; 25 km2 grid-square aggregation using the nearest five soil samples for each parent material to compute a representative grid-square GM (geometric mean).
    - Sediments and waters: similar approach for sediments; waters used geometric means where data were available; extrapolation for waters was not robust due to weaker element–geology relationships.
  - Normalisation and cross-dataset harmonisation:
    - Analytical method changes and different sample types necessitated normalisation across data sets (described in Beresford et al., 2007).
    - Normalisation between BGS and Wolfson Atlas data accomplished by linear quantile transformation in overlapping areas.
  - Spatial and materials mapping:
    - Bedrock and superficial geology (simplified codes) assigned to each soil sample location.
    - GM values computed for each 25 km2 square by area-weighted averaging of the nearest data points for each parent material present in the square.
  - Conversion to activity concentrations:
    - Specific activities used to convert total element concentrations to activity concentrations:
      - 40K: 31.6 Bq g-1 K
      - 232Th: 4.07 Bq mg-1 Th
      - 238U: 12.21 Bq mg-1 U
    - Assumed 232Th-series in approximate equilibrium; 238U-series assumed to be in secular equilibrium with 234U and progeny where applicable.
  - Data coverage considerations:
    - Spatial coverage for solids (soils, sediments) is relatively robust, with more limited coverage for waters.
  - Outputs:
    - Geometric mean activity concentrations per 25 km2 grid square; two tiers of surfaces: measured 1 km grid values and extrapolated surfaces covering all of England and Wales.

- Key limitations and considerations
  - Data gaps, especially for Wales and certain RAPs; reliance on non-targeted datasets calibrated to RAPs.
  - Temporal differences and methodological changes requiring normalisation across datasets.
  - Assumptions of secular equilibrium in U- and Th-series; potential deviations due to environmental and biological processes.
  - Extrapolation introduces uncertainty, particularly for waters and for RAPs with sparse data.

- References and sources
  - Beresford et al. (2008) on background exposure rates and terrestrial RAP categorisation; J. Environ. Radioactivity.
  - Jones et al. (2009) on assessment of naturally occurring radionuclides around England and Wales; application of G-BASE to estimate doses to non-human species; Radioprotection.