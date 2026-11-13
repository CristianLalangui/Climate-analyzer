## 🌦️ Project Design

📊 Climate Analyzer – ClimaPy

ClimaPy is an application developed in Python that allows checking and analyzing meteorological information of any city, also specifying its country. It obtains real-time climate data from a reliable source on the Internet so that users can see the temperature, wind speed, and other aspects of the climate.

**Project differences:**

📁 Creates a data history of different cities.

📊 Generates charts for easy understanding.

📝 Allows documentation and analysis of climate data.



## 🎯 Objectives

The user will have to enter the data through the console, entering the country and the city.

![introducirDatos](imagenesGithub/solicitudDatos.png)



Once this data is requested:

The latitude and longitude will be obtained through a first API.

Then a second API will be called, passing it the obtained latitude and longitude.

With these coordinates, real-time climate information will be obtained.

The obtained data will be stored in an Excel file, which will act as a database with columns for the climate information.

In our case we have chosen **Excel**
![introducirDatos](imagenesGithub/baseDeDatosExcel.png)

The main menu will have 10 options:

![introducirDatos](imagenesGithub/menu.png)

Options 1 and 2 will be used to enter and delete climate records in Excel.

The rest of the options (except 10) will use Pandas to filter data.

The filtered data will be used to build charts with Plotly to compare climate changes.

**Bar chart**
![introducirDatos](imagenesGithub/graficoBarrasIndiviidualesTiempo.png)


**Grouped bar chart**
![introducirDatos](imagenesGithub/graficoBarras.png)


**Radar chart**
![introducirDatos](imagenesGithub/graficoRadial.png)




## 🏗️ Structure and Main Functionality

The main functions of the application allow the user to obtain real-time climate information of a country and city through a graphical interface or console.

The user will be able to check:

**🌡️ Temperature in degrees Celsius (°C)**

**🏔️ Altitude**

**💨 Wind speed**

**🧭 Wind direction:**

North

South

East

West

Southwest

Northwest

**☁️ Weather condition:**

Cloudy

Clear

Raining

Sunny

In addition, they will be able to check:

**🔺 Maximum temperature**

**🌪️ Maximum wind speed**

## 🧩 Project Classes


![introducirDatos](imagenesGithub/estructuraProyecto.png)



There will be four main classes:

**1️⃣ Main Class**

The Main class is in charge of the main operation of the application. It controls user interaction and starts the queries when data is entered into the application.

**2️⃣ ApiClient Class**

The ApiClient class is in charge of making calls to the corresponding APIs to obtain:

Latitude

Longitude

Real-time climate data

**3️⃣ Analisis Class**

The Analisis class is used to filter the data that the user wants to obtain, allowing the information stored in Excel to be processed and preparing the data for its analysis and visualization.

**4️⃣ Interfaz Class**

This Interfaz class is used to process the data that has been stored in Excel, and generate charts with it


## 📰 Flowchart

```
START
↓
Show welcome message
↓
Request country and city
↓
Valid data?
↓           ↓
NO          YES
↓           ↓
Show error  Connect with API
↓
Correct response?
↓         ↓
NO        YES
↓         ↓
Show error    Process data
↓
Show information
↓
Save in history
↓
Generate chart
↓
END
```






