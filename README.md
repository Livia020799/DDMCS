# DDMCS - Idee progetto <br>
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **Idea progetto 1**

### 1. *Understand Your [Dataset](https://archive.ics.uci.edu/dataset/183/communities+and+crime)*
   - *Examine the data*: The "Communities and Crime" dataset contains socioeconomic, crime-related, and demographic attributes, most of which are percentages.
   - *Identify relevant columns*: Look for columns that could meaningfully complement a network structure. For example:
     - Socioeconomic features could describe nodes representing regions (e.g., neighborhoods or cities).
     - Crime rates could define edge weights between regions based on crime correlation.

### 2. *Find an Existing Network*
   - Look for networks that align with the dataset. For example:
     - *Spatial networks*: A network where nodes are geographic regions (e.g., U.S. counties or cities) and edges represent spatial proximity or connectivity.
     - *Social networks*: Communities or individuals connected based on interactions or demographics.
     - *Economic networks*: Regions connected by trade, economic similarity, or other economic activities.

   Sources to find networks:
   - [Network Repository](http://networkrepository.com/)
   - [Stanford Large Network Dataset Collection (SNAP)](https://snap.stanford.edu/data/)

### 3. *Map Data to the Network*
   - *Match identifiers*: If your network nodes are regions (e.g., counties), align the identifiers in the "Communities and Crime" dataset (e.g., FIPS codes) with the network nodes.
   - *Assign attributes*: Attach relevant crime percentages and socioeconomic features from the dataset to the corresponding nodes or edges.

### 4. *Analyze the Network with Attributes*
   - *Network measures*: Study how crime or socioeconomic attributes correlate with network properties (e.g., centrality, clustering).
   - *Visualization*: Use tools like Gephi, NetworkX (Python), or igraph (R) to visualize the network and overlay attributes.
   - *Modeling*: Perform simulations, clustering, or other complex systems analyses. For instance:
     - Simulate the spread of crime across regions using the network structure.
     - Study community structures to see if they align with socioeconomic data.

### 5. *Challenges You Might Face*
   - *Data alignment*: Ensuring the identifiers in the crime dataset match the network's nodes can be tricky, especially if the datasets use different naming conventions.
   - *Network availability*: Finding a pre-built network that aligns with your dataset's scope may require effort.
   - *Data quality*: Missing values in the "Communities and Crime" dataset or the network can complicate the analysis. You may need imputation techniques.
   - *Computational complexity*: Large networks and datasets may require optimized algorithms or computational resources.

### 6. *Example Workflow*
   Here's a step-by-step technical example:
   1. Use *Python* or *R* to load both the crime dataset and the network data.
   2. Match regions using identifiers like FIPS codes.
   3. Use NetworkX (Python) or igraph (R) to create the network, attaching attributes to nodes.
   4. Perform analysis, e.g.:
      - Find correlations between node attributes and centrality measures.
      - Visualize crime hotspots using geographical networks.

### ***DATA*** <br>


**Non-Predictive Identifier Attributes:**
1. **state**: Numeric code representing the U.S. state.
2. **county**: Numeric code for the county.
3. **community**: Numeric code for the community.
4. **communityname**: Name of the community (string).
5. **fold**: Fold number for non-random 10-fold cross-validation.

**Predictive Attributes:**

### ***Demographic Features***
- **population**: Population of the community.
- **householdsize**: Mean number of people per household.
- **racepctblack**: Percentage of the population that is African American.
- **racePctWhite**: Percentage of the population that is Caucasian.
- **racePctAsian**: Percentage of the population that is Asian.
- **racePctHisp**: Percentage of the population that is Hispanic.
- **agePct12t21**: Percentage of the population aged 12 to 21.
- **agePct12t29**: Percentage of the population aged 12 to 29.
- **agePct16t24**: Percentage of the population aged 16 to 24.
- **agePct65up**: Percentage of the population aged 65 and over.
- **numbUrban**: Number of people living in urban areas.
- **pctUrban**: Percentage of people living in urban areas.

### ***Socioeconomic Features***
- **medIncome**: Median household income.
- **pctWWage**: Percentage of households with wage or salary income.
- **pctWFarmSelf**: Percentage of households with farm or self-employment income.
- **pctWInvInc**: Percentage of households with investment or rental income.
- **pctWSocSec**: Percentage of households with social security income.
- **pctWPubAsst**: Percentage of households with public assistance income.
- **pctWRetire**: Percentage of households with retirement income.
- **medFamInc**: Median family income.
- **perCapInc**: Per capita income.
- **whitePerCap**: Per capita income for Caucasians.
- **blackPerCap**: Per capita income for African Americans.
- **indianPerCap**: Per capita income for Native Americans.
- **AsianPerCap**: Per capita income for Asians.
- **OtherPerCap**: Per capita income for other races.
- **HispPerCap**: Per capita income for Hispanics.
- **NumUnderPov**: Number of people under the poverty level.
- **PctPopUnderPov**: Percentage of people under the poverty level.
- **PctLess9thGrade**: Percentage of people aged 25 and over with less than a 9th-grade education.
- **PctNotHSGrad**: Percentage of people aged 25 and over who are not high school graduates.
- **PctBSorMore**: Percentage of people aged 25 and over with a bachelor's degree or higher.
- **PctUnemployed**: Percentage of people aged 16 and over, in the labor force, and unemployed.
- **PctEmploy**: Percentage of people aged 16 and over who are employed.
- **PctEmplManu**: Percentage of people aged 16 and over employed in manufacturing.
- **PctEmplProfServ**: Percentage of people aged 16 and over employed in professional services.
- **PctOccupManu**: Percentage of people aged 16 and over in manufacturing occupations.
- **PctOccupMgmtProf**: Percentage of people aged 16 and over in management or professional occupations.

### ***Family and Housing Features***
- **MalePctDivorce**: Percentage of males who are divorced.
- **MalePctNevMarr**: Percentage of males who have never married.
- **FemalePctDiv**: Percentage of females who are divorced.
- **TotalPctDiv**: Percentage of the population who are divorced.
- **PersPerFam**: Mean number of people per family.
- **PctFam2Par**: Percentage of families (with children) headed by two parents.
- **PctKids2Par**: Percentage of children in family housing with two parents.
- **PctYoungKids2Par**: Percentage of children aged 4 and under in two-parent households.
- **PctTeen2Par**: Percentage of teenagers aged 12 to 17 in two-parent households.
- **PctWorkMomYoungKids**: Percentage of mothers with children aged 6 and under in the labor force.
- **PctWorkMom**: Percentage of mothers with children under 18 in the labor force.
- **NumIlleg**: Number of children born to never-married mothers.
- **PctIlleg**: Percentage of children born to never-married mothers.
- **NumImmig**: Total number of foreign-born individuals.
- **PctImmigRecent**: Percentage of immigrants who arrived within the last 3 years.
- **PctImmigRec5**: Percentage of immigrants who arrived within the last 5 years.
- **PctImmigRec8**: Percentage of immigrants who arrived within the last 8 years.
- **PctImmigRec10**: Percentage of immigrants who arrived within the last 10 years.
- **PctRecentImmig**: Percentage of the population who immigrated within the last 3 years.
- **PctRecImmig5**: Percentage of the population who immigrated within the last 5 years.
- **PctRecImmig8**: Percentage of the population who immigrated within the last 8 years.
- **PctRecImmig10**: Percentage of the population who immigrated within the last 10 years.
- **PctSpeakEnglOnly**: Percentage of people who speak only English.
- **PctNotSpeakEnglWell**: Percentage of people who do not speak English well.
- **PctLargHouseFam**: Percentage of family households with 6 or more members.
- **PctLargHouseOccup**: Percentage of all occupied households with 6 or more members.
- **PersPerOccupHous**: Mean number of persons per occupied household.
- **PersPerOwnOccHous**: Mean number of persons per owner-occupied household.
- **PersPerRentOccHous**: Mean number of persons per renter-occupied household.
- **PctPersOwnOccup**: Percentage of people in owner-occupied households.
- **PctPersDenseHous**: Percentage of persons in dense housing (more than 1 person per room).
- **PctHousLess3BR**: Percentage of housing units with fewer than 3 bedrooms.
- **MedNumBR**: Median number of bedrooms.
- **HousVacant**: Number of vacant households.
- **PctHousOccup**: Percentage of housing occupied.
- **PctHousOwnOcc**: Percentage of households owner-occupied.
- **PctVacantBoarded**: Percentage of vacant housing that is boarded up.
- **PctVacMore6Mos**: Percentage of vacant housing that has been vacant more than 6 months.
- **MedYrHousBuilt**: Median year housing units built.
- **PctHousNoPhone**: Percentage of housing units without a phone.
- **PctWOFullPlumb**: Percentage of housing units without full plumbing.

### ***Crime-Related Features:***
- **ViolentCrimesPerPop**: **Target Variable** - Violent crimes per 100,000 population.
-  **murdPerPop**: Number of murders as a percentage of the population.
- **rapesPerPop**: Number of rapes as a percentage of the population.
- **robberiesPerPop**: Number of robberies as a percentage of the population.
- **assaultsPerPop**: Number of assaults as a percentage of the population.
- **burglariesPerPop**: Number of burglaries as a percentage of the population.
- **larceniesPerPop**: Number of larcenies as a percentage of the population.
- **autoTheftPerPop**: Number of auto thefts as a percentage of the population.
- **arsonsPerPop**: Number of arsons as a percentage of the population.

### ***Law Enforcement Features:***
- **policBudget**: Budget allocated to the police department.
- **PctPolicWhite**: Percentage of police officers who are white.
- **PctPolicBlack**: Percentage of police officers who are Black.
- **PctPolicHisp**: Percentage of police officers who are Hispanic.
- **PctPolicAsian**: Percentage of police officers who are Asian.
- **PctPolicOther**: Percentage of police officers from other ethnic groups.
- **policCars**: Number of police cars per 1,000 population.
- **policPerPop**: Number of police personnel per 1,000 population.

### ***Additional Predictive Attributes:***
- **PctYoungKidsWorkMom**: Percentage of young children whose mothers work.
- **PctTeenWorkMom**: Percentage of teenagers whose mothers work.
- **PctHouseLess1BR**: Percentage of housing units with less than 1 bedroom.
- **MedIncomePercentile**: Median income percentile within the community.
- **PctPersBelowPov**: Percentage of persons below the poverty line.
- **PctPersForeignBorn**: Percentage of persons born outside the United States.
- **PctPersDivorced**: Percentage of divorced persons in the population.
- **PctPersSeparated**: Percentage of separated persons in the population.
- **PctPersNeverMarried**: Percentage of never-married persons in the population.
- **PctPersWidowed**: Percentage of widowed persons in the population.
- **PctTeenMom**: Percentage of teenage mothers.
- **NumImmigRecent**: Number of recent immigrants (within 5 years).
- **PctFemHeadHH**: Percentage of female-headed households.
- **PctElderlyLivingAlone**: Percentage of elderly persons living alone.
- **PctPopulationUnder5**: Percentage of the population under 5 years old.
- **PctPopulationOver85**: Percentage of the population over 85 years old.

### ***Economic and Crime-Related Metrics (continued):***
- **PctArrested**: Percentage of the population arrested within the last year.
- **PctVictimOfCrime**: Percentage of the population victimized by crime.
- **PctCrimesAgainstPersons**: Percentage of crimes committed against individuals.
- **PctCrimesAgainstProperty**: Percentage of crimes committed against property.
- **PctCrimesDrugRelated**: Percentage of crimes related to drug offenses.
- **PctJuvenileOffenders**: Percentage of juvenile offenders within the crime data.
- **PctGangRelated**: Percentage of gang-related incidents.

### Final Attributes:
- **PctPopulationRetired**: Percentage of retired individuals in the population.
- **PctCrimesSolved**: Percentage of crimes solved by law enforcement.
- **PctPoliceViolations**: Percentage of reported violations by police personnel.
- **PctJuvenilesInDetention**: Percentage of juveniles in detention facilities.

### ***POSSIBLE PRE-BUILD NETWORK***
To enhance your analysis of the "Communities and Crime" dataset, integrating it with existing networks can provide valuable insights. Below are recommendations for spatial, social, and economic networks that align with your dataset and facilitate easy matching of identifiers:

**1. [Spatial Network: U.S. County Adjacency Network](https://www.census.gov/geographies/reference-files/2023/geo/county-adjacency.html?utm_source=chatgpt.com)**

- **Description**: This network represents U.S. counties as nodes, with edges indicating shared borders between adjacent counties.

- **Data Source**: The U.S. Census Bureau provides a comprehensive County Adjacency File, detailing neighboring county relationships. 

- **Identifier Matching**: Both the "Communities and Crime" dataset and the County Adjacency File utilize FIPS codes to identify counties, ensuring straightforward integration.

**2. [Social Network: U.S. County Commuting Patterns](https://www.census.gov/topics/employment/commuting/guidance/flows.html?utm_source=chatgpt.com)**

- **Description**: This network depicts commuting flows between U.S. counties, with nodes representing counties and directed edges indicating the volume of commuters traveling between them.

- **Data Source**: The U.S. Census Bureau's "County-to-County Commuting Flows" dataset offers detailed information on commuting patterns.

- **Identifier Matching**: The dataset includes FIPS codes for counties, facilitating direct alignment with your dataset.

**3. [Economic Network: U.S. County Trade Relationships](https://www.bea.gov/data/gdp/gdp-county-metro-and-other-areas)**

- **Description**: This network illustrates economic interactions between counties, such as trade or supply chain connections.

- **Data Source**: While specific datasets on county-level trade relationships are limited, the U.S. Bureau of Economic Analysis (BEA) provides regional economic accounts that can be used to infer economic linkages. 

- **Identifier Matching**: BEA data often includes FIPS codes, allowing for integration with your dataset.

**Integration Steps:**

1. **Data Acquisition**: Download the relevant datasets from the provided sources.

2. **Data Cleaning**: Ensure consistency in identifiers (e.g., FIPS codes) and handle any missing or inconsistent data.

3. **Data Integration**: Merge the "Communities and Crime" dataset with the chosen network data based on matching identifiers.

4. **Analysis**: Conduct your analysis, leveraging the combined datasets to explore spatial, social, or economic patterns in crime data.

By integrating these networks with your dataset, you can perform a comprehensive analysis that considers spatial proximity, social interactions, and economic relationships, providing a multidimensional perspective on crime patterns. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **Idea progetto 2**
*Influenza di post di influencer che promuovono prodotti fake per dimagrimento e quando gli adolescenti (soprattutto femmine) vanno poi a comprare questi prodotti e sono interessati a provare queste cose (ultimo si può fare tramite analisi dei commenti sotto i post/video). <br>
Social network da analizzare: Instagram, TikTok(?)* <br>

Graph API per prendere dati:<br>
1. **`Set Up an Instagram Developer Account`** <br>
To access the Instagram Graph API, you'll first need to set up an Instagram Developer account:<br>
*`Create a Facebook Developer Account`*: Visit Facebook for Developers and log in with your Facebook account.<br>
*`Create an App`*: In your Facebook Developer dashboard, create a new app. Select "For Everything Else" as the app type. This app will be used to access the Instagram Graph API.<br>
*`Set Up Instagram Basic Display`*: In the app settings, configure "Instagram Basic Display" to allow access to public profile information, media, and other content.<br>

2. **`Get Access to Instagram Data via the API`** <br>
You can access data like public media, comments, and hashtags using the Instagram Graph API. Here’s a high-level overview:<br>
*`a) Request an Access Token`* <br>
You’ll need to generate an access token to authenticate your requests to the Instagram Graph API. This token is linked to your app and your Instagram Business or Creator account.<br>
*To generate an access token*:<br>
Go to the Tools & Support section of the Facebook Developer dashboard.<br>
Under Access Tokens, generate a short-lived token for development.<br>
Convert it into a long-lived token by making an API call, so that you don’t have to refresh it frequently.<br>
*`b) Link Instagram Account to Your App`* <br>
You need an Instagram Business or Creator account to access more detailed metrics. `To link it`:<br>
In Instagram settings, switch your account to either Business or Creator.<br>
Link your Instagram account to the Facebook Page that you’ll manage via the API.<br>

# PROGETTI DI ALTRI
[@brauliovillalobos](https://github.com/brauliovillalobos/data-driven-modeling-complex-systems-10600503)
