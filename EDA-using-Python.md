
# Exploratory Data Analysis of Customer Sales database
**Exploratory Data Analysis (EDA)** is one of the core components of data analytics. It is also the part on which data analysts, data engineers and data scientists spend their majority of the time which makes it extremely important in the field of data analytics. This repository demonstartes some common exploratory data analysis methods and techniques using python. For purpose of illustration the **[Customer Sales database](https://www.kaggle.com/code/umairabbasi6/diwali-sales-eda-and-data-visualization)** dataset has been taken from kaggle since it is one of the ideal dataset for performing **EDA** and taking a step towards the most amazing and interesting field of data analytics.
### DataSet Overview
  + The dataset is taken from **kaggle** and contains details of the **Sales database**.
  + The dataset is not clean and hence data cleaning is carried out. 
 
  
### More Info
__*The main folder contains 9 folders*__.

  + Folders from Analysis1 - Analysis5 contain the **iPython Notebook**, **python scripts** along with the **Plots** for that analysis.
  + Folder for **[shell scripts](ShellScripts)** which automate the creation of files structures and splitting the data as mentioned above.
  + Datapreparation folder contains the **[Datapreparation iPython Script](DataPreparation/DataPreparation.py)** for cleaning of data.
  + CleanData folder contains the clean dataset and subsets of data as per the **[file structure](CleanData/DataForAnalysis)**.
  + RawData folder which contains the **[raw dataset](RawData)**.  <br/>
 
***
### Analysis 1 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[Analysis1.py](Analysis1/Analysis1.py)&emsp;[Analysis1.ipynb](Analysis1/Analysis1.ipynb)&emsp;[Plots](Analysis1/Plots)
+ This analysis gives the distribution of prices of vehicles based on vehicles types.
+ Output before the cleaning the data is shown below in order to highlight the importance of cleaning this dataset.
+ **Histogram** and **KDE** before performing data cleaning.
+ It is clearly visible that the dataset has **many outliers** and **inconsistent data** as year of registration **cannot be more than 2016 and less than 1890**.

![alt text](DataPreparation/Plots/vehicle-distribution.png "Logo Title Text 1")

> Boxplot of prices of vehicles based on the type of vehicles after cleaning the dataset. Based on the vehicle type how the prices vary is depictable from the boxplot. low, 25th, 50th(Median), 75th percentile, high can be estimated from this boxplot.

![alt text](Analysis1/Plots/price-vehicleType-boxplot.png "Logo Title Text 1")
***
### Analysis 2 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[Analysis2.py](Analysis2/Analysis2.py)&emsp;[Analysis2.ipynb](Analysis2/Analysis2.ipynb)&emsp;[Plots](Analysis2/Plots)

+ This analysis gives the number of cars which are available for sale in the entire dataset based on a particular brand. 

![alt text](Analysis2/Plots/brand-vehicleCount.png "Logo Title Text 1")

> Barplot of average price of the vehicles for sale based of the type of the vehicle as well as based on the gearbox of the vehicle.

![alt text](Analysis2/Plots/vehicletype-gearbox-price.png "Logo Title Text 1")
***
### Analysis 3 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[Analysis3.py](Analysis3/Analysis3.py)&emsp;[Analysis3.ipynb](Analysis3/Analysis3.ipynb)&emsp;[Plots](Analysis3/Plots)

+ This analysis gives the average number of price for the vehicles based on the fueltype of the vehicle and also based on the type of the vehicle.

![alt text](Analysis3/Plots/fueltype-vehicleType-price.png "Logo Title Text 1")

> Barplot of average power of the vehicle based of the fueltype of the vehicle and also on the type of the vehicle.

![alt text](Analysis3/Plots/power-vehicleType-fuelType.png "Logo Title Text 1")
***
### Analysis 4 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[Analysis4.py](Analysis4/Analysis4.py)&emsp;[Analysis4.ipynb](Analysis4/Analysis4.ipynb)&emsp;[Plots](Analysis4/Plots)

+ This analysis gives you the average price of the brand of vehicles and their types which are likely to be found in the dataset.

![alt text](Analysis4/Plots/heatmap-price-brand-vehicleType.png "Logo Title Text 1")
***
### Analysis 5 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;[Analysis5.py](Analysis5/Analysis5.py)&emsp;[Analysis5.ipynb](Analysis5/Analysis5.ipynb)&emsp;[Plots](Analysis5/Plots)

+ This analysis gives you the distribution of the total no of days a partiular vehicle has been online for sale before it was purchased. 
+ This is a **dynamic analysis** and can be applied to **any vehicle** by specifying the brand of choice as argument to the python script.
+ To run this file on your terminal type: __*Analysis5.py 'brand'*__  
+ where **'brand'** is the choice of brand vehicle you would like to see analysis about from the column **'brand'** in the dataset.

![alt text](Analysis5/Plots/vehicletype-NoOfDaysOnline.png "Logo Title Text 1")
***
### Conclusion
__*Analysis 1*__

+ Many **outliers** with *registration year greater than 2016 and less than 1890* which are removed to make the dataset ready for analyis.
+ Vehicles with registration year **1990-2016** are available **maximum** for sale. Year **2000** being the **highest** with **24313** vehicles.

__*Analysis 2*__

+ Vehicles of type **SUV** and **Cabrio** are the **most expensive** with **greater than $5000** as compared to **Coupe**, **Bus** etc which are **moderately expensive** in the range of **$2650 to $5000** where as the **least expensive** being **Andere** and **Others** with price **less than $1800** on an *average*.
+ Vehicles of brands **Volkswagen**, **Opel** and **BMW** are the **maximum for sale** in the decreasing order with *Volkswagen being the maximum*.
+ As a general trend vehicles which are **automatic** are the **most expensive** as compared to manual and other unspecified gearbox type.

__*Analysis 3*__

+ **Average prices** of vehicles that are **Hybrid** are **most expensive** as compared to other fuel types like Diesel and Gasoline
+ **SUV** type of vehicles with gearbox type **automatic** has the **maximum power** and **Kleinwagen** with the **least**.

__*Analysis 4*__

+ Vehicles of brand **Audi** and type **SUV** are the **most expensive** of the avialable vehicles for sale.
+ Vehicles of brand **Porsche** and type **Kleinwagen** are the **least expensive** of the available vehicles for sale.

__*Analysis 5*__

+ Based on selected brand of choice, it can be found out what **type of vehicles** in the **selected brand** tend to get **sold quickly online** as compared to others.

***
