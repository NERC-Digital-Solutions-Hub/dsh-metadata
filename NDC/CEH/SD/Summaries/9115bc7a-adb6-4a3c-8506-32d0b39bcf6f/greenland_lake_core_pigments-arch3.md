# SS17c_sed_pigments

- The dataset provides chlorophyll and carotenoid pigment measurements in sediment cores from six lakes in the Kangerlussuaq area, West Greenland, sampled in summer 2017.
- Pigments serve as biomarkers of photosynthetic organisms to offer a long-term view of lake primary production and ecosystem change.

## Study design and sampling

- Lakes sampled: SS17c, SS17b, SS85, SS1590, SS906, SS901 with precise latitude/longitude provided for each lake.
- Sediment collection: deepest part of each lake using a HON-Kajak corer; cores sectioned in the field, stored refrigerated in sealed bags, then frozen prior to subsampling.
- Sampling aims: to provide a long-term perspective on lake changes; subsamples prepared for pigment analysis.
- Personnel: clay Prater collected samples; Suzanne McGowan and Amanda Burson analyzed pigments.

## Analytical methods and units

- Pigments extracted from freeze-dried sediment using an acetone:methanol:water (80:15:5) mixture; extracts dried under nitrogen and redissolved for HPLC analysis.
- Instrumentation: Agilent 1200 series HPLC with a Thermo Scientific ODS Hypersil column; detection by photodiode array and UV-Vis scanning (350–750 nm).
- Separation and quantification: gradient elution with specified solvent system; calibration to commercial standards (DHI, Denmark); pigment identifications based on retention times and spectral characteristics; quantification using peak areas at 435 nm.
- Units: pigment concentrations reported as nanomoles per gram organic matter (nmol/g OM), with OM fraction determined by LOI at 550 °C.
- Pigments named using standard nomenclature (e.g., Chl_a, Chl_b, Chl_c2; various Pheophytin and Carotenoids).

## Data structure and contents

- Six CSV files corresponding to each lake pigment dataset:
  - SS17c_sed_pigments
  - SS1b_sed_pigments
  - SS85_sed_pigments
  - SS1590_sed_pigments
  - SS906_sed_pigments
  - SS901_sed_pigments
- Each file format:
  - First column: sample depth (cm) from the core.
  - Remaining columns: pigment concentrations (nmol/g OM) with column names specific to each lake (e.g., Chl_a, Fucoxanthin, Zeaxanthin, Pheophytin variants, etc.).
  - Depth sampling details vary by lake (e.g., max depths and interval schemes described for each dataset).

## Quality control and data validation

- Pigments calibrated with an 8-point calibration curve annually.
- An extract from green plants added at start and end of each HPLC run to monitor retention time stability and prevent misidentifications.
- All pigment identifications and baseline integrations performed manually by a trained expert to ensure accuracy.
- Method references and quality checks align with prior work (Chen et al., 2001; Heiri et al., 2001; Prater et al., 2021).

## Data governance, provenance, and accessibility

- Data are structured as six separate CSV files, with explicit sampling metadata (depth, depth range, and sample interval details) and a fully documented analytical workflow.
- LOI data and references used for context are provided, linking to published sources for broader methodological grounding (Heiri et al. 2001; Prater et al. 2021; Chen et al. 2001).
- Datasets are described with clear provenance, enabling reproducibility and integration into monitoring frameworks, though explicit open data licensing is not stated in the excerpt.

## Relevance for monitoring frameworks and policymaking

- Provides a standardized approach to extracting long-term biological indicators from lake sediments, which can inform:
  - Historical baselines of lake primary production and ecosystem shifts.
  - Assessments of nutrient dynamics and stoichiometry influences on productivity.
  - Evaluation of policy interventions aimed at protecting freshwater ecosystems under changing climate.
- The detailed metadata, rigorous QA/QC, and explicit data structure support transparent reporting, audit trails, and stakeholder trust.

## Considerations and challenges for implementation

- Metadata completeness is strong, but users may need to consult the original references for full methodological context and any updates to data processing.
- Potential barriers in broader monitoring deployment include the need for ongoing QA/QC, data standardization across datasets, and timely sharing of updated datasets to avoid silos.
- The requirement to align legacy data formats with current data governance standards may require data transformation and metadata harmonization.

## References

- Chen, N., Bianchi, T.S., McKee, B.A., Bland, J.M. (2001) Historical trends of hypoxia on the Louisiana shelf: applications of pigments as biomarkers Organic Geochemistry 32: 543-561.
- Heiri, Oliver, André F. Lotter, and Gerry Lemcke. "Loss on ignition as a method for estimating organic and carbonate content in sediments: reproducibility and comparability of results." Journal of Paleolimnology 25, no. 1 (2001): 101-110.
- Prater, C., Bullard, J.E., Osburn, C.L., Martin, S.L., Watts, M.J. and Anderson, N.J., 2021. Landscape controls on nutrient stoichiometry regulate lake primary production at the margin of the Greenland Ice Sheet. Ecosystems, pp.1-17.