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

📂 Explanation of Folder Structure
🛠 pipelines/

    Contains the JSON pipeline file:

        Dynamics365ToSnowflakePipeline.json → Defines the logic, activities, and flow of the data transfer between Dynamics 365 and Snowflake.

📄 datasets/

    Stores Dataset JSON files:

        Dynamics365Dataset.json → Defines the dataset pointing to your Dynamics 365 (Dataverse) data.

        SnowflakeDataset.json → Defines the dataset for Snowflake where the data will be transferred.

🔗 linkedServices/

    Stores Linked Services JSON files:

        Dynamics365LinkedService.json → Defines the connection to your Dynamics 365 (Dataverse).

        SnowflakeLinkedService.json → Defines the connection to Snowflake.

⏰ triggers/

    Stores Trigger JSON files:

        DailyTrigger.json → Defines a scheduled trigger to run the pipeline every day at midnight.

⚙️ parameters/

    Contains any parameterized JSON files for pipeline variables or configuration:

        Examples: file paths, table names, and dynamic settings.

📖 README.md

    Documentation file explaining:

        The purpose of the repository.

        Setup instructions for configuring the pipeline.

        Steps for deployment in Azure Data Factory.

## 📂 Files Description

1. **`Dynamics365ToSnowflakePipeline.json`**  
   Defines the pipeline that moves data from Dynamics 365 to Snowflake.

2. **`Dynamics365Dataset.json`**  
   Dataset for retrieving data from Dynamics 365.

3. **`SnowflakeDataset.json`**  
   Dataset for writing data into Snowflake.

4. **`Dynamics365LinkedService.json`**  
   Linked service configuration for Dynamics 365 (Dataverse).

5. **`SnowflakeLinkedService.json`**  
   Linked service configuration for Snowflake.

6. **`DailyTrigger.json`**  
   Defines a scheduled trigger to run the pipeline every day at midnight.

7. **`PipelineParameters.json`**  
   Defines parameters that can be used within the pipeline for dynamic configuration.

---

## ⚙️ Setup Instructions

1. **Clone the repository to your local environment:**  
   ```sh
   git clone https://github.com/your-username/adf-d365-snowflake-pipeline.git

2. Navigate to the `ADF` folder:

3. Edit and populate the necessary files using `nano` or your preferred editor.

4. Follow Azure Data Factory deployment steps to import these JSON files and configure the pipeline.**
