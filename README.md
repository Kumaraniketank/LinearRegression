# LinearRegression
prediction of marks on the basis of study hours by using LinearRegression. The Spark Foundation TSF GRIP task #1
import pandas as pd
from sklearn.linear_model import LinearRegression
url = "https://raw.githubusercontent.com/AdiPersonalWorks/Random/master/student_scores%20-%20student_scores.csv"
dataSet = pd.read_csv(url)
print(dataSet.shape)
print(dataSet.head(10))
X = dataSet.iloc[:,:-1].values
Y = dataSet.iloc[:,-1].values
Model = LinearRegression()
Model.fit(X,Y)
Hours = [[9.25]]
Model.predict(Hours)
