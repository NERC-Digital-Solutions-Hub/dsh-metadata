# Experimental Design/Sampling Regime

## Purpose and scope
- Analytical study to assess how irrigation affects the abundance of mosquito species that are important for Rift Valley fever transmission.
- Compare within and outside the irrigation scheme; consider seasonal variation (dry vs wet seasons).
- Repeated sampling design to cover wet/dry seasons and irrigation-active vs inactive periods.

## Study design and sampling plan
- Sampling sites identified inside and outside the irrigation scheme to enable comparison.
- Each sampling visit involved trapping for three consecutive days to reduce catch variability.
- Fieldwork included ten CO2-baited CDC light traps per night, located in homesteads and irrigated farms across ten villages.
- Control site: Murukani village (15 km east of irrigated areas and pastoral regions in Ijara, Garissa).

## Field methods and data capture
- Traps operated from 4:00 pm to 6:00 pm for three consecutive days; Mosquitoes collected each morning.
- Specimens immobilized with 99.5% triethylamine and preserved in liquid nitrogen for transport to KEMRI laboratory.
- Field data recorded using a data collection tool; traps placed in livestock night sheds, bushes, houses, farms, and forested areas.
- Sample handling evolved from direct transfer from collection bags to EPF tubes to using CNTs later for field-to-lab transport.
- All trapping and larval collection sites georeferenced for mapping.

## Specimen processing and identification
- Mosquitoes identified to species using established taxonomic keys (Edwards; Gillies & de Meillon; Jupp et al.; Gillies & Coetzee; Harbach).
- Mosquitoes pooled up to 25 per pool; initial processing and pooling occur on ice to preserve samples for subsequent virus isolation work.
- Identified specimens preserved at -70°C for future analysis.
- Identification validated by expert taxonomists and internationally certified specialists prior to pooling/preservation.

## Dataset and data structure
- Single CSV dataset: DDDAC_Kenya_entomology.csv.
- Variables (9): date (sampling date), latitude (decimal degrees), longitude (decimal degrees), cbg (collection bag/trap ID), cnt (centrifuge tube ID; empty if no sample), epf (Eppendorf tube/pool of identified mosquitoes), species (mosquito species in the pool), sex (sex of mosquitoes by species in the pool), Pool_size (number of mosquitoes in the pool).
- Notes on data: na indicates no data; missing latitude/longitude due to equipment failure; some CNTs were not used (empty) when samples were transferred directly to EPF after sorting.

## Data quality, provenance, and controls
- Species identification conducted by expert taxonomists with cross-checks by internationally certified taxonomists before pooling.
- All sampling and larval collection sites georeferenced to support mapping and spatial analyses.
- Detailed sample tracking through CBG, CNT, and EPF identifiers to maintain provenance.

## Implications for data governance and reuse (for Data Leaders)
- Demonstrates end-to-end data workflow from field collection to laboratory processing and data curation.
- Highlights the importance of standardized metadata, clear pooling rules, and robust provenance for reproducibility.
- Emphasizes the need for geo-referenced, time-stamped data to enable longitudinal and spatial analyses across seasons and management regimes.