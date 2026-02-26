# Physiological responses of marine phytoplankton to acute and chronic thermal stress.

- This dataset supports the research grant "Identifying the mechanisms and resource use implications of acclimation to high temperature in marine cyanobacteria" (NE/P002374/1) led by Richard J. Geider.
- It comprises physiology-based measurements on four phytoplankton: Synechocystis sp. (PCC 6803), Synechococcus sp. (CCMP 2370), Phaeodactylum tricornutum (CCMP 2561), and Emiliana huxleyi (CCMP 1516).
- Experiments include ramp (gradual heating), steady-state (acclimation to sub-, optimal-, supra-optimal temperatures), and thermal-performance/mortality responses across thermal gradients.
- Omics data are mentioned as separate depositories; all laboratory work was conducted at the University of Essex (2017–2021), with data collated and quality-controlled by July 2021.
- The dataset consists of 18 CSV files, with standardized column headings and detailed methodological descriptions to support data integration and reuse.

## Data scope and content

- Organisms and growth conditions
  - Synechocystis sp. PCC 6803: maintained at 30°C in BG-11 medium with 10 mM TES-KOH pH 7.5; 1% CO2-enriched air; continuous light (~150 µmol photons m-2 s-1).
  - Synechococcus sp. CCMP 2370: grown in K medium with 3 mM bicarbonate; ~325 µmol photons m-2 s-1; 26°C.
  - Phaeodactylum tricornutum CCMP 2561: grown in K medium with silicic acid; ~325 µmol photons m-2 s-1; 20°C.
  - Emiliana huxleyi CCMP 1516: grown in K medium with silicic acid; ~325 µmol photons m-2 s-1; 20°C.
- Experimental designs
  - Ramp: stepwise temperature increases (species-specific ramps) with hourly or daily sampling for physiology, transcripts, proteins, metabolites, and omics.
  - Steady State: cultures acclimated to sub-, opti-, and supra-optimal temperatures; replicate-driven physiological and biochemical measurements after at least 4 cell cycles.
  - Thermal Performance: exposure to a matrix of temperatures and light levels to characterize performance under varying conditions; replicated across several cycles.
- Measurements and methods (high-level)
  - Growth and cell abundances (flow cytometry or chlorophyll a proxy via fluorometry; growth rate by linear regression on log-transformed data).
  - Particulate organic carbon (POC), particulate organic nitrogen (PON), and particulate organic phosphorus (POP) with corresponding normalisations to cell density or carbon content.
  - Chlorophyll a (Chl a) concentrations and normalisations.
  - Macromolecular composition: bulk protein, lipids, carbohydrates (with detailed extraction and quantification procedures).
  - FRRf-based photosystem II metrics (Fv/Fm, effective yield, cross-section, etc.) and FLC (fluorescence light curves).
  - Oxygen dynamics: O2 evolution and uptake using MIMS with 18O2, across light gradients.
  - Photoinactivation and mortality: photoinactivation rates (with/without lincomycin) and live/dead cell counts via SYTOX staining.
  - Flow cytometry profiles: cell size (FSC) and pigment content (Chl a, phycoerythrin) for population characterization.
- Datasets
  - 18 CSV files detailing mortality, steady-state physiology, ramp experiments, photoinhibition, oxygen evolution, FRRf/FLC, and related parameters for the different species.
  - File names reflect species, measurement type, and experimental context (e.g., mortality data for Phaeodactylum tricornutum; steady-state data for Emiliana huxleyi; ramp data for Synechocystis, etc.).
  - Table 3 lists file names, sizes, and descriptions; Table 4 (column headings) documents units and variable descriptions.

## Data structure and key variables

- Temporal and experimental descriptors
  - Time (hours) and discrete timepoints per experiment.
  - Biological replicate identifiers and sample IDs.
  - Temperature at acclimation and assay temperatures; gradient temperatures for thermal experiments.
  - Growth rate (per day) and Mortality Rate (per day).
- Measurement-specific variables
  - Cell concentrations (cells mL-1 or per sample).
  - POC, PON, POP concentrations (per cell or per unit carbon/nitrogen/phosphorus content) and derived C:N, C:P, N:P molar ratios.
  - Chlorophyll a per cell and Chl a per carbon.
  - Macromolecular contents: protein, carbohydrate, lipid, and low-molecular-weight carbohydrates per cell or per carbon.
  - FRRf-derived metrics: Fv/Fm, effective quantum yield, and related fluorescence parameters.
  - O2 dynamics: gross, net, and uptake rates per cell, per carbon, or per Chl a.
  - Photoinactivation rates (with and without lincomycin) across light intensities.
  - Mortality data from live/dead discrimination (SYTOX; live cells per mL, dead cells per mL).
- Data normalization and units
  - Normalizations include per cell, per carbon, per Chl a, and molar ratios (C:N, C:P, N:P).
  - Units span copies across cells, picograms per cell, femtograms per cell, µmol photons m-2 s-1, mL, hours, and d-1 (per day).

## Data provenance and quality

- Laboratory work conducted at the University of Essex (2017–2021); data collated and quality-controlled by July 2021.
- Experimental replicates: multiple biological replicates per condition (e.g., ramp experiments with three independent replicates per species; Thermal Performance and Steady State experiments with four replicates).
- Methodological consistency: standardized gating and instrument settings for cytometry; consistent sample handling and calibration for biochemical analyses.
- Omics data are stored separately; this dataset focuses on physiology-based measurements and associated metadata.

## How this data can support GIS-driven visualization and analysis

- Although the study is laboratory-based (no spatial sampling described), the dataset provides quantitative, temperature- and light-dependent physiological responses that can be linked to environmental layers in GIS.
- Potential map-based products
  - Global or regional projections of phytoplankton sensitivity to thermal stress by combining lab-derived response functions with ocean temperature maps.
  - Risk maps for changes in primary production potential under warming scenarios, using species-specific physiological thresholds (growth, photosynthetic efficiency, mortality) as model inputs.
  - Temporal dashboards that relate environmental heat stress indices to predicted shifts in pigment content or nutrient cycling proxies (e.g., C:N, C:P ratios) in marine ecosystems.
- Data integration potential
  - Merge with species distribution data, oceanographic layers (temperature, light, nutrient availability), and climate projections to create decision-support visuals for policy, conservation, or marine management audiences.

## Access and documentation

- Data are organized into 18 CSV files with consistent column headings and comprehensive documentation within Tables 3 and 4 (describing file contents and column definitions, including units).
- Primary references for methods underpinning the datasets are provided in the accompanying section (e.g., Andersen 2005; Guillard & Ryther 1962; Kana 1990; Suggett et al. 2008; Baker & Geider 2021).

## Limitations and scope considerations

- The dataset reflects controlled laboratory conditions for four specific phytoplankton taxa; extrapolation to in-situ ecosystems should consider environmental complexity and community interactions.
- Omics data are stored separately; this summary focuses on physiology-based measurements accessible in the 18 CSV files.