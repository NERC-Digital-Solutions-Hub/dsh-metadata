# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

## Aim
- Use a BACI (before-after-control-impact) design to assess how added organic matter influences suspended organic matter (SOM) stocks in Welsh upland rivers.
- Produce standardized data to support evaluation of environmental health and policy performance over time.

## Experimental Design
- Each stream divided into:
  - Upstream reference (control) zone
  - Downstream experimental (manipulated) zone
- Zones similar in length, habitat, slope, flow, substratum, and land use; ~20–50 m separation to ensure independence.
- Time periods:
  - Before (T1): 61–65 days (early Nov 2012 to early Jan 2013) with no manipulation
  - After (T2): 57–62 days (early Jan to Mar 2013) with leaf litter addition in the experimental zone
- Leaf litter manipulation:
  - One-tonne bags of deciduous leaves (oak, birch, alder) deployed above the experimental zone to simulate natural senescence and abscission
  - Vegetation nets maintained to ensure minimum wet weight of 1.7 kg m−2 in experimental zone
  - Additional 630 kg (wet weight) of leaf litter added to each stream on 12 Feb and 5 Mar 2013 after two large storm-flow events

## Methods: Collection and Analysis
- SOM definition: suspended particles >10 µm and <1 mm
- Sampling location: lower end of each reach
- Sampling procedure: filter 100 L of stream water through a stacked pair of 10 µm and 1 mm filters (n = 3)
- Sample handling: refrigerated (~4°C), frozen within 24 h, freeze-dried (-20°C) for 48–72 h, weighed to 0.0001 g
- Analytical workflow:
  - Ground and homogenize freeze-dried SOM
  - Subsample (3 mg ±0.3 mg) for elemental (C, N) and stable isotope (δ13C, δ15N) analyses via mass spectrometry (UC Davis)
  - Correct SOM for inorganic content using an ash-free conversion factor derived from combusting a subset of samples at 550°C for 5 h
- Measurements reported:
  - Coarse Particulate Organic Matter (CPOM) and Fine Particulate Organic Matter (FPOM)
  - Masses (g per sample), ash-free dry matter (AFDM), concentrations (mg L−1)
  - Subsample characteristics: C and N content (µg), δ13C and δ15N values
- Field/Lab equipment:
  - Water filtration setup; elemental/isotopic analyses performed at a stable isotope facility

## Data Structure and Units
- Data format: flatbed CSV files
- Main data columns (33 total) include:
  - site_code, landuse, region, time (Before/After), date, discharge (L s−1), reach (Experimental/Control), replicate
  - CPOM and FPOM metrics per sample:
    - CPOM FPOM masses (g per sample, AFDM g per sample)
    - Concentrations (mg L−1)
    - Subsample weights (µg)
    - Carbon and nitrogen contents (µg)
    - δ13C and δ15N values (with optional comments)
- Data quality: weightings to nearest 0.01 g; inorganic correction applied

## Miscellaneous Supporting Documentation
- Site descriptions provided in a separate CSV:
  - Site_code, name, grid references, latitude/longitude, elevation, survey/catchment details
- Data structure designed to support standardised monitoring and cross-site comparisons

## Relevance to Environmental Monitoring
- Features a robust, repeatable monitoring design (BACI) with transparent manipulation and standardized sample processing.
- Produces comprehensive SOM datasets (CPOM/FPOM, concentrations, and isotopic composition) suitable for long-term environmental health assessments and policy evaluation.
- Metadata and site descriptors enable data integration, interoperability, and potential linkage with other environmental datasets to increase data value and accessibility.