# Cafe_Data_Hygiene_Example
This is an example project that involves cleaning a dirty dataset and turning into a presentable and usable dataset hypothetical cafe.
The following summarizes the entire project briefly. For more information, check out the files listed.

## Initial State
The dataset initially had 8 columns and 10,000 rows. It had missing values and error values like “ERROR” and “UNKNOWN”. Every column in the dataset 
had the exact same type, which was “string”. The “Transaction ID” column was the only one with no missing values in it. The dataset was overall rather broken and messy
and would be hard for a company to use properly, especially for analysis or accurate tracking for records.

*The original dataset:*
<img width="1885" height="217" alt="Screenshot 2026-09-30 151955" src="https://github.com/user-attachments/assets/28dad5f3-ce22-4c09-8bc6-6438621847fe" />


## Fixes performed
The column types and names were tidied to be easier processed for computers. Whitespace was removed throughout the dataset. The dataset had it's missing values analyzed and replaced using special calculations: by analyzing the data that was present, the missing data could be inferred, which was used to fill most of the missing values. Other categorical columns were filled using proportional imputation, a technique that fills missing values in based on the proportions of the existing values. This helped repair a large portion of the data, as some columns reach nearly 40% missing value rates - much too high to be ignored

*A generated bar graph counting the amount of missing values per column. These were all fixed.*
<img width="616" height="450" alt="missing_count_plot_cafe" src="https://github.com/user-attachments/assets/6dddb5db-1fa3-4869-8db3-806773547e45" />

Outliers were detected and flagged. A clean version of the csv was provided alongside a new excel table with the data also provided.

## Reports and generated assets

An in-depth report of the work was provided in the form of an audit log, which explains every action performed on the dataset and why. The actual python code itself was provided in a jupyter notebook, which also contains a novice friendly guide for properly viewing and running the code.

Charts on the missing data and an initial profiling report were also provided to help visualize and understand the process of cleaning the dataset. 

All of these assets are linked below. Check the notebooks/ or outputs/ directories in the rest of the repository to see more. The best asset to look at for an overview of everything (other than this one) is the audit log, which is in the outputs directory.

## Key visualizations

A catalogue of all visualization made during the cleaning process:

<img width="616" height="450" alt="missing_count_plot_cafe" src="https://github.com/user-attachments/assets/6dddb5db-1fa3-4869-8db3-806773547e45" />

<img width="2068" height="967" alt="Fake_Cafe_Business_matrix" src="https://github.com/user-attachments/assets/0dca6014-c1ab-4be3-a70d-da9ba60946d5" />

<img width="1637" height="1109" alt="Fake_Cafe_Business_heatmap" src="https://github.com/user-attachments/assets/c3da755e-b378-47e2-bc26-b9483a28589e" />


## Tools used
Python was the language used. The main libraries used were:
pandas, numpy, plotly, openpyxl, ydata-profiling, ipywidgets, missingno
The work was done in a jupyter notebook file in VScode.

## Insights and reflection

I think it would have been beneficial to take out the dirty columns as separate variables so I could have used them for analysis and double checking as I went through the process of cleaning the dataset. 

I could have quantified my claim of the dataset being MCAR by calculating stats about the missing values and them putting them against each other in the same way that the heatmap does, only this way would give me an actual number instead of me saying it based on judgement.

I also could have done more checks across the notebook as I was working to double check whether I was doing everything right. This could have helped me catch some problems earlier that I was working through with my analysis and clean up.

## Acknowledgments and Licenses

Original dataset comes from Ahmed Mohamed on Kaggle: https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training 

License: CC BY-SA 4.0: https://creativecommons.org/licenses/by-sa/4.0/
