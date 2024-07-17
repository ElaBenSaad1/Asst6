#assignment 6
#question 2
#install.packages("Sleuth3")

#a
library(Sleuth3)
#display data
ex0523
#box plot data
boxplot(Oxygen ~ Bone, data= ex0523)

anova_result <- aov(Oxygen ~ Bone, data = ex0523)

summary(anova_result)

#b
subset_data <- subset(ex0523, Bone %in% c("Bone1", "Bone2"))

subset_data
nrow(subset_data)

#c
overall_mean <- mean(ex0523$Oxygen)
overall_mean
SS_total <- sum((subset_data$Oxygen - overall_mean)^2)
SS_total

#d

SS_within_bone1 <- sum((subset_data$Oxygen[subset_data$Bone == "Bone1"] - overall_mean)^2)
SS_within_bone1
SS_within_bone2 <- sum((subset_data$Oxygen[subset_data$Bone == "Bone2"] - overall_mean)^2)
SS_within_bone2

SS_within_bone1+SS_within_bone2

#e
mean_bone1 <- mean(subset_data$Oxygen[subset_data$Bone == "Bone1"])
mean_bone2 <- mean(subset_data$Oxygen[subset_data$Bone == "Bone2"])

SS_total1 <- sum((subset_data$Oxygen - mean_bone1)^2)
SS_total1
SS_total2 <- sum((subset_data$Oxygen - mean_bone2)^2)
SS_total2


SS_between <- sum( (mean_bone1 - overall_mean)^2 + (mean_bone2 - overall_mean)^2 )
SS_between



#h


