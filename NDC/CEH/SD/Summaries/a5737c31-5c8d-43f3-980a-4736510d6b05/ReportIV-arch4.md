# SUMMARY

- Four years into the NERC Soil Biodiversity Thematic Programme at Sourhope, the site has been monitored to assess aboveground biomass (productivity), species composition, and relative abundance (diversity) in relation to three major management processes: mowing, fertilisation, and insecticide application.
- Primary aim is to understand links between soil biodiversity and aboveground plant communities, and how management shapes both systems over time.

## Data Architecture and Site Management

- Site layout and treatments
  - Location: Rigg Foot Experimental Site, Sourhope, Stirling Borders; 5 replicate blocks along a downslope gradient.
  - Each block contains 6 main plots, subdivided into 10 sub-plots; a 0.5 m x 0.5 m cell-system is used to allocate plots to different research groups.
  - Main treatments (plot-level): Control 1, Control 2 (no treatment), Nitrogen, Lime, Nitrogen & Lime, Insecticide.
  - Site-level task: regular mowing of vegetation to approximately 6 cm (May–Sept annually since 1999); insecticide applied after mowing in designated plots.
- Treatments and data streams
  - Fertilisation: NH4NO3 nitrogen and/or lime (CaCO3) applied in spring/early summer; annual rates specified in appendices.
  - Insecticide: Dursban 4 (chlorpyrifos) applied to insecticide plots; mistimed or seasonally adjusted applications documented.
  - Data streams include: weather data from on-site Automatic Weather Station; above-ground biomass from 0.5 m2 cell clipping; baseline and subsequent plant surveys; point analysis surveys; bryophyte identification; soil pH and moisture; various supplementary botanical surveys.
- Data collection timeline and scope
  - Baseline botanical survey completed in 1998; regular vegetation sampling since 1999.
  - Point Analysis surveys conducted in 2000, 2001, 2002 with a 100-hole frame on a 0.5 m2 cell per sub-plot (S, T, U, V).
  - Bryophyte identification expanded in 2002; soil moisture measured in 2002 in core cells; soil pH monitored since 1998.
  - Total soil samples collected since start: 11,621.
- Data management and accessibility
  - Data are distributed across multiple appendices and project reports, including biomass data by plot (Appendix 6), biomass rankings (Appendix 7), and species hit-rankings (Appendix 8).
  - Results and datasets are described as available via the Soil Biodiversity website and Centre for Ecology and Hydrology (Windermere Road).

## Key Findings and Data Trends

- Productivity and treatment effects
  - Overall biomass productivity increased from 1999 to 2002 across most treatments, but 2002 showed a broad decline compared with 2001.
  - Highest productivity in plots receiving both nitrogen and lime; Control 2 plots consistently less productive than Control 1 in later years.
  - A negative gradient with slope location: Block 5 (upper slope) showed larger declines than Block 1 (bottom), indicating micro-topographic effects on productivity.
  - Split-plot ANOVA indicates significant treatment effects and year-by-treatment interactions, underscoring multi-year, multi-treatment data complexity.
- Soil chemistry, moisture, and productivity
  - Lime markedly increased soil pH toward 7.0 (notably in upper soil horizons); nitrogen also increased pH but to a lesser extent.
  - Strong negative correlation between soil moisture and pH (r ≈ -0.68).
  - Positive association between soil pH and biomass when pooling treatments; within some treatments, especially with nitrogen or lime alone, this relationship weakens; with both nitrogen and lime, the positive relationship may become negative, suggesting Mg or moisture interactions or other limits.
