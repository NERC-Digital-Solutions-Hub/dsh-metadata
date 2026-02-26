# SS17c_sed_pigments

## Overview
- Dataset of chlorophyll and carotenoid pigments measured in sediment cores from six lakes in the Kangerlussuaq area, West Greenland, collected in summer 2017.
- Pigments serve as biomarkers of past primary production and photosynthetic organisms in lake sediments.
- Data are provided as six CSV files, one per lake, with detailed pigment concentration measurements and depth information.
- Metadata note the sampling context, storage, and analysis provenance, enabling traceability and reuse.

## Experimental design, collection, and sample handling
- Lakes and sampling sites are identified by lake codes and depth coordinates (latitude N and longitude W).
- Sediment cores were collected from the deepest part of each lake using a HON-Kajak corer in 2017.
- Cores were sectioned in the field, stored refrigerated in sealed bags, then subsampled for pigment analysis; samples stored frozen prior to analysis.
- Clay Prater supervised sample collection; Suzanne McGowan and Amanda Burson conducted sample analysis.

## Analytical methods
- Pigments extracted from freeze-dried sediment using an acetone:methanol:water (80:15:5) solvent, with overnight extraction at -4°C.
- Extracts filtered, dried under nitrogen, and re-dissolved for HPLC analysis.
- HPLC setup: Agilent 1200 with a Thermo Scientific ODS Hypersil column; mobile phases include methanol, ammonium acetate, acetonitrile, water, and ethyl acetate; gradient program specified.
- Detection: photodiode array/VIS scan from 350–750 nm; pigment identification by retention time and spectral characteristics, with reference to standards.
- Quantification: based on peak areas at 435 nm calibrated to commercial standards; results expressed as nmol pigments per gram organic matter (nmol g-1 OM). OM determined by LOI at 550 °C (LOI550); LOI data cited from Prater et al. (2021).
- Pigment nomenclature follows standard conventions; derivatives of pheophytins and specific chlorophyll pigments noted.

## Data and units
- Pigment concentrations reported as nanomoles per gram organic matter (nmol g-1 OM).
- LOI550 used to estimate the organic matter fraction; LOI data linked to Prater et al. (2021).
- Pigment identifications rely on retention times and spectral data, with calibration against DHI Denmark standards.
- Common pigments include Chl_a, Chl_b, Chl_c2, fucoxanthin, diadinoxanthin, diatoxanthin, zeaxanthin, lutein, canthaxanthin, pheophytins, among others. Abbreviations and derivatives (e.g., Pheophytin_b1) noted.

## Data structure and content
- Six CSV files, each corresponding to a lake: SS17c_sed_pigments, SS1b_sed_pigments, SS85_sed_pigments, SS1590_sed_pigments, SS906_sed_pigments, SS901_sed_pigments.
- Each file begins with a sample depth column (depth interval in cm); subsequent columns contain pigment concentrations for that lake.
- Depth sampling: varies by lake (e.g., maximum depths between ~14.75 cm and ~35.5 cm); sampling intervals typically 0.25 cm above 10 cm and 0.5 cm below 10 cm, with contiguous samples above 1 cm depth and alternate sampling below 1 cm depth.
- Variable columns differ by lake; examples of reported pigments per file include Chl_a, Chl_b, Chl_c2, Fucoxanthin, Diadinoxanthin, Diatoxanthin, Myxoxanthophyll, Alloxanthin, Lutein, Zeaxanthin, Canthaxanthin, Pheophytins, Pyropheophytin_a, B-carotene, among others.
- Column naming varies slightly between files (e.g., "Sample_depth_(cm)" vs "Sample depth (cm)"), reflecting dataset-specific conventions.

## Quality control and provenance
- Calibration: eight-point calibration for each pigment by HPLC, conducted at least annually.
- Process controls: extraction blank or plant extract spike added at start and end of each run to monitor retention time stability and prevent misidentifications.
- Manual curation: pigment identifications and baseline integrations performed by a trained expert.
- Provenance: data generation steps and analysts are documented (sample collection by Prater; analysis by McGowan and Burson); references provided for methods and LOI basis.

## Reuse, caveats, and references
- Primary references for methodology and context:
  - Chen et al. 2001 for pigment biomarker applications.
  - Heiri et al. 2001 for LOI method details.
  - Prater et al. 2021 for landscape controls on nutrient stoichiometry and lake production context.
- Practical notes for data stewards:
  - Cross-lake harmonization is needed due to varying column sets and minor naming differences.
  - Ensure LOI-based OM corrections are applied consistently when aggregating pigments across lakes.
  - Maintain alignment between depth intervals and pigment columns for accurate longitudinal comparisons.
  - Document sample collection and processing provenance to support reproducibility and future data integrations.