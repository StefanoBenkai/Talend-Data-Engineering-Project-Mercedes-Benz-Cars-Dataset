# Talend Data Engineering Project: Mercedes-Benz Cars Dataset

This Data Engineering project focuses on retrieving, cleaning, and visualizing data from a Kaggle dataset containing information about cars. The project involves using Talend Studio for data integration, MySQL for data storage, and Power BI for data visualization. Below, you'll find a detailed description of the project, including how to set it up and replicate the results.

## Project Overview 

The project follows these key steps:

1. **Data Collection:** The initial dataset was sourced from Kaggle, providing information about cars stats.

2. **Data Loading:** The CSV dataset was loaded into a locally hosted MySQL database using Talend Studio. This database was set up to store and manage the Mercedes-Benz car data.

3. **Data Cleaning:** Talend Studio was used to filter the data related to Mercedes-cars and address data quality issues. Some columns contained currency symbols ($) and commas (,) which were removed to ensure data consistency.

4. **Database Setup:** A MySQL database named `mercedes` was created to store the car data. The `car_data` table was defined to accommodate the dataset's structure.

5. **Data Visualization:** A Power BI dashboard was created to visualize specific aspects of Mercedes-Benz cars. Note that the Power BI MSQ connector requires version 8.0.28.

## MySQL Database Setup

To replicate this project, follow these steps to set up the MySQL database and table:

```sql
-- Create the 'mercedes' database
CREATE DATABASE `mercedes` /*!40100 DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci */ /*!80016 DEFAULT ENCRYPTION='N' */;

-- Define the 'car_data' table
CREATE TABLE `car_data` (
  `Make` varchar(255) DEFAULT NULL,
  `Model` varchar(255) DEFAULT NULL,
  `Type` varchar(255) DEFAULT NULL,
  `Origin` varchar(255) DEFAULT NULL,
  `DriveTrain` varchar(255) DEFAULT NULL,
  `MSRP` int DEFAULT NULL,
  `Invoice` int DEFAULT NULL,
  `EngineSize` int DEFAULT NULL,
  `Cylinders` int DEFAULT NULL,
  `Horsepower` int DEFAULT NULL,
  `MPG_City` int DEFAULT NULL,
  `MPG_Highway` int DEFAULT NULL,
  `Weight` int DEFAULT NULL,
  `Wheelbase` int DEFAULT NULL,
  `Length` int DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
```

## Power BI Dashboard

The Power BI dashboard provides insightful visualizations and analytics for the Mercedes-Benz cars dataset.

## Getting Started

To replicate this project or explore the code:

1. Clone this GitHub repository.
2. Set up a MySQL database as described above.
3. Use Talend Studio to load and clean the dataset, ensuring consistent data quality.
4. Create a Power BI dashboard to visualize the data.
5. Customize the dashboard and analysis based on your preferences and requirements.

## Project Structure

The project repository is structured as follows:

- `data/`: Contains cars stats dataset in CSV format.
- `talend/`: Includes Talend Studio job files for data loading and cleaning.
- `powerbi/`: Contains the Power BI project file for the dashboard.
- `README.md`: This project documentation.

Feel free to explore and modify the project to suit your needs and gain insights from the Mercedes-Benz cars dataset. If you have any questions or encounter issues, please don't hesitate to reach out for assistance.

**Note:** Ensure you have the necessary software tools (Talend Studio, MySQL, and Power BI) installed and configured to execute this project successfully.