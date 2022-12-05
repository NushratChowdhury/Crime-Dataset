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
