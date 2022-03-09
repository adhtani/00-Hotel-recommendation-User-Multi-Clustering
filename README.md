# Hotel Recommendation-Applied User Clustering Algorithm
**Overview**  
 
This project was launched as a competition by Expedia in Kaggle. The challenge was to contextualize customer data and predict the likelihood a user will stay at a 100 different hotel groups. So, this is a large multi class classification problem. Expedia provides two data sets for this project.  Training data is between 2013-2014 data and test data is for 2015. Basically, we will be using previous years data to make predictions for the future. In this Project I attempt to create my own algorithm using collaborative filtering and the two-dataset provided.

**Data Sources**  
 
Expedia Hotel Recommendation: [Kaggle.com](https://www.kaggle.com/c/expedia-hotel-recommendations/data)


**Key Steps**  

•	Data Collection - After loading the data, I filtered the dataset to only "is_booking" = 1, because the problem statement states predict the hotel cluster a customer will likely book. 0 means it was only a click.
•	EDA - After this I performed some Exploratory data analysis and realized it is a 100-class classification problem. Moreover, none of the variables had any correlation to the target variable thus, linear models will not be appropriate techniques for this data.
•	Data preparation - After this I checked for missing values and performed some feature engineering to time stamp and check-in check-out time variables.
•	Feature Selection - Performed some feature selection before modeling using Chi2 and Mutual Information method.  
  
**Modeling:**   

I used a different approach. I decided to combine unsupervised and supervised learning to this problem. I recalled collaborative-filtering concepts and applied it in this problem. Instead of applying one trained model to all users, I decided to divide users into 5 different user clusters based on user similarity using KMeans clustering. Further I wrote an algorithm that will train KNN model for each user cluster. The accuracy rate improved significantly using this approach to 36%
