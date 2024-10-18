# **🍽️ Restaurant Tips Analysis**

![image](https://github.com/user-attachments/assets/0433addc-1d29-4ca5-aa79-9542ec975435)

This project aims to use the restaurant tips dataset to practice creating composition plots and visualizations. We will examine the relationship between different variables and the tips given.

The dataset consists of information from 244 restaurant bills, collected in the US in 1987.

It includes details about the tips given to restaurant staff, such as the total bill, tip amount, gender of the person paying, smoking status, day of the week, time of day, and party size.

**Data details**

**Source:** Swiss coding academy

**The main goal of this analysis:**
We will learn more the relationship between different variables and the tips given

**We need to answers below to find main goal:**
1. What is the data like?
2. What does the data need to clean?
3. What does the data group customer by?
4. What does the data need to calculate?
6. How do we need to compare groups by criteria?

**How do we do to answer?**

What is the data like?
   1. Import pandas ,matplotlib
   2. Read and Check data
   Results as :                      
*    The day it occurred
*    If it was at lunch or dinner
*    The total bill
*    The sex of the person
*    If they were a smoker or not
*    The size of the party

You can see table 5 first row of data :

||Id|Total_bill|Tip|Sex|Smoker|	Day|Time|Size|
|---|---|---|---|---|---|---|---|---|
|0|0|16.99|1.01|Female|No|Sun|	Dinner|	2|
|1|1|10.34|1.66|Male|No|Sun|	Dinner|	3|
|2|2|21.01|3.50|Male|No|Sun|	Dinner|	3|
|3|3|23.68|3.31|Male|No|Sun|	Dinner|	2|
|4|4|24.59|3.61|Female|No|Sun|	Dinner|	4|

What does the data need to clean?
   1. Check values is null, Check values is duplicate. Results: they are fine
   2. Check typyes and We have string columns considered as objects. So we fix their types correct.

      Result: We have dtypes: Float64(2), Int64(2), string(4). They fixed correct.

What does the data group customer by?

We need to calculate the tip figures between the two customer files. And we categorize the datas to be compared as follows:
* Smokers and non-smokers
* Male and Female
* Weekends and weekdays
* Lunch and dinner ( *We checked data about column time, and the result is the restaurant only has 2 service times*)

What does the data need to calculate?
  1. View describe data
  2. Calculate the metrics for the customer groups listed above as: Min, Max, Mean, Median

How do we need to compare groups by criteria?
We use T-test to compare groups by criteria. And we use matplotlib to distribution comparison. 

You can see how I do them in detail here: https://colab.research.google.com/drive/1ZyT3H1C8TqUXtE99oqKlXoY_WLR1vGZl?usp=sharing

### **📝 SUMMARY**

After We have results. We have some Insights and conclussion as :

### **The First: smokers and non-smokers**

![image](https://github.com/user-attachments/assets/308d6d8f-4553-43bc-a8e2-5926f79e5209)

###### Insights based on measures of central tendency comparison:
Based on the measure :

1. The max tip value is belong smokers group. It's 10USD
2. The average tip value: The smokers is higher than non-smokers

##### General conclusion: The smokers usually give tip higher non-smokers

![image](https://github.com/user-attachments/assets/6883d4f7-b4aa-42c8-9da7-40442d6a0361)

We have TtestResult: 

* statistic=0.09222805186888201
* pvalue=0.9265931522244976

###### Insights based on distribution comparison:
Based on the T-test between smokers and non-smokers, we have the result is pvalue = 0.926 > 0.05. We can conclude that these two customer groups do not have much difference in the amount of money tipped to the restaurant's service staff.

###### General conclusion:
Through the calculation table of min, max, median parameters and the distribution image, we can see that: The average tip amount is 2.9 USD. The highest tip amount is 10 USD. The smokers group give tip more than non_smokers. But there isn't significant difference .Amount tip from 1 USD - 2.5 USD that is amount for restaurant staff receive the most.

### **The second: Female and male**

![image](https://github.com/user-attachments/assets/a920b618-beb7-4270-9958-711a97ef8781)

###### Insights based on measures of central tendency comparison:
Based on the measure :

1. The max tip value is belong male. It's 10USD
2. The average tip value: male is higher than female

##### General conclusion: The male usually give tip higher female

![image](https://github.com/user-attachments/assets/9da4fd16-8dc2-4117-bfeb-940304e7a965)

We have TtestResult: 

* statistic=-1.387859705421269
* pvalue=0.16645623503456755

###### Insights based on distribution comparison:
Based on the T-test between male and female, we have the result that pvalue = 0.16 > 0.05. We can conclude that these two groups of customers do not have much difference in the amount of tips for restaurant's service staff.

###### General conclusion:
Through the table of min, max, average parameters and the distribution image, we see that: The male give tip more than female.But there isn't significant difference.

### **The third: Weekends and Weekdays**

![image](https://github.com/user-attachments/assets/406ec05a-6625-4050-b026-1fbfa9f45a07)

###### Insights based on measures of central tendency comparison:
Based on the measure :

1.   The max tip value is on Weekends. It's 10USD
2.   The average tip value: The weekends is higher than weekdays

###### General conclusion: The weekends usually give tip higher weekdays

![image](https://github.com/user-attachments/assets/644b0257-096d-4b4a-85f2-6f96919b77e1)

We have TtestResult: 

* statistic=1.1028993019409794
* pvalue=0.27154326510606286

###### Insights based on distribution comparison:
Based on the T-test between weekends and weekdays, we have the result that pvalue = 0.27 > 0.05. We can conclude that these two groups of customers do not have much difference in the amount of tips for restaurant's service staff.

###### General conclusion:
Through the table of min, max, average parameters and the distribution image, we see that: The weekend's customers usually tip more than weekday's customers.But there isn't significant difference.

### **The last: Dinner and lunch**

![image](https://github.com/user-attachments/assets/77a66cfc-69d0-4322-afcb-c7e561baab40)

###### Insights based on measures of central tendency comparison:
Based on the measure :

1.   The max tip value is dinner. It's 10USD
2.   The average tip value: The dinner is higher than lunch

###### General conclusion: The dinner usually give tip higher lunch

![image](https://github.com/user-attachments/assets/906982ec-c192-46fe-8504-af2787e31344)

We have TtestResult: 

* statistic=1.9062569301202392
* pvalue=0.05780153475171558

###### Insights based on distribution comparison:
Based on the T-test between dinner and lunch, we have the result that pvalue = 0.0578 > 0.05. We can conclude that these two groups of customers do not have much difference in the amount of tips for restaurant's service staff.

###### General conclusion:
Through the table of min, max, average parameters and the distribution image, we see that: The dinner group usually tip more than lunch group. But there isn't significant difference.

You can see how I do them in detail here: https://colab.research.google.com/drive/1ZyT3H1C8TqUXtE99oqKlXoY_WLR1vGZl?usp=sharing
   
## **📝 CONCLUSION**     

###### **After processing and calculating the data, we have the highlights:**

* The smokers tip more than non-smokers
* The male tip more than female
* The weekends have tip more than weekdays
* The dinner group have tip more than lunch group

**However, there aren't any much difference between the relationship variables and the tips given.**







