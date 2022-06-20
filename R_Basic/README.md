#  <p align="center"> 😸😸 R Crush Course 😸😸
## R Basic 
### Basic Data Type 
* Basic Arithmetic 
  * Addition ` 1+2 `
  * Subtraction  ` 9-2 `
  * Division ` 30/2 `
  * Exponents ` 3^2 `
  * Modulo ` 9 %% 2 `

* Variables, we can use the ` <- ` character to assign a variable

* Data Types
  * Numerics ` n <- 89.2 `
  Decimal (floating point values) are part of the numeric class in R
  * Integers ` i <- 9 `
  Natural (whole) numbers are known as integers and are also part of the numeric class
  * Logical 
  ` t <- TRUE `  
  ` f <- FALSE `
  Boolean values (True and False) are part of the logical class. In R these are written in All Caps
  * Characters  ` char <- "Hello World!" `
  Text/string values are known as characters in R. We use quotation marks to create a text character string
  
### Vector
Vectors are one of the key data structures in R. A vector is a 1 dimensional array that can hold character, numeric, or logical data elements.
We can create a vector by using the combine function ` c() ` To use the function, we pass in the elements we want in the array, with each individual element separated by a comma. We can't mix data types of the elements in an array, R will convert the other elements in the array to force everything to be of the same data type.
```R
  # Using c() to create a vector of numeric elements
nvec <- c(3,2,1,4)
class(nvec)
'numeric'
  # Vector of characters
cvec <- c('I', 'N', 'D', 'O', 'N', 'E', 'S', 'I', 'A' )
class(cvec)
'character'
  # Vector of logical
lvec <- c(TRUE,FALSE)
class(lvec)
'logical'
```
* Basics arithmetic with vectors and operations, will occur on an element by element basis, for example:
```R
v1 <- c(1,2,3)
v2 <- c(5,6,7)

v1+v2  # Adding Vectors
6 8 10

v1-v1  # Subtracting Vectors 
0 0 0

v1*v2 # Multiplying Vectors
5 12 21

v1/v2  # Dividing Vectors
0.2 0.333333333333333 0.428571428571429
```
We can also check for things like the standard deviation, variance, maximum element, minimum element, product of elements:
```R
v <- c(12,45,100,2)

sd(v)  # Standard Deviation
44.1691823182937

var(v)  #Variance
1950.91666666667

max(v)  # Maximum Element
100

min(v)  # Minimum Element
2

prod(v1)  # Product of elements
6
```
* Comparison Operators
```R
v1 <- c(1,2,3)
v2 <- c(10,20,30)
v1 < v2   # Greater Than, Element by element comparisons for two vectors
TRUE TRUE TRUE

6 >= 5   # Greater Than or Equal to
TRUE

2 <= 2   # Less Than and Less than or Equal To
TRUE

5 != 5   # Not Equal
FALSE

v <- c(1,2,3,4,5)  
v == 3     #  Equal
FALSE FALSE TRUE FALSE FALSE
```
* Vector Indexing and Slicing
```R
v1 <- c(100,200,300)
v2 <- c('a','b','c')
v1[2]   # Grab second element
200

v1[c(1,2)]   # Grab multiple items from a vector
100 200

v <- c(1,2,3,4,5,6,7,8,9,10)
v[2:4]  # Slicing
2 3 4
```

### R Matrices
* Basic Matrices
A matrix will allow us to have a 2-dimensional data structure which contains elements consisting of the same data type. To create a matrix, we use the ` matrix() ` function. We can pass in a vector into the matrix:
```R
 v <- 1:10 
 v 
 1 2 3 4 5 6 7 8 9 10
 
 matrix(v)
 ```

| 	1 |	
| :---: |
|  2	|	
| 	3 |
| 	4	|
| 	5	|	
| 	6	|	
| 7	 |	
| 	8	|	
| 	9	|	
| 10 |

 ```R 
 matrix(v,nrow=2)
 ```
 |  1 | 2 | 3 | 4 | 5 | 
 | :---:|:---: |:---:|:----:| :-----: |
 | 2  | 7 | 8 | 9 | 10 | 
 
 * Creating Matrices from Vectors

 We can combine vectors to later input them into a matrix. For example imagine the following vectors below of stock prices:
 
 ```R
 # not real prices
goog <- c(450,451,452,445,468)
msft <- c(230,231,232,236,228)
stocks <- c(goog,msft)
stock.matrix <- matrix(stocks,byrow=TRUE,nrow=2)
 stock.matrix
 ```
 |  450 | 451 | 452 | 445 | 468 | 
 | :---:|:---: |:---:|:----:| :-----: |
 | 230  |231 | 232 | 326 | 228 | 
 
 * Naming Matrices

 Now that we have our matrix, it would be nice to name the rows and columns for reference. We can do this similarly to the `names()` function for vectors, but in this case we define `colnames()` and `rownames()`. So let's name our stock matrix:
 ```R
days <- c('Mon','Tue','Wed','Thu','Fri')
st.names <- c('GOOG','MSFT')
 
colnames(stock.matrix) <- days
rownames(stock.matrix) <- st.names
 
stock.matrix
```
 
|  |Mon | Tue | Wed | Thu | Fri |
| :---:  | :---:|:---: |:---:|:----:| :-----: |
| GOOG  |  450 | 451 | 452 | 445 | 468 | 
|MSFT | 230  |231 | 232 | 326 | 228 |

 
 
 ### ✨ Contribution

Contributions, issues, and feature requests are welcome!

To contribute, see the GitHub documentation on **[creating a pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)**.

### 👏 Support

Give a ⭐️ if you like this project!
___________________________________

<p>&copy; 2022 Haolia</p>
