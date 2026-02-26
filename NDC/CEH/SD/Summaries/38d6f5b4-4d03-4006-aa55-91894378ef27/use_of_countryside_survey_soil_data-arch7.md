# Sampling design

- The Countryside Survey (CS) soils program has sampled soils in 1978, 1998, 2007 and a rolling survey from 2019 onward, with ~100 squares targeted each year for five years before repeating.
- In 1978 and 1998 the same 256 CS squares were sampled; in 2007 all 591 CS squares were sampled, though not all measurements were made on every sample.
- A pilot survey occurred in 2018, leading to the rolling survey starting in 2019.

## Spatial framework and plots

- Soils are sampled from CS X-plots, with 5 X-plots randomly spaced within each CS square.
- X-plots within a square are not replicates; plots may be relocated over time due to land-use change, access issues, or other uncertainties.
- Each sampling location has a unique repeat identifier (e.g., 2RPT1), corresponding to square 2, repeat plot 1.
- Location within a square: exact sampling points move around the 2 m x 2 m permanently marked plot, typically 2–3 m apart across the four corners.
- Relocation and occasional loss of plots mean exact coordinates can shift, but the repeat identifier links samples to a known location.

## Sampling and depth

- Depths: top 15 cm sampled (8 cm depth for invertebrate samples); in 1978, sampling used a soil pit rather than a core.
- In 1998, 2007 and the rolling survey (2018/19–2023), multiple cores were taken per X-plot; core collection methods evolved (e.g., cores hammered in and pulled out; photos and measurements of core dimensions recorded in 2007).
- Some soils may not yield a full 15 cm core due to stones or shallow soils.

## Measurements and data characteristics

- Measurements vary by year and core; in 1978 only pH and loss-on-ignition (LOI) were measured.
- In later years, a range of measurements were taken across cores; samples are homogenised before pH and LOI analyses.
- Bulk density was measured in 2007 and again in 2018/19–2023, but not using ISO bulk density methods.
- Some core measurements (e.g., black cores, N mineralization cores) were specifically noted in 2007.
- Not all cores have the same set of measurements; data availability depends on year and core type.

## Data structure and interpretation

- Sampling design emphasizes multiple X-plots per CS square, leading to spatial clustering within squares.
- Analyses should account for land class structure; ignoring land classes can yield population stock/change estimates rather than class-weighted national estimates.
- Bootstrapping is not consistently used; where spatial structure is not of interest, a dispersed set of observations is efficient for regional estimates.
- Recommended analytical approach: use a mixed model with square as a random factor to account for multiple X-plots per square.
- For design-based analyses, note that only one core per location is typical, but the CS design aims for broad spatial coverage to improve precision and regional estimates.
- Users are advised to consult UKCEH before analysis and interpretation and to review CS publications available on the CS website.

## Practical notes for GIS applications

- The dataset provides a spatially explicit, time-series framework suitable for map-based visualization of soil properties across CS squares and X-plots.
- Key spatial identifiers: CS square, X-plot, and the repeat identifier (e.g., 2RPT1) to link samples across years.
- Be mindful of plot relocations and varying measurement availability when integrating data across years into maps or spatial models.

## References

- Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA.
- Emmett, BA, et al. (2008) on power analyses and methodological details.