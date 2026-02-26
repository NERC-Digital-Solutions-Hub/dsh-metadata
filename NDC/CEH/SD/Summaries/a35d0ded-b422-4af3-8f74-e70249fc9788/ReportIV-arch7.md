Soil Biodiversity Thematic Programme: Sourhope Site Summary

## Overview
- Four years of intensive study at the Sourhope field site (Scottish Borders) investigating soil biodiversity and its links to above-ground plant communities.
- Primary focus: above-ground productivity, plant species composition, and diversity under different management treatments.
- Key management drivers: mowing (site-wide), fertilisation (nitrogen and/or lime), and insecticide application; trampling effects also noted.
- Aim to understand how below-ground biodiversity interacts with above-ground plant communities and how functional traits shift under treatments.

## Spatial Design and Data Layers
- Experimental layout: Rigg Foot site with 5 replicate blocks on a downslope gradient; each block contains 6 main plots subdivided into 10 sub-plots, with 0.5 m x 0.5 m cells used for data collection.
- Treatments mapped to plots (Appendix 1 map available; 2002 field changes noted: Biocide plots renamed Insecticide).
- Data collection per cell/sub-plot includes:
  - Above-ground biomass (seasonal 0.5 m2 cell samples, oven-dried and weighed)
  - Point analysis surveys (0.5 m2 cell; 100-hole grid; yearly July/August surveys in 2000–2002)
  - Soil pH (5 cm depth) and soil moisture (theta probe in 2002)
  - Weather data from on-site Automatic Weather Station (1999 onward)
- Additional data: species lists (vascular + bryophytes), litter hits, and diversity indices (Shannon).

## Treatments and Management
- Site-level management: monthly mowing May–Sept to ~6 cm; insecticide application after mowing.
- Plot-level treatments (constant yearly schedule since 1999):
  - Control 1: no treatment
  - Control 2: no treatment
  - Nitrogen (NH4NO3): estimated annual N input; applied spring
  - Lime (CaCO3): annual spring application
  - Nitrogen & Lime (N&L)
  - Insecticide: Dursban 4 (chlorpyrifos), applied after mowing on insecticide plots
- Data interpretation considers both fertilisation and disturbance/management effects (e.g., mowing vs grazing history).

## Key Findings by Theme

### Mowing and Disturbance
- Regular mowing promotes Festuca rubra in fertile plots and reduces Agrostis spp.; bryophyte expansion observed across the site, linked to a ~6 cm sward height and reduced disturbance.
- Disturbance regime (mowing-only vs prior grazing) influences functional groups; stress-tolerant species increase under unimproved conditions.

### Fertilisation (Nitrogen and Lime)
- Fertilised plots show higher productivity, especially where N and lime are applied together; productivity may be peaking in these plots (soil pH near 7.0 in lime-treated plots).
- Higher soil pH and reduced soil moisture in fertilised plots may contribute to stress under drought, with chlorosis observed in lime-treated areas.
- Functional shift: nitrogen-and-lime plots show expansion of competitive-stress-ruderal (CSR) and C-S-R groups; pure lime or nitrogen effects differ, with pH often more influential than nitrogen alone for CSR dynamics.

### Insecticide Effect
- Diversity (Shannon) and species composition show changes that could be consistent with reduced herbivory allowing more palatable plants to persist; however, direct causation between insecticide and diversity is not definitively proven.
- Patterns align with prior work suggesting complex interactions between herbivory and plant community composition.

### Trampling and Disturbance
- C2 plots (under some experimental periods) show reduced productivity, likely due to trampling during 13CO2 pulse experiments; disturbance magnitude affects biomass outcomes.

## Data Collected and How It Maps Geospatially
- Temporal data (1999–2002) show year-to-year changes, with long-term trends of increasing biomass across most treatments, but 2002 reductions relative to 2001.
- Spatial patterns:
  - Slope effects: Block 5 shows greater declines in biomass than bottom-block Block 1 in some years.
  - Fertile treatment zones (N and/or lime) show the strongest biomass response, while unimproved plots lag.
  - Bryophyte expansion is widespread, with higher bryophyte hits in unimproved plots and greater moss diversity in later years.
- Multivariate analyses:
  - Principal Components Analysis (PCA) of point-analysis data reveals clear separation between improved (fertilised) and unimproved plots; lime-treated plots cluster distinctly, and nitrogen-treated plots show mixed associations by block.
  - Functional-group composition (S, CSR, SR/CSR) tracks across plots and years, highlighting spatially variable ecological responses.

## Data Quality, Gaps, and Considerations for GIS
- Data gaps and anomalies:
  - 2002 weather data gaps due to station malfunction; Konza station data substituted for missing periods.
  - New site activity in 2002 for some plots (C2) due to specialised campaigns; some plots surveyed inconsistently in early years.
- Data heterogeneity:
  - Multiple data types (biomass, species hits, bryophyte counts, litter, soil chemistry, moisture) across several years and nested plots.
- For GIS use:
  - Build layered, time-aware datasets: blocks → plots → sub-plots → cells; attach attributes for Treatment, Year, Biomass, pH, Moisture, Diversity, Bryophyte hits.
  - Include appendices as reference layers: site map (Appendix 1), species lists (Appendix 3), biomass per plot (Appendix 6), PCA/PC loadings (Figure 5), and rank abundance data (Appendix 8).

## GIS-ready Data Products and Recommendations
- Suggested map layers:
  - Treatment allocation map by plot and block (static)
  - Yearly biomass heatmaps by plot/sub-plot (1999–2002)
  - Soil pH and moisture rasters by plot/year (where available; 2002 data emphasized)
  - Bryophyte and vascular plant distribution maps by treatment (from Point Analysis; bryophyte 1998–2002 trends)
  - Flowering/functional-group distribution maps (S, CSR, SR/CSR) by year and treatment
- Time-series analytics:
  - Track changes in biomass, diversity indices, and functional group composition over time per treatment and spatial block.
  - Analyze slope/position effects by integrating block geometry with productivity and soil chemistry layers.
- Decision-support visuals:
  - Overlay maps showing areas with highest productivity gains (N+L) and areas with bryophyte expansion (potential habitat shift indicators).
  - Dashboard-style views combining biomass, pH, moisture, and diversity across years to assess trade-offs of management options.

## Practical Takeaways for GIS Specialists
- The Sourhope dataset provides a rich, multi-layered geospatial view of how management interventions influence above- and below-ground ecology.
- Efficient GIS product design should:
  - Maintain a robust, time-stamped schema (year as a key dimension).
  - Preserve plot-level and cell-level granularity for detailed spatial analyses while enabling summary views by block and treatment.
  - Integrate biological classification (vascular bryophytes; CSR functional groups) with environmental variables (pH, moisture, rainfall) for composite indicators.
- Data products should accommodate both static treatment maps and dynamic, year-by-year analyses to support policy and research audiences interested in land-use impacts on biodiversity and productivity.