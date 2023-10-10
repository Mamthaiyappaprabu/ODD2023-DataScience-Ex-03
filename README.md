# EX-03 UNIVARIATE ANALYSIS :
## AIM :
To read the given data and perform the univariate analysis with different types of plots.
## Explanation:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.
## Algorithm:
### Step1: 
Read the given data.
### Step2: 
Get the information about the data.
### Step3: 
Remove the null values from the data.
### Step4: 
Mention the datatypes from the data.
### Step5: 
Count the values from the data.
### Step6: 
Do plots like boxplots,countplot,distribution plot,histogram plot.
## Program:

### NAME : MAMTHA I
### REG NO : 212222230076

### DIABETES.CSV :
```
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files

uploaded=files.upload()
df=pd.read_csv('diabetes.csv')

df.head()

df.describe()

df.isnull().sum()

df.info()

sns.boxplot(x="Glucose",data=df)

Glucose_q1 = df['Glucose'].quantile(0.25)
Glucose_q3 = df['Glucose'].quantile(0.75)
Glucose_IQR = Glucose_q3 - Glucose_q1
Glucose_low = Glucose_q1 - 1.5 * Glucose_IQR
Glucose_high = Glucose_q3 + 1.5 * Glucose_IQR
df=df[((df['Glucose']>=Glucose_low)&(df['Glucose']<=Glucose_high))]

sns.countplot(x="Glucose",data=df)

sns.distplot(df['Glucose'])

sns.histplot(x="Glucose",data=df)

```
### OUTPUT :


![Screenshot 2023-10-10 194630](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/2e608a6f-f8e3-4309-9534-cdcbcebec750)



![Screenshot 2023-10-10 194640](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/519f859d-9ff0-4d00-912f-ef39a74d31ac)

![Screenshot 2023-10-10 194647](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/ceb8e25b-ea7b-4a6b-891e-8ab66690dc25)


![Screenshot 2023-10-10 194654](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/231c474a-2090-4abc-8538-051473486012)


![Screenshot 2023-10-10 194703](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/bed3c3c1-f6e3-4903-a042-9160f21eeb9d)


![Screenshot 2023-10-10 194714](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/e288cbfe-0916-450e-8df2-c72efe65850a)


![Screenshot 2023-10-10 194727](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/18eddce8-7135-4fde-8755-bcff429ba7fe)

![Screenshot 2023-10-10 194737](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/c624374e-3769-4b5f-95df-aab54b49e5e8)

### SUPER STORE.CSV :
```

import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('SuperStore.csv')

df.head()

df.describe()

df.isnull().sum()

df.info()

df['Postal Code']=df['Postal Code'].fillna(method='ffill')

sns.boxplot(x='Postal Code', data=df)

sns.countplot(x='Postal Code',data=df)

sns.distplot(df["Postal Code"])

sns.histplot(x="Postal Code",data=df)

```
### OUTPUT :

![Screenshot 2023-10-10 195810](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/efd626bd-6804-490c-89ba-99afec105f2b)

![Screenshot 2023-10-10 195824](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/7efa6037-8238-48f4-b0b1-7be9297e330e)

![Screenshot 2023-10-10 195831](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/bd394655-af4b-471c-8ba9-0ab80c39cf2f)


![Screenshot 2023-10-10 195839](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/ea414e32-e080-4baa-949f-b1a1c037c104)

![Screenshot 2023-10-10 195848](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/ab382a92-1a21-4462-b574-c06313cf6969)

![Screenshot 2023-10-10 195856](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/72e30c03-e069-4748-9621-3e5e098a61b0)


![Screenshot 2023-10-10 195906](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/0b869e5e-01b9-4c64-bae3-86a349b90625)


![Screenshot 2023-10-10 195915](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/e3aa5db5-7043-4780-a66f-d56635162a32)

### EMPLOYEESAL.CSV :
```
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('employeesal.csv')


df.head()

df.describe()

df.isnull().sum()

sns.boxplot(x='Experience_Years',data=df)

sns.countplot(x="Experience_Years",data=df)

sns.distplot(df['Experience_Years'])

sns.histplot(x="Experience_Years",data=df)

```
### OUTPUT :

![Screenshot 2023-10-10 200944](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/0e75eab9-e985-4097-bbb3-35d1b2a8d7a5)

![Screenshot 2023-10-10 200951](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/a8f61b4c-0155-4dd3-8577-4cb2c538baf9)

![Screenshot 2023-10-10 200956](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/5938bb95-a9f8-4bc2-93aa-03d175892df0)


![Screenshot 2023-10-10 201008](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/eef04f13-95a8-46d3-944a-ac01ee2700d1)


![Screenshot 2023-10-10 201016](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/58870fde-adf5-47cd-b8da-557d8fa8c0b0)

![Screenshot 2023-10-10 201024](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/cdba1617-3799-4f44-ae51-82753b4888c6)
![Screenshot 2023-10-10 201033](https://github.com/Mamthaiyappaprabu/ODD2023-DataScience-Ex-03/assets/119393563/667947ad-c1f7-49da-bbf7-ea657875f719)


## Result:
Thus we have read the given data and performed the univariate analysis with different types of plots.
