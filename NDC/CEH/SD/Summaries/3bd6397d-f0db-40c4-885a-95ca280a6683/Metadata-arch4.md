# Data files: Chemistry_PorewaterLitterSoil.csv; LitterBagData.csv; TBI_Data.csv

- Field and site setup
  - Field experiment conducted at two UK locations: Migneint (North Wales) and Peaknaze (Northern England).
  - At each site, two soil types were used: peat and peaty podzol, forming four experimental sites: Migneint Peat, Migneint Podzol, Peaknaze Peat, Peaknaze Podzol.
  - Experimental design: randomized blocked design with four replicates of each treatment (control, acid, alkaline) per site.
  - Plot details: each site has twelve 9 m² plots; treatments were applied from Oct 2008–Dec 2012 and re-established 2015–2016 with identical methods and allocations.
  - Treatments
    - Acid plots: H2SO4 with rainwater, 50 kg S ha⁻¹ yr⁻¹ (podzol) or 100 kg S ha⁻¹ yr⁻¹ (peat) to match environmental deposition; followed by rinsing.
    - Alkaline plots: NaOH and KOH, followed by rinse with MgCl2 and CaCl2 to maintain base cation ratios similar to rainfall.
    - Control plots: rainwater only.
  - Data collection leadership: Dr. Catharine Pschenyckyj; part of a PhD project on acidity and carbon cycling in organic soils.

- Data files and contents (metadata-focused)
  - Chemistry_PorewaterLitterSoil.csv
    - Sample types: pore water, decomposing surface litter, soil.
    - Sampling: monthly pore water samples Sep 2015–Oct 2016 (about one week after treatments); depth of 10 cm; four locations per plot; samples pooled to one per plot.
    - Extraction and preparation: cold-water extraction with MilliQ water (litter 1:20 w/v; soil 1:10 w/v); shaking, centrifugation, and filtration.
    - Analyses: pH, electrical conductivity (EC), total organic carbon (TOC), ultraviolet absorbance; DOC concentration derived by subtracting TIC from TC using Thermalox TC-TN analyser.
    - Units: pH, EC (μS), DOC (mg/L) for pore water; DOC per g dry material for litter/soil extracts.
    - Optical properties: UV-Vis absorbance 240–600 nm; SUVA254 calculated with pathlength correction.
    - Acronyms: M = Migneint, PN = Peaknaze, Pod = Podzol, EC = Electrical conductivity, DOC = Dissolved organic carbon, PW = Pore water, DSL = Decomposing surface litter.
    - Data format: CSV; includes CD (acronyms) and unit definitions.

  - LitterBagData.csv
    - Objective: assess acidity effects on litter decomposition using litter bags buried in plots.
    - Litter types: Calluna vulgaris, Eriophorum vaginatum, Festuca ovina, Pleurozium schreberi, Sphagnum spp. (from respective sites); vascular plants from above-ground biomass; bryophytes collected as blocks.
    - Preparation and burial: dried, masses chosen per species (3 g Calluna/Eriophorum/Festuca; 1 g Sphagnum/Pleurozium); bags 10 × 10 cm with 0.5 mm mesh; buried at 5 cm depth in Oct 2015.
    - Incubation and measurements: retrieved Oct 2016 after 12 months; quarterly mass loss measurements over the year; additional incubations (3, 6, 9 months) in control plots for Calluna and Eriophorum.
    - Analyses: litter post-extraction pH, EC, DOC, SUVA254; mass loss calculated as percentage.
    - Units and acronyms: similar to above, with extra TN (total nitrogen) and %ML (percentage mass loss); species-specific codes included (CM, CP, F, E, S, etc.).
    - Data format: CSV; includes site and species coding (M/PN/Pod).

  - TBI_Data.csv
    - Objective: Tea Bag Index to standardize decomposition rate (k_TBI) and stabilisation factor (S) across ecosystems.
    - Tea types: Green and Rooibos (Lipton tea bags); three sets per plot.
    - Burial and retrieval: buried July 2016 for 90 days; retrieved Oct 2016; decomposition metrics calculated per Keuskamp et al. (2013).
    - Outputs: k_TBI (decomposition rate) and S (stabilisation factor).
    - Acronyms: S = Stabilisation factor, K = Decomposition rate (for Tea Bag Index); site codes as above (M, PN, Pod).
    - Data format: CSV.

- Data provenance and usage context
  - Data collected as part of a PhD project: “The effects of acidity on recent changes in carbon cycling in organic soils” (C. Pschenyckyj) at the University of Reading.
  - Related references: Evans et al. 2012; Keuskamp et al. 2013; Duddigan et al. 2020 (contextualizes Tea Bag Index chemistry).

- Data quality, interoperability, and management considerations for Data Leaders
  - Comprehensive metadata across three distinct data streams (porewater/soil chemistry, litter decomposition, and Tea Bag Index) to support cross-study synthesis.
  - Standardized measurement approaches and units within each dataset, with explicit acronyms and data processing steps to aid discoverability and reuse.
  - Cross-site design enables comparisons across soil types and acidity treatments, facilitating system-wide data analysis and prioritization.
  - Potential data harmonization needs: align units across files (e.g., DOC concentrations, SUVA254) and ensure consistent sampling timing and depth references.
  - Provenance and governance: data stewardship attributed to a principal researcher with documented methods; clear links to published literature for reproducibility.

- Potential uses for data leaders
  - Assess end-to-end data lifecycle: planning, collection, processing, metadata, and dissemination.
  - Inform data strategy on multi-site ecological experiments, including data standardization and cross-domain compatibility.
  - Support development of data sharing and discovery practices by exemplifying structured metadata and clear data provenance.
  - Facilitate cross-dataset analyses of acidity effects on DOC dynamics, litter decomposition, and decomposition rate stabilization.