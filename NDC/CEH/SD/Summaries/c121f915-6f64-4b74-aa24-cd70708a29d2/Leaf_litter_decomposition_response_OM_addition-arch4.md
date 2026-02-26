# Leaf litter decomposition of Welsh upland rivers in response to organic matter addition

## Purpose and scope
- Quantify leaf litter decomposition in Welsh upland streams under organic matter addition using a BACI design.
- Compare decomposition between upstream reference (control) and downstream experimental zones using fine and coarse mesh litter bags.
- Derive decomposition rates and track changes in leaf mass remaining over time.

## Experimental design
- Before-after-control-impact (BACI) framework with upstream reference and downstream experimental zones within each stream.
- Zones similar in length and habitat; ~20–50 m separation to ensure independence.
- Time periods: before (T1; 61–65 days, Nov 2012–Jan 2013) with equal treatment of zones, and after (T2; 57–62 days, Jan–Mar 2013) with leaf litter addition in the experimental zone only.
- Leaf litter addition: proportionally distributed 1-tonne bags of deciduous leaves (oak, birch, alder) to the experimental zone; minimum wet weight target of 1.7 kg m^-2 maintained.
- Additional litter: 630 kg (wet weight) added on 12 Feb 2013 and 5 Mar 2013 after storm events.

## Field procedures and data collection
- At end of the before period (T1), half of litter bags were removed and six new fine-mesh and six new coarse-mesh bags were added to each pole to measure decomposition during the after period (T2).
- Bags removed at the end of the experiment: bags added at T0 (approx. 18 weeks in situ) and bags added at T2 (start of after manipulation).
- Sample preservation: on-site 70% ethanol in labeled polystyrene bags; transported to laboratory.
- Laboratory processing: rinsing of leaf material, air-drying to constant mass; macroinvertebrates separated from litter bag contents.
- Analytical method for leaf mass: ash-free dry mass (AFDM) determined by combusting a 1 g subsample at 500°C, following standard methods (Benfield 2006, Methods in Stream Ecology).

## Data collected and structure
- Primary metric: percentage of leaf mass remaining in fine and coarse mesh bags over time.
- Decomposition rates: calculated as percent mass loss per day for fine and coarse mesh bags.
- Data files (flatbed CSV) include 10 columns:
  - site
  - Code of the sampling site
  - landuse
  - region
  - reach (experimental or control site)
  - t0 (date bags placed)
  - t1 (date of leaf addition to experimental reach)
  - t2 (end date of experiment)
  - days (length of experiment)
  - time (Before or After manipulation)
  - replicate
  - fine.percent.remaining
  - coarse.percent.remaining
  - fine.precent.loss.day-1
  - coarse.precent.loss.day-1

## Supporting materials and metadata
- DURESS_CU_site_description.csv provides site-level metadata:
  - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation
  - Survey campaign details (e.g., WAWS-Wye survey, Plynlimon catchment, Llyn Brianne catchment)
  - Catchment information for contextualization and spatial mapping

## Data quality, provenance, and references
- Methodology aligned with established stream ecology practices (Benfield 2006).
- Clear linkage between field manipulation (T1 vs T2) and measured outcomes (fine vs coarse litter bag decomposition).
- Metadata includes site descriptions and standardized data fields to aid discoverability and reuse across studies and networks.

## Implications for data strategy and governance
- Demonstrates a well-documented, reproducible data workflow from field manipulation to laboratory processing and data structuring.
- Provides a standardized CSV schema with explicit variable definitions and units, facilitating data integration across studies.
- Emphasizes the importance of linking data with site metadata to enable cross-site analyses and collaboration within wider data communities.