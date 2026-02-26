# Chemistry_PorewaterLitterSoil.csv; LitterBagData.csv; TBI_Data.csv

## Overview
- Field experiment conducted in the UK to study how acidity affects carbon cycling and litter decomposition in organic soils.
- Two sites (Migneint, Peaknaze) with two soil types (peat, peaty podzol) and a randomized blocked design across plots with control, acid, and alkaline treatments.
- Treatments applied from 2008–2012 and re-established 2015–2016; pH changes driven by sulfuric acid (acid) or base reagents (alkaline) with corresponding rinses to ensure infiltration and curb foliage toxicity.
- Data collected and interpreted by Dr. Catharine Pschenyckyj as part of a PhD project.

## Field Experiment Design
- Locations: Migneint (North Wales) and Peaknaze (Northern England).
- Plots: Twelve 9 m² plots per site, across four experimental sites named Migneint Peat, Migneint Podzol, Peaknaze Peat, Peaknaze Podzol.
- Experimental setup: Randomised blocked design with four replicates per treatment (control, acid, alkaline).
- Treatments:
  - Acid: H2SO4 + rainwater (50 kg S ha⁻¹ yr⁻¹ at podzol; 100 kg S ha⁻¹ yr⁻¹ at peat to account for buffering).
  - Alkaline: NaOH and KOH, followed by MgCl2 and CaCl2 rinse to maintain base cation ratios.
  - Control: Rainwater only.
- Schedule: Initial treatments Oct 2008–Dec 2012; re-established Jan 2015–Oct 2016.
- Field operations: 20 L rainwater or treatment solution applied, followed by a 10 L rinse to promote infiltration.

## Data Files and Metadata
- Data files included:
  - Chemistry_PorewaterLitterSoil.csv
  - LitterBagData.csv
  - TBI_Data.csv
- Data collection scope:
  - Samples taken from field plots with pore water, surface litter, and soil.
  - Pore water: monthly sampling Sep 2015–Oct 2016 at 10 cm depth from four plot locations; samples pooled per plot.
  - Litter: litter types from dominant vegetation; collected autumn 2015; litter bags buried at 5 cm depth (Oct 2015) and retrieved Oct 2016; quarterly mass loss measurements over 12 months.
  - Tea Bag Index (TBI): Green and Rooibos tea bags buried Jul 2016 for 90 days; three sets per plot; retrieved Oct 2016.
- Data collection and processing:
  - All data handling performed by the researchers listed; linked to published methods and prior studies (Evans et al. 2012; Keuskamp et al. 2013; Duddigan et al. 2020).
  - Each data file includes acronyms and units relevant to the measurements (see below).

## Sampling and Analytical Methods
- Chemistry_PorewaterLitterSoil.csv
  - Sample types: pore water, decomposing litter, soil.
  - Pore water: depth 10 cm; samplers used (Rhizon); four locations per plot; samples bulked per plot.
  - Litter: collected from 10 cm from plot edge to avoid compaction effects.
  - Soil: extracted from 10–20 cm depth.
  - Analyses: pH, electrical conductivity (EC), total organic carbon (TOC), dissolved organic carbon (DOC), ultraviolet absorbance; TIC and TC used to derive DOC for extracts.
  - DOC reporting: pore water DOC in mg/L; litter/soil extracts reported as mg DOC per g dry material.
  - Spectroscopy: UV-Vis scans 240–600 nm; correction factors applied for plate vs cuvette pathlength differences; SUVA254 calculated.
- LitterBagData.csv
  - Litter types: Calluna vulgaris, Eriophorum vaginatum, Festuca ovina, Pleurozium schreberi, Sphagnum spp.; collected per site.
  - Preparation: 2 cm pieces; litter bags (0.5 mm mesh) buried 5 cm deep; initial dry mass specified per species.
  - Retrieval: 12 months incubation; mass loss measured quarterly; post-extraction analysis of pH, EC, DOC, SUVA254.
- TBI_Data.csv
  - Tea Bag Index: two tea types (Green, Rooibos); 90-day burial; k_TBI and stabilisation factor S calculated per plot (per Keuskamp et al. 2013).
  - Data collected to compare decomposition rates under different pH treatments.

## Data Units and Acronyms
- Common abbreviations:
  - M = Migneint, PN = Peaknaze, Pod = Podzol, PW = Pore water, DSL = Decomposing surface litter
  - EC = Electrical conductivity, DOC = Dissolved organic carbon, SUVA254 = Ultraviolet absorbance proxy for DOC quality
  - TN = Total nitrogen, %ML = Percentage mass loss
- Data-specific units:
  - pH (pH units)
  - EC (μS)
  - DOC (mg/L for pore water; mg/L for extracts converted per gram of dry material)
  - SUVA254 (mg C⁻¹ m⁻¹)
  - TN (mg/L)
  - %ML (percentage)
  - DOCmgg (mg/L; specific to certain extract measurements)

## Data Governance, Sharing, and Quality
- Metadata completeness: detailed sampling protocols, depths, locations, and processing steps described to support verification and reuse.
- Open data considerations: notes on public sharing of underlying data and the need for clear metadata to facilitate reuse across agencies and researchers.
- Data quality: emphasis on quality assurance, cleaning, transformation, and clear presentation of findings via reports, charts, or dashboards.
- Data provenance: all data associated with a defined field experiment framework and linked to the researchers and publications cited.

## Key References
- Duddigan, S. et al. 2020. Chemical Underpinning of the Tea Bag Index: An Examination of the Decomposition of Tea Leaves. Applied and Environmental Soil Science.
- Evans, C. D. et al. 2012. Acidity controls on dissolved organic carbon mobility in organic soils. Global Change Biology.
- Keuskamp, J. A. et al. 2013. Tea Bag Index: a novel approach to collect uniform decomposition data across ecosystems. Methods in Ecology and Evolution.