# Data overview

- Dataset of metadata and measurements from an experiment imposing four climatic disturbances on soils from 30 European grassland sites, covering diverse soil types and climates.
- Disturbances: drought (10% WHC), flooding (100% WHC), freezing (-20°C), and heatwave (35°C), plus a control; followed by a recovery period.
- Assessed microbial communities (bacterial and fungal) via whole-genome metagenomics and amplicon sequencing; soil functioning via enzymatic activities, substrate-induced respiration, and carbon/nitrogen fluxes.
- Includes detailed site descriptions, treatments, measurements, and accession numbers for molecular data submitted to European Nucleotide Archive.

## Experimental design

- Grassland network across Europe: 30 replicate sites from 10 locations spanning alpine, subarctic, arctic, Atlantic, boreal, continental, Mediterranean, and steppic climates.
- Soils span multiple types (7 categories; mainly Haplic Cambisols, plus Haplic Podzols, Kastanozems, Luvisols, Calcisols, Leptosols, Gleysols).
- Three replicate sites per country, capturing a wide range of soil types; sites within countries are 0.05–11.76 km apart.
- Total planned microcosms: 600 (10 countries × 3 replicate sites × 5 treatments × 4 sampling times). One Russian site at S2 excluded due to insufficient soil.
- Initial sampling and preparation included measurement of moisture, nutrients, and DNA for baseline comparisons.

## Sampling regime

- Microcosms: 20 pots per replicate site, standardized to 100 g dry soil per pot.
- Acclimation: 7 days at 18°C, 60% WHC.
- Disturbance period: 14 days with five treatments (Ct, D, Fd, Fz, H).
- Sampling times: S1 (before final moisture/temperature adjustment for some treatments), S2, S3, S4 (1 day, 1 week, 4 weeks after disturbance end).
- For each sampling time, greenhouse gas fluxes (CO2, N2O, CH4) measured in sealed jars; additional soils collected for chemical, microbial, and DNA analyses.

## Treatments

- Control: 18°C, 60% WHC.
- Drought: 18°C, 10% WHC.
- Flood: 18°C, 100% WHC.
- Freeze: -20°C, 60% WHC.
- Heat: 35°C, 60% WHC.
- Moisture and temperature adjustments performed to reach target conditions; repeated watering by weight for moisture maintenance.

## Measurements and analyses

- Greenhouse gas fluxes: CO2, N2O, CH4 measured by gas chromatography; fluxes normalized to soil dry weight.
- Microbial activity: substrate-induced respiration profiles (MicroResp) across substrates (glucose, fructose, cellulose, citric/malic acids, amino acids) to estimate CO2 production.
- Enzymatic activity: potential activities for acetyl esterase, β-glucosidase, phosphatase, leucine-aminopeptidase using fluorescent substrates.
- Soil chemistry: dissolved organic/inorganic nitrogen, dissolved organic carbon, total C and N, soil pH.
- Additional soil properties: initial and microcosm moisture and nutrient concentrations.

## Molecular data and sequencing

- DNA extraction from initial soils (n=30) and microcosm samples (n=590); total 620 samples considered.
- Amplicon sequencing:
  - Bacteria: 16S rRNA gene (V4-V5) with 515f/806r primers; Earth Microbiome Project PCR protocols; Illumina MiSeq (2-step Nextera, V3 chemistry).
  - Fungi: ITS2 with primers targeting ITS2 region; Illumina MiSeq.
  - Bioinformatics: DADA2 for ASV generation; SILVA (v132) for bacteria, UNITE for fungi; minimum 2,000 reads per bacterial sample threshold.
- Metagenomics:
  - Functional gene composition assessed on 308 samples (initial subset and across treatments/time points): 28 initial samples (ES1/ES3 excluded) plus 28 replicate sites × 2 times × 5 treatments.
  - Library prep: TruSeq PCR-free; sequencing on NovaSeq (2 × 150 bp).
  - Annotation: MG-RAST SEED Subsystems (M5nr).
- Data quality and exclusions: Spain samples with insufficient DNA and other low-quality sequences removed; final DNA analyses include 574 samples.
- Data sources and references for primers and pipelines provided (e.g., DADA2, SILVA, UNITE).

## Data structure and access

- Two CSV files:
  - Disturbance_data.csv: 620 samples × 91 columns; contains sample provenance (site, replicate, treatment, description), measured metrics (functional measures, soil properties), and ENA accession numbers.
  - Disturbance_metadata_header_description.csv: detailed descriptions for all 91 column headers.
- Data points labeled as NA where information is missing or not collected for certain rows (e.g., baseline field vs. lab manipulations; subset-only measures such as enzymes or metagenomics).
- Metadata and molecular data linked via European Nucleotide Archive accession numbers.

## Limitations and considerations

- Some measurements are only available for lab-manipulated samples or initial field samplings, leading to uneven data coverage across time points and treatments.
- Certain datasets (e.g., DNA for some sites) were incomplete or excluded due to yield/quality issues.
- Variation in site characteristics and logistics required careful standardization and documentation to enable cross-site comparisons.

## Potential uses

- Identify correlations between climatic disturbances and shifts in microbial community composition and function.
- Model the impact of drought, flooding, freezing, and heat on soil enzyme activities, carbon/nitrogen fluxes, and substrate metabolism.
- Compare metagenomic functional potential with taxonomic profiles across disturbance regimes and time after disturbance.
- Integrate with environmental data (WorldClim-derived climate variables) for broader ecological or biogeochemical analyses.
- Use the structured metadata and accession-linked molecular data to reproduce analyses or to combine with external datasets for meta-analyses.