# Overview

- Dataset from the in-stream N-cycling component of the PRINCe project, led by Prof. Mark Trimmer (Queen Mary University of London), focusing on nitrogen transformations in riverbeds.
- Field campaigns conducted in two seasons: winter (February 2018) and summer (July 2018).
- Study sites: 12 rivers with permeable beds (sand or chalk geology) across the Hampshire Avon catchment, Kent, and Essex.
- Objective: measure in situ rates of nitrogen transformations, porewater chemistry, and microbial gene abundance/transcripts to understand N cycling dynamics under varying phosphorus conditions.

- Field and sampling methods
  - Push-pull in-stream measurements using 15 bespoke stainless steel probes installed at two depths (7 probes at 5 cm, 8 probes at 10 cm) across three unvegetated sediment patches per sediment patch.
  - Porewater sampling via syringe with slight vacuum; measured O2 and pH in porewater; preserved samples for Iron(II) and gas analyses; filtered and frozen for nutrient and chloride analyses.
  - In situ 15N tracer experiments: inject 15N-labelled ammonium or nitrite into riverbed (approx. 300 µM; 98 atom % 15N) with 25 mL tracer, retrieving at four time points over up to 60 minutes.
  - Sediment cores: single 2 cm core per patch, subsampled at 5 and 10 cm for molecular analyses; cores placed ≥20 cm from probes to avoid contamination; cryopreserved in liquid N2.

- Measurements and metrics
  - Nitrogen transformation rates: R_NO3 (15N-NO3 production) and R_N2 (15N-N2 production); both in µmol N L-1 h-1; calculated via linear regression of time-series data.
  - Nitrification efficiency: (R_NO3 / (R_NO3 + R_N2)) × 100.
  - Physicochemical parameters: temperature (temp, °C), pH, dissolved oxygen (O2, µM).
  - Inorganic nitrogen and phosphorus: NO2 (µM), NO3.NO2 (NOx, µM), NO3 (µM), NH3 (µM), PO4 (µM); analyses via Skalar auto analyser and standard colorimetric methods with specified detection limits and calibration references.
  - Data provenance: methodology aligned with Lansdown et al. (2014) for fine-scale in situ measurements in permeable riverbeds.

- Molecular and genomic data
  - RNA (transcripts) targets: Comammox amoA, Anammox hzo, nirS (clade I), nosZ (clade I).
  - DNA (gene copies) targets: AOA amoA, AOB amoA, Bac 16S rRNA, Anammox hzo, Anammox hzsA, NirK (clades I–III), NirS (clade I–II), NosZ (clade I–II), Nitrospira nxrB, Thaumarchaeota ureC.
  - Units: transcripts per g dry weight sediment (RNA targets); gene copies per g dry weight sediment (DNA targets).
  - Primer sets and methodologies referenced for each target; DNA extraction using PowerSoil kit; qPCR and absolute quantification against calibration curves.
  - Metadata for sequencing: NCBI BioProject accession provides raw amplicon sequence data (archaeal and bacterial 16S, hzo, nirK_C3, nirS_C1, nosZ_C1, AOA_amoA, AOB_amoA, comammox_amoA, Nitrospira_nxrB); data embargoed until publication.

- Data structure and accessibility
  - Identifying information fields included for each sample: Sample_ID, SiteCode, SiteName, Lat, Long, Geology (Chalk or Sand), Season (Winter or Summer), Treatment_15A_15N, Depth (cm), Core (core identifier).
  - Data collection notes emphasize scale, cross-site standardization, and the potential to link environmental conditions with microbial activity and gene abundances.
  - Data and datasets may be uploaded to portals with metadata to support discoverability; sequence data currently embargoed and will be released upon manuscript publication.

- Relevance for analysis
  - Enables exploration of correlations between physicochemical conditions, nitrogen transformation rates, and microbial community gene/transcript abundances.
  - Supports modelling of in-stream N-cycling responses to environmental variables (e.g., temperature, oxygen, nutrient pools) across multiple sites and seasons.
  - Provides rich multi-omics data (RNA and DNA) alongside in situ process rates for holistic interpretation of nitrification, anammox, comammox activities in permeable riverbeds.