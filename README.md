# Harvard Artifact Explorer

This project provides an interactive web application to explore artifacts from the Harvard Art Museums. It uses a modern data stack to extract data from the official Harvard Art Museums API, store it in a MySQL database, and present it through a user-friendly Streamlit interface.

### ✨ Features
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

```git clone https://github.com/Maryam-Feroz/Harvard-Artifact-Explorer-Final-Project-.git
cd Harvard-Artifact-Explorer-Final-Project-```
