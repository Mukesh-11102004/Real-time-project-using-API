# Real-time-project-using-API

# Power BI Real-Time Weather Dashboard Using OpenWeatherMap API

## Overview
This project creates a real-time weather dashboard in Power BI using data from the OpenWeatherMap API. The dashboard displays live weather updates, including temperature, humidity, wind speed, and other key metrics.

## Prerequisites
Before starting, ensure you have:
- **Power BI Desktop** installed
- An **OpenWeatherMap API Key** (Get it from [OpenWeatherMap](https://home.openweathermap.org/api_keys))
- An active **internet connection**

## Steps to Create the Dashboard

### Step 1: Get API Key
1. Sign up on [OpenWeatherMap](https://home.openweathermap.org/).
2. Navigate to the **API Keys** section.
3. Copy the API key for later use.

### Step 2: Fetch Weather Data in Power BI
1. Open **Power BI Desktop**.
2. Click **Get Data** → **Web**.
3. Enter the following API URL:
   ```
   https://api.openweathermap.org/data/2.5/weather?q=Hyderabad&appid=YOUR_API_KEY&units=metric
   ```
   (Replace `YOUR_API_KEY` with your actual API key.)
4. Click **OK**.
5. If prompted, select **Anonymous Authentication** and click **Connect**.

### Step 3: Transform Data in Power Query
1. Expand the JSON fields:
   - `main` (temperature, humidity, pressure)
   - `weather` (description)
   - `wind` (speed, direction)
   - `clouds` (percentage)
2. Rename the columns for clarity.
3. Click **Close & Apply** to load data into Power BI.

### Step 4: Build the Dashboard
1. **Cards** for key metrics (Temperature, Humidity, Wind Speed).
2. **Line Chart** for temperature trends.
3. **Map Visualization** using latitude & longitude.
4. Customize colors and formatting.

### Step 5: Enable Auto-Refresh
1. Go to **Data Source Settings** → **Edit Permissions**.
2. Set **Refresh Frequency** (e.g., every 30 minutes).
3. (Optional) Use **Power Automate** to push live data.

### Step 6: Publish and Share
1. Click **Publish** → Choose a workspace.
2. Set up **Scheduled Refresh** in Power BI Service.
3. Share the dashboard link.

## Troubleshooting
- **401 Unauthorized Error?**
  - Check if your API key is correct and active.
- **Data not loading?**
  - Ensure you selected **Anonymous Authentication**.
- **Old data showing?**
  - Refresh the dataset manually or schedule auto-refresh.

## Next Steps
- Add **multiple city weather data** dynamically.
- Integrate **forecast data** from OpenWeatherMap.
- Embed the dashboard into a website.

## Conclusion
This Power BI dashboard provides real-time weather insights using OpenWeatherMap API. With further improvements, you can enhance it to display forecasts, historical trends, and more!

