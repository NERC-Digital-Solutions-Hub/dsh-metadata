# Invertebrate community assembly data across a natural soil temperature gradient in Iceland from May-July 2015

- Purpose and scope
  - Dataset of environmental data, total invertebrate abundance, and mean invertebrate body mass.
  - Collected at 60 soil habitat patches in the Hengill geothermal valley, Iceland, from May to July 2015.
  - Patches span a soil temperature gradient of 5–22 °C on average, within 2 km of each other.
  - Patches sampled across 10 geothermally heated streams; three patches sampled per bank (left/right) per stream.

- Sampling regime and collection methods
  - Soil temperature monitored for each plot during the study (May 13 – July 3, 2015) with hourly readings using Maxim DS1921G iButton loggers buried 5 cm below the surface.
  - Only 49 of 60 loggers recovered; missing data represented as NAs.
  - Soil moisture measured with TRIME-TDR probes; soil cores collected for carbon, nitrogen, and pH analyses.
  - Soil carbon and nitrogen measured by CN analyzer after drying homogenized soil samples.
  - Epigeal invertebrates sampled with five 48-hour pitfall traps per habitat patch at four time points: May 19, June 4, June 23, July 5.
  - Collected samples stored in ethanol; identified to species where possible, otherwise to higher taxonomic levels (e.g., Diptera, Hymenoptera to family level).

- Data files and structure
  - Three CSV files, each row representing one sampling time point for one patch (60 patches total).
  - Common first three columns across files: stream (numeric code referencing prior publications), bank (left/right), and patch (1–3; proximity to river).
  - hengill_seasonal_environmental_data.csv
    - Additional columns: (4) temperature (mean soil temperature during study in °C); (5–6) total_carbon and total_nitrogen (g kg^-1); (7–8) moisture (%) and pH.
  - hengill_seasonal_abundance.csv and hengill_seasonal_mass.csv
    - Column 4: sampling date.
    - Columns 5–128: names of invertebrate taxa quantified.
    - hengill_seasonal_abundance.csv contains total individuals per taxon per patch per time point.
    - hengill_seasonal_mass.csv contains mean dry weight (mg) per taxon per patch per time point.

- Analytical opportunities
  - Examine how soil temperature gradients influence invertebrate community structure and diversity.
  - Assess temporal dynamics of communities across the growing season and following snowmelt.
  - Explore relationships between environmental soil properties (moisture, pH, carbon, nitrogen) and both abundance and body mass of assemblages.
  - Utilize taxon-specific and community-wide metrics to test temperature-size relationships and community responses to warming.

- Data quality, caveats, and considerations
  - Temperature data gaps due to partial logger recovery (NA entries).
  - Taxonomic resolution varies; some groups identified only to family or higher levels.
  - Spatially proximate patches reduce broad geographical separation but enable gradient analyses within a localized geothermal valley.
  - Datasets are tied to 2015 sampling; linking to prior and subsequent studies provides broader context for temporal comparisons.

- Related references and context
  - Studies on Hengill streams and temperature effects across multiple ecological scales (e.g., Friberg et al. 2009; Woodward et al. 2010; O'Gorman et al. 2012, 2016, 2017; Robinson et al. 2018, 2021).
  - Documentation of effects of soil temperature on plant and invertebrate communities and temporal dynamics in subarctic temperate systems.

- Use for decision-making and reporting
  - Data are suitable for meta-analyses of temperature-driven changes in soil invertebrate communities.
  - Useful for modeling predictions of community responses to environmental warming at fine spatial scales.
  - Provides a structured dataset with accompanying environmental covariates to support reproducible analyses and data sharing.