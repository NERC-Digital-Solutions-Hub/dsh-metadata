# Vegetation change at whim Moss (2002 -2016) Materials and methods

- Objective and scope
  - Long-term experimental study to understand how vegetation on Whim bog responds to different nitrogen (N) deposition regimes.
  - Combines dry (NH3) and wet (NH4+, NO3−) deposition manipulations with varying intensities to simulate atmospheric N inputs over time.
  - Establishes a framework for monitoring ecological responses to policy-relevant environmental pressures.

- Field site
  - Whim bog, Scottish Borders, UK: transition between lowland raised bog and blanket bog.
  - Deep peat (3–6 m); mean air and soil temperatures around 7.9°C and 7.6°C (2002–2016 means).
  - Annual rainfall ~1141 mm; water table typically ~10 cm below surface (damp hollows) with drier year noted in 2013.
  - Peat very acidic (pH ~3.4). Vegetation dominated by Calluna vulgaris with Sphagnum species; hummocks higher than hollows.

- Experimental design and treatments
  - Two nitrogen deposition systems:
    - Dry deposition: free-air NH3 release system using pure liquid NH3 diluted with ambient air; operation conditioned by wind direction, temperature, and wind speed.
    - Wet deposition: spraying of NH4Cl or NaNO3 solutions in rainwater onto plots; designed to achieve targeted total N deposition rates.
  - Treatment levels (ambient control plus three N-deposition levels without PK, two N-deposition levels with PK, and two levels using NO3− with/without PK):
    - Target total N deposition rates: 1.6, 3.2, and 6.4 g N ha−1 y−1, in addition to ambient control (0.8 g N ha−1 y−1).
  - PK addition: applied with lowest and highest N treatments in a 1:14 P:N ratio to align with amino acid P:N balance.
  - Experimental design: four blocks with 11 treatment combinations per block, totaling 44 plots.
  - Application schedule: sprinkler system triggered ~every 15 minutes during suitable conditions; ~120 applications per year; distribution spread throughout the year with some winter gaps.

- Measurements and data collection
  - Soil chemistry
    - Soil water samples collected monthly from dipwells (from 2006 onward).
    - Ion concentrations measured by ion chromatography; detection limits for NH4+-N and NO3−-N specified.
  - Vegetation monitoring
    - Surveyed in all plots, typically every two years.
    - Permanent quadrats: three per plot (40 × 40 cm), subdivided into 16 sub-quadrats (10 × 10 cm).
    - Within each sub-quadrat, percent cover recorded for all species; species list tailored to this study.
  - Spatial transects
    - For transect plots, distance from NH3 source recorded along transects to capture spatial deposition effects.
  - Flux calculations and treatment metadata
    - Deposition fluxes calculated for NH3 (Fnh3), NH4+ (Fnh4), and NO3− (Fno3) per plot; cumulative dose (DOSE) captured as total N deposition.
    - Expt, PK, BLOCK, TREATMENT, FORM fields encode treatment type and deposition form (Ammonia, Nitrate, Ammonium).

- Data structure and recorded values
  - Primary dataset: Whim_veg_2002-2006.csv (and related data streams).
  - Key variables include:
    - year, PLOT, QUADRAT, ASSESSMENT.DATE, SPECIES.LIST.NUMBER, SPECIES.LIST.NAME
    - SUB.SQUARE.1-16 (percent cover per species per sub-square)
    - distance_m (distance from NH3 source for transect plots)
    - Expt (Wet or Dry deposition), PK (presence or absence of PK), BLOCK, TREATMENT
    - FORM (Ammonia, Nitrate, or Ammonium)
    - Fnh3, Fnh4, Fno3 (fluxes of respective species to plots)
    - DOSE (total N deposition to each plot)

- References and methodology basis
  - Cape et al. (2008) deposition estimates for NH3 dry deposition
  - Leeson et al. (2017) nitrous oxide emissions after 13 years of N deposition
  - Leith et al. (2004) quantifying dry NH3 deposition to an ombrotrophic bog
  - Rodwell (1998) British Plant Communities classification
  - Sheppard et al. (2004) automated wet deposition system
  - Tang et al. (2001) development of passive samplers for NH3 and NO2

- Notable features relevant to monitoring frameworks
  - Combined parallel manipulation of dry and wet N deposition with multiple dose levels and PK co-addition to reflect nutrient balance considerations.
  - Robust experimental design with four blocks, randomized treatment combinations, and replication across plots.
  - Longitudinal vegetation and soil monitoring with clearly defined sampling intervals and standardized survey protocols.
  - Detailed metadata and explicit variable definitions to support data transparency, reuse, and cross-study comparability.
  - Spatial measurements (distance to NH3 source) integrated to assess gradient responses.
  - Use of established analytical methods (ion chromatography, kriging for deposition interpolation) to derive high-quality, traceable data products.