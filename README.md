Description:

This Python script calculates the average temperature and humidity for multiple cities based on weather data records. It handles missing data gracefully, ensuring robust and accurate results.

Features:
Aggregates city-wise weather data.
Handles missing temperature and humidity data.
Outputs average temperature and humidity for each city.
How to Run:
Ensure Python 3.x is installed.
Place the script in your working directory.
Run the script using:
bash :

python weather_aggregation.py

Example Input:

python :
weather_records = [
    {'city': 'New York', 'temperature': 22, 'humidity': 55},
    {'city': 'Los Angeles', 'temperature': 28, 'humidity': 45},
]

Example Output:

python :

{
    'New York': {'average_temperature': 22.0, 'average_humidity': 55.0},
    'Los Angeles': {'average_temperature': 28.0, 'average_humidity': 45.0}
}

Contact:
For queries, email: 220283@kit.ac.in
