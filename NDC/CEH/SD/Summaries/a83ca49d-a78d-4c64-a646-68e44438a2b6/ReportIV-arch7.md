# NERC Soil Biodiversity Thematic Programme: Sourhope Site Summary

- Purpose and scope
  - Four-year longitudinal field study at Sourhope to understand soil biodiversity and its feedbacks with above-ground plant communities.
  - Focus on above-ground productivity, species composition, and relative abundance (diversity) under varied management.

- Spatial design and data architecture (GIS-ready)
  - Site: Rigg Foot Experimental Site, Sourhope, on a downslope environmental gradient.
  - Layout: 5 replicate blocks; within each block 6 main plots with treatments randomly allocated; each main plot subdivided into 10 sub-plots; data collected in 0.5 m x 0.5 m cells within sub-plots S, T, U & V.
  - Treatments (plot level): Control 1, Control 2 (unfertilised), Nitrogen, Lime, Nitrogen and Lime (N&L), Insecticide.
  - Management and data layers: mowing all-site (~6 cm) monthly May–Sept; insecticide applied after mowing on designated plots; spring applications of nitrogen and/or lime; accompanying datasets include 1999–2002 biomass, soil pH, soil moisture, weather, and detailed species inventories.
  - Data products to build: spatial layers for blocks, plots, sub-plots, and 0.5 m2 data cells; time-series layers for biomass, pH, moisture, diversity indices, and species/hits at year level; Appendix maps and lists provide baseline and activity context.

- Treatments and management regime
  - Site-level: annual mowing to ~6 cm from May to September.
  - Plot-level: nitrogen and/or lime applied in spring; insecticide (Dursban 4 OPA) applied to insecticide plots after mowing.
  - Yearly timing: detailed per Appendix 2 (dates and rates for nitrogen, lime, and insecticide across 1999–2002).

- Data collection and processing (timeseries and spatial detail)
  - Weather: on-site Automatic Weather Station with continuous data since 1999; occasional data gaps in 2002 due to equipment issues later corrected with nearby station data.
  - Above-ground productivity: quarterly biomass samples from randomly selected 0.5 m2 cells within sub-plots; samples dried and weighed.
  - Baseline and longitudinal vegetation surveys:
    - Baseline 0.5 m2 quadrat with 25-point sampling (July 1998).
    - Annual point analysis surveys (2000–2002) using a 0.5 m2 cell with a 100-hole grid; species touched by the pin recorded per point.
  - Soil data: soil pH at ~5 cm depth (since 1998; measured March 2002 and August 2002 in plots and point-analysis cells); soil moisture (theta probe) measured in 2002 across point-analysis cells.
  - Taxa inventories: vascular plants and bryophytes recorded; bryophytes identified to species level in 2002; Appendix 3 lists full species accounts.
  - Data analyses: ANOVA (split-plot), PCA for point-analysis data, and diversity indices (Shannon) calculated across years; biomass time-series summarized per plot and year (see Appendix 6–8 for detailed tables and figures).

- Key results (highlights aligned to GIS-ready interpretation)
  - Productivity and treatment effects
    - Nitrogen and Lime together yield the strongest and most sustained biomass production; fertilised plots outperform unfertilised ones.
    - In 2002, biomass generally declined relative to 2001 across most treatments, with Control 2 showing the largest drop; bottom slopes showed greater reductions than lower blocks.
  - Soil chemistry and its links to productivity
    - Lime markedly increases soil pH toward ~7 in treated plots; nitrogen also raises pH but to a lesser extent.
    - A strong negative correlation exists between soil moisture and pH; higher pH plots tend to be drier, influencing productivity patterns.
    - Across all plots, higher pH correlates with higher biomass when considered collectively, but treatment-specific patterns show nuanced relationships (e.g., positive, neutral, or negative trends within individual treatments).
  - Biodiversity and plant functional groups
    - Point analyses show shifts in species composition: Festuca rubra and Poa pratensis dominate in improved plots; Festuca ovina and Anthoxanthum odoratum dominate in unimproved plots.
    - Bryophyte abundance increases across the site, particularly in unimproved plots, contributing substantially to overall hits in 2002.
    - Shannon diversity: increases in several treatments over time but declines notably in nitrogen+lime plots by 2002 relative to baseline; insecticide plots show notable diversity gains in some years.
    - Functional group dynamics (based on CSR framework):
      - Stress-tolerators (S) expand most in unimproved plots.
      - Competitive-stress-ruderal (CSR) and SR/CSR groups become dominant in nitrogen+lime plots.
      - Insecticide and lime treatments reduce SR/CSR dominance; overall, C-S-R groups increase where fertility rises.
  - Species and community structure analyses
    - PCA of point-analysis data separates improved vs. unimproved plots; lime-treated plots cluster together, with some nitrogen-treated plots showing similarities to limed plots.
    - Dominant bryophyte genus Rhytidiadelphus squarrosus increases across years; bryophytes are relatively rare on N&L plots.
  - Trampling effects
    - 2002 C2 plots show reduced productivity, likely due to trampling during 13CO2 pulse activities rather than a direct treatment effect.

- Data sources and appendices (for GIS data validation and integration)
  - Appendix 1: Site map showing orientation and treatment allocations.
  - Appendix 2: Summary of site and plot-level treatments with timing and rates.
  - Appendix 3: Species lists for vascular plants and bryophytes (2002 is detailed at species level).
  - Appendix 4: Site activity timeline.
  - Appendix 5: Weather station data and notes on 2002 data gaps.
  - Appendix 6–7: Biomass data per plot and yearly/ cumulative totals per block.
  - Appendix 8: 2000–2002 point-analysis species rank data and bryophyte contributions.

- Implications for GIS-enabled data products
  - Rich, multi-layer temporal dataset ideal for interactive maps, time-series dashboards, and spatial models linking management actions to vegetation outcomes.
  - Potential map products
    - Block/plot-level productivity heatmaps over time; slope-gradient visualizations to show spatial productivity patterns.
    - Soil pH and moisture distribution maps across plots and over years, with links to corresponding biomass.
    - Species-hits distribution maps by treatment and year; bryophyte distribution maps highlighting unimproved plots.
    - Functional-group maps showing shifts from stress-tolerators to competitive/ruderal groups under fertilisation.
    - PCA ordination overlays to illustrate spatial clustering of plots by treatment and year.
  - Data quality and caveats to consider
    - Data gaps in 2002 due to weather-station issues; some 2002 data were substituted from a nearby station.
    - Control 2 plots were not surveyed in 2000–2001 for some datasets; account for this in longitudinal analyses.
    - Field-scale data reflect nested spatial design (blocks, plots, sub-plots, 0.5 m2 cells) requiring careful hierarchical data modeling for GIS analyses.

- Overall takeaway for GIS specialists
  - The Sourhope site provides a well-documented, spatially explicit, multi-year dataset linking management actions (mowing, fertilisation, insecticide, trampling) to plant productivity, community composition, and functional traits.
  - It enables the development of robust, map-based data products and spatial analyses to support ecological interpretation, policy communication, and stakeholder-facing visualisations.