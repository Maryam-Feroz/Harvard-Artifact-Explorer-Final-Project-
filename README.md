# Harvard Artifact Explorer

This project provides an interactive web application to explore artifacts from the Harvard Art Museums. It uses a modern data stack to extract data from the official Harvard Art Museums API, store it in a MySQL database, and present it through a user-friendly Streamlit interface.

### Features
* **ETL Pipeline**: Fetches data for various artifact classifications (Paintings, Sculpture, etc.) and loads it into a structured MySQL database.
* **Secure Credential Management**: Uses Streamlit's native `secrets.toml` file to securely manage database credentials and API keys.
* **Interactive Interface**: A Streamlit web app that allows you to trigger the data pipeline and view the data.
* **Data Querying**: Run pre-defined SQL queries directly from the web interface to analyze the artifact data.
* **Live Data Exploration**: View the contents of the database tables in real-time.


### Getting Started

Follow these steps to set up and run the application on your local machine.

#### Prerequisites
You need to have the following software installed:
* **Python 3.10+**
* **MySQL Database** (and the MySQL service running)

#### Step 1: Clone the Repository
Clone this repository to your local machine.

``` git clone https://github.com/Maryam-Feroz/Harvard-Artifact-Explorer-Final-Project-.git
cd Harvard-Artifact-Explorer-Final-Project-  
```
#### Step 2: Install Dependencies
Navigate to the project directory and install the necessary Python libraries.

``` pip install -r requirements.txt ```

If you don't have a requirements.txt file, create one with the following content:
```
streamlit
mysql-connector-python
pandas
sqlalchemy
requests
```
#### Step 3: Configure Your Secrets
To connect to the database and the Harvard API, you need to set up a secrets.toml file.

1) Create a new folder named .streamlit in the project's root directory.

2) Inside the .streamlit folder, create a new file named secrets.toml.

3) Copy and paste the following content into secrets.toml, and replace the placeholder values with your own MySQL credentials.
```
[mysql]
host="127.0.0.1"
user="root"
password="your_mysql_password"
database="harvard_artifacts"

[harvard]
api_key="your_harvard_api_key"
```
#### Step 4: Run the Application
From the project's root directory, start the Streamlit application using your terminal.
```nstreamlit run harvard3.py ```
The application will automatically open in your default web browser at ``` http://localhost:8501. ```

#### Usage
* Fetch & Insert Data: Use the sidebar to select an artifact classification. Click the "Fetch & Insert Data" button to call the Harvard API and populate your local MySQL database.

* View Database Tables: Select a table from the dropdown menu and click "Show Table Data" to view the raw data stored for the selected artifact classification.

* Query & Visualization: Choose one of the pre-built queries from the dropdown list. Click "Run Query" to execute the query and see the results displayed in a table. Some queries require you to enter an ID or a department name before running.
