# 🌦 Weather Dashboard using WeatherAPI + Power BI

An interactive and visually appealing dashboard built in *Power BI* to display *real-time weather* and *air quality data* for multiple cities like *Mohali, Dehradun, and Noida. This project integrates **WeatherAPI.com* data using API calls, and transforms it into actionable visual insights including temperature, wind speed, precipitation, and air quality indicators (PM2.5, PM10, CO, NO2, etc.).

---

##  Why WeatherAPI?

[WeatherAPI.com](https://www.weatherapi.com/) is a simple and powerful weather data service that provides:

-  Live weather data  
-  7-day forecast  
-  Historical records  
-  Air Quality Index (AQI)

It returns data in *JSON format, making it easy to process and transform within **Power BI*.

---

##  Prerequisites

-  A free or paid account on [WeatherAPI.com](https://www.weatherapi.com/)  
-  Power BI Desktop installed  
-  Basic understanding of Power BI (data modeling, transformation, visualization)

---

##  Step 1: Get Your WeatherAPI Key

1. Sign up at [WeatherAPI.com](https://www.weatherapi.com/signup.aspx)  
2. Copy your API key from the dashboard  
3. This key is required to authenticate API calls

---

##  Step 2: Build the API URL

Replace YOUR_API_KEY and CITY_NAME in the URL below:

https://api.weatherapi.com/v1/current.json?key=YOUR_API_KEY&q=CITY_NAME

You can use this for multiple cities dynamically by changing the q value.

---

##  Step 3: Connect Power BI to WeatherAPI

1. Open *Power BI Desktop*  
2. Click *Get Data → Web*  
3. Paste your WeatherAPI URL  
4. Click *OK*

---

##  Step 4: Transform the Data

1. Power BI will open the *Power Query Editor*  
2. Expand the current record  
3. Expand nested records like condition and air_quality  
4. Rename columns for clarity  
5. Click *Close & Apply*

---

##  Step 5: Build Your Dashboard

Use the transformed data to add the following visuals:

-  Cards for *temperature, **humidity, **visibility, **wind speed*  
-  Gauges or KPIs for AQI (*PM2.5, **PM10, **NO2, **CO*)  
-  Line charts for *forecasted weather trends*  
-  Info cards for *Sunrise/Sunset, **UV index, and **chance of rain*

---

##  Step 6: Styling & Interactivity

- Use weather icons or custom shapes (e.g., sunny, rainy)  
- Add slicers to select between cities like *Mohali, **Noida*, etc.  
- Customize dark/light themes  
- Add tooltips and hover interactions for user-friendly experience

---

##  Step 7: Adding AQI Indicators with Reusable DAX Measures

To create dynamic AQI indicators, use DAX like:

DAX
AQI_PM25 = SELECTEDVALUE(current_air_quality[pm2_5])
AQI_CO = SELECTEDVALUE(current_air_quality[co])

---

## Technologies Used

- Power BI
- WeatherAPI
- JSON & Web API Integration
- Power Query
- DAX (for calculations and AQI logic)

## Project Status

- Live weather data
- AQI visualizations
- Multi-city dynamic filtering

## Future Enhancements:

- 7-day Forecast APIs
- Weather Alerts integration
- Historical data comparison
