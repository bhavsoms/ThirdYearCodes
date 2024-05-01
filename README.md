# R_Programming
**1. Introduction to R Programming and Installation of RStudio**

R is a powerful and widely used programming language for statistical computing and data analysis. It provides a rich set of libraries and packages for various tasks, making it a valuable tool for researchers, data scientists, and analysts.

**RStudio:**

RStudio is a free and open-source integrated development environment (IDE) specifically designed for R. It offers a user-friendly interface with code editing, console output, data visualization tools, and package management capabilities.

**Installation Steps:**

1. **Download R:** Visit the official R website ([https://www.r-project.org/](https://www.r-project.org/)) and download the appropriate installer for your operating system. Run the installer and follow the on-screen instructions.
2. **Download RStudio:** Go to [https://posit.co/download/rstudio-desktop/](https://posit.co/download/rstudio-desktop/) and download the RStudio installer for your operating system. Run the installer and follow the on-screen instructions.

**2. Arithmetic and Logical Operators and Basic Functions**

**Arithmetic Operators:**

* `+`: Addition
* `-`: Subtraction
* `*`: Multiplication
* `/`: Division (real division)
* `%%`: Integer division (remainder)
* `^`: Exponentiation

**Logical Operators:**

* `<`: Less than
* `>`: Greater than
* `<=`: Less than or equal to
* `>=`: Greater than or equal to
* `==`: Equal to
* `!=`: Not equal to

**Basic Function:**

Here's a simple function that calculates the area of a rectangle:

```R
rectangle_area <- function(width, height) {
  return(width * height)
}

# Example usage:
area <- rectangle_area(5, 3)
cat("Area of rectangle:", area, "\n")
```

**3. Atomic Classes: Numeric, Character, and Factors**

**Numeric:** Numbers (integers and floating-point)

```R
x <- 10  # Integer
y <- 3.14  # Double precision floating-point
```

**Character:** Text strings

```R
name <- "Alice"
message <- "Hello, world!"
```

**Factors:** Categorical variables with defined levels

```R
gender <- factor(c("Male", "Female", "NA"))
color <- factor(c("Red", "Green", "Blue"), levels = c("Blue", "Red", "Green"))
```

**Logical:** Boolean values (TRUE or FALSE)

```R
is_sunny <- TRUE
is_weekend <- FALSE
```

**4. Atomic Classes: Lists and Missing Values**

**Lists:** Ordered collections of elements of different types (numeric, character, etc.)

```R
data <- list(name = "Bob", age = 30, hobbies = c("Reading", "Hiking"))
```

**Missing Values:** Represented by `NA` (Not Available)

```R
income <- c(50000, NA, 72000)
```

**5. Loading and Reading Data from Subfolders**

```R
# Set working directory to the folder containing subfolders (modify as needed)
setwd("/path/to/your/data/folder")

# Function to read data from a subfolder
read_data <- function(filename) {
  # Construct file path
  filepath <- paste0("subfolder/", filename)

  # Read data using appropriate function (e.g., read.csv(), read.table())
  data <- read.csv(filepath)
  return(data)
}

# Example usage:
my_data <- read_data("my_data.csv")
```

**6. Matrix-Vector Multiplication (2 Loops)**

```R
matrix_vector_multiply <- function(matrix_A, vector_a, vector_b) {
  # Check dimensions compatibility
  if (nrow(matrix_A) != nrow(vector_a) || ncol(matrix_A) != 1) {
    stop("Incompatible dimensions for matrix and vectors!")
  }

  # Result vectors for Ab and Aa
  Ab <- rep(NA, nrow(matrix_A))
  Aa <- rep(NA, ncol(matrix_A))

  # Outer loop for rows of matrix and elements of vector_a
  for (i in 1:nrow(matrix_A)) {
    # Inner loop for columns of matrix (vector multiplication)
    for (j in 1:ncol(matrix_A