# ELK Earthquake Monitoring Project (Python Backend)

This project utilizes the ELK stack (Elasticsearch, Logstash, Kibana) along with Flask for the backend server and React for the frontend to display and filter earthquakes that occurred during the last month. The earthquake data is sourced from the [United States Geological Survey (USGS)](https://earthquake.usgs.gov/).

## Technologies Used:

- [Elasticsearch](https://www.elastic.co/elasticsearch/): A distributed, RESTful search and analytics engine, used to store and search earthquake data efficiently.

- [React](https://reactjs.org/): A JavaScript library for building user interfaces, utilized for the frontend to create a dynamic and interactive earthquake monitoring dashboard.

- [Flask](https://flask.palletsprojects.com/): A lightweight WSGI web application framework in Python, used for the backend server logic and handling HTTP requests.

- [Axios](https://axios-http.com/): A promise-based HTTP client for the browser and Node.js, used to make HTTP requests to the USGS API to fetch earthquake data.

## Project Description:

This project aims to provide a user-friendly interface to visualize and filter earthquakes that occurred in the last month. Users can filter earthquakes based on various parameters such as magnitude, location, date, etc., to gain insights into seismic activity.

The workflow of the project is as follows:

1. **Data Collection**: Axios is used to fetch earthquake data from the USGS API.

2. **Data Storage**: Elasticsearch is employed to store the fetched earthquake data efficiently.

3. **Backend**: Flask is utilized to create API endpoints for handling requests from the frontend. These endpoints interact with Elasticsearch to fetch earthquake data based on user filters and serve it to the frontend.

4. **Frontend**: React is used to build the frontend interface, where users can interact with the earthquake data. Users can view earthquakes on a map, filter them based on different criteria, and visualize them in various ways.

5. **Deployment**: The ELK stack components (Elasticsearch, Logstash, Kibana) are deployed and configured to store, process, and visualize the earthquake data. The Flask backend and React frontend are also deployed to serve the application to users.

## Setup Instructions:

1. Clone this repository.
2. Install dependencies for frontend and backend:
    ```bash
    cd client
    npm install
    cd ../server
    pip install -r requirements.txt
    ```
3. Start Elasticsearch, Kibana, and Logstash. Refer to the respective documentation for installation and setup.
4. Start the Flask backend:
    ```bash
    python app.py
    ```
5. Start the React frontend:
    ```bash
    cd client
    npm start
    ```
6. Access the application at `http://localhost:3000` in your web browser.
