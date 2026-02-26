# Soil respired radiocarbon as CO2 and CH4 from peatland plateaus and thawing peatland plateaus and from burnt and unburnt forests from permafrost in subarctic Canada

## Overview
- Study measuring radiocarbon content (14C) of soil-respired CO2 and CH4 from subarctic Canadian peatland plateaus, thawing peatland plateaus, and associated burnt/unburnt forests near Teslin and Yellowknife.
- Data collected in summer 2013 (near Teslin) and 2014 (near Yellowknife) across multiple sites with replicate sampling.

## Sites and sampling design
- CO2 sampling sites (radiocarbon analysis for CO2): 
  - FFU (FireFox Unburnt), FFB (FireFox Burnt), TPP (Teslin Peatland Plateau), TWM (Teslin Wetland Margin), MCU (Mosquito Creek Unburnt), MCB (Mosquito Creek Burnt), WTP (White Truck Plateau), WTM (White Truck Moss), WTS (White Truck Sedge), WTW (White Truck Wetland).
- CH4 sampling sites (radiocarbon analysis for CH4): 
  - TW (Teslin Wetland; includes TW5m at 5 m and TWMID at thaw center), WTM (White Truck Moss), WTS (White Truck Sedge), WTW (White Truck Wetland).
- Replication: three replicate locations per site (e.g., FFU1, FFU2, FFU3) for both CO2 and CH4.
- Sample types per replicate: DEEP, BOTTOM, PROBE (three sample types per replicate).
- Depths:
  - DEEP and BOTTOM: typical depths around 35/40 cm (or 30 cm at TPP).
  - PROBE: depth determined by probe deployment; end of tube in soil, perforated, connected to above-ground tubing.

## Sampling methods
- CO2 sampling (DEEP and BOTTOM collars):
  - PVC collars installed when thaw depth permitted.
  - Surface vegetation clipped at CO2 sites (to remove vascular plant influence); CH4 sites not clipped.
  - PVC chamber placed on collar; CO2 accumulates to ~800 ppm, then circulated with soda lime to ~200 ppm, reducing atmospheric CO2 component.
  - Zeolite Type 13X sieve connected to chamber to absorb CO2; left connected for several days.
  - Process repeated twice during the growing season (late July/early August and late August/early September) with the same sieve.
- CH4 sampling (DEEP, BOTTOM collars; PROBE):
  - CH4 headspace monitored with a DP-IR CH4 analyzer; CH4 transferred to 10 L foil gas bags for lab processing.
  - PROBE sampling degasses soil water; CH4 collected into a 10 L gas bag.
  - For PROBE, CH4 captured from the soil via a gas-tight system with a perforated membrane, avoiding atmospheric contamination.
  - No clipping performed for CH4 sampling to preserve natural transport pathways.
  
## Laboratory analysis and data products
- Lab processing:
  - CO2 samples: CO2 removed; CH4 samples: CH4 combusted to CO2; CO2 and derived CO2 then trapped on a zeolite sieve (Type 13X).
  - Sieves sent to the NERC Radiocarbon Facility (East Kilbride, UK) for graphitization and AMS 14C analysis; each sample given a Publication_code.
- Data outputs:
  - Radiocarbon enrichment expressed as percent modern carbon (pMC).
  - Ages reported as conventional radiocarbon age in years BP (before present, defined as AD 1950).
- References:
  - Methodology for CH4 analysis follows Garnett et al. (2012); radiocarbon analysis conducted at AMS facility after graphitization.

## GIS and data integration considerations
- Spatially explicit data across multiple site types (burnt/unburnt forests, peatland plateaus, thawed features) suitable for comparative mapping of 14C in soil-respired CO2 and CH4.
- Data structure includes site, replicate, gas type (CO2/CH4), sample type (DEEP/BOTTOM/PROBE), and depth, enabling layer joins with land cover, permafrost status, burning history, and thaw extent.
- Important considerations:
  - Standardization across sites with varying depths and vegetation states.
  - Consistency of replicate labeling (e.g., FFU1, FFU2, FFU3) for spatial analyses.
  - Vegetation clipping was applied only for CO2 sampling, potentially affecting comparability with CH4 samples.
  - Differences in sampling depths (DEEP/BOTTOM vs. PROBE) require careful harmonization when aggregating data.

## Summary of key points
- Extensive, replicate-based radiocarbon measurements of soil-respired CO2 and CH4 across diverse subarctic peatland and forest sites, including burnt vs unburnt and thawed vs intact areas.
- Detailed sampling protocols to separate contributions from different soil depths and transport pathways.
- Laboratory processing uses AMS 14C analysis, with results expressed as percent modern carbon and conventional age (years BP).
- Data are well-suited for GIS-based visualization and analysis of spatial patterns in soil respiration radiocarbon signatures, aiding interpretation of carbon dynamics under permafrost thaw and disturbance.

## References
- Garnett, M. H., Hardie, S. M. L. & Murray, C. Radiocarbon analysis of methane emitted from the surface of a raised peat bog. Soil Biology and Biochemistry 50, 158-163 (2012).