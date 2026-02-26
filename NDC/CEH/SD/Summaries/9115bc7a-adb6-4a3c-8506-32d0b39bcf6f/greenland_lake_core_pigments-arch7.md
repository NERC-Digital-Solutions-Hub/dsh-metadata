# SS17c_sed_pigments

## Overview
- Dataset of chlorophyll and carotenoid pigments measured in sediment cores from six lakes in the Kangerlussuaq area, West Greenland.
- Sampling occurred in summer 2017.
- Pigments analyzed as biomarkers of photosynthetic organisms; cores collected from the deepest part of each lake and subsampled for pigment analysis.
- Analysts: Clay Prater (collection); Suzanne McGowan and Amanda Burson (analysis).

## Location, sampling design and collection
- Lakes and coordinates (latitude N, longitude W):
  - SS17c: 66°58'47.7", 50°31'00.7"
  - SS1b: 66°58'47.0", 50°33'04.4"
  - SS85: 66°58'59.2", 51°03'23"
  - SS1590: 67°00'28.6", 50°59'16.5"
  - SS906: 67°07'10.9", 50°15'20.4"
  - SS901: 67°07'49.3", 50°14'00.6"
- Core collection: deepest part of each lake using a HON-Kajak corer.
- Handling: cores sectioned into depth intervals in the field and stored refrigerated; pigment samples frozen for analysis.
- Depth coverage and sampling: each lake has a defined maximum depth (varies by lake) with nested sampling intervals (0.25 cm above 10 cm, 0.5 cm below 10 cm; 1 cm contiguous intervals above 1 cm, alternating below 1 cm as applicable).

## Analytical methods
- Pigment extraction: sediments freeze-dried, extracted in acetone:methanol:water (80:15:5), left overnight at -4 °C, filtered, and dried under nitrogen.
- HPLC analysis: separation on a C18 column with a three-solvent system (A, B, C) and a 4–75 minute gradient; flow rate 1 mL/min; detection with a photodiode array, 350–750 nm scan.
- Quantification: pigment peak areas calibrated to commercial standards; concentrations expressed as nanomoles of pigment per gram organic matter (nmol/g OM) using LOI550 for OM fraction.
- Pigment identification: based on retention times and spectral characteristics relative to standards; key pigments include chlorophylls (Chl_a, Chl_b, Chl_c2) and various carotenoids and derivatives (e.g., fucoxanthin, lutein, zeaxanthin, canthaxanthin, β-carotene, pheophytins).

## Nature and units of recorded values
- Primary unit: nmol pigment per g organic matter (nmol/g OM).
- OM fraction determined by LOI550 (loss on ignition at 550 °C) and used to express pigment concentrations.
- Pigment identifications rely on retention time and spectral matching, with calibrations against commercial standards.

## Data structure and files
- Six CSV files (one per lake):
  - SS17c_sed_pigments
  - SS1b_sed_pigments
  - SS85_sed_pigments
  - SS1590_sed_pigments
  - SS906_sed_pigments
  - SS901_sed_pigments
- Each file format:
  - First column: sample depth (cm) from the core.
  - Remaining columns: pigment concentrations (nmol/g OM) with column names corresponding to pigment names.
- Lake-specific details (sample counts and depth ranges) provided for each file:
  - SS17c: 35 samples; max depth 22.5 cm; sampling intervals as described.
  - SS1b: 35 samples; max depth 24.5 cm; similar interval scheme.
  - SS901: 26 samples; max depth 14.75 cm; interval scheme as described.
  - SS906: 33 samples; max depth 21.5 cm; interval scheme as described.
  - SS1590: 47 samples; max depth 35.5 cm; interval scheme as described.
  - SS85: 40 samples; max depth 28.5 cm; interval scheme as described.

## Quality control
- Each HPLC pigment calibration uses an eight-point calibration annually.
- An extract from green plants is added at the start and end of each run to monitor retention time stability and prevent misidentifications.
- Pigment identification and baseline integration performed manually by an experienced analyst to ensure accuracy.

## How this data can be used in GIS and map-based analyses
- Spatial integration:
  - Link lake coordinates to a GIS layer of sampling locations; map pigment concentrations by lake.
  - Create depth-resolved pigment profiles as attribute data or as derived raster slices to visualize vertical pigment distribution across lakes.
- Data fusion and visualization:
  - Combine pigment data with LOI-based OM and other ecological layers (e.g., productivity proxies) to generate composite indicators of historical lake productivity.
  - Compare pigment distributions across lakes to infer spatial patterns in primary production and community composition during 2017.
- Temporal context:
  - Treat as a single-year snapshot (summer 2017) for temporal comparisons with other paleo- or modern datasets.
- Data preparation guidance:
  - Ensure LOI550-derived OM is consistently applied when comparing nmol/g OM across lakes.
  - Handle missing values as appropriate for depth intervals; align sampling depths where comparing across lakes.
  - Use pigment sets per lake as provided, noting any lake-specific pigments present or absent in the data.

## References
- Chen, N., Bianchi, T.S., McKee, B.A., Bland, J.M. (2001). Historical trends of hypoxia on the Louisiana shelf: applications of pigments as biomarkers. Organic Geochemistry, 32: 543-561.
- Heiri, Oliver; Lotter André F.; Lemcke Gerry. (2001). Loss on ignition as a method for estimating organic and carbonate content in sediments: reproducibility and comparability of results. Journal of Paleolimnology, 25(1): 101-110.
- Prater, C.; Bullard, J.E.; Osburn, C.L.; Martin, S.L.; Watts, M.J.; Anderson, N.J. (2021). Landscape controls on nutrient stoichiometry regulate lake primary production at the margin of the Greenland Ice Sheet. Ecosystems.