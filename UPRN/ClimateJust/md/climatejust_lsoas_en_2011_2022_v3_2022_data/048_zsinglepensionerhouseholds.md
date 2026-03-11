### pensioner households (Z-Score)

**Description:**
This field (identified internally as `ZSinglePensionerHouseholds` in the spatial dataset) represents the standardized Z-score for the percentage of single-pensioner households (people aged 65 and over living alone) within a given Lower Super Output Area (LSOA). It measures how the local concentration of older adults living alone in a specific neighbourhood compares to the national average across England.

**Vulnerability Rationale:**
This metric is a core indicator within the "Social Networks" domain, which is used to evaluate a community's "(In)ability to Respond" and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

A higher proportion of single-pensioner households acts as a proxy for a higher likelihood of social isolation, which increases social vulnerability. Social isolation significantly restricts a person's adaptive capacity during an extreme weather event for several reasons:
*   **Assistance and Community Support:** Socially isolated individuals are less likely to ask for assistance and less likely to benefit from community knowledge, community activities, and informal emergency responses.
*   **Practical Difficulties:** Adults who live alone face significant practical challenges when responding to warnings, such as finding it physically impossible to move furniture or install property-level protections without help.
*   **Psychological Stress:** Individuals living alone may feel more uncertain and anxious during a crisis because they have no one immediately present to confide in or share the burden of the response.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher proportion of single-pensioner households than the national average, indicating a higher level of social isolation and relative vulnerability.
*   **Values around 0** indicate that the proportion is approximately average for England.
*   **Negative values** signify a lower proportion than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, no direct update was available, so the underlying data relies on the 2011 UK Census (table QS113). It specifically measures the number of 'One-person household: Aged 65 and over' divided by the total number of households. The indicator carries a weight of 0.500 within the broader "Social Networks" domain alongside indicators like a lack of school-related networks.