# InfluxDB_with_Milvus
A tutorial on how to vectorize your time series data from InfluxDB to use in a similarity search with Milvus.

The purpose of this notebook is to highlight how to convert your time series data into vectors to be inserted in a vector database like Milvus.

Imaginary Use Case: Imagine you're developing a platform that offers real-time traffic monitoring and pattern recognition to improve city traffic management. Specifically, you want to create a solution that identifies when traffic conditions are operating anomalously and determine the type traffic anomaly that is present like an accident, traffic, or construction. fluxDB would store the time-series data from the sensors, while Milvus would store the image data and manage the search indices for complex queries. In this scenario you could continuously monitor traffic data like average speed and vehicle count in InfluxDB. You might also be collecting traffic image data in Milvus. When your traffic conditions fall outside of norm, you send this anomalous traffic data to Milvus. Then you perform a similarity search in Milvus to identify what type of anomaly it is.

## Requirements and Run
Have [Jupyter Notebooks](https://jupyter.org/) and [Docker](https://www.docker.com/) installed on your machine. 

Run a stanalone instance of Milvuz with:
```
 docker-compose -f milvus-standalone-docker-compose.yml up
```

Run the Jupyter Notebook with: 
```
jupyter notebook
```
And visit `http://localhost:8888/` to run the notebook. 

