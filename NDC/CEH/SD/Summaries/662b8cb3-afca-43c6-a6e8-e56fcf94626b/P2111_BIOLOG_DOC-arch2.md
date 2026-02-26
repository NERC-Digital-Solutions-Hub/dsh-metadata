# Substrate utilisation profiles for saprotrophic fungi and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland, 2001 [NERC Soil Biodiversity Programme] - Supporting Information

## Context and aims
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) studying soil biota diversity and functional roles within a large upland grassland field experiment at Sourhope, Scottish Borders.
- Primary aims: understand soil biological diversity and the functional roles of soil organisms in key ecological processes (carbon and nitrogen cycles, decomposition).
- Site details: Sourhope field site, ~309 m a.s.l., mean annual temp 7.8°C, rainfall 952 mm; brown forest soil; prevalent vegetation includes Agrostis capillaris, Festuca rubra, Nardus stricta, Anthoxanthum odoratum, Poa pratensis.
- Programme context: 24 research projects on soil structure, processes, micro- to macro-fauna; emphasis on linking diversity to function.
- Data focus: substrate utilisation profiles of saprotrophic fungi (via BIOLOG) and soil moisture content to understand decomposition dynamics and functional roles of a diverse fungal community.

## Data and what they comprise
- Substrate utilisation data for saprotrophic fungi using BIOLOG methodology; soil moisture data from July 2001 samples.
- Data collected across main Sourhope plots with treatments: Control, Lime, Nitrogen, and Nitrogen + Lime.
- Soil horizons sampled: litter fermentation (LF), humus (H), and mineral (A).
- Fungal isolates derived from soil, standing-dead plant material, and basidiomata; taxa selected to represent abundant and occasional community members.
- Final data outputs include:
  - Isolation frequencies and taxon identifications (soil and standing-dead litter).
  - Functional tests for substrate utilisation on solid media (cellulose, lignin, pectin, starch, chitin).
  - BIOLOG SF-N2 microplates testing utilisation of 95 low molecular weight carbon sources.
  - Summary activity metrics from BIOLOG testing as a measure of carbon utilisation diversity.

## Experimental design and methods
- Isolation and culture:
  - Field sampling across five replicates per treatment; soil cores from LF, H, and A horizons.
  - Warcup soil plating method to estimate active fungal occurrence; isolations from soil and standing-dead litter; basidiomata collected when available.
  - Identification confirmed by culture methods or ITS sequencing; taxa ranked by occurrence across treatments/horizons.
- Substrate utilisation on solid media:
  - 48 fungal isolates tested (26 frequent, 22 occasional) across substrates: cellulose, lignin, pectin, starch, chitin.
  - Standardised inoculum density; inoculated into semi-defined media; incubated at 15°C; substrate utilisation inferred from colorimetric indicators.
- BIOLOG substrate utilisation (12 isolates in depth):
  - 12 isolates (6 frequent, 6 occasional) chosen to compare functional capabilities within putative guilds.
  - Pairs matched by function to compare abundance vs. occurrence in relation to substrate use.
  - BIOLOG SF-N2 plates used for 95 carbon sources; inoculum prepared in carageenan agar to standardise density.
  - Plates incubated at 15°C; absorbance read at 590 nm; plates read up to 25 days, twice weekly.
  - Total activity per taxon calculated as sum of absorbance across wells; total activity used as a proxy for overall carbon utilisation versatility.
- Taxa and isolates:
  - Focus on a mix of Penicillium, Aureobasidium, Absidia, Gliomastix, Trichoderma, Mucor, Cladosporium, Leptosphaeria, and others; some functionally unique isolates identified for deeper study.
- Data structure and metadata:
  - Four CSV datasets accompanying the study:
    - Dataset 1105: Percentage Soil Moisture Content (P2111_PERCENT_SOIL_MOISTURE.csv) with fields such as ROWNO, SUID, SAMPLE_DATE, BLOCK, MAIN_PLOT, TREATMENT, HORIZON, WEIGHT_..., PERCENTAGE_MOISTURE.
    - Dataset 1130: Substrate utilisation assay results (P2111_BIOLOG_RESULTS.csv) with SPECIESID, REPLICATE, TIME, ISOLATE_TYPE, BIOLOGCELLID, OPTICAL_DENSITY.
    - Dataset 1131: Details of BIOLOG SF-N2 microplates (P2111_BIOLOG_INFORMATION.csv) listing SUBSTRATE and SUBSTRATE_TYPE per BIOLOGCELLID.
    - Dataset 1132: Species examined on BIOLOG SF-N2 plates (P2111_BIOLOG_SPECIES.csv) with SPECIESID and SPECIES_NAME.
  - Supporting references and related datasets cited for context (D. Deacon et al. 2006; Sourhope Field Data Handbook 2003; Usher et al. 2006).

## Key findings (summary)
- Functional redundancy: High overlap in substrate utilisation among abundant and infrequent taxa; many taxa use similar substrates.
- Functional importance of infrequent taxa: Some infrequent microfungi show higher activity, broader substrate ranges, and greater competitiveness, indicating meaningful roles in decomposition.
- Interactions and resilience:
  - When abundant and occasional taxa from the same guild co-occur on grass litter, there is slight evidence of positive indirect effects on decomposition and cellulose degradation.
  - Some negative effects on lignin degradation observed, likely due to competitive interactions.
  - Occasional taxa may bolster temporal resilience of decomposition, potentially "waiting in the wings" to replace abundant taxa during ecological shifts.
- Potential role of uncultured taxa: Greater functional diversity could be captured by taxa not cultured in this study, suggesting additional layers of ecosystem function.
- Overall implication: Diversity within saprotrophic fungal communities supports decomposer function and ecosystem resilience, with functional roles distributed across both abundant and non-abundant members.

## Data quality, usage, and caveats
- Data underwent quality assurance procedures; however, as with many ecological datasets, the accuracy and fitness for specific uses are not guaranteed.
- NERC explicitly disclaims liability for the data’s accuracy or reliability and for any outcomes arising from their use.
- For users, see original references for methodological details and related datasets (e.g., Sourhope Field Data Handbook 2003; UK Soil Biodiversity Programme studies).
- For analysts: the datasets enable cross-tabulation by horizon, treatment, and date, supporting analyses of moisture impacts, fungal diversity, and functional capacity across environmental gradients and management regimes.