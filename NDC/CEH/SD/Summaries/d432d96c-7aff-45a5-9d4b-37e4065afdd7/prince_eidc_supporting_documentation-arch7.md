# Overview

- Compilation of in-stream N-cycling results from the PRINCe project (A new dynamic for Phosphorus in Riverbed Nitrogen Cycling) led by Mark Trimmer (QMUL). 
- Data generated from two field campaigns in 2018 (winter February and summer July) across 12 permeable-bed rivers in Hampshire Avon catchment, Kent, and Essex.
- Methods include in situ 15N tracer experiments in riverbeds, porewater chemistry, and microbial gene abundance/transcripts analyses.
- Core sampling and porewater collection used a push-pull technique with 15 bespoke probes at depths of 5 cm and 10 cm in unvegetated sediment patches.
- Aims to quantify nitrogen transformations (rates and nitrification efficiency) and characterize microbial communities involved in nitrogen cycling.

## Study Design and Sampling

- Field campaigns: Winter (Feb 2018) and Summer (Jul 2018).
- Habitat: Permeable riverbeds (sand or chalk geology); 12 sites across Hampshire Avon catchment, Kent, and Essex.
- Sample collection per sediment patch:
  - Deploy 15 probes at two depths (7 at 5 cm, 8 at 10 cm) across three patches.
  - Porewater sampling via syringe and vacuum; measure O2 and pH on site.
  - Preserve porewater for Fe(II) and gas analysis; filter and freeze for nutrient and chloride analysis.
  - 15N-labelled tracer injections (NH4+ or NO3-) in riverbed; 25 mL tracer, 4 time points, up to 60 minutes total.
  - A single 2 cm sediment core from each patch for molecular analyses; core placed >20 cm from probes and cryopreserved in liquid N2.
- Core and porewater sampling designed to avoid surface water contamination and to capture in situ transformation rates.

## Metadata and Spatial/Temporal Coverage

- Sampling metadata fields (examples):
  - Sample_ID, SiteCode, SiteName, Lat, Long, Geology (Chalk or Sand), Season (Winter or Summer), Depth (cm), Core.
- Spatial scale: 12 river sites with geo-coordinates; GIS-ready attributes include site location, underlying geology, and season.
- Temporal scale: two seasons across a single year (Winter 2018, Summer 2018).

## Measurements, Units, and Methodologies

- Nitrogen transformation rates (per litre per hour):
  - R_NO3: mean rate of 15N-NO3 production after NH4+ injection; unit µmol N L-1 h-1; calculated by linear regression of 15NO3- over time.
  - R_N2: mean rate of 15N-N2 production after nitrite injection; unit µmol N L-1 h-1; calculated by linear regression.
  - nitrification_efficiency: percentage, calculated as (R_NO3 / (R_NO3 + R_N2)) × 100.
- Porewater chemistry (on-site measurements):
  - temp: °C (River water temperature; measured with Hach multi-meter).
  - pH: unitless (measured with Hach multi-meter).
  - O2: µM (dissolved oxygen in porewater; corrected for contamination).
  - NO2: µM (nitrite; automated colorimetry).
  - NO3.NO2: µM (nitrite + nitrate; cadmium reduction for nitrate).
  - NO3: µM (nitrate derived from NOx minus nitrite).
  - NH3: µM (ammonium; indophenol blue method).
  - PO4: µM (phosphate; molybdenum blue method).
- Molecular analyses (gene abundances and transcripts; dry weight basis):
  - RNA targets (transcripts per g dry weight): Comammox amoA, Anammox hzo, nirS_C1, nosZ_C1.
  - DNA targets (gene copies per g dry weight): AOA amoA, AOB amoA, Bac 16S, Anammox hzo, Anammox hzsA, nirK_C1/2/3, nirS_C1/2, nosZ_C1/2, Nitrospira nxrB, Thaum_ureC.
  - DNA and RNA extraction and quantification methods (PowerSoil kits, qPCR with absolute quantification against standards).
- Sequence data and data access:
  - NCBI BioProject accession for raw amplicon data (16S, hzo, nirK, nirS, nosZ, AOA/AOB amoA, comammox amoA, Nitrospira nxrB, Thaum_ureC); sequences embargoed until publication.
  - DNA extraction, PCR amplification, library prep (Nextera XT), sequencing on Illumina MiSeq (4 runs).
- Key sources for methodology:
  - 15N tracer protocol and riverbed rate calculations (Lansdown et al., 2014).
  - Push-pull sampling and tracer matrix (Smart and Barko, 1985).

## Data Quality, Standards, and Access

- Quality notes:
  - On-site calibration and correction for O2 contamination; reported detection limits and precision for chemical measurements.
  - Nitrification efficiency and rate estimates rely on linear regression of time-series tracer data.
- Data standards:
  - Consistent units across measurements (µmol N L-1 h-1; µM; °C; etc.).
  - Metadata fields align with site-level geography, geology, season, and sampling depth.
- Access and provenance:
  - Raw sequence data embargoed; access via NCBI BioProject upon publication.
  - Detailed lab protocols and references provided for reproducibility.

## GIS and Data Integration Considerations

- Suitable for multi-layer GIS analyses combining:
  - Spatial layers: site locations, geology (chalk vs. sand), season, and sampling depths.
  - Attribute layers: porewater chemistry, temperature, pH, O2, NOx species, and trace nutrient concentrations.
  - Biological layers: gene/transcript abundances and presence/absence of key nitrogen-cycling taxa.
- Potential use cases:
  - Map spatial patterns of nitrification efficiency and nitrate production across permeable riverbeds.
  - Correlate nitrogen transformation rates with porewater chemistry and sediment geology.
  - Integrate molecular data to explore links between microbial community structure and observed biogeochemical rates.
- Important considerations:
  - Data span multiple resolutions (site-level summaries vs. depth-specific porewater and core samples; seasonal replication).
  - Embargoed sequencing data means some components may not be immediately available in GIS workflows.

## References and Documentation

- Lansdown et al. (2014): methodology for fine-scale in situ measurement of riverbed nitrate production and consumption.
- Smart and Barko (1985): tracer methodology for 15N-based rate measurements.
- Additional methodological references cited for specific genes and qPCR protocols within the dataset documentation.