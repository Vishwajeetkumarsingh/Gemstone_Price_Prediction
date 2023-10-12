
#  Gemstone Price Prediction Project

Welcome to the Gemstone Price Prediction project. This project is part of my data science journey and focuses on predicting gemstone prices. We use a dataset from Kaggle, provided by Gem Stones Co Ltd, a cubic zirconia manufacturer. The company aims to optimize profits by accurately predicting gemstone prices and understanding the most influential factors.


![Alt Text](https://upload.wikimedia.org/wikipedia/commons/thumb/b/bd/CZ_brilliant.jpg/260px-CZ_brilliant.jpg)

**cubic zirconia**
## Objective

Our client, Gem Stones Co Ltd, a leading cubic zirconia manufacturer, has entrusted us with a critical task. They have provided us with a comprehensive dataset comprising the pricing and various attributes of nearly 27,000 cubic zirconia gemstones. These gemstones, often regarded as an affordable diamond alternative with comparable qualities, are instrumental in driving the company's diverse profit margins.

The client's primary challenge is to optimize their profit margins by predicting the price of these cubic zirconia gemstones accurately. This predictive model will enable them to differentiate between highly profitable and less profitable gemstones, ultimately contributing to a more efficient distribution of resources and profit allocation. Furthermore, our task extends to identifying the top five attributes that exert the most significant influence on gemstone pricing.

By achieving these objectives, we aim to empower Gem Stones Co Ltd with actionable insights, enabling them to make informed decisions and enhance their profitability in a competitive market.
## Dataset

The dataset contains information about almost 27,000 cubic zirconia gemstones, including attributes such as:

- Carat
- Cut
- Color
- Clarity
- Depth
- Table
- Length (X)
- Width (Y)
- Height (Z)
- Price
## Data Dictionary


- **Carat**: Carat weight of the cubic zirconia.
- **Cut**: Describes the cut quality of the cubic zirconia, with quality increasing in the order of Fair, Good, Very Good, Premium, Ideal.
- **Color**: Color of the cubic zirconia, with D being the best and J the worst.
- **Clarity**: Cubic zirconia clarity refers to the absence of inclusions and blemishes. It follows the order from best to worst: FL (flawless), IF, VVS1, VVS2, VS1, VS2, SI1, SI2, I1, I2, I3.
- **Depth**: The height of a cubic zirconia, measured from the Culet to the table, divided by its average Girdle Diameter.
- **Table**: The width of the cubic zirconia's table expressed as a percentage of its average diameter.
- **Price**: The price of the cubic zirconia.
- **X**: Length of the cubic zirconia in millimeters.
- **Y**: Width of the cubic zirconia in millimeters.
- **Z**: Height of the cubic zirconia in millimeters.


## Insights

In the course of this project, we've gathered several key insights:

**A.) 4 C's of Diamond - Cut, Color, Clarity, and Carat:**


- **Cut Analysis:** We can see that we have the most number of ideal cuts and very few fair cuts.
- **Color Analysis:** We know that for the color grades of cubic zirconia, D is the best, and J is the worst. Most of our diamond colors are of decent grade.
- **Clarity Analysis:** Clarity order from best to worst is FL, IF, VVS1, VVS2, VS1, VS2, SI1, SI2, I1, I2, I3. Most of our cubic zirconia are not of optimal clarity.
- **Carat Analysis:** Most of our cubic zirconia diamonds, almost 75%, have less than 1 carat.

**B.) Dimensions:**

- **Depth Analysis:** Our diamonds' depth is in a good range, affecting value and brilliance.
- **Table Analysis:** Our table size is optimal, playing a vital role in brilliance and light performance.
- **Length(X), Width(Y), Height(Z) Analysis:** Diamond dimensions are within the typical ranges.

**Price Analysis:**

- 75% of diamonds have prices below 5000, with some as high as 18000.

**C.) Effects of Categorical Columns on Price:**

- **Analysis of 'Price' by 'Cut':** On average, premium cuts are more costly, followed by very good cuts, good, fair, and then ideal.
- **Analysis of 'Price' by 'Color':** The average price of J color diamonds is the highest, while E is the lowest.
- **Analysis of 'Price' by 'Clarity':** The average price of S12 clarity diamonds is the highest, while IF and WS1 are the lowest.

