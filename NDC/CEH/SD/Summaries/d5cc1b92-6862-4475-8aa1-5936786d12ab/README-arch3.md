# Home range size and habitat availability data for 39 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018

## Overview
- Dataset accompanying a manuscript on inter-individual variability in habitat selection and functional habitat relationships in European nightjars during landscape change.
- Focuses on quantifying home range size, habitat availability within ranges, and habitat selection for 39 nightjars over 2015–2018.

## Data content
- Home range size: 95% use-level home ranges (hectares).
- Habitat availability: percentage availability of habitat categories within each nightjar’s 95% home range.
- Habitat selection: Manly's Selection Ratios (positive values indicate selection; values <1 indicate avoidance).
- 95% home ranges derived from GPS metadata.
- Habitat selection ratios calculated using habitat availability values and GPS points via Manly’s equation.
- Independent habitat map used to define habitat categories and calculate availability.

## Methods
- Nightjars captured with mist nets (21:00–01:00) at Thorne or Hatfield Moors; fitted with nanoFix mini GPS tags (Pathtrack, Otley, UK).
- Tags are archival (non-transmitting); data recovered by recapturing birds after 7–16 days.
- Tracking schedule: 3- to 5-minute intervals depending on year.
- GPS data used to construct foraging tracks, estimate home ranges, and assess habitat selection in relation to landscape change.
- Data quality checks: remove points with <3 satellites; visually inspect for points outside plausible foraging range; ArcMap used for spatial verification.
- GPS fixes calibrated to estimate error (approximately 5–25 m, depending on habitat).

## Data structure and key variables (Home Range and Habitat Availability CSV)
- Individual: Unique identifier for each bird.
- Size_HR: Home range size (hectares).
- Year: Year of tracking (factor for fixed effects).
- Av_woodland, Av_Scrub, Av_Dry, Av_cleared, Av_wetland, Av_water: Habitat availability percentages within the 95% home range.
- SR_Water, SR_Bare_peat, SR_Woodland, SR_Wetland, SR_Cottongrass, SR_Bracken, SR_Heather, SR_Scrub, SR_Cleared+1, SR_Cleared+2, SR_Cleared, SR_Grass, SR_Building, SR_Off_Site: Habitat selection ratios for each habitat type (per individual).

## GPS tracking data (GPS data CSV)
- ID: Bird identifier.
- Date: Date (DD/MM/YYYY).
- Year: Year (factor for fixed effects).
- Time: Time of fix (21:30 to 04:30, nearest minute).
- Lat, Long: Latitude and longitude in WGS84.
- Data collected at Thorne and Hatfield Moors within Humberhead Peatlands NNR, South Yorkshire.
- Fix interval: 3 or 5 minutes (2015–2016: 3 min; 2017–2018: 5 min).
- Period: June–August, 2015–2018.
- Note: Some fixes may be spurious or missing; estimates include an error calibration.

## Use in monitoring and policy frameworks
- Provides measurable metrics for evaluating landscape change effects on species’ space use and habitat preferences.
- Facilitates tracking behavioural responses to habitat change and informing land-management decisions.
- Data are structured to support reproducibility and integration with other monitoring datasets (e.g., through explicit metadata, data checks, and clear derivation of 95% home ranges and selection ratios).

## Data governance and accessibility considerations
- Underlines the need for data quality, metadata completeness, and open sharing practices.
- Highlights potential barriers: data access delays, data silos, and requirements to publicly share datasets.
- Demonstrates transparency through explicit processing steps (GPS filtering, visual validation, and analysis with standard tools like ArcMap).

## Limitations and considerations
- Archival GPS tags limit duration to 7–16 days per bird; represented samples per individual may vary.
- Selection ratios depend on the accuracy of habitat availability estimates from the independent habitat map.
- Some GPS fixes may be inaccurate in certain habitats; error estimates are provided but remaining uncertainty should be considered in analyses.