"R/RStudio Beginner Workshop"




INSTALL

If you don't have R and RStudio, you can follow the link and install both.

https://posit.co/download/rstudio-desktop/ 


INTRODUCTION TO BASICS

Arithmetic with R
```{r}

#An addition
10 + 7

# A subtraction
10 - 5 

# A multiplication
3 * 5

 # A division
(5 + 5) / 2 

# Exponentiation
2^5

# Modulo
28 %% 6

```


Variables

```{r}

x <- 17
x

```


BASIC DATA TYPES IN R

Numerics & Integers

* Decimal values like 1.7 are called numerics.

* Whole numbers like 13 are called integers. Integers are also numerics.

```{r}

a <- 1.7
b <- 13

```

```{r}

#We can check the data type with class() function
class(a)
class(b)

```

Logical Operations

```{r}

z <- a > b
z

```

```{r}

class(z)

```

Character

* Text (or string) values are called characters.

```{r}

k <- "BMG Lab"
k

```

```{r}

x <- as.character(x)
x

```

```{r}

fname = "John"; lname = "Doe"
paste(fname, lname)

```

```{r}
?paste
```


VECTORS

Vectors are one-dimension arrays that can hold numeric data, character data, or logical data. In other words, a vector is a simple tool to store data.

In R, you create a vector with the combine function c(). You place the vector elements separated by a comma between the parentheses.

```{r}

#creating vectors
vector1 <- c(7, 13, 17, 20)
vector2 <- c("a", "b", "c", "d")
vector3 <- c(10, 20, 30, 40)

```

You can find out the lenght of vectors with lenght() funtion.

```{r}
length(vector1)
```

```{r}

#combining vectors
c(vector1, vector2)

```

Arithmetics with vectors

```{r}
vector1
vector3
```

```{r}
#multiply by 3
vector1 * 3
```

```{r}
vector1 - 5
```

```{r}
vector1 + vector3
```

```{r}
2 * (vector1 + vector3) / 7

#using round()
round(2 * (vector1 + vector3) / 7, 2)

```


Vector Indexing

In R, indexing starts from 1 unlike python.

```{r}

d <- c("A", "B", "C", "D", "E", "F")

d[2]

```

```{r}
#Selecting values between indexes
d[2:4]
```

```{r}
#Selecting values with multiple indexes
d[c(1,3,5)]

d[c(4,2,5)]
```

```{r}
#Selecting values with logical indexing
d[c(FALSE, FALSE, TRUE, TRUE, FALSE, TRUE)]
```

```{r}
#Removing a value from the vector
d[-3]
```

Naming A Vector

```{r}
y <- c("Duygu", "KEREMİTÇİ")
y
```

```{r}
names(y) <- c("Firt", "Last")
y
```


MATRIX

In R, a matrix is a collection of elements of the same data type (numeric, character, or logical) arranged into a fixed number of rows and columns.

You can construct a matrix in R with the matrix() function.

```{r}
A <- matrix(c(5, 26, 13, 6, 7, 17),#the data
            nrow =2,#number of rows
            ncol = 3,#the number of columns
            byrow = TRUE) #fill matrix by row
A
```

Naming A Matrix

```{r}
rownames(A) <- c("x","y")
colnames(A) <- c("a","b","c")
A
```

Selecting Values with Index

```{r}
#A[row, column]
A[1, 3] 
```

```{r}
#1st row
A[1, ]

#2nd column
A[,2]
```

Transpose The Matrix

```{r}
#Creating a new matrix 
B <- matrix(c(2,4,6,8,10,12),
            nrow = 3,
            ncol = 2)
B
```

```{r}
t(B)
```


Combining The Matrices

```{r}
#Adding a column or multiple columns
cbind(A, t(B))
```

```{r}
#Adding a row or multiple rows
rbind(A, t(B))
```

Arithmetic With Matrices

```{r}
A * 2
```

```{r}
A + t(B)
```

DATA FRAMES

In basic terms, a data frame is a two-dimensional array-like structure where:

* Each column represents a variable and can contain data of different types (numeric, character, factor, etc.).
* Each row represents an observation or a record.

```{r}

name <- c("John", "Josh", "Mark")
age <- c(32, 29, 25)
n <- c(FALSE, TRUE, FALSE)

#using data.frame() funtion to create a data frame
df <- data.frame(name, age, n)
df

```

```{r}
mtcars
```

```{r}
head(mtcars)
```

```{r}
tail(mtcars)
```

Investigate the structure of data frame

```{r}
str(mtcars)
```


Selecting Values From Data Frame

```{r}
#using indexes
#df[row, column]
mtcars[13,7]
```

```{r}
#using names of columns and rows
mtcars["Merc 450SL", "qsec"]
```

```{r}
##Getting the all values in a row with name
mtcars["Merc 450SL", ]
```


```{r}
#Getting the all values in a column with name
mtcars[["qsec"]]
```
```{r}
mtcars$qsec
```

```{r}
#Select first 5 values of a column
mtcars[1:5, "qsec"]
```

Sorting your data frame

```{r}
#using order() to sort the df
mtcars[order(mtcars$qsec), ]
```

```{r}
#using order() to sort the df - decreasing
mtcars[order(mtcars$qsec, decreasing = TRUE), ]
```

Subsetting The Data Frame

```{r}
#using which() funtion to subset data frame
index <- which(mtcars$qsec > 17) #this gives us indexes for given condition

mtcars[index,]
```














