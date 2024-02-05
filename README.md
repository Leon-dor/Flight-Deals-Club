# Flight-Deals-Club
This code is designed to search for flight data and update a Google Sheets document with the data.

DataManager class: This class is responsible for interacting with the Google Sheets document via the Sheety API.
It fetches the data from the Google Sheets document (get_destination_data method) and updates the IATA codes for each city in the document (update_destination_codes method).

FlightData class: This class is a simple data class that holds information about a flight, including price, origin and destination cities and airports, and departure and return dates.

FlightSearch class: This class is responsible for interacting with the Tequila API to get flight data.
It can get the IATA code for a city (get_destination_code method) and check for flights between two cities within a certain date range (check_flights method).

The main part of the script first creates instances of DataManager, FlightSearch, and NotificationManager.
It then fetches the data from the Google Sheets document and updates the IATA codes if necessary.
It then checks for flights for each destination in the Google Sheets document from tomorrow to six months from today.
If a flight is found, it sends a notification.
