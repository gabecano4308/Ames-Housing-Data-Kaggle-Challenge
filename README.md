# Ames Housing Data and Kaggle Challenge

### Overview
For this project, I assume the role of a consultant hired by an aspiring home flipper. I advise her on which factors of homes in Ames she should focus on improving in order to maximize sale price.

With this mission in mind, the project compares, synthesizes, and analyzes information from the 2006-2010 Ames Housing dataset. The dataset is provided by the Ames Assessor's Office and the data documentation can be found [here](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt).

### Problem Statement
>When upgrading a home, it is difficult to decide which features to renovate because it's often unclear which focus areas will lead to a higher sale price. This project analyzes a wide array of features for homes across Ames, Iowa to recommend which factors to emphasize when flipping houses in the region.

### Background
This Ames Housing Dataset describes the sale of individual residential property in Ames, Iowa
from 2006 to 2010. It contains 2930 observations and a relatively large number of variables (23 nominal, 23 ordinal, 14 discrete, and 20 continuous) involved in assessing home values ([source](http://jse.amstat.org/v19n3/decock.pdf)).

### Methodology
* The Ames Housing dataset was cleaned and certain house factors were dropped based off an initial analysis that showed little to no correlation between them and the corresponding sale prices.
* A model was created with scaled data to evaluate how accurately different house factors predicted sale price.
* Primary findings were visualized using a variety of graphs and charts, in order to better communicate insights with a non-technical audience.

##### Provided Datasets
* [`train.csv`](./datasets/train.csv): train dataset, including sale prices.
* [`test.csv`](./datasets/test.csv): test dataset to make predictions on (doesn't include sale price).

##### Datasets Created During Project
* [`final_submission.csv`](./datasets/final_submission.csv): submission dataset consisting of my model's sale price predictions and corresponding IDs.
* [`train_cleaned_x_vars.csv`](./datasets/train.csv): cleaned version of the original train.csv dataframe.
* [`train_transformed_x_vars.csv`](./datasets/train.csv): transformed version of the cleaned train.csv dataframe (applied dummy variables and polynomial features).
* [`test_cleaned_x_vars.csv`](./datasets/train.csv): cleaned version of the original test.csv dataframe.
* [`test_transformed_x_vars.csv`](./datasets/train.csv): transformed version of the cleaned test.csv dataframe (applied dummy variables and polynomial features).

### Conclusion from Analysis  
#### Key Takeaways:
* Improving factors related to square foot area and overall quality are more indicative of a higher sale price than adding quantity to certain amenities such as pools and fireplaces. For area, the correlation with sale price lessens once it passes the 4,000 square feet mark. The high accuracy of my model backs up these assessments, but note that the accuracy slightly decreases once sale prices exceed $400,000.

#### Recommendation:
The home flipper should invest more of her time and resources on annexing new rooms in the house to increase indoor square footage, as well as renovate existing spaces such as the kitchen, basement, or garage to improve quality. The home flipper should focus less on building new amenities for the home, such as constructing a larger pool or adding multiple fireplaces.
