# Carbon_Nitrogen_Biomass_data_Supporting.docx

## Aim and scope
- Dataset from an ex situ experiment to test growth (mass) and carbon and nitrogen concentration in the needles of birch and pine seedlings.
- Compare seedlings grown in soils from forest stands that are pine-only, birch-only, or a 1:1 mixture.
- Data enable analysis of species effects, stand composition, and potential mycorrhizal associations on foliar chemistry and biomass.

## Study site and experimental design
- Location: Hambleton Forest, Yorkshire, UK (Forestry Commission managed).
- Stands: monocultures of silver birch (Betula pendula), Scots pine (Pinus sylvestris), and a 1:1 mix; planted in 1961, thinned in 1998 and 2003.
- Stand size: 0.2 ha per stand; ~900 trees per stand.
- Mixed-stand layout: 25 trees in a 5x5 m plot with alternating birch and pine in a checkerboard pattern.
- Ex situ component: on 19 September 2019, ten replicate soil samples from each stand type were used to establish seedling tubes for growth under controlled conditions.

## Ex situ procedures
- Soil handling: samples stored at 4°C and used within 5 days; each sample homogenised and allocated to seedling tubes.
- Seedling setup: tubes contained either two Scots pine seeds, 4–10 birch seeds, or a mix of one pine and 2–6 birch seeds; seeds stratified and washed in 1% hydrogen peroxide.
- Growth conditions: tubes placed in bags to prevent cross-contamination; growth chamber at 18°C with 16 hours light / 8 hours dark; watering as needed.
- Seedling composition per tube: designed to achieve either one pine seedling, two birch seedlings, or one pine + one birch seedling, ensuring adequate root coverage.
- Harvest: destructively sampled between 19 and 22 weeks after seed addition.
- Observations: seedlings recorded as potentially mycorrhizal (Myc) or non-mycorrhizal (NM).
- Sample processing: shoots dried at 60°C; roots stored for future analyses; dry shoot mass recorded; foliar carbon and nitrogen ratio (C:N) calculated with a Vario EL Cube.

## Data organisation and content
- Data structure: organized in columns with five key headers representing the experimental design.
- Key columns:
  - Plot_replicate: specific plot from the field site
  - Stand: Pine, birch, or mixed
  - Tube_content: Pine (only), birch (only), or a mixture of both species
  - Seedling: pine or birch
  - Replicate: ex situ replicate derived from each plot
- Derived/measure data columns:
  - foliar_CN_ratio: foliar carbon-to-nitrogen ratio
  - mass_g: dry mass of individual seedlings (shoots and roots)
  - myc_status: mycorrhizal status observed on roots (Myc or NM)
  - %N: nitrogen concentration in foliage
  - %C: carbon concentration in foliage
- Data note: when a tube contained the same species, data are the average across harvested seedlings from that tube.

## Measurements and calculation details
- Primary measurements: dry mass (mass_g), foliar C:N ratio (foliar_CN_ratio), %N, %C.
- Mycorrhizal assessment: recorded as Myc or NM at harvest.
- C:N ratio derived from foliar measurements using the specified instrumentation (Vario EL Cube) for CN assessment.

## Context and usage considerations
- Purpose-built dataset for exploring how stand composition and species interact to influence seedling biomass and foliar chemistry, with a Myc/NM dimension.
- Suitable for self-serve data exploration, cross-study integration, and analysis of relationships between biomass, foliar chemistry, and mycorrhizal status.
- Carefully documented experimental setup (seed stratification, contamination control, growth conditions, replication) supports data quality assessment and reuse.

## Reference
- Mason, B. and T. Connolly. 2016. Long-term development of experimental mixtures of Scots pine (Pinus sylvestris L.) and silver birch (Betula pendula Roth.) in northern Britain. Annals of Silviculture Research 40: 11-18.