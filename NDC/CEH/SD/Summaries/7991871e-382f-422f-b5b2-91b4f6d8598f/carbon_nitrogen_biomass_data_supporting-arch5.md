# Carbon_Nitrogen_Biomass_data_Supporting.docx

## Overview
- Dataset from an experiment examining growth (mass) and carbon and nitrogen concentration in the needles of birch and pine seedlings grown in soil from forest stands with monocultures or a 1:1 mix of both species.
- Includes ex situ growth data, seedling measurements, and foliar C:N metrics, linked to a published long-term study.

## Study Site and Experimental Design
- Location: Hambleton Forest, Yorkshire, UK (54°13' N, 001°07' W); Forestry Commission managed site.
- Stand structure: three stand types with replicates — silver birch (Betula pendula) only, Scots pine (Pinus sylvestris) only, and a 1:1 mixture.
- Planting details: planted in 1961; thinned in 1998 and 2003; each stand ~0.2 ha with ~900 trees per stand; mixture pattern arranged in a 5x5 m grid.
- Experimental context: soil and seedling material collected/examined to compare growth and foliar C:N across stand types.

## Ex Situ Study and Data Collection
- Date of ex situ sampling: 19 September 2019.
- Soil sampling: ten replicate soil samples (5x5 cm, 20 cm deep) from each stand type; in mixtures, samples taken equidistant between birch and pine trees.
- Seedling setup: soil samples homogenised and divided into three seedling tubes; tube contents included pine-only, birch-only, or mixed seeds; stratified seeds followed by surface sterilization to reduce contamination.
- Growth conditions: seedlings grown in a controlled growth chamber at 18°C with 16 hours of light and 8 hours of dark; watering and seedling adjustments performed to maintain desired composition (1 pine seedling, 2 birch seedlings, or 1 pine + 1 birch per tube as needed).
- Harvest and analysis: destructive harvest between 19–22 weeks after seed addition; shoots dried at 60°C; roots stored for future analysis; measurements included dry mass (mass_g) and foliar carbon and nitrogen concentrations; mycorrhizal status recorded (Myc vs NM); foliar C:N ratio calculated.

## Data Organization and Variables
- Data structure: organized in columns with five header fields describing the experimental design.
  - Plot_replicate: field-site plot identifier.
  - Stand: Pine, birch, or mixed stand type.
  - Tube_content: Pine only, birch only, or a mixture.
  - Seedling: species represented in the seedling tube (pine or birch).
  - Replicate: individual ex situ replicate derived from each plot.
- Data relationships: when a tube contained the same species, data reflect the average of seedlings harvested from that tube.
- Measurements included:
  - mass_g: dry mass of individual seedlings (roots and shoots).
  - foliar_CN_ratio: total foliar carbon to nitrogen ratio.
  - %N: nitrogen concentration in foliage.
  - %C: carbon concentration in foliage.
  - myc_status: presence of ectomycorrhizas on roots (Myc) or not (NM).

## Provenance and Reference
- Primary reference for context: Mason, B. and T. Connolly. 2016. Long-term development of experimental mixtures of Scots pine and silver birch in northern Britain. Annals of Silviculture Research 40: 11-18.
- Data lineage: ex situ growth data linked to field stand design; detailed methodology and measurement steps captured to support reuse and replication.

## Data Governance and Sharing Considerations
- Metadata completeness: clear definitions for each column and the experimental design; consider adding explicit units for all numeric fields (e.g., mass_g, %N, %C) and the exact method for C and N determination.
- Standardization: ensure consistent naming for Stand and Tube_content categories; verify that myc_status coding is standardized (Myc vs NM).
- Access and reuse: dataset is well-structured for discovery and reuse in studies of plant-soil-microbial interactions, especially comparisons across stand types and donor/recipient species.
- Documentation needs: include collection date, location coordinates, soil handling details, growth chamber conditions, and description of any data processing steps to improve transparency.
- Update and versioning: consider a mechanism for updating with additional replicates or follow-up measurements; document any changes to the experimental setup or measurement methods.