---
title: "class 1"
output: github_document
date: "2023-02-20"
---

```{r, echo = FALSE}
knitr::opts_chunk$set(
  fig.path = "README_figs/README-"
)
```

```{r}
2*3
1+1
3*3
2*2
# tt
## tt
2+3*5
2^3
3*c(4,2,6)
c(3,6,2)*c(3,4,5)
1:100
seq(3,5,0.1)
seq(from=3,to=5,by=0.1)
seq(to=5,from=3,by=0.1)
seq(3,5,length.out=5)
seq(3,5,length=5) #隱藏版，說明沒寫
seq(3,5,,5)
```

## Including Plots

You can also embed plots, for example:

```{r pressure, echo=FALSE}
plot(pressure)
```

## 物件
```{r}
x <- seq(-2*pi,2*pi,length=20)
y <- sin(x)
plot(x,y,pch=16,col="blue",type="b",
     xlab="我是X軸",asp=1)
```

```{r}
rep(3,5) #3被執行5次
rep(c(6,3,2,4),5) #向量(6,3,2,4)被執行5次
rep(c(6,3,2,4),times=3)
rep(c(6,3,2,4),each=3)
rep(c(6,3,2,4),times=c(1,2,3,4))
```
## 1.5
```{r}
rep(c(1,2,3,4,5),times=c(5,4,3,2,1))
```
## 1.6(b)
```{r}
seq(1,20,3)
```
## 1.7
```{r}
rep(LETTERS[c(1,2,3,4,5)],times=c(5,4,3,2,1))
```


## 特殊指令
```{r}
pi
letters #小寫26個字母
letters[]
letters[c(1,3,5)] #3個字母
letters[-c(1,3,5)] #23個字母
LETTERS #大寫26個字母
LETTERS[c(14,20,16,21)]
englet <- c("abcdefghij","klmnopqrst")
englet
substr(englet,c(1,2),c(2,4))
englet
substr(englet,c(1,2),c(2,4)) <- c("A","BC")
englet
substr(englet,c(1,2),c(2,4)) <- c("AB","BCD")
englet
substr(englet,c(1,2),c(2,4)) <- c("AB","BCDE")
englet
```
```{r}
paste(1:12) #paste(c(1:12))
paste("x",1:12,sep="")
paste("x",1:12,sep="+")
paste("x",1:12,sep="+",collapse="...")

```
```{r}
x <- seq(-5,5,0.1)
y <- x^2+2*x-3
#color in R, rgb, #000000 都可以找顏色
plot(x,y,type="l",col="blue")
plot(x,y,type="l",col="#0000FF")
plot(x,y,type="l",col="#0000FF",lwd=2)
plot(x,y,type="l",col="#0000FF40",lwd=10) #加上透明度
points(x,y+1,type="l",col="#FF000040",lwd=10)
```
```{r}
#在R非本體，plot跟points等都要包起來一起執行(就是下面這些無法單獨執行)；若在R本體則可分開、逐步執行
plot(x,y,type="l",col="#0000FF40",lwd=10,main="一元二次方程式",xlab="支出",ylab="效益")
points(x,y+1,type="l",col="#FF000040",lwd=10)
abline(h=seq(-10,30,5),v=seq(-6,6,2),col="#BEBEBE80",lty=2) #abline是背景格線、lty是線條的形式
lines(c(-2,0,2),c(0,10,5),type="b")
text(c(-2,0,2),c(0,10,5),c("A","B","C"))
```
