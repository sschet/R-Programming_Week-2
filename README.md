# R-Programming_Week-2
This is the week 2 programming assignment from the Coursera R Programming course in the Data Science Specialization from Johns Hopkins. This assignment is done in Python instead of R.

## Introduction

For this first programming assignment you will write three functions that are meant to interact with the dataset that accompanies this assignment. The dataset is contained in a zip file **specdata.zip** that you can download from the Coursera web site. 

## Data

The zip file containing the data can be downloaded here:

[specdata.zip](https://d396qusza40orc.cloudfront.net/rprog%2Fdata%2Fspecdata.zip) (2.4MB)

The zip file contains 332 comma-separated-value (CSV) files containing pollution monitoring data for fine particulate matter (PM) air pollution at 332 locations in the United States. Each file contains data from a single monitor and the ID number for each monitor is contained in the file name. For example, data for monitor 200 is contained in the file "200.csv". Each file contains three variables:

- Date: the date of the observation in YYYY-MM-DD format (year-month-day)
- sulfate: the level of sulfate PM in the air on that date (measured in micrograms per cubic meter)
- nitrate: the level of nitrate PM in the air on that date (measured in micrograms per cubic meter)

For this programming assignment you will need to unzip this file and create the directory 'specdata'. Once you have unzipped the zip file, do not make any modifications to the files in the 'specdata' directory. In each file you'll notice that there are many days where either sulfate or nitrate (or both) are missing (coded as NA). This is common with air pollution monitoring data in the United States.

###### Part 1

Write a function named 'pollutantmean' that calculates the mean of a pollutant (sulfate or nitrate) across a specified list of monitors. The function 'pollutantmean' takes three arguments: 'directory', 'pollutant', and 'id'. Given a vector monitor ID numbers, 'pollutantmean' reads that monitors' particulate matter data from the directory specified in the 'directory' argument and returns the mean of the pollutant across all of the monitors, ignoring any missing values coded as NA.

You can see some example output from the 'pollutantmean' function below. The function that you write should be able to match this output. Please save your code to a file named pollutantmean.R.

[pollutantmean-demo.html](https://d18ky98rnyall9.cloudfront.net/_3b0da118473bfa0845efddcbe29cc336_pollutantmean-demo.html?Expires=1616371200&Signature=G06VfnHg8YaCby3Rr1kk-p1u9vJMKE4O39nkvSTfLjrhVUHuQn~v0RICes3QcPUQaYPdUqgQKfyyhHu~-Hxo5Kk1LBXc1dU32KfgFOyfujCLNWfbFuZLw1G84nStXItO9oNsSd90IZ7Gg6TCjHNiGFcaGmcya~EMlT8jW~KXT1Q_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

###### Part 2

Write a function that reads a directory full of files and reports the number of completely observed cases in each data file. The function should return a data frame where the first column is the name of the file and the second column is the number of complete cases.

You can see some example output from this function below. The function that you write should be able to match this output. Please save your code to a file named complete.R.

[complete-demo.html](https://d18ky98rnyall9.cloudfront.net/_3b0da118473bfa0845efddcbe29cc336_complete-demo.html?Expires=1616371200&Signature=fxsAjZ4zAB1VNgN6IiloWg0OjyO4QqIq9tJtBoHCjJlKct996n7YO7~D4KKTEJtN0pErB2U5TScGfQRFoyHR0xRsf5SN0U-FZUE3PKKOn1-LRU1gcXm84MvZ-GOUMwPcnf9q5hzsZ3G4cEniWqcbjvJ8hW0t2Z8~Z5dZKOMTrWk_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

###### Part 3

Write a function that takes a directory of data files and a threshold for complete cases and calculates the correlation between sulfate and nitrate for monitor locations where the number of completely observed cases (on all variables) is greater than the threshold. The function should return a vector of correlations for the monitors that meet the threshold requirement. If no monitors meet the threshold requirement, then the function should return a numeric vector of length 0.

For this function you will need to use the 'cor' function in R which calculates the correlation between two vectors. Please read the help page for this function via '?cor' and make sure that you know how to use it.

You can see some example output from this function below. The function that you write should be able to approximately match this output. Note that because of how R rounds and presents floating point numbers, the output you generate may differ slightly from the example output. Please save your code to a file named corr.R.

[corr-demo.html](https://d18ky98rnyall9.cloudfront.net/_e92e575b8e62dcb1e3a086d2ff0d5a1e_corr-demo.html?Expires=1616371200&Signature=Mlq1ZiRf3xUbkj7MU~CB~u2ZkX3hfh6d3hVYTRwZbv9CNjvYVHc~4P63AwKeIlWDvjeBtuuHhFqmjuiC4wofwBZmscNiDCFjbfC69ZQa2Usi0~8UDbtst5eSg0GLkonOKzZU18KpLxOYc8kv2mGVypjhpIx6vaO8AGDHbKjS1Mg_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
