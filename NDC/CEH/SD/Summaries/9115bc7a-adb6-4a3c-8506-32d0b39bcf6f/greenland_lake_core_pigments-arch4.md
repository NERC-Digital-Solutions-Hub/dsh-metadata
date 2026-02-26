# SS17c_sed_pigments

- The dataset comprises chlorophyll and carotenoid pigments measured in sediment cores from six lakes in the Kangerlussuaq area, West Greenland, sampled in summer 2017.
- Six CSV files correspond to six lakes: SS17c, SS1b, SS85, SS1590, SS906, and SS901.

## Sampling, study area, and collection

- Lakes and sampling sites with coordinates provided for each lake.
- Cores collected from the deepest part of each lake using a HON-Kajak corer in 2017.
- Cores sectioned into depth intervals in the field; subsamples stored refrigerated in sealed bags, then frozen for pigment analysis.
- Sampling aimed at providing a long-term view of lake changes; pigments analyzed as biomarkers of photosynthetic organisms.
- Key personnel: Clay Prater (collection); Suzanne McGowan and Amanda Burson (analysis).
- Related references for context: Prater et al. (2021) on landscape controls of lake primary production; Chen et al. (2001); Heiri et al. (2001) on LOI methodology.

## Analytical methods

- Sample preparation: sediment frozen, freeze-dried, weighed; extracted in acetone:methanol:water (80:15:5); overnight at -4°C; filtered and dried under nitrogen.
- Instrumentation: HPLC with an Agilent 1200 series module, using a Thermo Scientific ODS Hypersil column.
- Chromatography: multi-solvent mobile phase with designated ramps; UV-visible detection from 350–750 nm.
- Quantification: based on peak areas at 435 nm; calibration with commercial standards (DHI, Denmark); identification by retention time and spectral characteristics with reference checks.
- Units: pigment concentrations reported as nanomoles per gram organic matter (nmol g-1 OM), using LOI550 (loss on ignition at 550°C) to determine OM fraction.
- Pigment names follow standard nomenclature; some derivatives noted (e.g., Pheophytin variants).

## Data structure and content

- Six CSV files named after each lake:
  - SS17c_sed_pigments
  - SS1b_sed_pigments
  - SS85_sed_pigments
  - SS1590_sed_pigments
  - SS906_sed_pigments
  - SS901_sed_pigments
- Each file structure:
  - First column: sample depth (cm) from the core.
  - Remaining columns: pigment concentrations (nmol g-1 OM) with pigment names as column headers.
- Depth sampling details:
  - Varies by lake; typically up to about 22–35 cm depth with finer sampling near the top (0.25–0.5 cm intervals above 10 cm, and 0.5 cm intervals below 10 cm).
  - Sample sequences include contiguous top samples and alternating deeper samples.
- Example pigments included (varies by lake): Chl_a, Chl_b, Chl_c2, Fucoxanthin, Neoxanthin, Violaxanthin, Lutein, Zeaxanthin, Canthaxanthin, Pheophytins, Pyropheophytin, B-carotene, Diadinoxanthin, Diatoxanthin, Myxoxanthophyll, Alloxanthin, Phaeophorbide_a, Phaeophorbide_a, UV-absorbing compounds, and others.

## Quality control and data quality

- Calibrations: 8-point calibration for each pigment, at least annually.
- Stability checks: extract from green plants added at start and end of each HPLC run to monitor retention-time stability and prevent misidentifications.
- Manual review: pigment identifications and baseline integrations performed by a trained expert.

## Provenance and references

- Primary references:
  - Chen, N., et al. 2001. Organic Geochemistry.
  - Heiri, Oliver, et al. 2001. Journal of Paleolimnology.
  - Prater, C., et al. 2021. Ecosystems.
- Data collection and analysis contributors: Clay Prater (collection); Suzanne McGowan and Amanda Burson (analysis).

## Reuse potential and considerations for data leaders

- Long-term, multi-lake pigment dataset enabling:
  - Temporal and spatial comparisons of lake primary production proxies.
  - Cross-lake assessments of nutrient stoichiometry and ecosystem responses at the Greenland Ice Sheet margin.
- Strengths:
  - Consistent analytical approach across six lakes with detailed depth-resolution.
  - Quantitative, standardized pigment measurements linked to organic matter via LOI550.
  - Clear metadata on sampling, methods, and quality control.
- Considerations for integration:
  - Some pigment sets vary by lake; align column mappings when merging datasets.
  - Depth and sampling schemes differ slightly by lake; account for these when performing meta-analyses.
  - Metadata supports traceability to original collection and analysis workflows.