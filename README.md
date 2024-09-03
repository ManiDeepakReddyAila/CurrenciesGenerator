# CurrenciesGenerator

CurrenciesGenerator is a powerful tool designed to automate the fetching, processing, and management of currency data. The project leverages APIs to provide real-time currency exchange rates and offers a flexible setup for integrating with various financial applications.

## Tools and Technologies Used

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![AWS](https://img.shields.io/badge/AWS%20CDK-orange?logo=amazon&logoColor=white)

## Table of Contents

- [Technical Approach](#technical-approach)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)

## Technical Approach
The CurrenciesGenerator project utilizes AWS CDK to provision and manage cloud resources, focusing on efficient data storage and cataloging for currency data processing. The technical approach involves the following key components:

1. **AWS CDK (Cloud Development Kit)**:
   - AWS CDK is used to define and provision cloud infrastructure in code using Python.
   - Both Level 1 (L1) and Level 2 (L2) constructs are employed for resource creation and management.

2. **S3 Bucket**:
   - An S3 bucket is used as the primary storage for currency data, allowing for scalable and cost-effective data storage.

3. **AWS Glue Data Catalog**:
   - Glue is used to create a data catalog for managing metadata and making data easily searchable and queryable.
   - **L2 Constructs**: Used for creating databases and tables and S3 buckets, providing a simplified interface for defining these resources.
   - **L1 Constructs**: Used for defining projections, specifically to handle partitioning logic and optimize data organization.

4. **Partitioned Data**:
   - Data is partitioned in the S3 bucket using `year`, `month`, and `date` columns to improve query performance and data management.
   - This partitioning strategy allows for efficient data retrieval, minimizes costs, and enhances overall processing speed.

5. **Infrastructure as Code (IaC)**:
   - The use of AWS CDK for defining infrastructure ensures consistency and repeatability across environments.
   - Changes to the infrastructure are managed through version-controlled code, facilitating easier updates and maintenance.

This approach not only ensures scalable data processing but also leverages AWS’s managed services to reduce operational overhead and enhance the robustness of the solution.

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

