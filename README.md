This is the documentation of the workflow. <br>
The project focuses on getting real-time updates of weather conditions of different places.

## Data Source
To make this possible we will use a Live Weather API which provides real-time updates in 3 seconds

## Data Ingestion
We will use Azure Databricks and Azure Functions which will both connect to the API and pull the data and send it as an event to Event Hub which is used for streaming millions of events per second.
Event Hub streams the data to the next processing and loading step which in this case we will use Microsoft Fabric

## Event Processing, Loading and Reporting
Microsoft Fabric is a good tool since it has wonderful realtime intelligence features. Using Microsoft Fabric + Azure is the best approach for modern data engineering projects

I'll be creating a workflow pipeline using EventStream which connects to the EventHub and pull the streaming weather data continuously and load them to EventHouse specifically KustoBD database which is ideal for real-time analytics

KustoBD - Loads all the streaming weather data <br>
I'll use Event Stream pipelines to connect to EventHub which pulls the streaming weather data and load it continuously to the database

## Data Reporting
Once the data is loaded to the database, we then build an interactive weather report using PowerBI.<br>
This report will be a real-time dashboard that updates automatically with the latest weather data

## Configuring Alerts
Data Activator - Used to send realtime alerts via email 

## Workflow
Data Source -> Data Ingestion -> Data Streaming -> Event Processing, Loading and Reporting 
