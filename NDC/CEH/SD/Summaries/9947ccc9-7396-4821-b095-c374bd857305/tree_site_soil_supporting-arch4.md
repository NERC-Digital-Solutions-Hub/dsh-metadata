# Soil, site and tree characteristics for acute oak decline (AOD) symptomatic and non-symptomatic oak in three UK woodlands, southern England, 2016

- A dataset from a study linking Acute Oak Decline (AOD) symptoms with local-scale environmental factors across three UK oak woodlands in southern England.
- Focuses on interactions between tree and soil properties at a local level to understand AOD onset and progression.
- 60 sampled oak trees (symptomatic and asymptomatic) across three sites, with comprehensive tree, site context, and soil measurements.
- Data intended to support analyses of how local environmental conditions relate to AOD status and to inform broader data-driven understanding of disease ecology.

## Data files and structure

- Tree_characteristics.csv
  - Tree-level data: site, unique Tree_ID, geographic coordinates (Latitude, Longitude), AOD symptom status, species classification (morphometric leaves; SNP-based genetic), tree dimensions (Height, DBH, Crown Width EW/NS), crown density reduction, rooting depth.
- Site_characteristics.csv
  - Site-level context for each tree: AOD status, Depth_to_Gleying_cm, Basal_Area_0_20m, Basal_Area_20_40m, Compound_topographic_index, Social_class.
- Soil_characteristics.csv
  - Soil samples per tree: Sample_depth (5-15 cm or 40-50 cm), OM_%, pH, Clay_%, Silt_%, Sand_%, TotalC_%, TotalN_%, NitrateN_mgkg, AmmoniumN_mgkg, OlsenP_mg/kg, CEC_mmolc kg, and exchangeable cations (Al, Ca, Fe, K, Mg, Mn, Na) + BulkDensity_gcm3.
- All values follow the provided units; missing values indicated as 'nd'. Data collection and analysis details, including instrument use and replication, are documented in the methods.

## Study design and context

- Three woodland sites in England: Monks Wood (Cambridgeshire), Writtle Forest (Essex), Stratfield Brake (Oxfordshire).
- Experimental design: at each site, 10 AOD-symptomatic trees and 10 asymptomatic trees selected (total 60 trees: 3 sites × 20 trees/site).
- Symptomatic trees identified by visible bleeding canker lesions on the lower stem; asymptomatic trees selected via a random bearing from symptomatic trees and then locating the first asymptomatic tree >20 m away.
- Field sampling included tree measurements, soil pits excavated near each tree, and leaf material for species confirmation.

## Methods and measurements

- Tree and site measurements follow standard forestry methods for structure and crown condition; social status recorded (dominant to dying).
- Soil sampling: eight soil cores per depth (5-15 cm and 40-50 cm) per tree, pooled by depth to create one composite sample per depth per tree; samples air-dried and analyzed for physical and chemical properties.
- Laboratory analyses:
  - Organic matter by loss on ignition; pH in water; particle size distribution by laser granulometry; Total C and N by elemental analysis.
  - Exchangeable cations via BaCl2 extraction and ICP-OES; Olsen P; mineral N by 1 M KCl extraction and colorimetric analysis.
  - Replicates: LOI (3), pH (3), particle size (5), Total C and N (2), exchangeable cations (2), Olsen P (2), mineral N (2).
  - Handling below-detection values by assigning LoD/2 as per USEPA guidance.
- Leaf morphometry and species identification:
  - Morphometric measurements (lamina, petiole, sinus, lobes, intercalary veins, basal auricle, hairiness) for species classification (Quercus robur, Q. petraea, or hybrids) and genetic SNP-based confirmation (Sequenom) per Kremer et al. and Guichoux et al. references.
- Topography and site context:
  - Depth to gleying measured from soil surface using Munsell chart reference.
  - Micro-topography captured along radial transects; Topographic Wetness Index computed per Sørensen et al.
  - Basal area calculated within 0-20 m and 20-40 m around each tree.

## Spatial and temporal coverage

- Spatial: three oak woodlands in England; precise tree coordinates provided in Tree_characteristics.csv.
- Temporal: single field campaign conducted July–November 2016; one-time observations and samples per tree.

## Data quality, provenance, and governance

- Metadata: explicit variable descriptions, units, and data provenance; missing values indicated as 'nd'.
- Quality control: instrument-specific replication and calibration details summarized (Table 4 in the source); QA includes blanks, reference materials, and in-house QC checks.
- Data lineage: dataset underpins a pre-print study on local-site and soil factor influences on AOD (link provided); references to standard methods and harmonized sampling practices cited.

## Access and related materials

- Data are organized into three CSV files:
  - Tree_characteristics.csv
  - Site_characteristics.csv
  - Soil_characteristics.csv
- Pre-print foundation: Liz J. Shaw et al., The cause-effect conundrum of local-scale site and soil factors in acute oak decline (AOD). https://doi.org/10.1101/2025.01.24.634765
- Method references provide context for measurement techniques and data processing.

## Relevance to Data Leaders (data system perspective)

- Demonstrates end-to-end data collection, from field measurements to laboratory analyses, with explicit replication and QC protocols.
- Provides a structured data asset with clear metadata, variable definitions, units, and data governance considerations (data provenance, standard methods, handling of non-detects).
- Highlights how to integrate multi-domain data (tree metrics, site context, soil chemistry/physics, and genetic species identification) to study a complex ecological phenomenon.
- Illustrates practical challenges and design decisions relevant to data strategy:
  - Managing scattered, multi-source measurements (field, soil, lab) into coherent assets.
  - Ensuring discoverability and usability of product-level datasets for stakeholders (policy colleagues, researchers, practitioners).
  - Addressing data quality, standardization, and metadata completeness to enable reuse across networks and studies.
- Potential for downstream data products: integrated environmental factors analyses for AOD risk, cross-site comparisons, and meta-analyses with other oak datasets.