# SS17c_sed_pigments

## Overview
- Dataset of chlorophyll and carotenoid pigments measured in sediment cores from six lakes in the Kangerlussuaq area, West Greenland, sampled in summer 2017.
- Pigments used as biomarkers of photosynthetic organisms to provide a long-term view of lake primary production.
- Data organized into six CSV files corresponding to each lake/core: SS17c_sed_pigments, SS1b_sed_pigments, SS85_sed_pigments, SS1590_sed_pigments, SS906_sed_pigments, SS901_sed_pigments.
- Authors: Clay Prater (sample collection); Suzanne McGowan and Amanda Burson (sample analysis).

## Experimental design and sampling
- Lakes and sampling sites are detailed with precise latitude/longitude coordinates for each lake (SS17c, SS17b, SS85, SS1590, SS906, SS901).
- Cores collected from the deepest part of each lake using a HON-Kajak corer in 2017; cores sectioned in the field and stored refrigerated before subsampling.
- Pigment samples stored frozen until analysis.
- Depth sampling schemes:
  - SS17b: up to 24.5 cm depth with 0.25 cm intervals above 10 cm and 0.5 cm intervals below 10 cm; contiguous samples above 1 cm, alternate samples below 1 cm (35 samples; max depth 24.5 cm).
  - SS17c: up to 22.5 cm depth with 0.25 cm intervals above 10 cm and 0.5 cm intervals below 10 cm (35 samples).
  - SS901: up to 14.75 cm, 0.25 cm above 10 cm and 0.5 cm below 10 cm (26 samples).
  - SS906: up to 21.5 cm, 0.25 cm above 10 cm and 0.5 cm below 10 cm (33 samples).
  - SS1590: up to 35.5 cm, 0.25 cm above 10 cm and 0.5 cm below 10 cm (47 samples).
  - SS85: up to 28.5 cm, 0.25 cm above 10 cm and 0.5 cm below 10 cm (40 samples).
- Subsamples processed for pigment analysis; long-term overview via pigment biomarkers of photosynthetic organisms.

## Analytical methods
- Sediments freeze-dried, then extracted in acetone:methanol:water (80:15:5); extracts stored at -4 °C overnight, filtered, and dried under nitrogen.
- Known quantity redissolved in injection solution (acetone:ion-pairing reagent: methanol) and injected into HPLC.
- HPLC setup: Agilent 1200 with quaternary pump; mobile phases A (80:20 methanol:0.5 M ammonium acetate), B (9:1 acetonitrile:water), C (ethyl acetate); Thermo Scientific ODS Hypersil column.
- Gradient: 4 min ramp A→B, 34 min ramp to 25% B/75% C, 5 min hold, 4 min return to A with 9 min reequilibration.
- Detection: photodiode array from 350–750 nm; pigments identified by retention times and spectral characteristics; quantified using peak areas at 435 nm and calibration against commercial standards (DHI Denmark).
- Internal QC: 8-point pigment calibrations annually; green plant extract added at start and end of each run to monitor retention-time stability.
- LOI (loss on ignition) at 550 °C used to estimate organic matter (OM) fraction; LOI data referenced from Prater et al. (2021).
- Pigments expressed as nanomoles per gram OM (nmol g^-1 OM).

## Nature and units of recorded values
- Pigment concentrations reported as nmol pigment g^-1 OM.
- LOI550 provides the OM fraction to normalize pigment data.
- Pigment identification follows standard nomenclature:
  - Chl_a, Chl_b, Chl_c2
  - Carotenoids: Fucoxanthin, Neoxanthin, Violaxanthin, Lutein, Zeaxanthin, Canthaxanthin, Pheophytin derivatives (Pheophytin_b, Pheophytin_b1, Pheophytin_a, Pheophytin_a1, Pyropheophytin_a, etc.), B-carotene, Diadinoxanthin, Diatoxanthin, Myxoxanthophyll, Alloxanthin, Phaeophorbide_a, Phaeophorbide_a, UV-absorbing compounds, and others listed per lake.
- Each lake file lists depth and pigment columns specific to that lake; sample depths are in cm.

## Quality control
- Pigment calibrations performed eight-point per year; retention-time stability checked with green plant extract at start and end of each run.
- Manual peak identification and baseline integration performed by a trained expert to ensure accuracy.

## Data structure
- Six CSV files corresponding to the lakes:
  - SS17c_sed_pigments
  - SS1b_sed_pigments
  - SS85_sed_pigments
  - SS1590_sed_pigments
  - SS906_sed_pigments
  - SS901_sed_pigments
- Each file: first column is sample depth (cm); subsequent columns are pigment concentrations (nmol g^-1 OM).
- Lake-specific pigment sets vary; examples of columns per lake include a broad suite of chlorophylls and carotenoids (e.g., Chl_a, Chl_b, Chl_c2, Fucoxanthin, Diadinoxanthin, Diatoxanthin, Lutein, Zeaxanthin, Pheophytins, Pyropheophytin_a, B-carotene, etc.).
- LOI data used to derive OM for normalization (LOI550; details in Prater et al., 2021).

## References
- Chen, N., Bianchi, T.S., McKee, B.A., Bland, J.M. (2001). Historical trends of hypoxia on the Louisiana shelf: applications of pigments as biomarkers. Organic Geochemistry, 32: 543-561.
- Heiri, Oliver; Lotter, André F.; Lemcke, Gerry. (2001). Loss on ignition as a method for estimating organic and carbonate content in sediments: reproducibility and comparability of results. Journal of Paleolimnology, 25(1): 101-110.
- Prater, C.; Bullard, J.E.; Osburn, C.L.; Martin, S.L.; Watts, M.J.; Anderson, N.J. (2021). Landscape controls on nutrient stoichiometry regulate lake primary production at the margin of the Greenland Ice Sheet. Ecosystems, 1-17.