# Soil profile descriptions, biomass data and vegetation species from a joint sampling event at Sourhope, Scotland, 2000 [NERC Soil Biodiversity Programme]

- Background and aims
  - The NERC Soil Biodiversity Thematic Programme (established 1999) focused on intensive study of a large field experiment at Sourhope, Scottish Borders, to understand soil biota diversity and functional roles in key ecological processes.
  - 24 research projects explored soil structure, soil processes (carbon and nitrogen cycles), and roles of microfauna, flora, and macro-fauna.
  - The joint sampling event sought to link aboveground biomass, species composition, and soil biota with spatial and temporal data.

- Joint sampling event (dates and scope)
  - Held: 27–28 July 2000 at Sourhope Rigg Foot Field Experiment Site.
  - Design: a single soil block sampled from each sub-plot (S, T, U, V) within each main-plot; excluding Control 2 plots.
  - Purpose: baseline measurements for the initial 100 sample blocks; sub-samples were distributed to participating groups to cover biomass, vegetation, soil profiles, pH, and moisture data.

- Datasets available from the Joint Sampling Event
  - Root Cores Dataset (JT_SAMPLING_2000_ROOTS.csv)
    - Content: biomass data for roots, shoots, and litter from soil cores (4 x 4 x 8 cm approximate; sub-samples of larger blocks).
    - Measurements: dry weights (roots, litter) and densities (DWTSHDENS, DWTDENSLITT, DWTDENSROOT); volumes for litter and core; dry weights after 48 h at 80°C.
    - Metadata: SUID (unique sampling unit), sampling date, block/main-plot/sub-plot, X/Y cell, height/width/breadth of core, treatment type (Control, Insecticide, Lime, Nitrogen/Lime, Nitrogen), sampling location, dataset originator (MLRI), contact (J. Ross, L. Dawson), creation date (26-02-2001).
  - Vegetation Survey Dataset (JT_SAMPLING_2000_VEG.csv)
    - Content: vegetation species abundance per soil block, recorded as abundance classes linked to approximate percent cover.
    - Metadata: SUID, sampling date, treatment type (Control 1, Lime, Nitrogen, Nitrogen+Lime, Biocide), block/main-plot/sub-plot, X/Y cell, species name (Stace 1997), abundance class, and percent cover mapping.
    - Dataset originator: Macaulay Land Use Research Institute; contact: S. Buckland; creation date: 05-10-2000.
  - Soil Survey Dataset (JT_SAMPLING_2000_SOIL.csv)
    - Content: soil profile descriptions (horizon types and depths) with horizon-specific pH and moisture values.
    - Measurements: pH_H2O, moisture readings (Thetaprobe and PC_Moisture as calibrated %vol), horizon types and subregions, depth_upper/depth_lower for horizons.
    - Metadata: SUID, sampling date, treatment type (Nitrogen+Lime, Lime, Nitrogen, Biocide, Control 1), block/main-plot/sub-plot, X/Y cell, horizon_type/subreg, depth values, moisture and pH readings.
    - Field methods: pH measured via soil-water suspension; moisture via Thetaprobe and calibration curves; location: Sourhope Rigg Foot Field Experiment Site; originators: University of Stirling and MLRI; contact: P. Bruneau; dataset creation date: 27-9-2000.
    - References: Hodgson & Avery (1974) for soil survey handbooks; Sourhope Field Data Handbook (2003) for data context and methods.

- Data structure and units
  - All datasets use a unique Sampling Unit Identifier (SUID) to tie blocks, main plots, sub-plots, and sampling events.
  - Variables cover spatial coordinates (Block, Main_plot, Sub_plot, X_Cell, Y_Cell), sampling date, and treatment type.
  - Measurements include biomass components (roots, litter, shoots), volumes and densities, vegetation species and abundance, horizon classification, and soil chemistry/moisture metrics.
  - Explicit field and data originators, creation dates, and contact persons are provided for traceability.

- Methods and quality assurance
  - Root biomass: cores sub-sampled from soil blocks; drying at 80°C for 48 hours; analyses conducted at MLRI.
  - Vegetation survey: species recorded within 18 x 18 cm blocks; abundance classes translated to percent cover.
  - Soil surveys: pH_H2O measured with standard wet methods; moisture via Thetaprobe with calibration to %vol; horizon depths recorded.
  - Quality control: numeric range checks, formatting checks, and logical integrity checks applied; data accompanied by standard QA with a liability disclaimer (NERC not guaranteeing accuracy or fitness for purpose).

- Access notes and references
  - Data linked to and described in sources including the Sourhope Field Data Handbook (2003) and related Scott et al. 2003 references.
  - Datasets include dataset codes, project codes, and creation dates to facilitate discoverability and reuse.

- Practical relevance for analysts
  - Enables integrated analysis of soil biodiversity, biomass production, and vegetation community structure in relation to soil horizons and chemistry.
  - Supports exploration of treatment effects (e.g., nitrogen, lime, biocide) on soil biota and aboveground diversity.
  - Provides a coordinated, multi-dataset platform with consistent sampling units and metadata for cross-dataset linking and reproducible analyses.