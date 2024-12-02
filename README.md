### 📊 **Air Quality Dashboard - 2024**  

📜 **Project Overview**  
The **Air Quality Dashboard** is an interactive data visualization project developed using Power BI. It provides detailed insights into air quality metrics across cities, empowering users to monitor pollution levels, track trends, and make informed decisions to promote environmental sustainability.  

✨ **Objective**  
The primary objectives of this project are:  
1. To analyze and monitor air pollution trends across cities.  
2. To identify the most and least polluted regions for targeted actions.  
3. To support data-driven environmental policy-making and public awareness campaigns.  

🔍 **Key Insights and Features**  

#### 1. **Key Metrics**  
- **Average CO**: 2.25  
- **Average NO**: 17.57  
- **Average SO₂**: 14.53  
- **Average PM2.5**: 67.45  

#### 2. **Top 3 Polluted Cities**  
- **Ahmedabad**: Average AQI ~ 450  
- **Delhi**: Average AQI ~ 400  
- **Patna**: Average AQI ~ 350  

#### 3. **Least Polluted Cities**  
- **Coimbatore**: Average AQI ~ 73.02  
- **Shillong**: Average AQI ~ 53.80  
- **Aizawl**: Average AQI ~ 34.77  

#### 4. **AQI Trend Overview**  
- Long-term trend analysis reveals an overall improvement in air quality between 2016 and 2030.  

#### 5. **Geographic Insights**  
- Area-wise AQI distribution is visualized using an interactive map to highlight pollution hotspots.  


📊 **Dashboard Features**  

| Insight                  | Visualization Type       | Purpose                                               |  
|--------------------------|--------------------------|-------------------------------------------------------|  
| Average Pollutant Levels | KPI Tiles                | Displays summary statistics for CO, NO, SO₂, PM2.5.  |  
| Top Polluted Cities      | Bar Chart               | Highlights cities with the highest AQI levels.       |  
| Least Polluted Cities    | Bar Chart               | Shows cities with the lowest AQI levels.            |  
| AQI Trends Over Time     | Line Chart              | Visualizes trends in AQI across years.              |  
| Geographic Distribution  | Map Chart               | Identifies high and low AQI regions.                |  


🛠️ **Tools and Technologies Used**  
- **Power BI**: For creating interactive dashboards and visualizations.  
- **DAX (Data Analysis Expressions)**: For calculating key measures like averages, trends, and moving averages.  
- **Data Source**: Air quality data processed and stored in CSV format.  


📂 **How to Use the Dashboard**  
**Download the Repository:** Clone or download this repository to access the Power BI file.
**Open in Power BI Desktop:** Load the .pbix file to explore the interactive dashboard.
**Interact with Visuals** Use slicers and filters to explore city-wise AQI, pollutant breakdowns, and time-series trends.  

📊 **Dashboard Preview**
![Dashboard Screenshot](https://github.com/JanviDhonde/Powerbi-AirQuality-Dashboard/blob/main/AirQuality%20Dashboard.png)  

📈 **Key DAX Measures**  

- **Average PM2.5**  
  ```DAX  
  AveragePM25 = AVERAGE(city_day[PM2.5])  
  ```  

- **AQI Trend (Moving Average)**  
  ```DAX  
  MovingAverageAQI =  
      AVERAGEX(  
          DATESINPERIOD(  
              city_day[Date],  
              LASTDATE(city_day[Date]),  
              -12,  
              MONTH  
          ),  
          city_day[AQI]  
      )  
  ```    

🌟 **Why This Project Matters**  
This project emphasizes the importance of leveraging data to understand and combat environmental challenges. By presenting air quality data in a user-friendly manner, it:  
- Facilitates monitoring of pollution hotspots.  
- Supports strategic interventions for improving air quality.  
- Promotes awareness and accountability for a sustainable future.  

⭐ **Feedback**  
If this project inspires you, please ⭐ the repository and share your feedback to help us improve further! 😊  
