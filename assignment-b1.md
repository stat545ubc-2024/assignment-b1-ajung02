# Assignment B1 - Creating Functions

The function that I am wanting to create is one that will take a file
(either a CSV, Excel, or TXT file) and input it into a data frame.

## Exercise 1

``` r
load_file_to_df <- function(file_path) {
  # Check that the file exists
  if (!file.exists(file_path)) {
    stop("The file does not exist at the specified path.")
  }
  
  # Get the file extension
  file_extension <- tools::file_ext(file_path)
  
  # Load the file based on the extension
  if (file_extension == "csv") {
    df <- read_csv(file_path)
  } else if (file_extension == "txt") {
    df <- read_tsv(file_path) # Assuming tab-separated for .txt
  } else if (file_extension %in% c("xlsx", "xls")) {
    df <- read_excel(file_path)
  } else {
    stop("Unsupported file type. Please provide a CSV, Excel (.xlsx or .xls), or TXT file.")
  }
  
  return(df)
}
```

## Exercise 2

``` r
#' Load a File into a Data Frame
#'
#' This function reads a file (CSV, Excel, or TXT) and loads it into a data frame. The function automatically detects the file type based on the file extension.
#'
#' @param file_path A string representing the path to the file. The file extension should be `.csv`, `.xlsx`, `.xls`, or `.txt`.
#'
#' @return A data frame containing the contents of the file.
#'
#' @examples
#' # Load a CSV file
#' df_csv <- load_file_to_df("data/sample.csv")
#'
#' # Load an Excel file
#' df_excel <- load_file_to_df("data/sample.xlsx")
#'
#' # Load a TXT file
#' df_txt <- load_file_to_df("data/sample.txt")
#'
#' @export
```

## Exercise 3

## Exercise 4
