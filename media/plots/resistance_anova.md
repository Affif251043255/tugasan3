model <- aov(PartResistance ~ Machine, data = X002..3.)
summary(model)
ggplot(X002..3., aes(x=as.factor(Machine), y=PartResistance)) + geom_boxplot()
