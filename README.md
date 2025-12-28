# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
 import pandas as pd df=pd.read_csv("C:\Users\admin\Downloads\titanic_dataset.csv") df
         <img width="1430" height="623" alt="image" src="https://github.com/user-attachments/assets/a99e92f4-1367-4282-afb0-bd566c5d0429" />
         df.shape
         <img width="1327" height="84" alt="image" src="https://github.com/user-attachments/assets/39a315a2-afd0-4959-b591-f2d0e1375c72" />
         df.set_index("PassengerId",inplace=True) df 
         <img width="1323" height="587" alt="image" src="https://github.com/user-attachments/assets/48b08a60-f71d-487d-be39-a215d2150ded" />
         df.unique()
         <img width="1147" height="314" alt="image" src="https://github.com/user-attachments/assets/dbed9468-767c-4e7c-900e-8430cf3b7a3d" />
         df['Survived'].value_counts()
         <img width="1191" height="134" alt="image" src="https://github.com/user-attachments/assets/143441b1-8fee-485b-9490-f7c8c0107fdb" />
         df.Pclass.unique()
         <img width="1216" height="81" alt="image" src="https://github.com/user-attachments/assets/6e641097-75d3-440d-9500-93331d949cc1" />
         df.rename(columns={"Sex":"Gender"},inplace=True) df
         <img width="1333" height="587" alt="image" src="https://github.com/user-attachments/assets/18173e60-5c81-4a24-bf8f-4d7081574a51" />
         import seaborn as sns sns.countplot(data=df)
         <img width="1376" height="674" alt="image" src="https://github.com/user-attachments/assets/c2410bf8-afe9-4aff-ac1c-a0ba82de5c42" />
         sns.countplot(x="Survived",hue="Gender",data=df)
         <img width="1167" height="637" alt="image" src="https://github.com/user-attachments/assets/a8e394e6-4a10-4258-8d0f-bd93169c93c7" />
         sns.catplot(x="Survived",hue="Gender",data=df,kind="count")
         <img width="1290" height="704" alt="image" src="https://github.com/user-attachments/assets/7bc517a6-3baa-4504-adf1-a50b302c3b03" />
         sns.boxplot(data=df)
         <img width="1045" height="621" alt="image" src="https://github.com/user-attachments/assets/fe3940ae-84a5-4e26-94e8-2e84bf847057" />
         df.boxplot(column="Survived",by="Gender")
         <img width="1148" height="658" alt="image" src="https://github.com/user-attachments/assets/55b29fd2-911a-4431-9138-2abd72ac95cb" />
         sns.scatterplot(data=df)
         <img width="1393" height="646" alt="image" src="https://github.com/user-attachments/assets/6ae786b5-00cb-4f6a-95c3-d797ec823549" />
         sns.scatterplot(x=df['Age'],y=df['Fare'])
         <img width="1389" height="645" alt="image" src="https://github.com/user-attachments/assets/b72f7335-874a-4919-ab28-21223b838061" />
         sns.jointplot(x='Age',y='Fare',data=df,kind='kde')
         <img width="1315" height="822" alt="image" src="https://github.com/user-attachments/assets/bec0c4fa-7104-428d-a64b-320d191e16bd" />
         sns.jointplot(x='Age',y='Fare',data=df,kind='hist')
         <img width="1387" height="839" alt="image" src="https://github.com/user-attachments/assets/5d7dfb37-3dc6-4c31-9f90-982ab664710d" />















         



# RESULT
   The EDA process has been done successfully
