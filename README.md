[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/s4oIzs8K)
# Assignment B1 - Stat 545B
## Allison Jung

### Exercise 1: 
- In this exercise, I created a function that reads a file (CSV, Excel, or TXT) and loads it into a data frame. The function automatically detects the file type based on the file extension, ensuring flexible inputs and no reliance on pre-selected “magic numbers.” The function is designed to be reusable for future data analysis tasks.

### Exercise 2: 
- I documented the function using roxygen2 tags. The documentation includes a title, a brief description of the function’s purpose, detailed descriptions of the parameters using the @param tag, and a description of the output using the @return tag.

### Exercise 3: 
- The function’s usage is demonstrated with 5 examples, showcasing different file types being loaded into a data frame. Code chunk options were used to show expected behavior and possible errors.

### Exercise 4: 
- Formal tests were written using the 'testthat' package to ensure the function works as intended. The tests included various inputs such as files with no missing values, files with missing values, and files of different lengths. All tests passed successfully.
