# Prediction-using-supervised-ML
url<-"https://raw.githubusercontent.com/Adipersonalworks/Random/master/student_scores%20-%20student_scores.csv"
data<-read.csv(url)
summary(data)
head(data)
str(data)
any(is.na(data))
x<-data$Hours
y<-data$Scores
plot(x~y)
abline(lm(x~y))
model<-lm(y~x)
score.prediction<-predict(model,data)
print(score.prediction)
obj<-data.frame(x=9.25)
prediction<-predict(model,obj)
print(prediction)
