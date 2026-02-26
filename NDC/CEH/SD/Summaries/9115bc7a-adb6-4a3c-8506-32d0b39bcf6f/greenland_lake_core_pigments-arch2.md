# SS17c_sed_pigments

## Overview
- Dataset of chlorophyll and carotenoid pigments measured in sediment cores from six lakes in the Kangerlussuaq area, West Greenland.
- Collected during summer 2017 to provide a long-term view of lake primary production via pigment biomarkers.
- Six CSV files correspond to six lakes: SS17c, SS1b, SS85, SS1590, SS906, SS901.

## Location, sampling and collection
- Lakes and sampling sites (latitude/longitude) provided for each lake.
- Cores collected from the deepest part of each lake using a HON-Kajak corer in 2017.
- Cores sectioned into depth intervals in the field; stored refrigerated in sealed bags prior to subsampling.
- Pigment samples stored frozen until analysis.
- Clay Prater collected samples; Suzanne McGowan and Amanda Burson analyzed them.
- Sampling design aims to deliver a long-term overview of changes in lake photosynthetic activity.

## Analytical methods
- Sediments were freeze-dried, weighed, then extracted in an acetone:methanol:water (80:15:5) mixture.
- Extracts left overnight at -4 °C, filtered, and dried under nitrogen.
- A known quantity redissolved in an injection solution and analyzed by HPLC (Agilent 1200) with a quaternary pump.
- Mobile phases: Solvent A (80:20 methanol:0.5 M ammonium acetate), Solvent B (9:1 acetonitrile:water), Solvent C (ethyl acetate); stationary phase: Thermo Scientific ODS Hypersil column.
- Gradient: 4 min ramp A→B, 34 min ramp to 25%B/75%C, 5 min hold, 4 min return to 100% A with 9 min re-equilibration.
- Detection: Photo-diode array detector scanning 350–750 nm; pigment identities confirmed by retention times and spectra against standards.
- Quantification: based on peak areas at 435 nm calibrated to commercial standards (DHI Denmark).
- Pigment concentrations expressed as nanomoles per gram organic matter (nmol g OM−1) using LOI550 (loss on ignition at 550 °C) to determine OM fraction.

## Units and data content
- Pigments reported as nmol pigment per g organic matter (OM); OM derived from LOI550.
- Pigments identified include chlorophylls (Chl_a, Chl_b, Chl_c2, Chl_a'), and a wide range of carotenoids and derivatives (e.g., Fucoxanthin, Diadinoxanthin, Diatoxanthin, Lutein, Zeaxanthin, Canthaxanthin, B-carotene, and pheophytins and related derivatives).
- Some loci include UV-absorbing compounds and rarer pigments (e.g., Okenone, Isorenieratene) depending on lake.

## Data structure and contents
- Six CSV files: SS17c_sed_pigments, SS1b_sed_pigments, SS85_sed_pigments, SS1590_sed_pigments, SS906_sed_pigments, SS901_sed_pigments.
- Each file starts with a depth interval (cm) column; subsequent columns contain pigment concentrations for that lake.
- Lake-specific depth sampling details:
  - SS17b/SS17c: max depth around 22–24.5 cm; 0.25 cm intervals above 10 cm, 0.5 cm below; contiguous samples above 1 cm, with alternating below 1 cm.
  - SS901: max depth ~14.75 cm; similar 0.25 cm above 10 cm and 0.5 cm below 10 cm.
  - SS906: max depth ~21.5 cm; same interval scheme.
  - SS1590: max depth ~35.5 cm; same interval scheme.
  - SS85: max depth ~28.5 cm; same interval scheme.
- Depths and pigment columns vary by lake but all follow the general pattern of depth-based pigment measurements.

## Quality control
- Pigment calibrations conducted with an 8-point calibration at least once per year.
- An extract from green plants added at start and end of each HPLC run to monitor retention time stability and avoid misidentifications.
- Manual verification: pigment identification and baseline integration performed by a trained expert to ensure accuracy.

## Provenance and references
- Primary sources for methodology and interpretation:
  - Chen et al. (2001) for historical pigment biomarker applications.
  - Heiri et al. (2001) for LOI-based organic content estimation.
  - Prater et al. (2021) for landscape controls on nutrient stoichiometry and lake primary production at the Greenland Ice Sheet margin.

## Data management and use
- Data are organized as six lake-specific CSV files for ease of cross-lake comparison and long-term monitoring.
- Pigment data can be integrated with LOI550-derived OM data to assess trends in lake primary production and shifts in photosynthetic communities over time.
- Outputs are suitable for standardized monitoring reports, trend analysis, and policy-relevant environmental health assessments.