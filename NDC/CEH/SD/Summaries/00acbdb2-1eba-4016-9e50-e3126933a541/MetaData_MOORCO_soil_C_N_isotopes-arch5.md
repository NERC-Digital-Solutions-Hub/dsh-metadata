# Dataset Title: Carbon and nitrogen stable isotopes in soil profiles at the Glensaugh and Ballogie MOORCO 'BIG' experimental tree planting sites.

## Overview
- Single CSV dataset (1 file) containing data for both Glensaugh and Ballogie MOORCO 'BIG' experimental sites in North East Scotland.
- Period of record: 10-Nov-2021 to 12-Nov-2021.
- 320 records.
- Contains 13C and 15N stable isotope data for organic soil profiles (from organic horizons to the top of the E horizon), plus total soil carbon and nitrogen stocks and bulk density.
- MOORCO-BIG experiment details: fenced plots vs unfenced controls; planted birch and pine trees at 1 m spacing; replication of n=4 (Glensaugh) and n=3 (Ballogie).

## Data structure and content
- File format: 1 CSV file.
- Key fields (examples): Site, Date, Sample.ID, Species, Quadrat, Horizon, Depth.cm, volume.cm3, g.OD.soil.plus.roots, OD.stones.g, calc.stone.vol.cm3, dry.bulk.density.DBf.g.per.cm3, per.C, per.N, CN.ratio, C.stock.kg.per.m2, per.SMC, delta.13.C.VPDB, delta.15.N.Air.
- Horizon categories: LFH (top litter/fermentation), Organic top, Organic lower, Mineral (top of mineral soil); field-identified and split where applicable.
- Units: various (percent C/N, isotope ratios in ‰, kg/m2 for stocks, g/cm3 for bulk density, cm for depth, cm3 for horizon volume, etc.).
- Data quality: missing value code NA; QC notes indicate ranges checked and no obvious outliers identified.

## Sampling and field methods
- Sampling tool: 5 x 5 cm steel box corers.
- Procedure: 4 randomly located cores per plot to full organic horizon depth and top 2 cm of mineral soil.
- Horizons separated in the field, bagged, and kept chilled for lab processing.
- Field example records show horizon segmentation and core-level documentation.

## Laboratory analyses and isotopic measurement
- Sample processing: air-dried at 30°C; organic horizons milled (Hammer mill to 2 mm; further processing to remove >2 mm stones and roots); subsamples oven-dried for weight determinations.
- Total C and N determination: automated Dumas combustion using Carlo Erba NA 1500 Elemental Analyser.
- Isotope analysis: 13C and 15N ratios measured by EA-IRMS (separate runs due to high C:N ratios); equipment and reactor specifics provided (chromium oxide/silvered copper oxide, reduction reactor, Carbosieve GC column, etc.).

## Calculations and derived data
- C stock calculations: Carbon Stock [kg/m2] derived from dry bulk density, C content, and core length.
- Bulk density and stone corrections: dry bulk density computed after stone removal; stone volume estimated from oven-dried stones.
- Volume and weight calculations: fresh and air-dried weights used to estimate oven-dry soil weight; soil moisture content and related parameters calculated.
- Units and derived variables consistently documented (e.g., C.stock.kg.per.m2, per.DWT, per.SMC).

## Data governance, provenance, and metadata
- Source context: MOORCO project focusing on woodland succession dynamics; BIG experiment includes Pinus sylvestris and Betula pubescens plots and heather controls; replication and plot treatments described.
- Maintainer: Lorna Street; contact: lstreet1@ed.ac.uk.
- Data are tied to a specific experimental design (fenced vs unfenced; planted birch/pine vs controls) and site locations (Glensaugh and Ballogie) with grid coordinates referenced in background.
- Comprehensive field and lab methods included to support reproducibility and provenance.

## Accessibility, Sharing, and update considerations
- Dataset is a single CSV with extensive metadata on variables, units, and methods.
- Data sharing considerations are addressed through detailed variable definitions, measurement methods, QC steps, and provenance notes.
- For updates or revisions, contact the maintainer; replication and study context should be preserved to maintain interoperability.

## Usage notes and limitations
- Data are limited to two MOORCO BIG sites and a short sampling window in November 2021; temporal dynamics beyond this period are not captured here.
- Isotopic values are reported alongside C and N stocks and bulk density, enabling studies of soil carbon/nitrogen status under tree planting treatments.
- Users should consult horizon definitions and field notes to ensure correct interpretation of LFH, Organic, and Mineral horizons and depth assignments.