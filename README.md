# King County Housing Price Analysis

### Context
This project explores the King County housing dataset (USA), which includes information about home prices and various features such as location, size, condition, and renovation history.

### Objective
To identify which property characteristics strongly affect house prices — size, grade, location, and renovations
Link to Kaggle Dataset - https://www.kaggle.com/datasets/harlfoxem/housesalesprediction/data
Link to Canva Presentataion - https://www.canva.com/design/DAG1mNCCFzg/cQYMf9Gi3gyEQJjy318TuA/edit?ui=eyJBIjp7fX0

Names and descriptions of the columns in the provided King County dataset:

- id - unique ID for a house
- date - date house was sold
- price - price of the house
- bedrooms - number of bedrooms
- bathrooms - number of bathrooms
- sqft_living - square footage of the home
- sqft_lot - square footage of total land area of the compound the house sits on
- floors - total floors (levels) in house
- waterfront - whether house has a view to a waterfront
- view - an index from 0 to 4 of how good the property's view is
- condition - how good the condition is (overall); ranked from 1 to 5, 5 being the greatest condition
- grade - classification by construction material and worksmanship quality. The higher the number, the better the grade
- sqft_above - square footage of house (apart from basement)
- sqft_basement - square footage of the basement
- yr_built - year when house was built
- yr_renovated - year when house was renovated
- zipcode - zip code in which house is located
- lat - Latitude coordinate
- long - Longitude coordinate
- sqft_living15 - The square footage of interior housing living space for the nearest 15 neighbors
- sqft_lot15 - The square footage of the land lots of the nearest 15 neighbors

### Data Preparation

Key preprocessing steps to make the data analysis-ready:

- Calculated house age (yr_sold - yr_built) to assess depreciation effects.
- Replaced 0 renovation years with NaN for clarity.
- Computed years since last renovation to measure recency.
- Created renovation status column (Yes/No) for comparison.
- Converted zipcode to string for categorical grouping.
- Parsed date to datetime dtype.
- Mapped waterfront (0 → “No”, 1 → “Yes”).
- Added column for resale homes (sold_more_than_once).
- Derived price per square foot as a value efficiency metric.

### Univariate Analysis
- Distribution of price, bedrooms, bathrooms, and sqft_living.
- Outlier detection and price skewness exploration.

### Bivariate Analysis
- Price vs Sqft Living: Larger homes generally sell for more.
- Price vs Grade: Strong positive relationship between construction quality and price.
- Price vs Zipcode: Clear location-based price differences.
- Price vs Condition: Weaker correlation than grade.

### Multivariate Analysis
- Price, Renovation & Age: Renovations raise prices only for older homes.
- Price, Grade & Condition: Grade explains price variation better than condition.
- Price, Sqft & Bedrooms: Bedrooms alone are not strong predictors without size.
- Price, Location & Sqft: Central zipcodes command higher prices even for smaller houses.

### Key Insights
- Most homes are priced below $1M with the median price between $400K–$600K
- The price has a Right-skewed distribution — a small number of very expensive homes (luxury properties) push the tail toward the right.
- Most houses have upto 3 or 4 bedrooms and 2.5 bathrooms with very few having more than 6 bedrooms and 3+ bathrooms
- Grades 7–9 dominate signaling average to above-average construction quality. The market is mostly mid-range, not luxury-dominated.
- Most house are in condition 3 indicating average condition thus market is not luxury-dominated
- 

### Tool Used
- Python
- Jupyter
- Github
