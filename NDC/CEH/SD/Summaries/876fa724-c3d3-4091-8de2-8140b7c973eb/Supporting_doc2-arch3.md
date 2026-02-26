# Global ECOSSE Model Simulation for the Red Soil Region of China

- The document presents simulation results for the red soil region of China using the Global ECOSSE model, a spatial application of the ECOSSE framework.
- Outputs include carbon dioxide emissions and soil organic carbon.

## Data inputs and assumptions

- Soil data: Harmonised World Soil Database (HWSD), resolution 0.083 degrees.
- Land cover: Copernicus Land Monitoring Service.
- Climate data: University of East Anglia Climatic Research Unit high-resolution gridded datasets, resolution 0.5 degrees.
- Soil types used: Acrisols, Alisols, Luvisols, Lixisols, Nitisols.
- Simulation period: 2016–2100.
- IPCC scenario: A2_MG1 (business as usual, CO2 emissions continue to rise).
- Land uses simulated across the entire red soil region (agriculture and forest).

## Simulation workflow

- Stage 1: Prepare national/province boundaries for CookieCut; reduce boundary points (thinning) to simplify polygons.
- Stage 2: CookieCut; define a bounding box using a GADM shapefile and the Countries utility to determine country/province extents.
- Stage 3: Create a JSON input specifying one or more provinces and one or more land cover types; each line includes coordinates, HWSD mu_global identifier, and land cover index.
- Stage 4: GlblEcosse; read the _hwsd.csv AOI file from stage 2 and generate ECOSSE input sets for each entry, skipping adjacent entries on the same latitude with the same HWSD mu_global; adjacent entries are recorded in a manifest file.

## Outputs and data files

- Agri_RS_co2.txt: Simulated CO2 emissions from soil under agriculture.
- For_RS_co2.txt: Simulated CO2 emissions from soil under forest.

## Quality control and data governance

- Input data are checked for accuracy.
- Data preparation steps include thinning of boundaries and careful selection of AOIs.
- Documentation of data flow and the manifest file supports traceability of included entries.