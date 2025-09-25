# Space X Data Analytcis and Falcon 9 First Stage Landing Prediction.
In this capstone, we will predict if the Falcon 9 first stage will land successfully. SpaceX advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. Therefore if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against SpaceX for a rocket launch.

This repository contains the files created as part of the 'Applied Data Science Capstone' course from the `'IBM Data Science Professional Certificate'` offered through Coursera.

## The analysis includes:

1. In the spacex-data-collection-api notebook we use the `SpaceX API` to collect rocket launch data, `format the JSON response` into a DataFrame, filter for only Falcon-9 Launches and perform some basic preprocessing like dealing with missing values in relevant columns.

2. In the webscraping notebook we scrape an html table on a Wikipedia page to `collect/parse data using BeautifulSoup`, filter for Falcon-9 launches, extract feature names from the table header and create a usable DataFrame.

3. In the wrangling notebook we perform `basic initial EDA and create a landing outcome label (Y)`.

4. In the eda sql notebook we gain a better understanding of the SpaceX dataset by `performing EDA, loading the dataset into the corresponding table in a Db2 database and executing SQL queries` to answer assignment questions.

5. For the eda data viz notebook we perform further EDA by `visualization of the relationships among features and between features and the target variable(outcome)`. Additionally, we perform some feature engineering (`one-hot-encoding, data type consistency for numeric columns`).

6. In the launch site location notebook we use `folium to Mark all launch sites on an interactive map, mark the success/failed launches for each site on the map using MarkerCluster() and calculate the distances between a launch site to its proximities`(like coastlines, railways, highways, cities).

7. The spacex-dash-app.py file is an `interactive dashboard built using Plotly Dash`. We can `filter launch data` based on the launch site(dropdown) and payload mass(slider). The `visualizations include a pie chart and scatter plot` which show success rates of launch sites and the correlation between outcome and payload mass based on selected launch site and/or booster version.

8. Finally, the Machine Learning Prediction notebook is where we seperate the dataset into X and Y, `standardize` the data, then `split it into train and test sets`, train SVC, DecisionTree, Logistic Regression and KNN models(with `hyperparameter tuning using GridSearchCV with CrossValidation`) and `compare their performances` using accuracy and their respective confusion matrices.
