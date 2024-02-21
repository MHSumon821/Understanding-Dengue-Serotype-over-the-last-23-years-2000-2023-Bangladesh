# Understanding-Dengue-Serotype-over-the-last-23-years-2000-2023-Bangladesh


library(ggplot2)
library(reshape2)


colors=c("blue","orange","brown","pink")
year<-c("2000","2002","2013","2014","2015","2016","2017","2018","2019",
        "2020","2021","2022","2023")
regions<-c("DENV1","DENV2","DENV3","DENV4")
values<-matrix(c(15.6,0,14.3,40,50,24.4,9,26,8.2,0,0,0,0,
                 6.8,0,85.7,60,50,75.6,41,41,0,0,0,0,56,
                 68.5,100,0,0,0,0,31,33,91.8,100,100,89,44,
                 9.1,0,0,0,0,0,0,0,0,0,0,11,0),
               nrow = 4,ncol = 13,byrow = TRUE)
dev.new(width=60,height=40,unit="cm")

barplot(values,main = "Dengue serotype analysis over the past 23 years",
        names.arg = year,las=2,
        xlab="Distribution by year",ylab="Number of cases for each serotype(%)",
        col=colors,ylim = c(0,110))

legend("top",regions,cex=1,fill = colors, horiz=TRUE)
ligands_long <- melt(ligands, id.vars = "Ligand")