- Plant community structure and functional groups
  - Functional groups show clear treatment-driven shifts:
    - Stress-tolerant (S) species expand in unimproved plots (no nitrogen or lime).
    - Competitive-stress tolerant and ruderal groups (CSR, SR/CSR) become more dominant in plots receiving nitrogen and/or lime, especially with both inputs.
    - SR/C-S-R species decline in lime- and insecticide-treated plots.
  - Dominant grasses and bryophytes shift with treatments:
    - Festuca rubra increases in fertile plots; Festuca ovina declines; Agrostis spp. decline with mowing.
    - Bryophyte abundance increases site-wide, particularly in unimproved plots, aided by mowing and absence of grazing.
- Diversity metrics
  - Shannon Diversity Indices show treatment-driven differences emerging since 2000; diversity increased in several treatments but declined in nitrogen-and-lime plots (about 15% relative to 1998 baseline by 2002).
  - Point Analysis reveals treatment-related shifts in species hits, with improved pastures (lime and/or nitrogen) favoring Festuca rubra and Poa pratensis, while unimproved plots favor Festuca ovina and Agrostis spp.
- Insecticide effects and herbivore interactions
  - Insecticide-treated plots show higher diversity in some years but the relationship is not conclusively causal; possible mechanism includes reduced herbivory allowing some palatable species to persist, though direct causal links require further evidence.
- Trampling and sampling effects
  - C2 plots (part of the trampling-intensive sampling during 13CO2 pulses) show reduced productivity relative to C1 plots, indicating trampling or pulse labeling effects on vegetation growth.

## Data Quality, Gaps, and Challenges

- Data consistency and measurement changes
  - Bryophyte identification broadened in 2002 to species-level, improving resolution for non-vascular components.
  - Weather data in 2002 had missing periods due to a station malfunction; some 2002 data substituted from nearby stations.
  - Control 2 plots had incomplete surveying in 2000 and 2001, impacting cross-year comparisons.
- Data complexity and integration needs
  - Multi-year, multi-treatment design with nested plots and sub-plots yields high-dimensional data requiring careful alignment of datasets (biomass, point analysis, bryophyte records, soil chemistry, moisture, and weather).
  - The site hosts 24 Phase I and 8 Phase II projects; cross-project data harmonization and metadata standards are critical for integrated analyses.
- Gaps in standardization and coordination
  - The scattered nature of data across appendices and project reports suggests a need for centralized metadata schemas, version-controlled datasets, and consistent data delivery pipelines across years and projects.

## Implications for Data Strategy and Collaboration

- Longitudinal, multi-modal data management
  - The Sourhope Data ecosystem demonstrates the value of collecting consistent, multi-domain data (biomass, species composition, soil chemistry, moisture, weather) over several years to understand ecosystem responses to management.
  - For data leaders, this underscores the importance of designing robust data architectures: standardized metadata, clear data dictionaries, and centralized repositories to support cross-year, cross-treatment analyses.
- Functional and taxonomic data integration
  - The CSR/S-R categories and their treatment-driven shifts illustrate the value of linking functional trait data with species hits to interpret ecosystem responses beyond species counts.
- Data sharing and community building
  - Results are linked to a central Soil Biodiversity website and CEH resources, highlighting the benefit of shared data portals and community of practice to improve discoverability and reuse.
- Data quality controls and governance
  - Documentation of measurement protocols, treatment dates, and adjustments (e.g., 2002 bryophyte resolution, weather data substitutions) points to the need for transparent, auditable data provenance and versioning.

## Takeaways for Data Leaders

- Build and maintain a cohesive data framework that can accommodate nested experimental designs, repeated measures, and cross-year analyses.
- Prioritize comprehensive metadata and data provenance to enable cross-project reuse and long-term storytelling of data-driven insights.
- Ensure data quality and continuity by documenting measurement methods, handling missing data, and accommodating equipment issues (e.g., weather station downtime) with transparent data substitutions.
- Leverage data harmonization practices to combine above-ground productivity, species diversity (including bryophytes), soil chemistry, and moisture data for integrated analyses.
- Foster data sharing and collaborative analytics by centralizing datasets and providing accessible documentation and tutorials for researchers across Phase I and Phase II projects.