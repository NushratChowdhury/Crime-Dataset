#Milstone 4 - Single variable distribution plots


# display the contents of Crime_dataset
library(readr)
Crime_NYC1 <- read_csv("Crime_NYC1.csv")
View(Crime_NYC1)

#Milestone 4 Single variable distribution plots...................
#Column 1
# Display the data in the Crime column ()
Crime_NYC1$Crime

# plot a barplot of the Crime_NYC data with a title, x axis label, and y axis label
barplot(table(Crime_NYC1$Crime), main  = "Crime in NYC", ylab = "Frequency", xlab = "Types of crimes" ,las =2 ,cex.name= 0.5 ,col = "pink",  border = "darkorange" , space= c(0.5,0.5) , ylim =c(0 , 100))

#column 2
# Display the data in the Current column ()
Crime_NYC1$Current

# plot a histogram of the Crime_NYC data with a title, x axis label, and y axis label
barplot(table(Crime_NYC1$Current), main = "Crimes in year 2021", xlab = "Crime types", ylab = "Ratio",col = "blue"  , border = "darkorange",space= c(0.5,0.5) , ylim =c(0 , 25))
 
#column 3
# Display the data in the prior column ()
Crime_NYC1$Prior

# plot a histogram of the Crime_NYC data with a title, x axis label, and y axis label
barplot(table(Crime_NYC1$Prior), main = "Crimes in year 2021", xlab = "Crime types", ylab = "Ratio",col = "green"  , border = "darkorange" , space= c(0.5,0.5), ylim =c(0 , 25))


#colunm4
# Display the data in the ElevenYr column (2010)
Crime_NYC1$ElevenYr

# plot a histogram of the Crime_NYC data with a title, x axis label, and y axis label
barplot(table(Crime_NYC1$ElevenYr), main = "Crimes in year 2010", xlab = "Crime types", ylab = "Ratio", col = "orange"  , border = "red", ylim =c(0 , 40))

#Milestone 5 Missing data and outliers.
#Milestone 6 Measures of center and spread.

#Compute the mean of the Current column
mean(Crime_NYC1$Current)
#Compute the mean of the ElevenYr column
mean(Crime_NYC1$ElevenYr)

# compute the median of the Current column
median(Crime_NYC1$Current)
# compute the median of the ElevenYr column
median(Crime_NYC1$ElevenYr)

# Compute the sample variance of the data in the Current column
var(Crime_NYC1$Current)
# Compute the sample variance of the data in the Prior column
var(Crime_NYC1$ElevenYr)

# Compute the sample standard deviation of the Current column data
sd(Crime_NYC1$Current)
# Compute the sample standard deviation of the Prior column data
sd(Crime_NYC1$Prior)

#Milstone 7 Scatterplots and correlation
# Scatter plot of the number of Current crime vs. number of prior crime
plot(Crime_NYC1$Current ~ Crime_NYC1$ElevenYr, data = Crime_NYC1,
     xlab = "Crime_NYC1$Current",
     ylab = "Crime_NYC1$ElevenYr",
     main = "Crimes in 2021 vs Crimes in 2010",
     pch  = 20,
     cex  = 2,
     col  = "PURPLE")

# Scatter plot of the number of Current crime vs. number of prior crime 
# same as previous plot but x axis is labeled by the years (from the data)
plot(Crime_NYC1$Current, Crime_NYC1$ElevenYr,  main = "Crimes in 2021 vs Crimes in 2010", type = "l", col = "purple")

#Milestone 8 Confidence interval...............................................
#95% CI so a = 1-0.95 = 0.05 and a/2 = 0.025
#find z value
qnorm(0.975)
#Find 95% confidence interval for the mean of year 2021
#Lower limit
(mean(Crime_NYC1$Current)-sqrt(var(Crime_NYC1$Current))/sqrt(276))*qnorm(0.975)
#Upper limit
(mean(Crime_NYC1$Current)+sqrt(var(Crime_NYC1$Current))/sqrt(276))*qnorm(0.975)
#vs sample mean 20.62319

#Find 95% confidence interval for the mean of year 2010
#Lower limit
(mean(Crime_NYC1$ElevenYr)-sqrt(var(Crime_NYC1$Current))/sqrt(276))*qnorm(0.975)
#Upper limit
(mean(Crime_NYC1$ElevenYr)+sqrt(var(Crime_NYC1$Current))/sqrt(276))*qnorm(0.975)


