# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Partial Least Squares Path Modeling ((PLS-PM) Use plspm With (In) R Software
install.packages("plspm")
library("plspm")
plspm = read.csv("https://raw.githubusercontent.com/timbulwidodostp/plspm/main/plspm/plspm.csv",sep = ";")
# Estimation Partial Least Squares Path Modeling ((PLS-PM) Use plspm With (In) R Software
IMAG <- c(0,0,0,0,0,0)
EXPE <- c(1,0,0,0,0,0)
QUAL <- c(0,1,0,0,0,0)
VAL  <- c(0,1,1,0,0,0)
SAT  <- c(1,1,1,1,0,0) 
LOY  <- c(1,0,0,0,1,0)
sat.mat <- rbind(IMAG, EXPE, QUAL, VAL, SAT, LOY)
sat.sets <- list(1:5,6:10,11:15,16:19,20:23,24:27)
sat.mod <- rep("A",6)
plspm <- plspm(plspm, sat.mat, sat.sets, sat.mod, scheme="centroid", scaled=FALSE)
summary(plspm)
# Partial Least Squares Path Modeling ((PLS-PM) Use plspm With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished