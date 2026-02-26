# Data overview

- This dataset includes metadata and measurements from a European grassland soil experiment testing four climatic disturbances (drought, flooding, freezing, heatwave) plus a control, with recovery measurements over time.
- Data cover microbial community profiling (bacteria and fungi) and soil functioning metrics (enzymatic activities, respiration profiles, carbon and nitrogen fluxes), plus detailed site and experimental metadata. Molecular data accession numbers are provided (European Nucleotide Archive).

## Spatial and climatic context

- 30 replicate sites across Europe, spanning diverse climates and soil types.
- Locations include alpine (Austria), subarctic (Sweden), arctic (Iceland), Atlantic (Oxford and Lancaster in the UK), boreal (Estonia), continental (Germany), Mediterranean (Spain, Greece), and steppic (Russia).
- Climate and location data linked to Worldclim (1960–1990, 2.5 arc-min resolution).
- Wide range of mean annual precipitation (MAP: ~223–1383 mm) and mean annual temperature (MAT: ~−2 to 14.5°C).
- Figure shows sampling site locations.

## Experimental design and sampling regime

- Grassland network: 10 locations across Europe, with 3 replicate sites per country (total 30 replicate sites).
- Within each replicate site: seven 1 m × 1 m plots arranged >5 m apart; soil cores collected and pooled to form one homogenized sample per replicate.
- Microcosm setup: 20 pots per replicate site, standardised to 100 g dry weight per pot.
- Disturbance period: 14 days with five temperature/moisture treatments:
  - Control (Ct): 18°C, 60% WHC
  - Drought (D): 18°C, 10% WHC
  - Flood (Fd): 18°C, 100% WHC
  - Freeze (Fz): −20°C, 60% WHC
  - Heat (H): 35°C, 60% WHC
- Sampling times: S1 (0 days, peak disturbance), S2 (1 day after end), S3 (8 days after end), S4 (26 days after end); 4 harvests per site × 5 treatments × 30 sites ≈ 600 microcosms (10 Russian samples at S2 were excluded).
- Treatments and sampling were randomized within countries; disturbances terminated by adjusting moisture/temperature to 60% WHC and 18°C for S2–S4.

## Measurements and analyses

- Gaseous fluxes: CO2, CH4, N2O measured from airtight jars with headspace sampling (0, 10, 20, 30 min) and calculated as fluxes per g dry soil per hour.
- Soil functional measures: substrate-induced respiration profiles (MicroResp) using diverse carbon substrates; microbial enzymatic activities (acetyl esterase, β-glucosidase, phosphatase, leucine-aminopeptidase) with MUB/AMC substrates.
- Soil chemistry and properties: moisture and nutrient concentrations, pH, dissolved organic/inorganic carbon and nitrogen, DON, total soil C and N.
- Sampling windows include initial field samples and lab-manipulated microcosm samples (620 total samples, including 30 initial field samples and 590 microcosm samples).
- Data management notes: some measurements (e.g., enzymes, metagenomics) performed only on a subset; initial baseline data included for context.

## Molecular data and sequencing

- DNA extraction from frozen soil (initial and microcosm samples).
- Bacterial and fungal community profiling:
  - 16S rRNA gene (V4–V5 region) for bacteria; primers: 515f/806r.
  - ITS2 region for fungi; primers described; Earth Microbiome Project protocol followed.
  - Sequencing on Illumina MiSeq (2 × 300 bp, V3 chemistry); data processed with DADA2 to generate ASVs; taxonomic assignment via SILVA (bacteria) and UNITE (fungi).
- Metagenomics:
  - Whole metagenome sequencing for a subset (308 samples after quality filtering); 28 initial samples plus 28 replicate-site×2 times×5 treatments minus exclusions.
  - Shotgun sequencing on NovaSeq; functional annotation via MG-RAST SEED subsystems (M5nr).
- Exclusions due to data limitations: DNA yield issues in Spain replicates; some low-quality sequences; final dataset contains 574 metagenomic samples for analysis.

## Data structure and accessibility

- Two CSV files:
  - Disturbance_data.csv: 91 columns, 620 samples; includes sample provenance, treatments, site descriptions, measured metrics (functional measures, soil properties), and ENA accession numbers.
  - Disturbance_metadata_header_description.csv: detailed description of the 91-column headers.
- Missing data denoted as NA; baseline INITIAL information and lab-manipulated measurements account for some gaps.
- Some measures limited to lab manipulations or INITIAL samplings; certain assays (enzymes, metagenomics) limited to subsets.

## Data quality, limitations, and processing notes

- Samples and data filtered for quality: 574 samples retained after removing insufficient DNA yields or low-quality sequences.
- Some fields subject to sampling constraints (e.g., not all sites measured for all metrics; subset analyses for metagenomics and enzyme assays).
- Spatially explicit data tied to specific sites, with climate and soil type metadata enabling geospatial analyses.

## GIS-focused opportunities and guidance

- Map layers to build: site locations, soil type classes, climate gradients, disturbance treatments, sampling times, and flux/enzymatic metrics.
- Integrate climate context with Worldclim variables and soil type categories (e.g., Haplic Cambisols, Haplic Podzols).
- Link spatial data to molecular datasets via ENA accession numbers for multi-layer analyses (taxonomy, functional genes, metagenomes).
- Use the 30 European grassland sites to visualize spatial patterns in microbial composition, enzyme activities, and greenhouse gas fluxes across disturbance regimes and over time.
- Consider data quality flags and missing values (NA) when constructing GIS visualizations or performing spatial analyses.