# ford_gobike_system_data_exploration

**ford_gobike_system_data_exploration** is an effort to wrangle and explore the [Ford GoBike System Data](https://www.fordgobike.com/system-data). This project was done as part of [Udacity's Data Analyst Nanodegree](https://www.udacity.com/course/data-analyst-nanodegree--nd002) program.

The dataset selected was the [Ford GoBike System Data](https://www.fordgobike.com/system-data). The data is from Bay Wheels's trip data and is for public use and is provided according to the Bay Wheels License Agreement. The data is contained within a csv file titled `2017-fordgobike-tripdata.csv` and was downloaded in a zip with the same name. The data consists of rows that represent a bike trip. Each trip is anonymized and includes:

- Trip Duration (seconds)
- Start Time and Date
- End Time and Date
- Start Station ID
- Start Station Name
- Start Station Latitude
- Start Station Longitude
- End Station ID
- End Station Name
- End Station Latitude
- End Station Longitude
- Bike ID
- User Type(Subscriber or Customer - "Subscriber" = Member or "Customer" = Casual)

## Summary of Findings

- The structure of the dataset consists of 519700 rows and 13 columns which are displayed above. Each row in the dataset represents a trip that can be conducted between two user types 'Customer' or 'Subscriber'. The rest of the columns describe the start and end times of those trips as well as the station names and latitude & longitudes.
- It appears that their are way more members or subscribers taking trips than the casual customer. Almost four times the amount more.
- `duration_sec` which I transformed to `duration_min` seems skewed to the right with the averaging being a less than a 20min bike ride
- I did have to transform `duration_sec` to `duration_min` by dividing by 60 to get the minutes. I then had to filter down even further in the graphs due to outliers in the set. There is also way more members than casual customers then I thought there would be.
- As mentioned I did transform the duration in seconds to duration in minutes close the gap on the min and max values and condense the dataset. This way it was a bit easier to graph, read, and understand.
- It appears that Subscribers generate more trips but of shorter lengths compared to Customer who seem to take less trips overall but they tend to take longer trips.
- I do not have time to do this but if I was interested in analyzing usage I code recode the start_time and end_time columns to days and hours of the day to see if there is usage relationships between user_type and duration... I could incorporate those features ID variables (start_station_id, end_station_id, bike_id, name, etc) into a bivariate analysis but I would much rather use them for the multivariate exploration part coming up.

## Key Insights for Presentation

- There seems to be a relationship between day of the week and usage as well as the trend of the usage through the week in relationship to user type. Additionally certain user groups ebb and flow differently depending on if its a weekend vs week day.
- Yes, it appears that the casual customer is the more stable user and has less variability in usage then the member/subscriber user which I would not expect. In fact, I would assume the opposite. The subscriber user is also making up the bulk of the trips through out the week with those mostly being smaller, shorter trips.

Please see the [notebook](https://github.com/Chilliwack/ford_gobike_system_data_exploration) for further details: https://github.com/Chilliwack/ford_gobike_system_data_exploration.ipynb
