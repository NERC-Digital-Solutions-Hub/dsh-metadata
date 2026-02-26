# Supporting documentation

## Overview
- Simulation results for the red soil region of China using the Global ECOSSE model (spatial application of ECOSSE).
- Model outputs include carbon dioxide emissions and soil organic carbon.
- Inputs come from multiple datasets: Harmonised World Soil Database (HWSD) at 0.083-degree resolution, Copernicus land cover, and CRU HRGD climate data at 0.5-degree resolution.
- Region and timeframe: 2016–2100; land uses include agricultural and forest areas.
- Climate scenario: IPCC A2_MG1 (business as usual, CO2 emissions continue to rise).
- Soils modeled include Acrisols, Alisols, Luvisols, Lixisols, and Nitisols.

## Data sources and inputs
- Soil data: HWSD with mu_global identifiers.
- Land cover: Copernicus land monitoring service.
- Climate data: CRU HRGD high-resolution gridded dataset.
- Site selection: predefined prevalent soil types in the grid cells for the red soil region.

## Simulation workflow and stages
- Stage 1: Prepare national or provincial boundaries for the CookieCut program to simplify boundary shapes.
- Stage 2: CookieCut - generate bounding boxes from ReformShapes outputs; determine country/province bounding boxes.
- Stage 3: Create a JSON file specifying one or more provinces and land cover types; each line includes coordinate sets, HWSD mu_global identifier, and land cover index.
- Stage 4: GlblEcosse - read the _hwsd.csv AOI file from Stage 2 and generate ECOSSE input file sets for each entry, skipping adjacent entries on the same latitude with identical HWSD mu_global identifiers; create a manifest file recording adjacent entries.

## Quality control
- Input data are checked for accuracy as part of the workflow.

## Data products and file outputs
- Agri_RS_co2.txt: Simulated CO2 emissions from soil under agriculture.
- For_RS_co2.txt: Simulated CO2 emissions from soil under forest.

## Data governance and stewardship considerations
- Provenance and lineage: clear association between input datasets (HWSD, land cover, climate data) and ECOSSE outputs; workflow stages provide traceable steps from boundary preparation to final input sets.
- Metadata needs: document data sources, resolutions, mu_global identifiers, land cover types, and the specific IPCC scenario used; include model version and software references (Global ECOSSE, ECOSSE_user_manual).
- Data formats and interoperability: multiple data formats (shapefiles, JSON, CSV, text outputs); ensure consistent encoding, coordinate reference systems, and naming conventions.
- Sharing and updates: define availability status, potential embargoes, and update mechanisms to reflect new climate or land-use data; ensure that updates propagate through all Stage outputs (Stage 4 manifests) and corresponding CO2 data files.
- Data completeness and user needs: the workflow supports users needing regional soil carbon and CO2 emission data, but users may require additional metadata, documentation of assumptions, and accessibility through a dataset catalog or portal.

## Practical implications for data stewards
- Manage and document the data lineage from HWSD/land cover/climate inputs to ECOSSE outputs.
- Maintain versioned metadata for model configurations (region, soil types, time period, scenario) and file-level provenance (which stage produced each file).
- Ensure robust handling of large datasets and multiple formats, with clear guidance for users on how to reproduce the simulations.
- Prepare for potential data sharing constraints by documenting any proprietary inputs, licensing, or embargoes and by creating a comprehensive dataset manifest.