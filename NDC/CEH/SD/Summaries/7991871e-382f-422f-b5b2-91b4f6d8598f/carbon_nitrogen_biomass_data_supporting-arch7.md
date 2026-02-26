# Carbon_Nitrogen_Biomass_data_Supporting.docx

- Dataset describing growth (mass) and carbon and nitrogen concentrations in pine and birch seedling needles, using soil from forest stands with monocultures or a 1:1 mixture.

## Overview
- Purpose: Test growth and foliar carbon and nitrogen concentrations in seedlings grown in soils from different stand compositions (birch-only, pine-only, mixed).
- Producers: David Johnson and Fay Voller; EIDC submission.
- Key outcome: Data suitable for mapping and analysis of biomass, C and N content, and mycorrhizal status in a GIS context.

## Study Site and Ex Situ Setup
- Location: Hambleton Forest, Yorkshire, UK (54°13' N, 1°07' W).
- Stand structure: Three replicate stands—silver birch only, Scots pine only, and a 1:1 mix. Planted 1961; thinned in 1998 and 2003.
- Stand dimensions: Each stand 0.2 ha; planted with 900 trees per stand; mixed stand in a 5x5 m checkerboard pattern with alternating species.
- Ex situ sampling: 10 replicate soil samples per stand (5 cm x 5 cm x 20 cm deep) collected Sept 19, 2019; soil stored at 4°C for up to 5 days.
- Seedling setup: Soil samples homogenized, split into seedling tubes; seedling compositions per tube varied to achieve specific pine/birch mixtures; seeds stratified, cleaned, and germinated before planting into tubes.
- Growth conditions: Growth chamber at 18°C, 16 h light / 8 h dark; maintained to achieve desired seedling compositions; destructive harvest between 19–22 weeks after seed addition.
- Measurements at harvest: Shoots dried at 60°C; roots stored for future analysis; foliar carbon-to-nitrogen ratio (C:N) measured with a Vario EL Cube.

## Data Structure and Variables
- Data organization: Columns reflect experimental design with five headers:
  - Plot_replicate
  - Stand (Pine, birch, or mixed)
  - Tube_content (Pine-only, birch-only, or mixture)
  - Seedling (pine or birch)
  - Replicate (individual ex situ replicate from each plot)
- Measured variables (data columns):
  - mass_g: Dry mass of individual seedlings (roots and shoots)
  - foliar_CN_ratio: Foliar carbon to nitrogen ratio
  - %N: Nitrogen concentration in foliage
  - %C: Carbon concentration in foliage
  - myc_status: Mycorrhizal status observed on roots (Myc or NM)
- Notes:
  - When a tube contained the same species, data reflect the average across harvested seedlings from that tube.
  - Mycorrhizal status recorded as observed on roots.

## Data Quality, Provenance, and Handling
- Sample handling: Soil samples stored at 4°C; seedling tubes destructively sampled; seeds and seedlings managed to maintain max root coverage and prevent cross-contamination.
- Measurements: Foliar C and N determined via Vario EL Cube; dry mass as a proxy for biomass.
- Provenance: Site-specific experimental design and sampling dates clearly described; reference provided for long-term context (Mason & Connolly, 2016).

## GIS Relevance and Integration
- Spatial context: Site-level coordinates provided; stands and plots structured with explicit stand type and replicate information, enabling spatial linking to polygons or raster layers in GIS.
- Potential map products:
  - Spatial distribution of foliar C:N, %C, and %N by stand type and tube content.
  - Visualization of mycorrhizal status patterns across pine, birch, and mixed plots.
  - Integration with other forest stand datasets (age, thinning history, soil characteristics) for broader ecological mapping.
- Data alignment: Table structure supports joins with stand-level GIS attributes (Stand, Plot_replicate) for map-based reporting and analysis.

## Reference
- Mason, B. and T. Connolly. 2016. Long-term development of experimental mixtures of Scots pine (Pinus sylvestris L.) and silver birch (Betula pendula Roth.) in northern Britain. Annals of Silviculture Research 40: 11-18.