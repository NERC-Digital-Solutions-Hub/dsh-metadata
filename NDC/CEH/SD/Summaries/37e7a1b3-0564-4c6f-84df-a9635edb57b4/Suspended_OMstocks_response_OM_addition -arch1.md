# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

## Aim
- Assess how suspended organic matter stocks respond to added organic matter (leaf litter) in Welsh upland rivers.
- Use a BACI design to identify potential changes in CPOM and FPOM stocks and their isotopic/elemental composition.

## Experimental design
- Before-after-control-impact (BACI) framework applied to multiple streams.
- Each stream divided into:
  - Upstream reference (control) zone
  - Downstream experimental zone
- Zones are similar in length and habitat; a 20–50 m gap maintained between zones to ensure independence.
- Time periods:
  - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013); no manipulation; reference and experimental treated identically.
  - After period (T2): 57–62 days (early Jan to Mar 2013); experimental zone manipulated with leaf litter addition; reference zone unchanged.
- Leaf litter source: deciduous leaves (oak, birch, alder) added in proportion to experimental zone area.

## Leaf litter manipulation
- At T2 start (Jan 2013), 1 tonnes of leaf litter distributed above the experimental zone and below the reference zone.
- Proportional distribution of vegetable net bags to maintain minimum wet weight of 1.7 kg m-2 (wet weight) in the experimental zone.
- Additional leaf litter added as two discrete pulses: 630 kg (wet weight) on 12 Feb 2013 and 630 kg on 5 Mar 2013, following two large storm events.
- Leaf litter packs were designed to reflect natural senescence and abscission with ongoing degradation to maintain leaf matter within the experimental stretch.

## Sampling and analytical methods
- Suspended Organic Matter (SOM) definition: particles >10 µm and <1 mm.
- Sampling location: lower end of each reach, on each occasion.
- Collection protocol:
  - Filter 100 L of stream water through a stack of 10 µm and 1 mm filters (n = 3 per sampling occasion).
  - Samples refrigerated at ~4°C, then frozen within 24 h.
  - Freeze-dried at -20°C for 48–72 h, weighed to the nearest 0.0001 g.
  - Ground, homogenised, and subsampled (3 mg ±0.3 mg) for elemental (C, N) and stable isotope (delta-13C, delta-15N) analysis via mass spectrometry.
  - Inorganic content corrected by ash combustion (550°C, 5 h) on a subset to apply ash-free conversions.
- Weighting/measurement precision: SOM stocks weighed to the nearest 0.01 g.

## Data, variables, and structure
- Data format: flatbed CSV files.
- Key SOM variables (per sample and replicate) include:
  - cpom.g.per.sample (CPOM per grab sample, g)
  - cpom.afdm.mg.l (CPOM concentration, mg/L)
  - cpom.subsample.wt.ug (CPOM subsample mass, µg)
  - cpom.ug.C.per.subsample and cpom.ug.N.per.subsample (C and N content, µg)
  - cpom.d13C and cpom.d15N (stable isotopes)
  - cpom.d15N Comment (qualitative notes)
  - fpom.g.per.sample, fpom.afdm.mg.l, fpom.subsample.wt.ug, fpom.ug.C.per.subsample, fpom.ug.N.per.subsample, fpom.d13C, fpom.d15N, and related comments
  - Discharge (L/s), time (Before/After), date, month, and replicate codes
  - Reach status (Experimental or Control), site_code, landuse, region, and other site descriptors
- Replicates: coded A–F.
- Additional datasets: site description file with coordinates, catchment, and survey metadata.

## Quality control and documentation
- Data quality control emphasizes precise weightings (to 0.01 g) and standardized sample handling (refrigeration, freeze-drying, ash correction).
- Dataset includes a detailed structural description (over 33 columns for SOM data) and a site description file to contextualize geographic and catchment data.

## Miscellaneous and accessibility
- Supporting site information includes exact coordinates, grid references, elevation, and survey campaigns.
- Data organization supports cross-stream comparisons of CPOM/FPOM stocks, concentrations, and isotopic signatures before and after leaf litter manipulation.