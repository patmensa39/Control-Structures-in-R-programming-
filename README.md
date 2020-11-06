# Control-Structures-in-R-programming-
This repository deals with Control structures function which includes if statements, if else statements, nested if statements, Ifelse statements, break, next, repeat, loop and many others.  
---
title: "Control structures"
output:
  pdf_document: default
  html_document: default
  word_document: default
date: "November 2020"
theme: cerulean
---

```{r}
## If statements
philant<-100
if (philant==100) {
  print("Philant like R programing", quote = FALSE)
}
```


```{r}
## if else statements to determine if a person is a teenager.
age<-19
if(age>12) {
  print("I am a teenager", quote = FALSE)
} else {
  print("I am not a teenager", quote = FALSE)
}
```


```{r}
## Nested if statements for my Elorm's score
score<-100
if(score>90) {
  print("Elorm is a briliant student", quote = FALSE)
} else if (score<70) {
  print("Elorm does not study well", quote = FALSE)
} else {
  print("Elorm should be very careful", quote = FALSE)
}
```

```{r}
### Nested if statement to determine if an number is positive or negative.
number<--5
if(number<0) {
  print("The number is a negative number", quote = FALSE)
} else if(number>0) {
  print("The number is a positive number", quote = FALSE)
} else {
  print("The number is zero")
}
```

```{r}
### Ifelse statement to determine odd and even numbers.
philant<- c(100, 9, 2998, 54, 678, 455)
ifelse(philant%%2==0, "even", "odd")
```

```{r}
### Ifelse statement to determine if a number is divisible by 5 from a sequence.
kp<-seq(10,100, by=4)
ifelse(kp%%5==0, "is divsible 5", "is not divisible by 5")
```

```{r}
## Switch statements helps to select a statement.
switch(2,"Ji", "Meng","Loh")
switch(1,"Ji", "Meng","Loh")
switch(3,"Ji", "Meng","Loh")
### this produce NULL
switch(4,"Ji", "Meng","Loh")
### Another way.
switch("first.name", "last.name"= "Mensah", "middle.name"="Senyo", "first.name"="Patrick")
```

```{r}
### For loops 
nash<-c(1:10)
for(val in nash) {
  print(nash)
}

nash<-c(1:10)
for(val in nash) {
  print(val)
}

### For loops to count the number of even numbers 
philant<-c(21,56,378,98,82,11,66, 100, 98,200,222,23)
count<-0
for(val in philant) {
  if(val %% 2==0) count= count+1
}
print(count)

###Another using breaks
philant<-c(1:20)
for(i in philant) {
  if(i==9) {
    break
  }
  print(i)
}
philant<-c(1:20)
for(val in philant) {
  if(val==13) {
    break
  }
  print(val)
}
### Next skip the value in question during when looping
philant<-c(1:20)
for(val in philant) {
  if(val==c(10)) {
    next
  }
  print(val)
}
```

```{r}
### While loop 
nash<-1
while(nash<10) {
  print(nash)
  nash=nash+1
}
```

```{r}
###Repeat loops and stop the on the 20th value.
nash<-1
repeat{
  print(nash)
  nash=nash+1
  if(nash==20) {
    break
  }
}
```

```{r}
### looping over a matrix.
philant<-matrix(1:20, nrow = 5, byrow = TRUE)
for (i in philant) {
  print(i)
}


### looping over a matrix and squaring the result
philant<-matrix(1:20,nrow=5, ncol=4, byrow = FALSE)
for (i in philant) {
  print(i^2)
}
```

```{r}
### Nested loop
philant<-matrix(1:20,nrow=5, ncol=4, byrow = FALSE)
for(row in 1:nrow(philant)) {
  for(col in 1:ncol(philant)) {
    print(philant[row, col])
  }
}

```

```{r} 

philant<-matrix(1:20,nrow=5, ncol=4, byrow = FALSE)
for(row in 1:nrow(philant)) {
  for(col in 1:ncol(philant)) {
    print(paste('Row = ', row, 'and Column = ', col, 'and the value is:', philant[row, col]))
  }
}
```

```{r}
### Finding the factorial of a number.Entering a number
number<- as.integer(readline(prompt = "Enter any number"))
factorial=1
### Figure out if the number is zero, negative, or  positive
if(number<0) {
  print("Daabi,the factorial of negative numbers does not exist", quote = FALSE)
} else if(number==0) {
  print(" 0 factorial is 1", quote = FALSE)
} else {
  for(i in 1:number) {
    factorial=factorial*i
  }
  print(paste("The factorial of ", number , "is", factorial), quote = FALSE)
}
```


```{r} 
### Loops with multiple conditions. 

for(i in 1:10) {
  if(i<3) {
    if(i %in% seq(2,10,2)) {
      print(i)
    }
  }
}
```

```{r}
### Loop with multiple statements in a single line. same as chunk above. 
for(i in 1:20) {
  if(i<20& i %in% seq(2,100,2)) {
    print(i)
  }
}
```


```{r}
### Using repeat loop to find the numbers divisible by 2 less than 15 and squaring the numbers.
patrick<-1:20
for(i in patrick)
if(i<15 & i%%2==0){
  print(i^2)
} 
```
