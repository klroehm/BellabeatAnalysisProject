After the data is collected, it must be cleaned and processed. These are the general steps I took in Excel:
-Ensure there are is missing or biased data 
-Remove any duplicate entries (Data -> Remove Duplicates)
-Sort entries by date and time (Format -> Sort & Filter -> Sort Oldest to Newest)
-Filter to only show necessary data (Data Validation -> Filter)

Once the data is cleaned and ready, it can be imported to R for further analysis.
In R, the first step is to istall all necessary packages. 
For this project, I used the Tidyverse package (This system contains several packages used for data manipulation, exploration, and visualization) and the Janitor package, which makes cleaning data easier
      install.packages("tidyverse")
      library(tidyverse)
      install.packages("janitor")
      library(janitor)
Then, import all databases needed
      dailyActivity_merged <- read_csv("dailyActivity_merged.csv”)
      hourlySteps_merged <- read_csv("hourlySteps_merged.csv")
      sleepDay_merged <- read_csv("sleepDay_merged.csv")
      hourlyCalories_merged <- read_csv("hourlyCalories_merged.csv") 
 Then, using the janitors package, make all the variable names consistent in one line of code, by leaving only characters and numbers
      clean_names(dailyActivity_merged)
      clean_names(hourlySteps_merged)
      clean_names(sleepDay_merged)
      clean_names(hourlyCalories_merged)
