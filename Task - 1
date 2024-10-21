# Function to calculate average temperature and humidity for each city from the given weather data
def calculate_citywise_average_weather_data(records):
    # Create a dictionary to hold aggregate values and counts for each city
    weather_data = {}

    # Loop through each record in the input
    for record in records:
        city = record['city']  # Get city name from the record
        if city not in weather_data:
            weather_data[city] = {
                'temp_total': 0, 'humidity_total': 0, 
                'temp_count': 0, 'humidity_count': 0
            }

        # Check and add temperature to the total if available
        if 'temperature' in record:
            weather_data[city]['temp_total'] += record['temperature']
            weather_data[city]['temp_count'] += 1

        # Check and add humidity to the total if available
        if 'humidity' in record:
            weather_data[city]['humidity_total'] += record['humidity']
            weather_data[city]['humidity_count'] += 1

    # Calculate and store average temperature and humidity for each city
    citywise_averages = {}
    for city, data in weather_data.items():
        avg_temp = (data['temp_total'] / data['temp_count']) if data['temp_count'] > 0 else None
        avg_humidity = (data['humidity_total'] / data['humidity_count']) if data['humidity_count'] > 0 else None
        citywise_averages[city] = {'average_temperature': avg_temp, 'average_humidity': avg_humidity}

    return citywise_averages

# weather records (Example data)
weather_records = [
    {'city': 'New York', 'temperature': 22, 'humidity': 55},
    {'city': 'New York', 'temperature': 25},
    {'city': 'Los Angeles', 'temperature': 28, 'humidity': 45},
    {'city': 'Los Angeles', 'humidity': 50},
    {'city': 'New York', 'humidity': 60},
    {'city': 'Chicago', 'temperature': 18, 'humidity': 65},
    {'city': 'Chicago', 'temperature': 20},
    {'city': 'San Francisco', 'humidity': 75},
    {'city': 'San Francisco', 'temperature': 19}
]

# Run the function and print the results
print(calculate_citywise_average_weather_data(weather_records))
