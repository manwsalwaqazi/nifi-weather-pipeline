# nifi-weather-pipeline
Automated data flow for fetching weather data from an API, transforming it, and storing it in MongoDB Atlas using Apache NiFi.


# NiFi Weather Data Pipeline 🌦️

This repository contains an **Apache NiFi flow** that fetches live weather data from an API, transforms it, and stores it in MongoDB.

---

## 1. NiFi Installation

1. Download the latest stable version of NiFi from: [https://nifi.apache.org/download.html](https://nifi.apache.org/download.html)  
2. Extract the zip/tar file to a folder, e.g., `C:\nifi-1.26.0`  
3. Start NiFi:
   - **Windows:** `bin\nifi.cmd start`  
   - **Linux/Mac:** `bin/nifi.sh start`  
4. Open NiFi in your browser: `http://localhost:8443/nifi`  
5. Log in using the **generated username and password** from `logs/nifi-app.log` (admin password).

---

## 2. Importing the Weather Flow

1. On the NiFi root canvas, **drag and drop a new Process Group** from the toolbar.  
2. In the **Name** option, click **Browse**, then select the file: LiveWeatherDataFlowAutomation.json
3. NiFi will import all processors and controller services.

---

## 3. Enabling Controller Services

1. Right click on Process Group and click **Enter Group**.
2. Enable all services by clicking the ⚡ icon (MongoDB, JsonTreeReader, JsonRecordSetWriter, etc.).
3. Update credentials if needed (MongoDB URI or API key).

---

## 4. Running the Flow

1. Select all processors inside the group (Ctrl + A).
2. Click the ▶️ **Start** button.
3. Monitor the flow using:
   - FlowFile counts on connections
   - **Data Provenance** tab
   - MongoDB collection to verify data insertion

---

## 5. Requirements

- Apache NiFi 1.26 or newer  
- MongoDB running locally or remotely  
- Valid weather API key

---

Created by **Man W Salwa**
