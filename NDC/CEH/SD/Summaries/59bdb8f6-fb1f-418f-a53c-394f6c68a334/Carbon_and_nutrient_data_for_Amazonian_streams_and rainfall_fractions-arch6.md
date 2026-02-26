# Sampling Regime

- Study location and scope: Data from two small streams (MT and NC) and four rivers (LT and TP) in the Western Amazonian basin at Tambopata National Reserve, Madre de Dios, Peru. Catchments extend toward the Andes; sampling aimed to capture hydrological and carbon dynamics across wet and dry seasons.

- Timeframe and campaigns: Field campaigns conducted Feb–Apr 2011, Sept–Dec 2011, and Mar–May 2012. MT is seasonally active and dries up during the dry season, causing a sampling gap Sept–Nov 2011.

- Data sets collected:
  - Fluvial carbon data for streams and rivers: dissolved inorganic carbon (DIC) and its δ13C-DIC, dissolved organic carbon (DOC), and particulate organic carbon (POC).
  - Nutrients and major ions: Ca, Mg, K, Na, total dissolved phosphorus (totP), and silicon (Si).
  - Rainfall fractions: rainfall water, throughfall, stemflow, and overland flow, with measurements for DIC, δ13C-DIC, DOC, POC, Ca, Mg, K, Na, totP, and Si.
  - Data point counts: provided per dataset in the accompanying tables (Table 1 for streams/rivers, Table 2 for rainfall fractions); prior submissions exist for parts of the data (DOIs noted).

- Sampling sites and scale:
  - Streams: NC (4.5–7.5 m wide; 7.2 km2 upstream), MT (3.5–5 m wide; 4.9 km2 upstream).
  - Rivers: LT (~2000 km2 upstream) and TP (~14,000 km2 upstream); sampling points where rivers were 40–80 m wide (LT) and ~200 m wide (TP).
  - Throughfall/stemflow: sampled at TAM9 biomass plot and explorer’s inn area, with eight trees providing stemflow data.

- Sampling and analytical methods:
  - DIC and δ13C-DIC: pre-acidified Exetainers; headspace method using Thermo-Fisher GasBench/DeltaV Plus; triplicate exetainers per occasion with a backup sample; randomised order; drift/c-trend standards included.
  - DOC: filtered water (GF/F 0.7 μm), acidified to pH 3.9, degassed, analysed by TOC combustion; filters dried and stored with desiccant.
  - POC: measured by loss on ignition after drying and combustion of filter papers; OC assumed 50% of organic carbon.
  - Cations and nutrients: Ca and Mg via Atomic Absorption Spectrometry (AAS); K and Na via flame photometry; totP and Si via colorimetric methods.
  - Rainfall fractions: throughfall and rain water collected with replicate buckets; stemflow collected with tubing around eight different trees; overland flow captured with a bank-side collector; samples collected after rain events and analysed similarly for DOC/POC (subset for DIC).

- Data quality control and calibration:
  - DIC: drift correction standards ~every 10 samples; randomised sample order; regular drift/long-term performance checks.
  - DOC: eight-point calibration with blanks and drift checks; replicates checked for consistency.
  - Cations and Si: calibration standards run to ensure instrument stability; blanks and mid-range standards repeated.
  - Data handling: NA indicates not analysed; calibrations and instrument drift monitored throughout runs.

- Data structure and format:
  - CSV files: "Amazon streams C and nutrients" and "Amazon rainfall fractions C and nutrients" containing data for streams/rivers (14 columns) and rainfall fractions (12 columns).
  - Common fields (Streams and Rivers): time (24h clock), date (dd/mm/yyyy), type (stream or river), site (MT, NC, LT, TP), collector ID (for rainfall fractions: TF, SF, OF, RW; and for streams: specific collector codes), and measured variables (DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, TotP, Si).
  - Rainfall fractions fields: time, date, type (TF, SF, etc.), site/collector details, and analogous measured variables where available.
  - Data notes: some fields not present in all datasets (e.g., TotP not available in rainfall fractions); data values are within method detection limits.

- Notable details and references:
  - Some data portions were previously submitted under DOIs; this dataset includes the full collection across campaigns.
  - Method references include standard water analysis methods and a 2014 study on DIC isotope measurement quality (Waldron et al., 2014) for context.

- Purpose and potential uses:
  - Enables assessment of hydrological controls on carbon concentrations and fluxes across multiple catchments and seasons.
  - Provides a comprehensive, self-serve data package for researchers and practitioners investigating fluvial carbon dynamics and nutrient chemistry in tropical rainforest basins.