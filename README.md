# Crime-Dataset

# display the contents of Crime_dataset
library(readr)
Crime_dataset <- read_csv("Crime_dataset.csv")
View(Crime_dataset)

# Display the data in the Crime column ()
Crime_NYC$Crime

# Display the data in the Current column ()
Crime_NYC$Current

# Make a histogram of the Current Crime counts                                         
hist(Crime_NYC$Current)

# plot a histogram of the Crime_NYC data with a title, x axis label, and y axis label
hist(Crime_NYC$Current, main = "Crime in NYC", xlab = "Current Crimes", ylab = "Number of days")


#colunm 2
# Display the data in the Prior column ()
Crime_NYC$Prior

# Make a histogram of the Prior Crimes                                         
hist(Crime_NYC$Prior)

# plot a histogram of the Crime_NYC data with a title, x axis label, and y axis label
hist(Crime_NYC$Prior, main = "Crime in NYC", xlab = "Prior Crimes", ylab = "Number of days")



#colunm3
# Display the data in the YTD_Prior column ()
Crime_dataset$YTD_Prior

# Make a histogram of the passenger counts                                         
hist(Crime_NYC$YTD_Prior)

# plot a histogram of the Crime_NYC data with a title, x axis label, and y axis label
hist(Crime_NYC$Prior, main = "Crime in NYC", xlab = "Prior Crimes", ylab = "Number of days")

#colunm4
# Display the data in the YTD_Prior column ()
Crime_NYC$Ratio

# Make a histogram of the passenger counts                                         
hist(Crime_NYC$Ratio)

# plot a histogram of the Crime_NYC data with a title, x axis label, and y axis label
hist(Crime_NYC$Ratio, main = "Crime in NYC", xlab = "Crimes Ratio", ylab = "Number of days")
