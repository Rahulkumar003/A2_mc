# Flight Analysis Application

This project is a **Flight Analysis Application** built using **Kotlin** and **Room Database**. It provides functionalities to analyze flight data, including calculating average flight times, delays, and retrieving flight statistics for a specific date range.

## Features

- **Flight Data Storage**: Uses Room Database to store flight information.
- **Flight Statistics**:
  - Average flight time.
  - Average delay.
  - Total flights analyzed within a date range.
- **Flight Data Retrieval**: Fetch flights based on departure and arrival times.
- **Coroutines and Flow**: Utilizes Kotlin Coroutines and Flow for asynchronous data handling.

## Technologies Used

- **Kotlin**: Primary programming language.
- **Room Database**: For local data storage.
- **Coroutines and Flow**: For asynchronous programming.
- **Gradle**: Build system.

## Project Structure

- `FlightModels.kt`: Contains data models for flights, flight statistics, and related entities.
- `FlightDatabase.kt`: Defines the Room database and DAO for accessing flight data.
- `FlightRepository.kt`: Handles data operations and provides an abstraction layer for the database.
- `DateConverter.kt`: Converts `Date` objects to and from timestamps for Room.

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Rahulkumar003/FlightAnalysisApp.git
   ```
2. Open the project in **Android Studio Ladybug Feature Drop | 2024.2.2 Patch 1**.
3. Sync the Gradle files.
4. Build and run the application on an emulator or physical device.

## Key Classes and Files

### `FlightModels.kt`
Defines the data models, including:
- `Flight`: Represents a flight entity stored in the database.
- `FlightStatistics`: Holds calculated statistics for flights.
- `FlightStatusResponse`: Represents the response structure for flight data.

### `FlightDatabase.kt`
- Defines the Room database with the `Flight` entity.
- Includes the `FlightDao` interface for database queries.

### `FlightDao`
Provides methods for:
- Inserting flight data.
- Fetching flights within a date range.
- Calculating average flight time and delay.
- Counting total flights.

### `DateConverter`
Handles conversion between `Date` objects and timestamps for Room compatibility.

## Example Queries

- **Get Flights for a Date Range**:
  ```kotlin
  flightDao.getFlightsForDateRange(startDate, endDate)
  ```
- **Calculate Average Flight Time**:
  ```kotlin
  flightDao.getAverageFlightTime(startDate, endDate)
  ```

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Author

Developed by **Rahulkumar003**. For any queries, feel free to reach out via GitHub.
