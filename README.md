# Regression Project Zillow 


## Deliverables
- A report in the form of a presentation, verbal supported by slides. The report/presentation slides should summarize findings about the drivers of the single unit property values.
- A github repository containing your work.
- A repository that contain the .py files necessary to reproduce work, and work must be reproducible by someone with their own env.py file.


## Goals
- Create a madel that predicts the values of single unit properties 
- Find the distribution rate of the tax rates for each county
- Find drivers for single unit property values
- Find county and state properties are located 


## Audience
- Zillow data science team


## Project Context
- Used Zillow data from the CodeUp SQL database.

260	Residential General
261	Single Family Residential
262	Rural Residence
263	Mobile Home
264	Townhouse
265	Cluster Home
268	Row House
273	Bungalow
274	Zero Lot Line
275	Manufactured, Modular, Prefabricated Homes
276	Patio Home
279	Inferred Single Family Residential

- Used two tables properties_2017 and predictions_2017  


## Data Dictionary
| Column Name       | Datatype | Description                                                                              | Use                   |
|-------------------|----------|--------------------------------------------------------------------------------|-----------------------|
| parcel_id       | int64 |Unique Identifier for each property                                         | Identifier|
| tax_value       | float64 | Tax appraised value of home. Original column name taxvaluedollaramount  | Target    |
| bathrooms       | float64 | Number of bathrooms. Original column name bathroomcnt                    | Variable  |
| bedrooms        | float64 | Number of bedrooms. Original column name bedroomcnt                                | Variable  |
| calculated_finished_sqft | float64 | Total Square footage of home. Original column name calculatedfinishedsquarefeet | Variable  |
| has_pool        | float64 | Indicator on whether the property has a pool or not from poolcnt       | Variable |
| has_garage      | float64 | Indicator on whether the property has a garage or not from garagecarcnt | Variable |
| tax_amount      | float64 | Amount of tax collected for property                                       | Information    |
| fips            | float64 | Federal Information Processing Standards Code. Indicator of county        | Information    |
| county          | float64 | County where the property is located from fip                   | Informatin     |
| tax_rate        | float64 | Percentage of value that was paid in taxes. Calculated from tax_value and tax_amount | Information    |
|transaction_date | object | The date a transaction is recorded with the county to transfer the real property from the Sellers to the Buyers | Information |
      
 
## Hypotheses

Pearson R Test Performed

Alpha
- a=.05

**Hypothesis 1**

H0: There is no linear coorrelation between total square footage and tax value

Ha: There is a linear correlation between total square footage and tax value

**Result - We rejected the null hypothesis**

**Hypothesis 2**

H0: There is no linear correlation between number of bathrooms and tax value  

Ha: There is a linear correlation between number of bathrooms and tax value

**Result - We rejected the null hypothesis**


## Reproduce My Project

- Python
- SQL
- pandas
- numpy
- matplotlib/seaborn
- sklearn
- stats
- You will need your own env file with database credentials along with all the necessary files listed below to run my final project notebook.
- Read this README.md
- Download the wrangle.py, evaluate.py, explore.py and final_report.ipynb files into your working directory
- Add your own env file to your directory. (user, password, host)
- Run the final_report.ipynb notebook