**Analysis of Color by Their Cuts:**

- Most number of ideal and premium cut diamonds are obtained from G colored diamonds.
- Most numbers of Very Good cut diamonds are obtained from E colored diamonds.

**Analysis of Clarity by Their Cuts:**

- Most number of Ideal cut diamonds are obtained from VS2 clarity diamonds.
- Most number of Premium cut and Very Good cut diamonds are obtained from SI1 clarity diamonds.

**Analysis of Clarity by Their Cuts:**

- Most number of Ideal cut diamonds are obtained from VS2 clarity diamonds.
- Most number of Premium cut and Very Good cut diamonds are obtained from SI1 clarity diamonds.## Data Preprocessing

In the data preprocessing phase, we've performed the following tasks:

- **Handling missing data:** In the "Depth" column, we identified 697 missing values. After analysis, we observed that the mean and median of this column were nearly equal at around 61.8. To address these missing values, we replaced them with the mean value.

- **Encoding categorical variables:** We employed ordinal encoding for our categorical columns:
  - **Cut:** Diamonds are graded into the following cuts (best to worst): Ideal > Premium > Very Good > Good > Fair. We encoded these variables with 1 representing the lowest and 5 the highest. For example, "Fair" was encoded as 1, and "Ideal" as 5.
  - **Color:** Diamonds are valued by how closely they come to being colorless. The less color, the higher their value. We encoded the color grades from D to J, with D as 1 and J as 7.
  - **Clarity:** The clarity of diamonds can be graded in the following grades (best to worst): IF > VVS1 > VVS2 > VS1 > VS2 > SI1 > SI2 > I1, with I1 as 1 and IF as 8.

- **Removing outliers:** We observed that almost all the columns contained outliers, but we specifically performed outlier treatment for our target column, "Price." Outliers were addressed using appropriate techniques.

Please note that the detailed code for these data preprocessing tasks can be found in the accompanying Model_Building Jupyter Notebook.

## Model Building

We've constructed multiple regression models to predict gemstone prices, including Linear Regression, Ridge Regression, Lasso Regression, Elastic Net, Decision Tree, Random Forest, AdaBoost, and Gradient Boosting.

## Model Evaluation

To evaluate the performance of the models, we've used metrics such as Mean Squared Error (MSE), Mean Absolute Error (MAE), R-squared (R2), and Adjusted R-squared (Adj R2).

## Model Comparison

We've compared the performance of different models to identify the most accurate one for gemstone price prediction.

The Random Forest Regressor appears to be the best-performing model based on the lowest Mean Squared Error, Mean Absolute Error, and the highest R-squared and Adjusted R-squared values. It offers a good balance between prediction accuracy and complexity.

## Conclusion

The project has provided valuable insights into gemstone pricing. By analyzing the "Four C's of Diamonds," dimensions, and categorical attributes, we've gained a better understanding of factors influencing gemstone prices. The predictive models will help Gem Stones Co Ltd optimize their profits.

## Factors Influencing Gemstone Pricing

Understanding the key factors influencing gemstone pricing is essential. Here are the top 5 attributes that exert the most significant influence on gemstone pricing:

1. **Carat:** The carat weight of the cubic zirconia is a major factor influencing the price. As the carat weight increases, the price of the gemstone also increases.

2. **Cut Quality:** The cut quality of the cubic zirconia plays a crucial role in determining the price. Premium and ideal cuts are associated with higher prices, while fair cuts are less expensive.

3. **Clarity:** Clarity, specifically, clarity grade SI1, has a notable impact on pricing. Diamonds with better clarity grades tend to be more expensive.

4. **Color:** The color of the cubic zirconia, with J color being the highest priced, also significantly

5. **Table Percentage:** The width of the cubic zirconia's table expressed as a percentage of its average diameter (table percentage) plays a role in pricing. Gemstones with optimal table percentages tend to be more valuable.
## 🚀 About Me
Hi i am vishwajeet kumar.
If you have any questions or suggestions, please feel free to contact me at [vishwajeetkumarsingh4209@gmail.com].

Happy coding!

## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/)https://www.linkedin.com/in/vishwajeet-kumar-95a27a1b4/


