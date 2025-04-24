# Tableau Data Visualization Project
This project takes a look into the "Crime Incidents in 2024" out of the District of Columbia. Our aim is to analyze crime patterns in the area in order to provide supported analysis to improve policing operations so that the police force is better prepared to address crime and protect its citizens in the most efficient and calculated manner.

## Authors
**MIST 4610 Section #47114 Group 3**
- [Andrew Bowman](https://www.github.com/andrewbowmn)
- [Kennedy Hankinson](https://www.github.com/kennedyhankinson)
- [Johnny Vo](https://www.github.com/jvjohnny99)
- [Sneha Neelagaru](https://www.github.com/sneelagaru03)
- [Charlie Nelson](https://www.github.com/ugarcn63826)

## Data Set

[Crime Incidents in 2024 dataset](https://catalog.data.gov/dataset/crime-incidents-in-2024)

### Dimensions
- **Rows:** 29,288  
- **Columns:** 24  

### Column Breakdown

>Unique identifiers

| Column             | Data Type | Description                                    |
|--------------------|-----------|------------------------------------------------|
| **CCN**            | string    | Case Control Number (MPD’s unique incident ID) |
| **OBJECTID**       | int     | ArcGIS object ID                               |
| **OCTO_RECORD_ID** | float   | Open Data system record ID (all null, excluded from column count)          |



>Date/time fields

| Column         | Data Type | Description                                             |
|----------------|-----------|---------------------------------------------------------|
| **REPORT_DAT** | string    | When the incident was reported             |
| **START_DATE** | string    | Incident start timestamp           |
| **END_DATE**   | string    | Incident end timestamp             |


>Incident attributes

| Column    | Data Type | Description                                  |
|-----------|-----------|----------------------------------------------|
| **SHIFT**   | string    | MPD shift code (“DAY”, “SWING”, “MID”) |
| **METHOD**  | string    | Method/weapon used (“GUN”, “KNIFE”)    |
| **OFFENSE** | string    | Offense type (“ROBBERY”, “ASSAULT”)    |



>Location descriptor

| Column     | Data Type | Description                                                        |
|------------|-----------|--------------------------------------------------------------------|
| **BLOCK**  | string    | Street‐block address (“1500 BLOCK OF PENNSYLVANIA AVE NW”)     |
| **BID**    | string    | Business Improvement District code (some null)                  |



>Planar coordinates

| Column                | Data Type | Description                                           |
|-----------------------|-----------|-------------------------------------------------------|
| **X**, **Y**          | float  | X & Y Flat-Map Grid Coordinates (2 Columns)                  |
| **XBLOCK**, **YBLOCK**| float   | X & Y Flat-Map Grid Coordinates of specific block (2 Columns)|


>Geographic identifiers

| Column                    | Data Type | Description                              |
|---------------------------|-----------|------------------------------------------|
| **WARD**                  | float   | D.C. political ward number               |
| **ANC**                   | string    | Advisory Neighborhood Commission         |
| **DISTRICT**              | float   | MPD patrol district                      |
| **PSA**                   | float   | Police Service Area                      |
| **NEIGHBORHOOD_CLUSTER**  | string    | D.C. neighborhood cluster code           |
| **BLOCK_GROUP**           | string    | U.S. Census block group                  |
| **CENSUS_TRACT**          | float   | U.S. Census tract                        |
| **VOTING_PRECINCT**       | string    | Voting precinct label                    |


>Geographic coordinates

| Column                      | Data Type | Description                    |
|-----------------------------|-----------|--------------------------------|
| **LATITUDE**, **LONGITUDE** | float   | GPS geographic coordinates (2 Columns)  |

## Questions & Analysis
### 1. Are certain neighborhoods or wards experiencing a disproportionate amount of violent crime compared to property crime?
![Question 1](./Question1.png)
#### Importance:
- Pinpointing areas with unusually high violent-vs-property crime ratios helps law enforcement deploy specialized units, adjust patrol hours, and invest in community programs where they’ll have the greatest impact.
- Neighborhoods saddled with more violent crime often face deeper issues—under-resourcing, economic disinvestment, or lack of youth services. Highlighting these hotspots can drive targeted social and economic interventions.

#### Analysis:
- All neighborhoods see more ![Property Crime](https://img.shields.io/badge/Property%20Crime-blue?style=flat-square) than ![Violent Crime](https://img.shields.io/badge/Violent%20Crime-orange?style=flat-square), but the ratio varies widely.
- **Cluster 2** (≈7.5 % of all incidents) has the **largest share** of **total crime**, with violent incidents making up ~1 %.
- **Cluster 25** (≈7 %) shows a higher proportion of violent crime (~1.1 %) relative to its total.
- **Clusters 25**, **39**, and **21** each have **violent-crime** shares that **exceed** their overall rank, suggesting these areas **endure a heavier violent burden** than their size alone would predict.
- **Clusters 30** and **24** show almost no violent crime (<0.2 % of total), indicating predominantly property-crime issues, or **effective local deterrents**.

#### Action:
- **Targeted policing**: Send rapid-response or specialized violent-crime units to clusters 25/39/21, while maintaining regular patrols elsewhere.
- **Community investment**: Direct social services (e.g., youth outreach, mental-health resources) into disproportionate violent-crime neighborhoods.
- **Policy & planning**: Use these insights to adjust street lighting, CCTV placement, and economic grants—aligning infrastructure spending with demonstrated need.


### 2. What shift (time of day) sees the highest rates of crime, and do these patterns vary by crime type?
![Question 2](./Question2.png)
#### Importance:
- Knowing peak crime hours enables police to schedule patrols and allocate officers where and when they’re needed most, reducing response times and improving coverage.
- Understanding temporal patterns supports targeted community outreach (such as neighborhood watches or lighting improvements) during vulnerable hours.

#### Analysis:
- ![Evening](https://img.shields.io/badge/Evening-orange?style=flat-square) shift has the highest total incidents (≈12K), followed by ![Day](https://img.shields.io/badge/Day-blue?style=flat-square) (≈10K) and ![Midnight](https://img.shields.io/badge/Midnight-red?style=flat-square) (≈8K).
- During the **Day** and **Evening** Shift, **Theft/Other** and **Theft/Auto** dominate, indicating opportunities for a higher percentage of property crimes.
- During the **Midnight** Shift, **Violent** offenses **(Assault, Robbery)** proportionally increase compared to property crimes, pointing to higher personal-risk incidents overnight.

#### Action:
- **Daytime** patrols should focus on **theft deterrence** (locks, being visible in the community).
- **Evening** units should focus on **property crime** and become more **prepared for a surge in violent crimes**.
- **Overnight** squads require specialized **violent crime training** and **rapid response capability**.

### Manipulations
No manipulations were required to the data in order to perform our analysis. 

### Tableau Packaged Workbook
![Coming Soon](https://img.shields.io/badge/Coming%20Soon-yellow?style=flat-square)
