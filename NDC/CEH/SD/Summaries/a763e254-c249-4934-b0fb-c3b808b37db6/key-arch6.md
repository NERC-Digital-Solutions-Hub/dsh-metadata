# Text

## Overview
- The document defines a small data schema for features, likely infrastructure-related, using two groups of coded fields: Type and Condition.
- It focuses on capturing categorization and status for two aspect areas: road/transport features and residential/industrial/municipal context.

## Data Schema

- Group 1: Road/transport features
  - Type:
    - 1 Major (paved)
    - 2 Major (unpaved)
    - 3 Minor (paved)
    - 4 Minor (unpaved)
    - 5 Track (unpaved)
  - Condition:
    - 1 Intact
    - 2 Obstructed/damaged

- Group 2: Area/asset context
  - Type:
    - 1 Residential (permanent)
    - 2 Residential (informal/temporary)
    - 3 Industrial (e.g., hydropower)
    - 4 Municipal
  - Condition:
    - 1 Intact
    - 2 Obstructed/damaged

## How to use for analysis

- Classify data records by road type and by area/asset type, enabling multi-dimensional filtering.
- Map features geographically by linking these codes with location data.
- Assess maintenance or risk by comparing Condition across Type categories.

## Data quality and integration considerations

- Possible data fragmentation across systems; harmonize Type and Condition codings.
- Ensure clear, consistent definitions for “Intact” vs “Obstructed/damaged.”
- Create and maintain a data dictionary; implement validation checks.
- Prepare for self-service exploration with filters for both Type and Condition groups.

## Practical next steps for data support

- Develop a lightweight dashboard or pivot table showing distributions by Type and Condition for both groups.
- Provide example queries and guidance for interpreting results.
- Document data provenance, update cycles, and promote outputs to stakeholders; gather feedback for refinements.