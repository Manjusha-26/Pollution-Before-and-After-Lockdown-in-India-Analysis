# Pollution Before and After Lockdown in India

## Overview
This project analyzes pollution levels in India before and after the COVID-19 lockdown in 2020. The dataset used includes various pollutants recorded across different states and cities in India from January 1, 2020, to May 19, 2020.

## Dataset Information
The dataset is sourced from [TUMI Data Hub](https://hub.tumidata.org/dataset/airpollutionbeforeandafterlockdownindelhi_delhi) and contains 15 columns and 687,205 rows, with data recorded hourly.

### Columns
- **datetime**: Date and time of recording
- **id**: Unique ID for each city and state
- **name**: Sector name (discarded)
- **longitude**: Longitude of the recording location
- **latitude**: Latitude of the recording location
- **live**: Boolean indicating if data was recorded live (discarded)
- **cityid**: City name
- **stateid**: State name
- **PM2.5**: Particulate Matter with diameter ≤ 2.5 micrometers
- **PM10**: Particulate Matter with diameter ≤ 10 micrometers
- **NO2**: Nitrogen Dioxide
- **NH3**: Ammonia
- **SO2**: Sulfur Dioxide
- **CO**: Carbon Monoxide
- **OZONE**: Ground-level Ozone

## Analysis Process
1. **Reading the Dataset**:
   - Loaded the dataset using `read_csv`.

2. **Tidying the Data**:
   - Removed unused columns (`live` and `name`).
   - Converted `datetime` to represent only dates.
   - Aggregated data to get the mean pollutant values per day.
   - Omitted rows with NA values.

3. **Creating Lockdown Phases**:
   - Added a new column `lockdown_phase` to indicate the lockdown phases:
     - Before Lockdown: 1st Jan 2020 - 24th March 2020
     - Phase 1: 25th March 2020 - 14th April 2020
     - Phase 2: 15th April 2020 - 3rd May 2020
     - Phase 3: 4th May 2020 - 17th May 2020
     - Phase 4: 18th May 2020 - 31st May 2020

4. **Visualization**:
   - Created several plots to visualize pollution levels across different phases of lockdown.

## Visualizations
- **Boxplot of Pollutants by Lockdown Phase**:
  <img width="735" alt="image" src="https://github.com/user-attachments/assets/33d98e21-0a06-497c-85a6-5b8b8bfa75f8">

- **Bar Plot of Pollutant Values by State**:
  <img width="721" alt="image" src="https://github.com/user-attachments/assets/9ef01094-a542-4f06-9f87-bf681e09aca6">

- **Monthly Pollution Levels**:
  <img width="714" alt="image" src="https://github.com/user-attachments/assets/3f6b75c4-6abc-4351-9d86-5fabcc979a0a">

- **Pollution Levels by State**:
  <img width="727" alt="image" src="https://github.com/user-attachments/assets/021c55a2-cf8f-4548-9e4a-ab95b085502d">

- **Pollution Levels on Map**:
  - Before Lockdown:
    <img width="497" alt="image" src="https://github.com/user-attachments/assets/5a21c7b9-ab6d-4731-8969-afa5dbded893">

  - After Lockdown:
    <img width="496" alt="image" src="https://github.com/user-attachments/assets/2f20a329-0232-408b-aeb5-3edaf4d908b0">


## Observations
- NH3 pollutant levels were significantly lower compared to other pollutants before and after lockdown.
- PM10 and PM2.5 were the most prevalent pollutants.
- Significant reduction in pollutants was observed after the lockdown, except for NH3 and SO2.
- Delhi remained the most polluted state before and after lockdown.

## References
- [IQAir](https://www.iqair.com/th-en/india)
- [PIB India](https://pib.gov.in/newsite/printrelease.aspx?relid=110654)

## Acknowledgments
Thanks to [TUMI Data Hub](https://hub.tumidata.org) for providing the dataset.
