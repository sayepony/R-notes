# R-notes
notes for R 
############################
we gave an example first 
************************
```r
set.seed(1)
n1<-rnorm(10000)
n2<-abs(n1)*50
n3<-matrix(n2,ncol=100)
n4<-round(rowMeans(n3))
hist(n4%%7)
*****************************
seems that data n1>n2>n3>n4> draw a picture hist
we know that magrittr has 4 basic functions 
1.%>% 2.%T>% 3. 4.
we changed the exmaple as 
set.seed(1)
rnorm(1000) %>%
abs%>% `*` (50) %>%   #符号必须用`x`带入，上面两个符号，且数字要用（）扩出来#
matrix(ncol=100) %>%
rowMeans %>% round %>%
`%%`(7) %>% hist #可以直接连接为，下一步，做完一件事情的下一步#
