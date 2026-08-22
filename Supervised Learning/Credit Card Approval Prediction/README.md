# 🍂 **[Credit Card Approval Prediction](https://www.kaggle.com/datasets/rikdifos/credit-card-approval-prediction/data?select=application_record.csv)** 🍂

### 🍄 Data Understanding

#### 1. Unzip Files 
  * Hi
  * Merge the two tables with the ID

#### 2. Importing Libraries

#### 3. Removing Missing values

  * Removing `nan` values in the target response feature `Status`.

#### 4. Splitting the data into training & testing sets

### 🍄 Data Wrangling


### 🍄 Feature Engineering 

#### Handling Numerical Features

**To avoid any potential multicollinearity**
a. Remove `CNT_CHILDREN` as it's correlated with `CNT_FAM_MEMBERS` <br>
b. `DAYS_BIRTH` convert it to Age <br>
c. `DAYS_EMPLOYED` converts to YOE <br>
d. Remove `DAYS_BIRTH` since `AGE` is created.

**After I converted `Days_Employed` to `Years To Experience`. It turns out that YOE has 999 values. It isn't realistic so I can treat them as "NaN" values and it's weight 17%. I'll delete these rows.**
After deleting the `999` values in the YOE column, the YOE is right-skewed.

**Variables will be deleted** <br>
a. `CNT_CHILDREN`: Because it's correlated to `CNT_FAM_MEMBERS` <br>
b. `DAYS_BIRTH`: Convert to `Age` <br>
c. `DAYS_EMPLOYED`: Convert to `YOE` <br>
d. `OCCUPATION_TYPE`: has 30% of missing values, so I replaced the "NaN" values with "Unknown" values because this how Decision Tree & Random Forest will understand & implemment <br>
e. `FLAG_WORK_PHONE`: is additional info, not primary & we've already `FLAG_PHONE`. I'll keep the later and exlcude the first one while training <br>
f. `FLAG_MOBIL`: I will delete it because it has one value only (1) <br>

#### Handling Categorical Features
##### Now I've handled the data processing for the numeric variables, the next steps are related to applying the categorical data handling/manipulation

**About the categorical variable** <br>
a. `ID` I don't want the ML model to handle it as a numeric varible but a categorical, to use it later to predict each instance <br>
b. `NAME_INCOME_TYPE` column
  - Applying **One Hot Encoding**, `Working` sets as the baseline, so I'll drop it.

c. `NAME_EDUCATION_TYPE` column
  - Applying **One Hot Encoding**, `Secondary / secondary special` sets as the baseline, so I'll drop it.

d. `NAME_FAMILY_STATUS` column
  - Applying **One Hot Encoding**, `Married` sets as the baseline, so I'll drop it.

e. `NAME_HOUSING_TYPE` column
  - Applying **One Hot Encoding**, `House / apartment` sets as the baseline, so I'll drop it.

f. `OCCUPATION_TYPE` column
  - I will focus on the primary instances with the highest total amount.
  - ['Laborers', 'Managers', 'Core staff', 'Sales staff', 'Drivers', 'High skill tech staff', 'Accountants']
  - Because these instances has a higher chance to accept or reject their loans. Especially that there bank accounts have the highest balance.

g. Rename the dataset columns because they don't look good. <br>
h. In the `NAME_INCOME_TYPE`, I can group these values [`State_servent`, `Pensioner`, and `Student`] under one label `Non-Commercial associate`
  - My distinct elements are now: [`Working`, `Commercial associate`, and `Non-Commercial associate`]

i. In the `NAME_HOUSING_TYPE`, I can group these values [`Municipal apartment`, `Rented apartment`, `Office apartment`, and `Co-op apartment`] under one label `Other apartment`
  - My Distinct elements are now: [`House/apartment`, `With parents`, and `Other apartment`]

j. In the `NAME_FAMILY_STATUS`, I can group these values [`Married`, and `Civil marriage`] under one label `Married`, then group values [`Single / not married`, and `Separated`] under one label `Single_Seperated`, and keep `Widow` as a distinct value.
  - My Distinct elements are now: [`Married`, `Single_Separated`, and `Widow`]

k.

l.

m.

n.

### 🍄 Model Training

### 🍄 Model Evaluation

### 🍄 Conclusion

