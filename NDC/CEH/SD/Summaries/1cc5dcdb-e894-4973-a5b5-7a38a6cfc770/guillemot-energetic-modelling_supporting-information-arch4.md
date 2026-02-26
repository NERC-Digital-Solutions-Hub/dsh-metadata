# Activity, energy expenditure and mass data from common guillemots from the Isle of May during the 2016-2017 annual cycle

## Overview
- Data describe common guillemots (Uria aalge) from the Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W) during the 2016-2017 annual cycle.
- Biologging approach: captured chick-rearing adults fitted with GLS devices (MK3006, Biotrack) on Darvic leg-rings; birds weighed to the nearest gram before deployment.
- Post-deployment: birds recaptured during the breeding season, GLS devices removed, and birds weighed again; handling time was under 5 minutes per bird.
- Measured variables on-device: light intensity, temperature, and conductivity.
- Derived daily data: activity (hours spent foraging), sea surface temperature (SST) from bird-borne loggers, energy expenditure, location fixes, and daily daylight hours.
- Access and data management: access granted by Scottish Natural Heritage; planning, collection and management contributions acknowledged; data processing performed by Ruth Dunn.

## Data Collection & Provenance
- Data collection involved deployment and later retrieval of GLS loggers on adult guillemots.
- Pre- and post-deployment weights were recorded with a Pesola spring balance.
- The dataset reflects a single annual cycle and includes both raw logger-derived measurements and derived daily metrics.

## Dataset Structure
- File: IoM_Guillemot_SST_F_DEE_Loc_Mass.csv
- Contents: one CSV file with ten columns, each representing a specific variable captured or derived from the study.

## Column Details
- logger.id: unique identification number for each individual
- Adult.E: daily adult guillemot energy expenditure (kJ)
- sst: sea surface temperature recorded by the logger (°C)
- Foraging: daily time spent foraging (hours)
- day.length: daily daylight hours (hours)
- lon: longitude
- lat: latitude
- distance.coast.km: distance to the closest coastline (km)
- start.mass: mass at GLS device deployment (grams)
- end.mass: mass at GLS device retrieval (grams)

## Data Quality, Metadata & Governance
- Data are gathered from standardized measurements with explicit units and derived metrics.
- Provenance is documented via deployment/retrieval workflow and processing attribution.
- Metadata includes contributor acknowledgments and processing by Ruth Dunn.
- Discoverability is aided by a named CSV file and clearly described columns.

## Access, Usage & Collaboration
- Access to the dataset was granted by Scottish Natural Heritage.
- Potential uses include analyses of foraging behavior, energy expenditure, spatial movement relative to SST, and relationships with daylight.
- Collaboration and planning contributions are acknowledged, supporting broader data-community engagement.