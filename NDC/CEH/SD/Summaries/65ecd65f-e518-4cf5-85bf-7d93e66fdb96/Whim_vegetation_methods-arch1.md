# Vegetation change at whim Moss (2002 -2016) Materials and methods

- Field site: Whim bog, Scottish Borders (3°16' W, 55°46' N); transition between lowland raised bog and blanket bog on 3–6 m peat depth; mean air and soil temperatures ~7.9°C and ~7.6°C (2002–2016); annual rainfall ~1141 mm; water table typically ~10 cm below surface (drier in 2013 to ~24 cm); hummocks ~20 cm higher than hollows; peat highly acidic (pH ~3.4); vegetation dominated by Calluna vulgaris with Eriophorum vaginatum and a mix of Sphagnum species; mosaic of Calluna and Sphagnum across plots.

- Experimental design and treatments:
  - Two nitrogen (N) deposition pathways:
    - Dry deposition of NH3 using a free-air release system; NH3 released from a 10 m pipe when SW wind (180–215°) and temperatures above freezing with wind speed >2.5 m s^-1; creates a downwind gradient measured 0.1 m above vegetation using passive samplers at 8, 12, 16, 20, 24, 32, 48 and 60 m from source; deposition estimated from concentration data and kriging interpolation assuming spatially uniform deposition velocity.
    - Wet deposition of NH4+ and NO3- via a sprinkler system; rainwater collected and concentrated solutions of NH4Cl or NaNO3 diluted in rainfall and distributed to plots; three total N deposition targets: 1.6, 3.2, 6.4 g N ha^-1 y^-1, plus ambient control (0.8 g N ha^-1 y^-1); PK (K2HPO4) added to the lowest and highest N levels in a 1:14 P:N ratio; NH4+ and NO3- treatments increased precipitation by ~10%.
  - Experimental layout: four blocks; 11 treatment combinations per block (1 control, 3 NH4+ without PK, 2 NH4+ with PK, 3 NO3- without PK, 2 NO3- with PK) for a total of 44 plots.
  - Application regime: sprinkler system triggered automatically ~every 15 minutes when rainwater and conditions allowed; ~120 applications per year, spread across the year except mid-winter.
  - Measurements: soil water sampled monthly from 2006 onwards; ions measured by ion chromatography after titration; detection limits 0.014 mg L^-1 for NH4+-N and 0.062 mg L^-1 for NO3--N.

- Vegetation survey:
  - In each plot, three permanent 40 x 40 cm quadrats are established before treatments (2002); each quadrat subdivided into 16 sub-quadrats (10 x 10 cm).
  - At each survey (typically every two years), percent cover of all species recorded in each sub-quadrat; species lists are bespoke to this study.
  - Data captured at the plot level, with mean sub-quadrat cover used for quadrat-level values.

- Nature and units of recorded values:
  - Dataset: Whim_veg_2002-2006.csv
  - Key fields:
    - year, PLOT, QUADRAT, ASSESSMENT.DATE (date of vegetation survey), SPECIES.LIST.NUMBER and SPECIES.LIST.NAME (Latin names), SUB.SQUARE.1-16 (percent cover per sub-square), distance_m (distance from NH3 source for transect plots), Expt (Wet or Dry), PK (presence/absence of PK), BLOCK (experimental block), TREATMENT (code for N-form, dose, PK), FORM (Ammonia, Nitrate, or Ammonium), Fnh3 (kg N ha^-1 y^-1), Fnh4 (kg N ha^-1 y^-1), Fno3 (kg N ha^-1 y^-1), DOSE (total N deposition in kg N ha^-1 y^-1).
  - Deposition fluxes (Fnh3, Fnh4, Fno3) and total dose (DOSE) enable linking atmospheric N inputs to vegetation responses; dry deposition NH3 and wet deposition forms are tracked separately.

- Data interpretation and analysis notes:
  - Dry NH3 deposition profile along transects is interpolated to plot locations under a spatially homogeneous deposition velocity assumption.
  - Wet deposition applied via controlled spray, with total N deposition levels and PK additions logged per plot, enabling dose–response analyses.
  - Vegetation data collected as percent cover per species per sub-square, with aggregation to quadrat-level means for analysis.

- References:
  - Cape et al. 2008; Leith et al. 2004; Leeson et al. 2017; Sheppard et al. 2004; Tang et al. 2001; Rodwell 1998; plus related methodological works on deposition measurement and targeted nutrient additions.