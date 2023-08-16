# Sales Predictions
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
   
 #### Average Item Sales by Type and Fat Content
![Capture]() 
- Comparing the sales by Item and their fat content, we can see that the sales of certain items are clearly influenced by whether they are low fat or regular. An observation I see is that items which tend to have high levels of sugars such as snacks, drinks and breakfast are the items that sell more low fat content.

### Item Outlet Sales by Outlet Type
![Capture2]()
- SupermarketType3 clearly has the most sales. It would be useful to understand more what the differences are between the different types of supermarket outlets to disect further why these outlets are selling more on average than its counterparts.


## Results and recommendations 
The Random Forest model outperforms both linear regression and the Decision Tree model and stands out with the highest R^2 value (72.2%) on the training data, indicating that it explains about 72.2% of the variance in the target variable. This model also performs relatively well on the test data, capturing 59.1% of the variance. With balanced performance and the highest R^2.

- Considering the given metrics, the Random Forest model seems to be the best option among the three. Its balance between training and test data performance, along with its ability to handle complex relationships, makes it a favorable choice for predicting the target variable in this scenario.

### For further information
For any additional questions, please contact **mohamediyadhtajouri@gmail.com**
