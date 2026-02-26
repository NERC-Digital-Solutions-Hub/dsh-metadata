# SUMMARY

- Context and aim
  - Four years into the NERC Soil Biodiversity Thematic Programme at Sourhope (Scottish Borders) focusing on above-ground productivity, plant species composition, and relative abundance (diversity) in a fenced, managed field experiment.
  - Three major management drivers influencing plant communities: mowing, fertilisation (nitrogen and/or lime), and insecticide application (Dursban 4; formerly Biocide).

- Experimental design and data collection (GIS-relevant structure)
  - Location: Rigg Foot Experimental Site, Sourhope, with 5 replicate blocks along a downslope gradient.
  - Plot layout: each block contains 6 main plots, subdivided into 10 sub-plots; data collected on 0.5 m x 0.5 m cells within sub-plots S, T, U, V; treatment allocation random (map in Appendix 1).
  - Treatments (plot-level): Control 1; Control 2; Nitrogen (NH4NO3); Lime (CaCO3); Nitrogen + Lime; Insecticide (Dursban 4, formerly Biocide).
  - Management regime: monthly mowing May–Sept to ~6 cm; insecticide applied after mowing; spring fertilisers applied to designated plots.
  - Data streams (GIS-ready): weather data from on-site Automatic Weather Station; biomass company from 0.5 m^2 sampling; baseline (1998) and annual/seasonal biomass (1999–2002); point analysis surveys (1998 baseline; 2000–2002); bryophyte/vascular plant species lists; soil pH (5 cm depth) and moisture (theta probe), with 2002 moisture/soil data tied to point surveys.
  - Survey cadence: baseline 1998; annual mowing-season biomass measurements; mid-summer point analyses in 2000–2002; additional floristic and bryophyte surveys; 11621 soil samples collected since start (Appendices 4–6).

- Key findings by factor (GIS interpretation and map-ready ideas)
  - Mowing effect
    - Decline of Agrostis capillaris and Agrostis vinealis across most plots since 2000; likely a site-wide response to uniform mowing rather than a treatment-specific effect.
    - Festuca rubra expands, particularly in fertile (N and/or lime) plots; bryophytes proliferate with a consistent sward height ~6 cm.
    - Across treatments, stress-tolerant species increase; potential reduction in SR/C-S-R communities due to lower disturbance.
  - Fertilisation effect
    - Nitrogen and/or lime improve above-ground productivity, with the strongest gains when both are applied (N & L).
    - Soil pH in limed plots approaches 7.0; higher pH correlates with higher productivity, but very high pH and/or reduced moisture may eventually limit gains.
    - In plots with both N and lime, C-S-R (competitive-stress-ruderal) species become dominant; stress-tolerant species predominate in unimproved plots.
    - Potential drought stress observed in high-pH, high-N plots; chlorosis reported in summer 2002.
  - Insecticide effect
    - Shannon diversity index higher in insecticide-treated plots; interpretation cautious due to lack of direct causality (insect herbivory vs. plant responses depends on insecticide type and life history).
    - Possible increased advantage for more palatable species under reduced herbivory, contributing to higher observed diversity in some plots.
  - Trampling effect
    - 2002 sampling in C2 plots (post-labelling 13CO2 pulses) suggests trampling reduced productivity in those plots relative to C1.
  - Temporal and spatial patterns
    - Biomass productivity rose from 1999 through 2001 but declined in 2002 across most treatments (variations by block on slope: lower on higher blocks).
    - PC-based separation shows improved (N, L, N&L, Insecticide) vs unimproved plots; lime plots cluster distinctly; nitrogen-treated plots show mixed affinities depending on block.
    - 2002 point analysis indicates shifts in bryophyte (mosses/liverworts) abundance, particularly Rhytidiadelphus squarrosus, with bryophyte hits rising across treatments, more so in unimproved plots.
    - Diversity metrics (Shannon) show a 15% drop in 2002 for N&L plots vs increases in other treatments (up to 29% in some insecticide plots).
  - Functional-group dynamics (CSR framework)
    - Over time, functional group composition shifts: stress tolerators (S) prominent in unimproved plots; C-S-R and SR/C-S-R groups dominate in fertilised plots, especially with N+L; shifts reflect pH and nutrient availability as drivers of ecological strategy.

- Data layers and GIS opportunities
  - Spatial layers to build
    - Treatment maps: plot-level (Control 1/2, Nitrogen, Lime, Nitrogen+Lime, Insecticide) and block layout.
    - Biomass productivity: annual and seasonal sums per plot and per 0.5 m^2 cell; normalized comparisons against controls.
    - Plant functional groups: distribution of stress-tolerant, competitive-stress-ruderal (CSR) and related SR/CSR groups per plot/year.
    - Species distribution: species hits per 0.5 m^2 cell, including bryophytes vs vascular plants; key species frequency maps (Festuca spp., Agrostis spp., Poa spp., Festuca rubra, Festuca ovina, etc.).
    - Bryophyte dynamics: presence/abundance by plot, year, and treatment.
    - Soil chemistry and moisture: pH per plot (5 cm depth) and moisture content per point-analysis cell; correlation surfaces with biomass.
    - Weather-derived variables: rainfall, temperature, radiation linked to plot productivity and stress indicators.
  - Temporal dimensions
    - Time-series stacks for 1999–2002 (and 1998 baseline) to analyze trends; identify lag effects of lime/N fertilisation on biomass and diversity.
  - Data quality notes for mapping
    - 2002 weather data gaps (July–Nov) due to station malfunction; data imputed with Konza station data for missing periods.
    - 2002 C2 trampling-related productivity drop requires careful interpretation in GIS summaries.
  - Data accessibility
    - Full project details, species lists, and data descriptions are available via Soil Biodiversity website and CEH contacts; 11621 soil samples catalogued to date.

- Enduring conclusions for GIS use
  - Spatially explicit management (mowing, fertilisation, insecticide) yields distinct, trackable patterns in productivity, plant composition, and functional strategies.
  - The most productive and sulphur-rich response occurs in plots with both N and lime, whereas unimproved plots shift toward stress-tolerant species and moss-dominated communities.
  - Moss expansion and bryophyte presence are strong, map-ready signals of disturbance and nutrient regimes.
  - 2002 data show meaningful, treatment-related shifts in diversity and functional group balance, with tractable relationships to soil pH and moisture that can be modelled spatially.
  - These data support GIS-enabled data products for policy, stakeholder communication, and public-facing maps showing how landscape management affects biodiversity and productivity over time.

- References and data notes
  - Comprehensive references and appendices covering site layout, species lists, weather data, biomass measurements, and point analyses are included in the report and appendices (Appendices 1–8; species lists; biomass data; PCA analyses).
  - Key data sources: on-site weather station; biomass harvests; 0.5 m^2 point analyses; soil pH and moisture; bryophyte and vascular plant surveys.
  - Primary data access: Soil Biodiversity website and CEH contact details provided in the document.