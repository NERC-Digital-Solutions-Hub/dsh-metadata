# Substrate utilisation profiles for saprotrophic fungi and moisture content data from soil sampled in an upland grassland experiment at Sourhope, Scotland, 2001 [NERC Soil Biodiversity Programme] - Supporting Information

## Context and aims
- Part of the NERC Soil Biodiversity Thematic Programme (1999–2001) at Sourhope, Scotland, focused on understanding soil biota diversity and their functional roles in key ecological processes.
- Aimed to link high saprotrophic fungal species richness with decomposition processes and to assess functional roles and potential redundancy within fungal communities.

## Site and treatments
- Location: Sourhope Field Experiment, Roxburghshire, Scotland; upland grassland at 309 m asl.
- Climate/soil: mean annual temperature 7.8°C, rainfall 952 mm; brown forest-type soil, pH 4.54–4.81; dominant grasses include Agrostis capillaris, Festuca rubra, Nardus stricta, Anthoxanthum odoratum, Poa pratensis.
- Experimental treatments: control, lime (6000 kg ha−1 yr−1 as CaCO3), nitrogen (120 kg ha−1 yr−1 as NH4NO3), and lime plus nitrogen.
- Sampling framework: plots with replicates across blocks; horizons sampled include litter fermentation (LF), humus (H), and mineral (A).

## Data collected and purpose
- Substrate utilisation profiles for saprotrophic fungi (via BIOLOG method) to determine how fungal diversity and relative abundance influence organic matter decomposition.
- Soil moisture content data from July 2001 to relate moisture regime to fungal activity and decomposition.
- Culturing and identification data to characterize fungal taxa, including both soil- and litter-associated isolates.

## Experimental design and methods
- Isolation of fungi:
  - Collected from soil, standing-dead plant material, and basidiomata.
  - Culturing used Warcup methods on mCDA and PDA media to estimate isolation frequency.
  - Taxa identified by sequencing ITS regions or confirmed by expert identification.
- Selection of taxa for functional assays:
  - From soil: 10 abundant and 10 occasional taxa.
  - From standing-dead litter: 5 abundant and 5 occasional taxa.
  - Basidiomata collections to supplement low isolation frequencies.
- Functional assays (three phases):
  1) Isolation and preliminary characterization of cultures from field material.
  2) Utilisation of specific substrates in semi-defined solid media (cellulose, lignin, pectin, starch, chitin) to assess broad functional capabilities.
     - Standardized inoculum, multiple replicates, negative and PDA-controls; incubation up to 28 days at 15°C.
  3) BIOLOG SF-N2 microplates to assess utilisation of 95 low molecular weight carbon sources.
     - 12 isolates selected for BIOLOG analysis (12: a mix of abundant and occasional taxa; pairs chosen to compare functionally similar isolates with different occurrence frequencies).
     - Inoculum prepared in carageenan gel to standardize density; plates incubated at 15°C; absorbance read at 590 nm over up to 25 days.
     - Total activity (sum of OD across wells) used as a measure of carbon-utilisation diversity and intensity.
- Data handling:
  - Four CSV datasets documenting moisture and BIOLOG results, plus metadata about BIOLOG plates and species.

## Datasets and data structure
- Dataset 1105: Percentage Soil Moisture Content (P2111_PERCENT_SOIL_MOISTURE.csv)
  - Key fields: ROWNO, SUID, SAMPLE_DATE, BLOCK, MAIN_PLOT, TREATMENT, HORIZON, WEIGHT_BOAT, WEIGHT_SOIL, TOTAL_DRYWEIGHT1, TOTAL_DRYWEIGHT2, DRYWEIGHT_SOIL, PERCENTAGE_MOISTURE.
  - Moisture measured by oven-drying (105°C) for samples across plots/horizons.
- Dataset 1130: Substrate utilisation assay (BIOLOG SF-N2) results (P2111_BIOLOG_RESULTS.csv)
  - Key fields: SPECIESID, REPLICATE, TIME, ISOLATE_TYPE, BIOLOGCELLID, OPTICAL_DENSITY.
  - Absorbance readings (590 nm) over time, hosted on BIOLOG plates incubated at 15°C.
- Dataset 1131: BIOLOG SF-N2 plate details (P2111_BIOLOG_INFORMATION.csv)
  - Key fields: BIOLOGCELLID, SUBSTRATE, SUBSTRATE_TYPE.
  - Substrate identities and types for each BIOLOG well.
- Dataset 1132: Species examined (P2111_BIOLOG_SPECIES.csv)
  - Key fields: SPECIESID, SPECIES_NAME.
  - Names and IDs of species used on BIOLOG plates.
- Supplementary references and resources:
  - Deacon et al. (2006) for diversity and function of decomposer fungi at Sourhope.
  - Sourhope Field Data Handbook (2003) and related UK soil biodiversity literature for context.

## Key findings (summary)
- Functional redundancy: high overlap in substrate use among abundant and occasional taxa; both groups largely utilized similar substrates.
- Role of infrequent taxa: despite lower abundance, infrequent taxa showed strong decomposition potential, wider substrate utilisation, and sometimes higher overall activity.
- Interactions among taxa: co-inoculations (abundant plus occasional) suggested slight positive indirect effects on cellulose degradation, with some negative effects on lignin degradation likely due to interspecific competition.
- Temporal resilience: occasional taxa may contribute to temporal resilience of decomposition processes, potentially waiting to replace abundant taxa when conditions shift.
- Gaps and future directions: greater functional diversity could be gained by including uncultured taxa not studied here; potential improvements in linking cultured function to broader soil processes.

## Implications for analysis and data use
- The datasets enable analyses of functional diversity, redundancy, and decomposition dynamics under different soil treatments (lime and nitrogen) and horizons.
- Possible analyses include:
  - Relationship between fungal community composition (abundant vs occasional) and substrate utilisation breadth.
  - Impact of soil moisture and horizon (LF, H, A) on functional profiles.
  - Temporal patterns in BIOLOG-determined carbon-source utilisation.
  - Interactions among taxa and their effects on decomposition rates (especially cellulose and lignin).
- Data quality and limitations:
  - Data are QA’d by NERC but not guaranteed for accuracy; users should validate suitability for specific analyses.
  - Cultured taxa may underrepresent uncultured fungal diversity; consider this in interpretation.

## Usage notes and caveats
- Data are supplied without liability for accuracy or fitness for a particular use.
- Raw data require careful metadata handling (sampling dates, plot treatments, horizons) to ensure appropriate comparisons.
- Cross-dataset integration should consider differences in isolate origin (soil vs litter), and the limited number of isolates used for BIOLOG in-depth analysis.

## References and related resources
- Deacon, L.J., et al. Diversity and function of decomposer fungi from a grassland soil. Soil Biology and Biochemistry, 2006.
- Sourhope Field Data Handbook, 2003. Available via EIDC catalogue record.
- Usher, M.B., et al. Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme. Applied Soil Ecology, 2006.