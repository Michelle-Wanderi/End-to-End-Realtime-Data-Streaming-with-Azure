This is the documentation of the workflow of this project
The project focuses on getting real-time updates of weather conditions of different places.

#Data Source
To make this possible we will use a Live Weather API which provides real-time updates in 3 seconds

##Data Ingestion
We will use Azure Databricks and Azure Functions which will both connect to the API and pull the data and send it as an event to Event Hub which is used for streaming millions of events per second.
Event Hub streams the data to the next processing and loading step which in this case we will use Microsoft Fabric

Event Processing, Loading and Reporting
Microsoft Fabric is a good tool since it has wonderful realtime intelligence features. Using Microsoft Fabric + Azure is the best approach for modern data engineering projects

I'll be creating a workflow pipeline using EventStream which connects to the EventHub and pull the streaming weather data continuously and load them to EventHouse specifically KustoBD database which is ideal for real-time analytics
