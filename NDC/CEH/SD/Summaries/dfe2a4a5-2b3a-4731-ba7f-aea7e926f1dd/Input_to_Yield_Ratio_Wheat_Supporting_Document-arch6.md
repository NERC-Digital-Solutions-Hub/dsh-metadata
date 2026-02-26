# Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017 Dataset Documentation

- ## Aim
  - Document methodology and metadata for the dataset mapping the Input to Yield Ratio (IYR) of winter wheat farming in England at 1 km resolution for 2010–2017.
  - IYR represents the ratio of agrochemical inputs to agricultural yield, with four mapped harms (nitrogen and phosphorus fertilisers; pesticide risk to earthworms and to honeybees). Values are scaled so the maximum in each dataset is 1, enabling proportional comparison across inputs and rewards.

- ## Data content and format
  - Four single-layer TIFF files, 1 km resolution, British National Grid reference:
    - input_to_yield_ratio_honeybees.tif
    - input_to_yield_ratio_nitrogen_fertilisers.tif
    - input_to_yield_ratio_phosphorus_fertilisers.tif
    - input_to_yield_ratio_earthworms.tif
  - Areas with no data where winter wheat was not grown are left unassigned.

- ## Methodology and processing
  - Spatially explicit, national-extent estimates assembled from 2010–2017 data; maps produced at 1 km resolution.
  - Datasets combined to derive IYR by comparing estimated fertiliser and pesticide inputs to estimated wheat yields.
  - Yearly data aggregated to average across years due to differing survey periodicities; yields used from 2018 inputs (and related surveys) to construct the average wheat yield map.
  - Data sources include:
    - FERA Pesticide Usage Surveys (pesticide applications)
    - Defra Fertiliser Usage (fertiliser applications)
    - UKCEH Land Cover Plus: Crops map (2017) to identify winter wheat areas
    - Defra June Survey of Agriculture and Horticulture (for yield)
    - Pesticide Properties Database (toxicity for risk mapping to honeybees and earthworms)
  - Processed in a workflow (Figure 2 in the document); see Bullock et al. (2023) for in-depth methodology.

- ## Outputs and interpretation
  - Outputs include maps and frequency distributions of IYR values across England.
  - Higher IYR values indicate greater potential environmental harm relative to yield for the given input type.
  - Useful for:
    - Evaluating trade-offs between arable yields and agrochemical inputs at large scales.
    - Targeting actions to improve sustainability, or identifying areas suitable for changing farming practices or land uses (e.g., ecosystem restoration).

- ## Data access, citation, and reuse
  - Citation: Fincham et al. (2023). Input to Yield Ratio (IYR) values for wheat farming in England, 2010-2017. NERC Environmental Information Data Centre. DOI to be inserted.
  - Access: Environmental Information Data Centre (http://eidc.ceh.ac.uk/).
  - Data is prepared to support broad data use and analysis; outputs are linked to a related Bullock et al. (2023) study for methodology and interpretation.

- ## Acknowledgements and references
  - Funding and data providers acknowledged (ASSIST, AgZero+, Fera, Defra, PPDB, UKCEH, and specific individuals).
  - References include Defra (survey methodology and fertiliser data), FERA (pesticide data), PPDB toxicity data, UKCEH land cover, and Bullock et al. (2023) for broader context.