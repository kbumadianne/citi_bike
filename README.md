# Data Preparation
Due to the size of the files for this project I chose to use a data clean and combination method in python.
The data for this project can be found on the Citi Bike public website : https://citibikenyc.com/system-data
I focused on years 2022 and 2023 to see if there were differences year over year.

File Handling:

The script looks for all CSV files in a specified directory (folder_path).
It uses a regular expression to extract the month and year from the filenames (formatted as YYYYMM-citibike-tripdata_XXXXX.csv).

Data Processing:
Each CSV file is loaded into a DataFrame.
A 'Month' and 'Year' column is added based on the extracted values from the filename.
If any CSV file is empty, it is skipped.

Combining Data:
All processed DataFrames are concatenated into a single combined DataFrame.
The final combined data is saved to 2022_combined_file.csv and 2023_combined_file.csv.

Quarterly Data Splitting:
The combined data is further filtered by quarters (Q1, Q2, Q3, Q4) based on the 'Month' column.
Each quarter’s data is saved as a separate CSV file (e.g., Q1_2022_data.csv).

Key Output Files:
The quarterly data files were then used to import Q2 for 2023 and 2022 into Tableau for further analysis.
