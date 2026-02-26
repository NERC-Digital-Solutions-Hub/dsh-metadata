# Data files: Chemistry_PorewaterLitterSoil.csv; LitterBagData.csv; TBI_Data.csv

## Overview
- Field experiment conducted at two UK locations (Migneint, North Wales; Peaknaze, Northern England) to study effects of acidity on carbon cycling in organic soils.
- Experimental design includes two soil types (peat and peaty podzol), with randomized plots and four treatments (control, acid, alkaline) applied in two phases: 2008–2012 and 2015–2016.
- Data cover chemistry of porewater, litter and soil; litter decomposition using litter bags; and Tea Bag Index (TBI) decomposition metrics.
- Data collection led by Dr. Catharine Pschenyckyj; linked to a PhD project on acidity and carbon cycling.

## Datasets and contents

- Chemistry_PorewaterLitterSoil.csv
  - Sample types: pore water (PW), decomposing surface litter (DSL), soil (S) from four locations within each plot.
  - Sampling regime: monthly pore water samples Sept 2015–Oct 2016, about one week after treatments; depth ~10 cm.
  - Sampling method: Rhizon suction samplers; bulked to one sample per plot.
  - Analyses: pH, electrical conductivity (EC), total organic carbon (TOC), dissolved organic carbon (DOC), ultraviolet absorbance; SUVA254 calculated from UV spectra.
  - Units: pH, EC (μS), DOC (mg/L), SUVA254 (mg C^-1 m^-1).
  - Acronyms: M (Migneint), PN (Peaknaze), Pod (Podzol), PW (Pore water), DSL (Decomposing surface litter).
  - Notes: Data describe chemistry of porewater and organic matter extracts; DOC for porewater is in mg/L, while litter/soil extracts report mg DOC per g dry material.
  - Metadata format: CSV; includes protocol references and lab methods.

- LitterBagData.csv
  - Litter types: Calluna vulgaris, Eriophorum vaginatum, Festuca ovina, Pleurozium schreberi, Sphagnum spp.; collected from respective sites.
  - Incubation: litter bags buried Oct 2015; retrieved Oct 2016 after 12 months; additional control incubations at 3, 6, 9 months.
  - Processing: cleaned, dried, weighed; cold-water extraction for DOC; subsequent analyses for pH, EC, DOC, SUVA254.
  - Mass loss: measured as percentage mass loss (%ML) over time.
  - Litter specifics: different dry mass equivalents per species (e.g., Calluna 3 g, Sphagnum 1 g).
  - Units: pH, EC (μS), DOC (mg/L), SUVA254 (mg C^-1 m^-1), TN (mg/L), %ML, DOCmgg (mg/L).
  - Acronyms: M (Migneint), PN (Peaknaze), Pod (Podzol), CM/CP (Calluna from Migneint/Peaknaze), etc.
  - Notes: Includes quarterly mass loss measurements and post-extraction weights.

- TBI_Data.csv
  - Tea Bag Index (TBI) methodology to assess decomposition rate (k_TBI) and stabilisation factor (S).
  - Deployment: Green and Rooibos tea bags buried July 2016 for 90 days; three sets per plot.
  - Retrieval: bags recovered Oct 2016; decomposition metrics calculated following Keuskamp et al. (2013).
  - Acronyms: M (Migneint), PN (Peaknaze), Pod (Podzol), S (Stabilisation factor), K (Decomposition rate).
  - Notes: Standardized approach to compare decomposition across ecosystems; provides comparable metrics to other studies.

## Sampling, methods, and provenance

- Locations and sites
  - Migneint (North Wales): 3°48.8′ W, 52°59.6′ N.
  - Peaknaze (Northern England): 1°54.5′ W, 53°28.3′ N.
  - Four experimental plots per site: Migneint Peat, Migneint Podzol, Peaknaze Peat, Peaknaze Podzol (each with randomized blocks and four replicates per treatment).

- Treatments and timeline
  - Acid treatments: H2SO4 with rainwater; dosing 50 kg S ha^-1 yr^-1 (podzol) or 100 kg S ha^-1 yr^-1 (peat) with 10 L rainwater rinse.
  - Alkaline treatments: NaOH and KOH; rinsed with MgCl2 and CaCl2 to maintain base cation ratios similar to rainfall; target OH- concentration to match H+ in acid plots.
  - Control: rainwater only.
  - Treatment periods: Oct 2008–Dec 2012 and re-established Jan 2015–Oct 2016.

- Data collection and QA
  - All data collection and interpretation performed by Dr. Catharine Pschenyckyj.
  - Methods align with the PhD project on acidity and carbon cycling in organic soils; data linked to published literature (Evans et al. 2012; Keuskamp et al. 2013; Duddigan et al. 2020).

## Data quality, standards, and integration notes for GIS

- Data integration
  - Three CSV datasets with plot- and site-level associations; include site identifiers, soil type, and treatment.
  - Spatial component includes precise plot locations at two sites, enabling GIS mapping and spatial analyses of treatment effects and soil chemistry.

- Data standards and resolution
  - Data come from multiple experiments and extraction methods; harmonization relies on plot-level identifiers and consistent acronyms.
  - Resolution is at the plot level with monthly (PW) or seasonal (litter, TBI) measurements; detailed temporal alignment may require cross-referencing treatment dates and sampling points.

- Potential GIS considerations
  - Use site coordinates and plot metadata to create GIS layers for each dataset.
  - Combine chemistry (DOC, pH, EC, SUVA254) with decomposition metrics (ML, k_TBI, S) to study spatial patterns of acidity effects.
  - Link to external publications for methodological context and units verification.

## References and data provenance

- Core sources
  - Evans et al., 2012: Acidity controls on dissolved organic carbon mobility in organic soils.
  - Keuskamp et al., 2013: Tea Bag Index methodology.
  - Duddigan et al., 2020: Chemical underpinnings of Tea Bag Index.

- Project attribution
  - Data collected under the field experiment associated with the PhD project: The effects of acidity on recent changes in carbon cycling in organic soils (C. Pschenyckyj, University of Reading).