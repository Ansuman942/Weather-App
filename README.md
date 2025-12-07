# Weather App


## Weather Information Application – ServiceNow Studio

A dynamic weather application built on the ServiceNow Platform that fetches real-time weather details based on user input.
This project demonstrates REST API integration, automation, and client–server scripting in ServiceNow.

## Features

 - Enter a location and fetch weather data automatically
 - Auto-populates:
 - State
 - Country
 - Local Time
 - Temperature
 - Wind Speed
 - Current Condition
 - Uses server-side processing for secure API calls
 - Clean UI and interactive form experience

## ServiceNow Concepts Used

- Custom Table (u_weather_information)
- Business Rules (server-side API call logic)
- Script Includes (API integration module)
- REST API Integration
- Client Scripts (trigger data fetch on user input)
- UI Policies (optional for form behavior)
- Data Validation
- Form/UI Customization

## Application Structure

 - u_weather_information	  - Stores weather data for each lookup
 - Business Rule	Calls Script - Include to fetch API response
 - Script Include - 	Handles REST call logic & response parsing
 - Client Script -	Sends request to server when location is entered
 - UI Policy -	Optional logic for visibility and UX
   
## External API Used

Response fields extracted:

 - location.name
 - location.country
 - location.localtime
 - current.temp_c / temp_f
 - current.wind_kph
 - current.condition.text

## Fields in the Weather Table

- u_location
- u_state
- u_country
- u_localtime
- u_temperature
- u_windspeed
- u_condition

## What I Learned from This Project

- Using Script Includes for reusable server-side logic
- How to perform REST API calls in ServiceNow
- How Business Rules handle server workflows
- Client–server communication using GlideAjax (if used)
- Data parsing and mapping API responses to table fields
- Designing user-friendly forms in ServiceNow Studio



## How to Test the App

- Open Weather Information System > Weather Lookup
- Enter a location name
- Wait for the form to auto-populate
- Verify fields such as temperature, condition, and local time
- Check logs or watch Script Include execution for debugging
