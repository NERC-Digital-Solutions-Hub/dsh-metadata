# Topsoil carbon model estimates [Countryside Survey]

- Overview
  - Dataset describes topsoil carbon for 0-15 cm depth, including loss-on-ignition (%), carbon concentration (g kg-1), and carbon density (t ha-1).
  - Based on 2614 cores from 591 1km x 1km squares across Great Britain, collected in 2007; sampling and methods detailed in Emmett et al. 2010 and related works.
  - Habitat and parent-material–level means estimated using data from 1978, 1998, and 2007 via a mixed-model approach; model inputs include Land Cover Map 2007 (LCM2007) and a Soil/Parent Material Model (2009).

- Model estimates and predictors
  - Means of habitat/parent-material combinations are modelled using dominant habitat and dominant parent material characteristics.
  - Dominant material characteristics:
    - Loss-on-ignition (LOI) and carbon concentration (CCONC) use Dominant Grain (DOM_GRAIN) as the parent material characteristic.
    - Carbon density (CDENS) uses Calcium carbonate content (CACO3_RANK).
  - Some areas (e.g., urban, littoral rock) are not sampled by Countryside Survey and have no data.
  - In some habitat/parent-material combinations, sample sizes were insufficient to estimate mean values.

- Data attributes and structure
  - Key attributes include:
    - LOI_78, LOI_98, LOI_07 with corresponding SE (standard error)
    - CCONC_78, CCONC_98, CCONC_07 with corresponding SE
    - CDENS_78, CDENS_98, CDENS_07 with corresponding SE
    - LCM_CLASS / LCM_NUMBER (derived from LCM2007)
    - DOM_GRAIN (dominant grain size; from Soil Parent Material Model)
    - CACO3_RANK (carbonate content ranking)
  - Units:
    - LOI: percent (%)
    - CCONC: g kg^-1
    - CDENS: t ha^-1
  - Spatial reference: OSGB 1936 / British National Grid (EPSG:27700)

- Experimental design and sampling regime
  - LOI values measured for:
    - 1197 plots within 256 1km squares in 1978
    - 1098 plots within 256 squares in 1998
    - 2614 plots within 591 squares in 2007
  - Field collection used 15 cm long by 5 cm diameter cores following Emmett et al. (2008).

- Collection, laboratory, and analytical methods
  - Core-based sampling with field protocol from Emmett et al. (2008).
  - LOI: 10 g sub-sample dried at 105°C, combusted at 375°C, with LOI calculated from weight loss.
  - Carbon concentration: measured with a total elemental analyser (CEH Lancaster UKAS SOP3102).
  - Carbon density: derived from carbon concentration and bulk density to express C per unit volume, then converted to area-based density.
  - Quality control: followed Defra/NERC Joint Codes of Practice; additional details in Emmett et al. (2008, 2010).

- Model interpretation and usage
  - Means are model-based estimates that link soil carbon characteristics to habitat and dominant parent-material factors.
  - Useful for understanding spatial patterns of topsoil carbon across GB at habitat and material levels, and for informing regional-scale carbon assessments.

- Limitations and challenges
  - Some habitat/parent-material combinations lack robust data due to small sample sizes.
  - Urban and littoral rock areas are not sampled, leaving gaps in coverage.
  - Model relies on dominant habitat/material classifications; unifying data from multiple sources and scales may introduce uncertainty.
  - Some details (e.g., boundaries and additional metadata) may be limited or not detailed within this dataset.

- References / supporting documents
  - Emmett et al. (2008, 2010): Countryside Survey technical reports and soils manual
  - Scott (2008): Statistical report
  - Morton et al. (2011): Land Cover Map 2007 dataset
  - Related materials: Soil Parent Material Model (British Geological Survey)