# Click-Thorugh-Rate-for-Advertising-Dataset

**Abstract**
This project presents a unique way of solving a real life question which
every company faces in digital marketing. Digital Advertising is a multibillion dollar industry which is growing rapidly with each year. The
project model focuses on determining whether a said person in the
dataset would click on the ad link on the particular site or not
depending on different parameters related to the person or the ad.

**Executive Summary**
In the past few years, digital marketing has taken over traditional
marketing. This is because even if traditional marketing brings a trickle
of business, digital marketing offers a productive and cost-effective
way to reach out to higher numbers. Consequently, companies have
been choosing to advertise their products on websites and social
media platforms. In any advertising agency, it is very important to
predict the most profitable users who are very likely to respond to
targeted advertisements. By predicting the click-through rate, an
advertising company selects the most potential visitors who are most
likely to respond to the ads, analyzing their browsing history and
showing the most relevant ads based on the interest of the user. This
task is important for every advertising agency because the commercial
value of promotions on the Internet depends only on how the user
responds to them. A user’s response to ads is very valuable to every
ad company because it allows the company to select the ads that are
most relevant to users.

**Hypothesis**
The report aims to answer the research question of what parameters
actually affect the customer’s decision of whether to click on the ad or
not. One would expect the time which the customer spends browsing
on the site and the location from where they are doing so would have
most significance on their decision. However, our hypothesis is that
Age, Income and Daily Time spent on Site will affect the most.

**Variable Name Data Type Description**
Daily Time Spent on Site Float Time spent on the site by
each customer in minutes
Age Integer Age of each customer in
years
Area Income Float Income of customers in
dollars
Daily Internet Usage Float Daily usage of customers on
all internet platforms
Ad Topic Line String The topic of each
advertisement shown to the
customer
City String From which city the customer
hails from.
Male Boolean Whether the customer is male
Country String From which country the
customer is from
Timestamp Date The time at which the
customer goes online
Clicked on Ad Boolean Whether the customer clicks
on the ad or not

**1. Daily Time Spent on Site vs Age**


