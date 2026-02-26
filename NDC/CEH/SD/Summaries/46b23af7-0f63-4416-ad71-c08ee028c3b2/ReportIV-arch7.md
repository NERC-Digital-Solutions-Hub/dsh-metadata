# NERC Soil Biodiversity Thematic Programme: Sourhope Site Summary

- Four years into the Soil Biodiversity Thematic Programme, focused on a large field experiment at Sourhope (Scottish Borders) examining above-ground productivity, plant composition, and diversity in relation to management interventions.
- Main goal: understand links between soil biodiversity and plant communities; monitor above-ground responses to site management and treatments.

## Site, layout, and treatments (spatial context for GIS)

- Location: Rigg Foot Experimental Site, Sourhope; 5 replicate blocks on a downslope gradient; each block contains 6 main plots, subdivided into 10 sub-plots, with a 0.5 m x 0.5 m cell system used to allocate treatments.
- Treatments (plot-level): 
  - Control 1 (no treatment)
  - Control 2 (no treatment)
  - Nitrogen
  - Lime
  - Nitrogen & Lime
  - Insecticide (Dursban 4 OPA; previously Biocide)
- Site-level management: monthly mowing to ~6 cm (May–Sept); insecticide applied after mowing to designated plots; fertilisers applied in spring as specified.
- Data collection scope: multi-year, multi-layer datasets including biomass, plant species composition (vascular plants and bryophytes), soil chemistry, and microclimate.

## Key datasets and GIS-ready variables

- Above-ground biomass
  - Monthly biomass measurements (May–Sept) per 0.5 m2 cell within sub-plots; annual totals by plot; trend across years (1999–2002).
  - Normalised biomass: each plot’s biomass expressed relative to its Control 1 baseline.
- Soil chemistry and moisture
  - Soil pH (5 cm depth) by plot (Aug 2002; baseline 1998; additional 2002 measurements).
  - Soil moisture content (theta probe) in 2002, measured in corners of point-analysis cells.
- Vegetation surveys
  - Point Analysis (2000–2002): 100-hole grid per cell; records of each touched species; bryophyte vs vascular plant identification enhanced in 2002.
  - Species frequency by treatment (control vs improved plots) and by year.
  - Functional grouping (as per CSR framework): stress-tolerators (S), competitive-stress-ruderals (CSR), stress-ruderal/competitive-stress-ruderals (SR/CSR).
  - Relative abundance by functional group and by taxon (monocots, dicots, bryophytes) for each treatment-year.
- Diversity metrics
  - Shannon Diversity Index by treatment across years; changes relative to baseline.
- Community structure analyses
  - Principal Components Analysis (PCA) of 2002 point-analysis data to separate improved vs unimproved plots and to visualize treatment clustering by species.
- Disturbance and management context
  - Mowing regime, absence of grazing since 1998, and observed trampling effects (notably on C2 plots during 13CO2 pulse experiments).
- Weather and site context
  - Automatic Weather Station data: rainfall, radiation, temperatures (notable year-to-year fluctuations and mild winter 2001/02).

## Key findings (highlights for GIS interpretation)

- Mowing effects
  - Decline of Agrostis capillaris and Agrostis vinealis across most plots since 2000, suggesting a site-level factor related to mowing regime rather than a single treatment.
  - Festuca rubra expansion, particularly in fertile plots (lime/N), and widespread bryophyte expansion linked to maintained sward height (~6 cm) and loss of grazing.
- Fertilisation effects
  - Nitrogen and/or lime generally increase above-ground biomass; plots with both nitrogen and lime show the strongest productivity, though signs of potential peak and moisture stress at high pH/low moisture.
  - Soil pH elevations near 7.0 in limed plots; higher pH relationships with biomass are strong overall, but positive links attenuate or reverse in plots with both N and lime.
  - Functional group shifts: N and/or lime promote C-S-R (competitive-stress-ruderal) species; stress-tolerators dominate unfertilised plots.
- Insecticide effects
  - Dursban-treated plots show higher diversity in some analyses; evidence is circumstantial, potentially related to changes in herbivory allowing certain palatable species to persist, though not a direct causation.
- Trampling and disturbance
  - First-time sampling in C2 plots in 2002 suggests trampling during 13CO2 pulse activities reduced productivity in those plots.
- Diversity and community structure
  - Shannon diversity: 2002 shows a 15% decrease in nitrogen-and-lime plots relative to baseline, with increases in other treatments.
  - Bryophyte abundance increased across treatments, especially in unimproved plots; mosses contribute notable biomass in later surveys.
  - PCA discriminates between improved (fertilised/limed) and unimproved plots; N- and Lime-treated samples show affinities with limed plots in multivariate space.
- Overall productivity trend
  - Net biomass increased from 1999 baseline across years, but 2002 saw reductions in several treatments; highest sustained productivity in plots receiving both nitrogen and lime.

## GIS-relevant implications and recommended map-based products

- Spatial layers to develop
  - Treatment map: spatial distribution of Control 1, Control 2, Nitrogen, Lime, N&L, Insecticide across blocks.
  - Biomass map: annual or seasonal biomass per plot/cell; relative biomass against Control 1.
  - Soil chemistry map: soil pH by plot and by year; moisture maps by cell (where available).
  - Diversity and community type maps: Shannon index by plot/year; CSR/S/R functional-group maps by plot/year.
  - Species distribution maps: point-analysis hits by species and by functional group; bryophyte vs vascular plant density maps.
  - Multivariate visualization: PCA score maps (Axis 1/Axis 2) to show plot grouping by treatment over years.
- Temporal analytics
  - Time-series dashboards per plot showing biomass, pH, moisture, and diversity trends (1999–2002).
  - Change-detection maps (e.g., biomass or Shannon index changes from 1999 to 2002).
- Spatial patterns and slope effects
  - Analyze productivity vs block position on the downslope gradient; identify lower productivity areas (e.g., Block 5) and potential microclimate influences.
- Data constraints to note in GIS workflows
  - Data density varies by year and by measurement type; C2 plots introduced in 2002 data, some years had gaps (e.g., weather station data loss July–Nov 2002).
  - 0.5 m2 cell-based sampling requires careful spatial alignment; ensure consistent georeferencing across years.
  - Bryophyte identifications improved in 2002; consider taxonomic consistency when integrating multi-year datasets.

## Summary for GIS use

- The Sourhope site provides a rich, multi-layered, spatially explicit dataset linking management treatments to plant productivity, composition, and diversity, with both vascular plants and bryophytes considered.
- Key GIS outputs can include multi-temporal, treatment-based biomass and soil-chemistry maps, species- and functional-group distribution layers, and PCA-based clustering visuals to explore the spatial effects of fertilisation, mowing, and disturbance.
- Integrated maps and dashboards can support visualization of how down-slope position, disturbance regimes, and nutrient amendments shape above-ground ecology and functional composition over time.