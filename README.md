# CurrenciesGenerator

CurrenciesGenerator is a powerful tool designed to automate the fetching, processing, and management of currency data. The project leverages APIs to provide real-time currency exchange rates and offers a flexible setup for integrating with various financial applications.

## Tools and Technologies Used

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![AWS](https://img.shields.io/badge/AWS%20CDK-orange?logo=amazon&logoColor=white)

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)

## Features

- **Real-Time Data:** Fetches live currency exchange rates using external APIs.
- **Customizable:** Supports multiple base currencies and target symbols to tailor data to your needs.
- **Easy Integration:** Easily integrates with other financial tools and applications.
- **Data Storage:** Configurable options to store data in various formats, such as CSV or databases.
- **Error Handling:** Robust error handling for API calls and data processing.

## Installation

Follow the steps below to set up the project on your local machine.

1. **Clone the repository:**

   ```bash
   git clone https://github.com/PranithaPoosa/CurrenciesGenerator.git
   cd CurrenciesGenerator/cdk
2. **Set up the virtual environment:**
   python3 -m venv .venv
   source .venv/bin/activate
3. **Install required dependencies:**
   pip install -r requirements.txt

## Usage
Once the project is set up, you can start generating currency data using the instructions below:

1. Running the Application:

   Run the main script to fetch and process currency data:
   ```bash
   python currencies_generator.py
2. Viewing results:
   The processed currency data will be saved in the output S3 bucket.

## Project Structure
Here's an overview of the project structure:
```bash
CurrenciesGenerator/
├── cdk/                  # Configuration and deployment scripts
├── currencies_generator.py # Main script
├── requirements.txt      # Python dependencies
└── README.md             # Project documentation

