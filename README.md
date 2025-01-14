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

# Data Analysis

Tableau Public Report : https://public.tableau.com/app/profile/kelsie.bumadianne/viz/citi_bike_17366166405620/CitiBike?publish=yes

Due to the size of the files, I focused my analysis on the months of May and June in years 2022 and 2023.  The data analyzed was over 13m total rides on a Citi Bike.
First off, the analysis shows that there is growth in rides from 2022 to 2023.
To further narrow down the data, I chose to analyze the top 20 stations and patterns between years.
There are two dashboards, one for each year, which display the top 20 stations on a map and display the size and color of the station by number of rides.  
The dashboard also shows a chart with each station name and number of rides, color coded by electric or classic bike.
Lastly the dashboard shows the number of rides per day of the month by electric or classic bike.

The first phenomenon was that in the 2023 Dashboard it appears that the  #1 station, W 21 St & 6 Ave, grew larger than the year prior.  However, looking at the station and years in combination the number of rides out of that station remained similar to 2022.  The reason it looked larger was because the West St & Chambers St station had a large reduction of rides year over year.
Looking at the daily rides from West St & Chambers St by month and year it appears that there is a small gap in 2023 May and the maximum rides for each month are lower than the corresponding months in 2022.

The second phenomenon is when looking at the hours of the day, there are peaks at 8am and 5pm that most likely tie with the work commute.  There is also a steady increase from 10am to 5pm indicating that riders are using Citi Bikes not only to commute to work, but also commute to other destinations during the day and work hours. 
Digging deeper into the second phenomenon, looking at the top 20 stations, the top two stations have peak hours of 6pm.  This could indicate that there is an extended rush hour after work lets out or additional reasons that these stations have peak traffic an hour later than the average of the stations.



