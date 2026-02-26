# Bulk density, carbon and nitrogen content in soil profiles from permafrost in subarctic Canada

## Overview
- Describes soil core sampling in 2013 and 2014 across multiple sites in subarctic Canada to measure bulk density, carbon, and nitrogen content.
- Focuses on contrasting peatland plateaus and thawing features, with both unburnt and burnt black spruce forests represented.
- Provides detailed information on site codes, sampling design, field methods, laboratory processing, and data interpretation notes.

## Sites and sampling design
- Site codes and descriptions cover a range of ecosystems:
  - FFU, FFB: FireFox Unburnt/Burnt (unburnt and burnt black spruce forests)
  - BLF, WHF: BlackFox and WhiteFox forests
  - TPP: Teslin Peatland Plateau (and thawing variants TW, TWM)
  - MCU, MCB: Mosquito Creek Unburnt/Burnt forests
  - WTP, WTM, WTS, WTW: White Truck Plateau/peatland features with various thaw stages
  - BCB, BCS: Boundary Creek Birch and Spruce forests
- Generally five soil cores per site (replicates); some sites had three or four cores.
- Core labeling example: TPP1–TPP5 at the Teslin Peatland Plateau; other sites use similar coding across cores.
- Depth goals: cores aimed to reach 1 meter; occasional rock encountered prevented deeper sampling.
- Note on data alignment: soil profile codes do not spatially match flux data (CO2/CH4) despite identical core IDs; GPS coordinates are provided separately in the data files.

## Field collection methods
- Frozen-ground sites (e.g., FFU, FFB, BLF, TPP, MCU, MCB, WTP, BCB, BCS):
  - Upper soil sampled by inserting a tin foil sheet (40 cm depth) to capture thaw depth, then peat extraction.
  - Deeper sections sampled with a powerhead corer; cores recovered, wrapped, and stored in PVC tubes.
- Non-frozen ground sites:
  - Upper 40 cm sampled with tin foil; deeper sampling with a Russian corer; samples placed in half-cut PVC tubes.
- Handling and transport:
  - Samples kept frozen in Canada during transport to the UK for analysis.
  - In the UK, cores are cut and processed with careful volume recording.

## Laboratory processing and measurements
- Core processing:
  - Upper core sections cut at 1 cm resolution for lead dating purposes.
  - Deeper sections divided into roughly 10 cm intervals, chosen by horizon (organic vs mineral content).
- Measurements:
  - Bulk density determined from freeze-dried samples and weights, expressed as grams of dry soil per cubic centimeter of wet soil.
  - Carbon and nitrogen content measured by combusting subsamples in a C and N analyzer; results expressed as percent of dry mass.
  - Calibration performed with standards for each batch of samples.
- Notes on data fields:
  - Remarks column may indicate over/underestimation due to thick roots or recovery issues, post-thaw vegetation changes, or presence of the Tephra (White River Ash) layer.
  - Tephra layer observations noted in some cores.

## Data structure and interpretation
- Variables reported:
  - Bulk density (g dry soil per cm3 wet soil)
  - Carbon content (% dry mass)
  - Nitrogen content (% dry mass)
- Upper 1 cm interval used for lead dating; deeper intervals defined by horizon consistency.
- Post-thaw vs Pre-thaw vegetation transitions are noted in the Remarks, providing context for soil profile changes.
- Cross-dataset linkage:
  - While soil profile data share coding with co-located flux data (CO2/CH4), they originate from different locations; GPS coordinates are provided to align datasets accurately.

## Data quality, limitations, and guidance for use
- Potential issues:
  - Overestimation or underestimation of bulk density due to root intrusion or incomplete soil recovery during sampling.
  - Vegetation changes associated with peatland thaw affecting soil properties.
  - Occurrence of the Tephra layer in some cores affecting interpretation.
- Important caveat for integration:
  - Do not assume spatial equivalence between soil core IDs and flux data IDs; verify coordinates in the accompanying files if integrating datasets.
- Implications for data strategy:
  - The dataset includes rich metadata on site context, sampling depth, and processing workflows, suitable for inclusion in a larger permafrost carbon dataset.
  - Metadata and coding conventions are essential for discoverability and cross-system integration across soil and flux datasets.