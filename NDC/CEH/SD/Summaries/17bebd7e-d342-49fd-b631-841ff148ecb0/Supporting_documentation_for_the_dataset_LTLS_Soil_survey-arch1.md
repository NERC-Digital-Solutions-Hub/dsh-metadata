# Supporting documentation for the dataset Soil survey in England, Scotland and Wales carried out during 2013 and 2014, 2016, Toberman et al.

## Overview and purpose
- Soil survey conducted in England, Scotland and Wales during 2013–2014 (with 2016 data) as part of the NERC Macronutrient Cycles LTLS project: Analysing and simulating long-term and large-scale interactions of carbon, nitrogen and phosphorus in UK land, freshwater and atmosphere.
- Aims to provide soil data to support analyses of carbon, nitrogen and phosphorus cycling, resource availability, and soil properties across major habitat types and scales.

## Sampling design and field methods
- Site layout: typical sampling within a 100 x 100 m area at each location.
- Sampling pattern: a central line with regular points spaced every 11 m (10 cores) or 16 m (6 cores), with random distances from points on the line for core selection.
- Core counts: 10 cores for semi-natural habitats; 6–10 cores for agricultural fields.
- Core collection: vegetation and loose litter removed; used a van Walt split corer.
- Depths and protocol:
  - Ribble site: full core driven into soil, then split to obtain top 20 cm and subsequent 20 cm layer.
  - Other locations: core driven to 15 cm, then sample collected for the next 25 cm (overall up to ~40 cm depth); in some cases not all 40 cm could be sampled, or slightly more than 40 cm in total was collected.
- Depths and sampling details are documented in the data sheets (e.g., “Soil cores and depths”).

## Habitat types and abbreviations
- AG: Acid grassland
- Ar: Arable
- C: Conifer plantation
- CG: Calcareous grassland
- H: Heathland
- IG: Improved grassland
- M: Montane
- SP: Scots pine woodland – ancient semi-natural
- W: Broadleaved woodland
- HOC: High organic content (soil texture not analysed)

## Data structure and contents (tables and key fields)
- Locations_and_dates: sample identifiers, site catchment, site name, OS grid reference, easting, northing, latitude, longitude, sampling date.
- Bulk_density_data (BD_T, BD_P, BD_F):
  - BD_T: bulk density for the total soil solids
  - BD_P: bulk density for the fraction of solids < 2 mm
  - BD_F: bulk density calculation incorporating the volume of solids > 2 mm
  - Units: g cm-3; includes measured dry weight and core volume
- Charcoal_and_coal_data: charcoal/coal content (% by mass), LOI (loss on ignition, %), charcoal fraction of LOI, and related measurements
- Radiocarbon_codes: sample identifiers linked to SUERC radiocarbon facility codes
- Site_vegetation_data: habitat type and details per site (including habitat_type and habitat_type_with_detail)
- Soil_chemistry_and_isotope_data:
  - Thickness of sampled soil layer (cm)
  - BD_T, BD_P, BD_F (as above)
  - pH (via glass electrode method)
  - C, N: carbon and nitrogen contents (% by mass)
  - P_tot_%: total phosphorus content (inorganic and organic breakdown)
  - P_org_%: organic phosphorus content
  - P_inorg_%: inorganic phosphorus content
  - Delta13C: soil 13C content (‰)
  - P_tot_% = delta13C and related data (pMC, 14C content)
  - 14C_pMC: percent modern carbon
  - Measurement methods: Vario EL elemental analyzer for C/N and isotopes; Aqua regia/microwave digestion with ICP-OES for P; pH measurements; LOI
  - Notes on samples where carbonate removal occurred (pH > 5.5 treated with HCl to remove carbonate)
  - s/d designation: “s” = surface soil, “d” = deeper soil
- Soil_classifications_England_and_Wales: NSI-based classifications, including NSI series, subgroup, brief, and modern_def descriptors; sourced from NSI
- Soil_classifications_Scotland: Scotland-specific classifications including site_code, connections to 250k/25k soil maps, dominant soil map units, and related survey information
- Soil_cores_and_depth: sample IDs, depth designation (shallow/deep), number of cores sampled, mean core thickness (cm)
- Soil_texture_data:
  - Clay: % clay by mass
  - Silt: % silt by mass
  - Size fractions for mineral matter (clay and silt)
  - Beckenmann Coulter LS200 laser granulometer used for texture
  - HOC flag indicating high organic content where texture not determined
- Note: Some fields include “ND” (not determined) or metadata about measurement methods and units; depth and thickness fields indicate the sampled horizon(s).

## Measurements, methods, and units of key properties
- pH: measured with a glass electrode using 10 g moist soil + 25 cm3 water
- Carbon and isotopes:
  - Total carbon and nitrogen: measured via Vario EL elemental analyzer
  - Delta13C: reported in per mil (‰)
  - 14C_pMC: percent modern carbon, measured by accelerator mass spectrometry (AMS)
- Phosphorus:
  - P_tot_%: total phosphorus content (inorganic + organic)
  - P_org_%: organic phosphorus content
  - P_inorg_%: inorganic phosphorus content
  - Extraction/analysis: Aqua regia digestion, microwave digestion, ICP-OES
  - Notes on carbonates removal where applicable (pH > 5.5 samples treated with HCl)
- Bulk density:
  - BD_T, BD_P, BD_F with definitions described under Bulk_density_data
  - Units: g cm-3
- Loss on ignition (LOI):
  - LOI_%: determined by muffle furnace at 450°C for 16 hours
- Charcoal content:
  - Charcoal and coal data include charcoal fraction of LOI and charcoal content as percent by mass
- Texture:
  - Clay and Silt: % by mass
  - Instrument: Beckman Coulter LS200 laser granulometer
  - HOC flag indicates high organic content where texture not determined

## Data provenance, access, and use
- Data produced as part of the LTLS project (Long-Term and Large-Scale Interactions of C, N, and P in UK land, freshwater and atmosphere).
- Tables include standardized column headings, explanations, units, and notes on measurement methodology.
- Some data points link to external classifications and maps (NSI, James Hutton Institute outputs, 25k/250k soils maps).
- Data are accompanied by metadata and are structured to be discoverable (e.g., via data portals) with dataset provenance tracked.

## Analyst-focused considerations and challenges
- Data scale and access: some data are at site/habitat level and require careful alignment to local or regional scales.
- Data standardization and integration: multiple tables with different units and measurement methods; harmonization needed for cross-table analyses.
- Gaps and variability: some fields may be not determined (ND) or incomplete per site; not all horizons reach the full 40 cm in every sample.
- Administrative and access barriers: historically data stored in journals, reports, site datasets, or local authority records; ensuring timely access may require navigating permissions and data protection considerations.
- Technical barriers: large datasets with depth-wise measurements; some datasets rely on specialized equipment for texture and isotopic analyses.
- Metadata quality: ensuring consistent interpretation of abbreviations (e.g., s vs d horizons) and classification schemes (NSI components; Scottish classifications).

## Potential analyses and practical applications
- Correlate soil texture (clay/silt) with bulk density and organic carbon content across habitat types and depths.
- Examine relationships between pH, phosphorus fractions (P_tot, P_org, P_inorg) and soil organic content (LOI, Charcoal content) to understand nutrient availability and cycling.
- Analyze carbon and nitrogen stocks by horizon (surface vs deeper soil) and by site catchment, linking to land use and vegetation data.
- Use radiocarbon data (14C_pMC) and Delta13C to infer soil age and carbon input sources across habitats and depths.
- Investigate the influence of calcareous vs non-calcareous soils on P dynamics and carbon storage in the UK landscape.