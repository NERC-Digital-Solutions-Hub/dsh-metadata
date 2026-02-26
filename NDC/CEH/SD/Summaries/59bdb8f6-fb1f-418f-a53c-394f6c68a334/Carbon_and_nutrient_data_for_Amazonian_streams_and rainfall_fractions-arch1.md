# Sampling Regime

- Location and period: Western Amazonian basin, Tambopata National Reserve, Madre de Dios, Peru (lat 12°49'54.30" S, lon 69°16'52.37" W); data collected February 2011 to May 2012 to capture wet and dry seasons.

- Systems sampled: Two small streams (NC: New Colpita; MT: Main Trail) and two rivers (LT: La Torre; TP: Tambopata). NC and MT are local drainage; LT and TP have larger upstream catchments (LT ~2000 km2; TP ~14000 km2). Stream widths and upstream drainage areas provided; MT dries in the dry season.

- Data scope: Fluvial carbon (DIC and δ13C-DIC, DOC, POC) with selective nutrient analyses; rainfall fractions (rain water, throughfall, stemflow, overland flow) analysed for DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, P, Si.

- Sampling campaigns: Three field campaigns for fluvial data (Feb–Apr 2011; Sept–Dec 2011; Mar–May 2012). Rainfall fractions sampled Apr–May 2012. MT not sampled Sep–Nov 2011 due to drying.

- Datasets and prior submissions: DIC, DOC for small streams previously submitted (DOI 10.5285/507a5e1f-e056-454c-8ff6-d185f3da8556); DIC for rivers and samples with flux and velocity data previously submitted (DOI 10.5285/02d5cea710aa-4591-938a-a41e1c5bc207). Current submission includes resubmission of data not previously included.

- Field sampling and measurement methods:
  - DIC: pre-acidified 12 mL Exetainers; headspace method; triplicate exetainers per event; δ13C measured; drift correction standards used.
  - DOC: filtered water (GF/F 0.7 μm); acidified to pH ~3.9; degassed; combustion (TOC analyzer) for concentration.
  - POC: determined by loss on ignition of filter papers after drying and combustion.
  - Nutrients: Ca and Mg by Atomic Absorption Spectrometry (AAS); K and Na by flame photometry; total dissolved P (totP) and Si by colorimetry.
  - Rainfall fractions: rain water and throughfall collected in buckets; stemflow collected from eight diverse trees using half-pipe collectors; overland flow collected with bank-side collectors; all collectors emptied after rain events; DOC and POC analyses conducted as above; limited subset for DIC.

- Tree and stemflow details: Eight tree individuals sampled for stemflow; species include Inga sp., Pseudolmedia sp., Virola sp., Oenocarpus sp., Clarisia racemosa, Tachigalia sp., Iriartea deltoidea; diameters ranged from ~16 cm to ~58.9 cm; identification at genus level; stemflow collection configured with 0.5-length tubing around stems.

- Overland flow: simple collector installed to capture surface runoff without quantification of volume; samples used for composition analyses.

- QA and calibration: routine drift-correcting standards every ~10 samples; long-term instrument performance checked with repeated standards; calibration spanning expected ranges (DIC, DOC, Ca, Mg, TotP, Si) with blanks and drift checks; samples randomized to minimize bias; data checked against detection limits.

- Data structure and content: CSV files (Amazon streams C and nutrients; Amazon rainfall fractions C and nutrients) with:
  - Streams and Rivers dataset: Time (24 h clock), Date (dd/mm/yyyy), Type (stream or river), Site (MT, NC, LT, TP), CollectorID (for rainfall fractions: TF as Throughfall 1–4; SF as tree name; OF as Overland Flow; RW as Rain Water).
  - Measured variables: DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, TotP, Si (units vary by parameter).
  - Rainfall fractions dataset: Time, Date, Type (TF, SF, OF, RW), Collector/Tree details, same set of chemical measurements where available; TotP and Si may be missing in some records.
  - Note: NA entries denote data not analysed.

- Units and detection: values within method detection limits; content notes include standard methods and reference materials for quality control.

- References and methodology context: detailed references for analytical approaches (e.g., Waldron et al. 2014 for DIC isotopic measurements; American Public Health Association methods for nutrients).