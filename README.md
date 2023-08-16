# Sales Predictions
![Data Science Cycle](https://github.com/iyadh97/food-sales-predictions/blob/main/Data/DS_CYCLE.png)
## Making Sales Predictions Using Machine Learning 
**Mohamed Iyadh Tajouri**: 
### Objective:
To help the retailer understand the properties of products and outlets that play crucial roles in increasing sales.
### Data:
[Link to original dataset](https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/) <br>
This dataset had a total of 8523 rows and 12 columns of information. There were a total 5 numeric columns and 7 categorical columns.

### Items that needed to be addressed: 
-  The data had 2 columns with missing items.
-  There was a column with inconsistent categories misspellings.
-  One of the columns was an Ordinal and had to changed to numerical.

### Preprocessing for Machine Learning Models
- Inconsistent categories were fixed
- Ordinal column was assigned numberic values
- Features and Target Values were assigned. In this case Item_Outlet_Sales was our Target.
- The data was split into a training and testing dataset using the default 75/25 split.
- Created a processor to include 2 Pipelines(one for categorical columns and one for numeric columns)
 - For categorical columns:
   - Addressed missing items using a constant SimpleImputer 
   - Converted categorical columns into numeric by using the OneHotEncoder
 - For numeric columns:
   - Addressed missing items usnig a mean SimpleImputer
   - Scaled all numeric columns
 
 ### Machine Learning Models
 - Created 2 Machine Learning models
   - Linear Regression Model
   - Decision Tree Model
   ### Data Dictionary
   ![Data/Screenshot 2023-08-16 114621.png](https://github.com/iyadh97/food-sales-predictions/blob/main/Data/Screenshot%202023-08-16%20114621.png)
   
 ### Exploratory Data Analysis

### Item Outlet Sales by Type
![Item Outlet Sales by Type](https://github.com/iyadh97/food-sales-predictions/blob/main/Data/Screenshot%202023-08-16%20114643.png)
- Based on the graph above we know that the Starchy Food Items have the most Outlet Sales and Others has the least sales.Sales are pretty similar across all the board and we can see that there isn't an item with overwhelmingly more sales in comparison to other items.


### Item Outlet Sales by Outlet Type
![Item Outlet Sales by Outlet Type](https://github.com/iyadh97/food-sales-predictions/blob/main/Data/Screenshot%202023-08-16%20114709.png)
- SupermarketType3 clearly has the most sales. It would be useful to understand more what the differences are between the different types of supermarket outlets to disect further why these outlets are selling more on average than its counterparts.

### Item Outlet Sales by Outlet Size
![Item Outlet Sales by Outlet Size](https://github.com/iyadh97/food-sales-predictions/blob/main/Data/Screenshot%202023-08-16%20114738.png)
- The graph above shows that Medium sized outlets sell the most and Small outlets sell the least.

#### Relationship between Item MRP and Outlet Sales
![Relationship between Item MRP and Outlet Sales](https://github.com/iyadh97/food-sales-predictions/blob/main/Data/Screenshot%202023-08-16%20114754.png) 
- This scatter plot shows the relationship between the item maximum retail price (MRP) and the corresponding outlet sales. Each point on the plot represents a specific item, with its MRP on the x-axis and the sales generated from the outlet on the y-axis. The plot helps identify any potential correlation or patterns between the MRP and sales, such as whether higher-priced items tend to generate higher sales.
- and in this case the higher the item MRP is, the higher sales (item outlet_sales) it generates
  
 #### Average Item Sales by Type and Fat Content
![ Item Sales by Type and Fat Content](https://github.com/iyadh97/food-sales-predictions/blob/main/Data/Screenshot%202023-08-16%20114811.png) 
- Comparing the sales by Item and their fat content, we can see that the sales of certain items are clearly influenced by whether they are low fat or regular. An observation I see is that items which tend to have high levels of sugars such as snacks, drinks and breakfast are the items that sell more low fat content.

 #### Average Item outlet sales by ItemType and outlet size
![Item outlet sales by ItemType and outlet size](https://github.com/iyadh97/food-sales-predictions/blob/main/Data/Screenshot%202023-08-16%20114925.png) 
- Using this barplot, we can observe all the Item outlet sales by ItemType (Frozen Foods, Seafood, soft Drinks etc...) and outlet size (small, medium and high)
- Based on the above graph:
We can tell that the Item Outlet Sales sell more medium Size items in all categories except for the Seafood.

## Results and recommendations 
The Random Forest model outperforms both linear regression and the Decision Tree model and stands out with the highest R^2 value (72.2%) on the training data, indicating that it explains about 72.2% of the variance in the target variable. This model also performs relatively well on the test data, capturing 59.1% of the variance. With balanced performance and the highest R^2.

- Considering the given metrics, the Random Forest model seems to be the best option among the three. Its balance between training and test data performance, along with its ability to handle complex relationships, makes it a favorable choice for predicting the target variable in this scenario.

### For further information
For any additional questions, please contact **mohamediyadhtajouri@gmail.com**
