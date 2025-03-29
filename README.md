# ADF Pipeline: Dynamics 365 to Snowflake

This repository contains an Azure Data Factory (ADF) pipeline setup that transfers data from **Dynamics 365 (Dataverse)** to **Snowflake**. The pipeline extracts data from Dynamics 365, processes it, and loads it into Snowflake for analytics.

## Project Structure

The project is structured as follows:

```plaintext
adf-d365-snowflake-pipeline/
├── ADF/
│   ├── pipelines/
│   │   └── Dynamics365ToSnowflakePipeline.json
│   ├── datasets/
│   │   ├── Dynamics365Dataset.json
│   │   └── SnowflakeDataset.json
│   ├── linkedServices/
│   │   ├── Dynamics365LinkedService.json
│   │   └── SnowflakeLinkedService.json
│   ├── triggers/
│   │   └── DailyTrigger.json
│   └── parameters/
│       └── PipelineParameters.json
└── README.md

Explanation of Folder Structure:

    pipelines/:

        Contains the JSON pipeline file, such as Dynamics365ToSnowflakePipeline.json. This file will define the logic, activities, and flow of the data transfer between Dynamics 365 and Snowflake.

    datasets/:

        Stores Dataset JSON files:

            Dynamics365Dataset.json: Defines the dataset pointing to your Dynamics 365 (Dataverse) data.

            SnowflakeDataset.json: Defines the dataset for Snowflake where the data will be transferred.

    linkedServices/:

        Stores Linked Services JSON files:

            Dynamics365LinkedService.json: Defines the connection to your Dynamics 365 (Dataverse).

            SnowflakeLinkedService.json: Defines the connection to Snowflake.

    triggers/:

        Stores Trigger JSON files, such as the daily trigger to schedule the pipeline.

    parameters/:

        Contains any parameterized JSON files for pipeline variables or configuration (e.g., file paths, table names, etc.).

    README.md:

        A README file to explain the purpose of this repository, setup instructions, and how to deploy the pipeline.


## Files Description

1. **`Dynamics365ToSnowflakePipeline.json`**: Defines the pipeline that moves data from Dynamics 365 to Snowflake.
2. **`Dynamics365Dataset.json`**: Dataset for retrieving data from Dynamics 365.
3. **`SnowflakeDataset.json`**: Dataset for writing data into Snowflake.
4. **`Dynamics365LinkedService.json`**: Linked service configuration for Dynamics 365 (Dataverse).
5. **`SnowflakeLinkedService.json`**: Linked service configuration for Snowflake.
6. **`DailyTrigger.json`**: Defines a scheduled trigger to run the pipeline every day at midnight.
7. **`PipelineParameters.json`**: Defines parameters that can be used within the pipeline for dynamic configuration.

## Setup Instructions

1. Clone the repository to your local environment:

2. Navigate to the `ADF` folder:

3. Edit and populate the necessary files using `nano` or your preferred editor.

4. Follow Azure Data Factory deployment steps to import these JSON files and configure the pipeline.
