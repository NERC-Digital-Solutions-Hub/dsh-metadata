# Countryside Survey Soils 2007: Method development, power analyses and protocols

## Purpose and scope
- Documents sampling design and measurement protocols for Countryside Survey soils across years (1978, 1998, 2007) and the power analyses used to determine sample sizes.
- Notes that not all measurements were made on all samples; data structure varies by year.

## Sampling design and plot structure
- Sampling occurred in 256 squares in 1978 and 1998; expanded to 591 CS squares in 2007.
- Within each CS square, five x-plots are randomly spaced.
- X-plots within a square are not replicates due to potential differences in land use, soil type, etc.
- Some plots are relocated over time due to destruction, access denial, or uncertainty in original locations; each location has a unique repeat identifier (e.g., 2RPT1).
- Repeat plots are intended to refer to the same approximate location, with actual sampling positions typically 2–3 m from other corners of the 2 m × 2 m plot.

## Sampling methods and depth
- Soils sampled from the top 15 cm (8 cm depth for invertebrate samples).
- 1998/2007 used soil cores hammered into the soil; 1978 used a soil pit to access the top 15 cm.
- In some cases, full core collection was not possible due to stones or shallow soils; core photographs and dimension measurements were taken in 2007 for some cores.

## Measurements and data collection
- 1978: laboratory measurements included pH and loss-on-ignition (LOI) only.
- 1990: soil mapping conducted; various cores collected across x-plots.
- 1998 and 2007: multiple cores per x-plot with a variety of measurements; different cores had different measurements (see Table 1).
- Not all measurements were conducted on all samples; examples include pH (in water and CaCl2), %C, %N, bulk density (measured in 2007, not by ISO method), soil moisture, depth of organic layer, texture, Olsen P, metals, mineralisable N, and photographs.
- Some data are associated with a specific core (e.g., black cores, invertebrate cores) and with particular sampling configurations (2 of the 5 x-plots in the original 256 squares for certain measurements).

## Data structure, quality, and interpretation guidance
- Data users are advised to account for land class structure in analyses; failure to do so can bias results toward stock and change of the population rather than national estimates.
- Bootstrapping is not consistently used; at minimum, analyses should include a mixed model with square as a random factor to reflect multiple x-plots within each square.
- CS design emphasizes spatial dispersion over tight replication; for regional estimates, widespread sampling improves precision and coverage.
- Users are urged to consult CEH before analysis and to check publications that exploit the data, as listed on the CS website.

## Data availability and documentation notes
- Some measurements and data were released only after the Soils Report published in November 2009 (denoted by asterisk in the data tables).
- References and methodological detail are documented in Emmett et al. (2008): Countryside Survey Soils 2007: Method development, power analyses and protocols.

## Governance, stewardship implications for Data Stewards
- Ensure robust metadata for each repeat identifier (e.g., 2RPT1) and for each plotting location, including relocation history and exact sampling depths.
- Track year-specific differences in measurement suites and core types to guide downstream data integration and analysis.
- Maintain clear data provenance: link measurements to specific cores, plots, and years; document any deviations from standard protocols (e.g., pit sampling in 1978, non-ISO bulk density method in 2007).
- Manage access permissions and release schedules, noting that certain data were restricted until after 2009.
- Provide guidance on appropriate statistical approaches (mixed models with square as a random factor; consideration of land class structure) and ensure users have references to foundational methodological work.