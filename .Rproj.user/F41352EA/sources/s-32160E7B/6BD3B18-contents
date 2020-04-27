library(plotly)
data<-read.csv("coldata.csv",header=TRUE)
attach(data)
data2<-table(Subclass,Interventions)
data3<-data.frame(data2)
subclassCount<-data3[,3]
falseSubclass<-subclassCount[2:25]
trueSubclass<-subclassCount[27:50]
subclass<-unique(data3[,1])
subclass<-subclass[subclass!=""]
data4<-data.frame(subclass,falseSubclass,trueSubclass)
fig <- plot_ly(data4, x = ~subclass, y = ~falseSubclass, type = 'bar', name = 'FALSE')
fig <- fig %>% add_trace(y = ~trueSubclass, name = 'TRUE')
fig <- fig %>% layout(yaxis = list(title = 'Interventions'), barmode = 'stack')
data5<-table(Decade,Interventions)
data6<-data.frame(data5)
decadeCount<-data6[,3]
decadeFalse<-decadeCount[2:18]
decadeTrue<-decadeCount[20:36]
decade<-unique(data6[,1])
decade<-decade[decade!=""]
fig2<-plot_ly(data6, x = ~decade, y = ~decadeFalse, type = 'bar', name = 'FALSE')
fig2<- fig2%>% add_trace(y = ~decadeTrue, name = 'TRUE')
fig2<-fig2%>% layout(yaxis = list(title = 'Interventions'), barmode = 'stack')

# updatemenus<-list(
#   list(active=-1,
#        type= 'buttons',
#        buttons = list(
#          list(
#            label="Subclass",
#            method = "update",
#            args = list(list(visible = c(FALSE, TRUE)),
#                    list(title = "Subclass"))),
#          list(
#            label="Date",
#            method = "update",
#            args = list(list(visible = c(FALSE, TRUE)),
#           list(title = "Date")))) 
#        )
#   )
#        
# chi<-cbind(falseSubclass,trueSubclass)
# chisq.test(chi)
# chi2<-cbind(decadeFalse,decadeTrue)
# chisq.test(chi2)
