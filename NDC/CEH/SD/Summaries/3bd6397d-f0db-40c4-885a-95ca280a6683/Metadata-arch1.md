# Data files

- Field experiment overview
  - Conducted at two UK sites: Migneint, North Wales (peat and peaty podzol soils) and Peaknaze, Northern England.
  - Experimental design: twelve 9 m2 plots per site in a randomised blocked layout with four replicates for each of four plot categories (Control, Acid, Alkaline) across two soil types.
  - Treatments administered 2008–2012 and re-established 2015–2016; acid plots received H2SO4 with rainwater, alkaline plots received NaOH/KOH with a rinse to balance base cations; controls received rainwater only.
  - Data collected by Dr. Catharine Pschenyckyj as part of a PhD project on acidity and carbon cycling in organic soils.

- Data files and contents
  - Chemistry_PorewaterLitterSoil.csv
    - Sample types: pore water, decomposing litter, and soil.
    - Sampling: monthly pore water samples (Sept 2015–Oct 2016) at 10 cm depth from four locations per plot, pooled per plot.
    - Measurements: pH, electrical conductivity (EC), total organic carbon (TOC), dissolved organic carbon (DOC), UV absorbance; SUVA254 calculated; pore water DOC in mg/L; litter/soil DOC per g dry material.
    - Methods: cold water extraction (litter: 1:20 w/v; soil: 1:10 w/v); TE-TN analyzer for DOC/TIC; UV-Vis spectroscopy with correction factor.
    - Abbreviations and units included (e.g., PW, DSL, DOC, SUVA254; pH, μS, mg/L).

  - LitterBagData.csv
    - Litter types: Calluna vulgaris, Eriophorum vaginatum, Festuca ovina, Pleurozium schreberi, Sphagnum spp. (from respective sites).
    - Burial and processing: litter bags buried Oct 2015 at 5 cm depth; 3 g Calluna/Eriophorum/Festuca or 1 g Sphagnum/Pleurozium per bag; 0.5 mm mesh; bags collected Oct 2016 after 12 months; quarterly mass loss measurements (3, 6, 9 months follow-up in control plots).
    - Measurements: mass loss (%ML), cold-water extract DOC, DOC concentration, pH, EC, SUVA254, total nitrogen (TN).
    - Data structure includes site codes (Migneint/Peaknaze; Podzol/Peat) and plant-type provenance (CM, CP, etc.).

  - TBI_Data.csv
    - Tea Bag Index (TBI) study to assess decomposition rate (K_TBI) and stabilisation factor (S).
    - Tea types: Green and Rooibos (Lipton), 3 sets per plot; buried July 2016 for 90 days; retrieval Oct 2016.
    - Outputs: K_TBI (decomposition rate) and S (stabilisation factor) following Keuskamp et al. methodology.

- Metadata, identifiers, and data standards
  - Acronyms: M (Migneint), PN (Peaknaze), Pod (Podzol), EC (electrical conductivity), DOC (dissolved organic carbon), PW (pore water), DSL (decomposing surface litter), etc.
  - Units: pH (units), EC (μS), DOC (mg/L), SUVA254 (mg C-1 m-1), TN (mg/L), %ML (percentage), DOCmgg (mg/L) for litter extracts.
  - Data provenance: explicitly states sampling protocols, extraction methods, instrumentation (Thermo-TAN analyzer, UV-Vis microplate reader), and correction factors for pathlength.

- Study methodology and measurements
  - Porewater, litter, and soil sampling procedures, including depth, timing, and handling to minimize disturbance.
  - Extraction and analysis protocols for DOC, TOC, TIC, SUVA254, pH, EC.
  - Litter bag incubation and post-extraction processing to determine mass loss and DOC contributions.
  - Tea bag methodology to enable cross-study comparability of decomposition and stabilisation metrics.

- Purpose and potential analyses for data analysts
  - Examine how acidity treatments influence DOC mobility and quality (DOC concentration, SUVA254) across porewater, litter, and soil.
  - Quantify effects of acid/alkaline treatments on litter decomposition rates and stabilisation (mass loss, TN, DOC, SUVA254).
  - Compare decomposition dynamics between peat and podzol soils, and between sites.
  - Integrate multiple data streams (chemistry, litter decomposition, and Tea Bag Index) to model carbon cycling responses to pH-altering treatments.
  - Use metadata and standardized units to enable cross-site and cross-study comparisons.

- Challenges and considerations relevant to analysts
  - Local-scale data and multi-source integration may require careful harmonisation of units and acronyms.
  - Access to detailed site-level metadata, treatment histories, and sampling windows is essential for robust modeling.
  - Data represent a mix of direct measurements and derived indices (e.g., K_TBI, S, SUVA254); documentation supports reproducibility and interpretability.
  - Privacy and data governance considerations are minimal here, but proper data provenance and citation are noted.