![image](https://user-images.githubusercontent.com/122759737/214117604-8c91567e-99de-4641-b612-313c232c8b3a.png)

We can see that a large number of people under
the age of 30 spend the most time on the internet, which is more
than 80 minutes. We can also see that the second-highest age
group is the late '30s, with an average of 40 minutes spent on
the internet. We can estimate that we should target a group of
people in their 30s and 40s based on this information.

**2. Area Income versus Age**


![image](https://user-images.githubusercontent.com/122759737/214117616-f5811ea1-2563-4c8d-b317-b6545445ab38.png)

We can determine that people between the
age range of mid 20’s to their late 30’s who have an income
between $50k to $70k are the ones who click on the ad the most.
Our next step should be targeting this group of people so that we
can increase our exposure as much as possible.

**3. Daily Time Spent on Site vs Daily Internet Usage**


![image](https://user-images.githubusercontent.com/122759737/214117632-4da7cc43-4bf1-4abc-9a13-05a3eef64799.png)

We can see there are 2 major groups of points
which we can target. One of them is between daily usage of 100
to 125 mins when the daily time spent on the specific site is
between 40 to 60 mins. The other one is between the daily
internet usage of 200 to 250 mins when the time spent on our
site is between 70 to 90 mins

**Correlation Analysis**

![image](https://user-images.githubusercontent.com/122759737/214117655-e28ee16a-9c87-4a01-8c2a-2d949aba3e05.png)

After importing Corrplot from Seaborn package we can
understand the correlation between the x variables and the y
variable i.e. - Clicked on Ad.
As we can see our y variable (Clicked on ad) is highly correlated
to Age, Area Income and Male.
The higher correlation shows the higher impact of the x variables
on the y variable and the lower correlation shows the lower
impact of the x variables on the y variable.

**Variable Selection**

![image](https://user-images.githubusercontent.com/122759737/214117726-f44041ea-4ddc-48f0-a51a-e98bb8b9c319.png)


In our dataset we have 10 variables which are as follows: Daily
Time Spent on Site, Age, Area Income, Daily Internet Usage, Ad
Topic Line, City, Male, Country, Timestamp, Clicked on Ad. We
have 9 independent variables and 1 dependent variable for our
model. The dependent variable (y) is “Clicked on Ad”, which is
our predicting variable. The other 9 other independent variables
(x) are used for predicting the dependent variable. By using
seaborn, we have used sns.corrplot to visualize the correlation
between the dependent and the independent variables. The
higher correlation value between the dependent and
independent variables depicts the higher dependency of the y
variable on the x variable, which shows that a change in the
values of the x variable, will highly affect the values of the y
variable.

**Final Model Description**


For the final model we have imported a Logistic regression
model from the from the python package, sklearn.linear_model
for the prediction of the y variable i.e. “Clicked on Ad”. Since we
have only one predicting variable, which is whether the person
clicks on an ad or not i.e. 0 or 1. First, we have split the training
and testing data into 70% as training data and 30% for testing
data using sklearn.model_selection. After which we have fit the
x_train and y_train into our model. After executing the logistic
regression model, we have predicted the data using y_test,
which is 30% of the total data. Later, we presented the
classification report from the sklearn.metrics package in python.
Finally from the classification report, we got the precision, the
recall, the f1-score and ultimately, accuracy of the model. This
generated classification report projects the performance of the
model.

**Model Overview**

![image](https://user-images.githubusercontent.com/122759737/214117887-c12c9810-f95a-422a-bbc1-49cd4dcb25bc.png)


Step 1: We downloaded the data set from kaggle.com
Step 2: We performed exploratory data analysis with
visualization of data and compared different variables to
understand the relation between them.
Step 3: We performed logistic regression on the data set to
predict the y variable i.e. click on ad.
Step 4: We predicted the accuracy, precision, recall and f1-score
of our logistic regression model.
Step 5: We imported the ROC-AUC curve of the regression
model.
Step 6: We imported the model summary of our logistic
regression model using statsmodels.api.

**Final Model Evaluation**

![image](https://user-images.githubusercontent.com/122759737/214117773-1c8ea0e2-14a5-4e90-9f12-b4dc6988faf2.png)


After the execution of our Logistic Regression Model we imported the
Classification Report from sklearn.metrics to get the Precision, recall
and f1-score of our model.
The accuracy of our Logistic Regression Model is 91%
The precision for the 0’s (people who do not click on ads) is 89%
The precision for the 1’s (people who click on ads) is 93%
The recall for 0’s (people who do not click on ads) is 94%
The recall for 1’s (people who click on ads) is 87%
The f1-score for 0’s (people who do not click on ads) is 91%
The f1-score for 1’s (people who click on ads) is 90%
As a result, we can say that the model executed successfully with high
accuracy, precision, recall and f1-score.

**Final Model Report**

![image](https://user-images.githubusercontent.com/122759737/214117951-fb9b8e9f-2167-4fdd-8307-d2077f5f3ed2.png)


An ROC-AUC curve determines the performance of the model
and gives us an idea about how well a model has been
executed.
So, we imported the roc_auc_score and roc_curve from
sklearn.metrics which we used to visualize our logistic regression
model’s performance.
The farther the Roc curve is from the line, the better is the
performance of the model.
As we can see, the Roc curve of our model is far from the line in
the above left corner of the graph which means that our logistic
regression model has performed well. The area covered by the
Roc curve of our logistic regression model above the line is 90%.
This ROC-AUC curve also shows the True Positive Rate and the
False Positive rate of the model.

**Model Summary**

![image](https://user-images.githubusercontent.com/122759737/214117973-a57ceb09-95b5-4f7f-80be-68b43d180e67.png)


After importing the ROC-AUC curve we imported the model
summary from statsmodels.api. This model summary determines
the Coefficients, Standard Errors, z-scores and p-values of the x
variables.

**Conclusion**
After successful implementation of the logistic regression model
on the data set, we can understand that we need to target the
audience with the age group between 30’s and 40’s as who are
spending the most time on the website and have higher chances
of clicking on the ad. We can also target the people between the
age group 20’s and 30’s having income of 50k to 70k are
spending more time on the website and have higher probability
of clicking the advertisement. We can also see that people with
daily internet usage of 100 to 125 mins and 200 to 250 mins are
spending the most time on website and hence have high
probability of clicking on the ads.

