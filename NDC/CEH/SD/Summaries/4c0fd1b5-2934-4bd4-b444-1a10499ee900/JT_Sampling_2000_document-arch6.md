# Soil profile descriptions, biomass data and vegetation species from a joint sampling event at Sourhope, Scotland, 2000 [NERC Soil Biodiversity Programme]

- Background
  - The NERC Soil Biodiversity Thematic Programme (established 1999) focused on understanding soil biota diversity and functional roles in ecological processes.
  - Location: Sourhope, Scottish Borders (Macaulay Land Use Research Institute, now James Hutton Institute).
  - 24 funded projects studied soil structure, processes (e.g., carbon and nitrogen cycles), micro- to macro-fauna, and their ecological roles.

- Joint Sampling Event (27–28 July 2000)
  - Coordinated sampling across project groups at Sourhope Field Experiment Site.
  - A single soil block was taken from each sub-plot (S T U V) within each main plot (excluding Control 2).
  - Initial 100 sample blocks were baseline-logged; sub-samples distributed to participants to create linked data across measurements and time.

- Datasets available from the Joint Sampling Event
  - Root Cores Dataset (JT_SAMPLING_2000_ROOTS.csv)
    - Biomass data for roots, shoots, and litter from soil cores.
    - Core sub-samples: approximately 4 x 4 x 8 cm; dried at 80°C for 48 hours after wet separation.
    - Field and processing metadata include: SUID, Sub_sample_ID, Sampling_Date, Block/Main_plot/Sub_plot, X_Cell/Y_Cell, Height/Width/Breadth, and treatment types (e.g., Control, Lime, Nitrogen, Nitrogen+Lime).
    - Measurements: Litter_DW, Root_DW, Vol_litter, Vol_core, DWTSHDENS, DWTDENSLITT, DWTDENSROOT, among others.
    - Data originators: Macaulay Land Use Research Institute; contacts J. Ross, L. Dawson; creation date 26-02-2001.
  - Vegetation Survey Dataset (JT_SAMPLING_2000_VEG.csv)
    - Vegetation species abundance within each soil block, recorded as abundance classes with percent cover equivalents.
    - Field and structure metadata include SUID, Sampling_Date, Block/Main_plot/Sub_plot, X_Cell/Y_Cell, Treatment_Type (e.g., Control 1, Lime, Nitrogen, Nitrogen+Lime, Biocide), and Species.
    - Abundance is recorded as an abundance class with a percent cover mapping (%Cover scores).
    - Data originators: Macaulay Land Use Research Institute; contact S. Buckland; creation date 05-10-2000.
  - Soil Survey Dataset (JT_SAMPLING_2000_SOIL.csv)
    - Soil profile descriptions with horizon types and depths; soil pH and moisture by horizon.
    - Methods: pH via soil-water extraction; moisture via Thetaprobe readings and calibration to %vol; horizons categorized per Soil Survey Field Handbook (Harpenden 1974).
    - Field and structure metadata include SUID, Sampling_Date, Block/Main_plot/Sub_plot, X_Cell/Y_Cell, Horizon_type, Horizon_subreg, Depth_upper/lower, pH_H2O, PC_Moisture, Moisture_voltage.
    - Data originators: University of Stirling / MLURI; contact P. Bruneau; creation date 27-09-2000.
  - Data standards and references
    - Stace, C. (1997) New flora of the British Isles (for vegetation nomenclature).
    - SOURHOPE FIELD DATA HANDBOOK (Scott et al., 2003) as supporting information.

- Data structure and metadata highlights
  - SUID: Unique Sampling Unit Identifier linking block/main-plot/sub-plot/date and sampling unit details.
  - Sub_sample_ID: Unique identifier for sub-samples.
  - Core measurements include dimensions (Height, Width, Breadth), volume-related metrics, and dry weights for litter and roots.
  - Vegetation data include Species names and Abundance with corresponding %Cover.
  - Soil data include Horizon_type, Depth_upper/lower, and moisture/pH measurements with explicit measurement methods.
  - Treatment types cover several management regimes (e.g., Control, Lime, Nitrogen, Biocide, Nitrogen+Lime).

- Quality control and usage considerations
  - Quality checks included numeric range verification, formatting conformity, and logical integrity assessments.
  - Data are subject to quality assurance procedures; however, NERC does not warrant accuracy or fitness for a specific use and disclaims liability for any losses arising from use.

- Access, provenance, and context
  - Datasets are linked to the NERC Soil Biodiversity Programme and associated datasets from Sourhope (Rigg Foot Field Experiment Site, Sourhope, NT8545019630).
  - Dataset creation dates range around 2000–2001; primary contacts include researchers from MLURI and the University of Stirling.
  - Additional context and methodology are documented in the 2003 Sourhope Field Data Handbook and related EIDC catalogue records.