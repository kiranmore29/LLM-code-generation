# **LLM Agents for Data Engineering Code Generation**

## **Problem Statement**

LLM agents should be able to generate the code to read the data from the given location and also be able to perform basic tasks of data wrangling such as:
- Group By
- Filter
- Aggregation
- Sorting

This code should be generated in a manner compatible with the specified development environment, such as **Databricks, AWS Glue, Google BigQuery**.

---

## **Project Overview**

This solution leverages **AutoGen AI agents** to automatically generate data engineering code for reading data from files (CSV, Parquet, TSV, XLSX, etc.) and performing common data wrangling tasks, including:
- Grouping
- Filtering
- Aggregation
- Sorting

### **Agents Used:**
1. **Programmer Agent**: Generates the required code based on the provided prompts.
2. **Tester Agent**: Analyzes the generated code, detects errors, and provides feedback.

---

## **Environment Setup**

### **1. Python Installation**
Ensure you have **Python 3.x** installed on your system.

### **2. Install Required Packages**
Install the necessary Python packages by running:

pip install -r requirements.txt

### **3. Update OpenAI API key**
Update your OpenAI API key in main.py file.

---

## Code Flow
1. The **Programmer Agent** is given a task via a prompt (e.g., "Generate PySpark code that reads a TSV file, filters rows, groups by 'department', and calculates max salary").
2. The **Tester Agent** then checks the generated code for any syntax issues or errors.
3. If the code passes validation, it is returned to the user.
4. If issues are found, the **Tester Agent** provides suggestions for improvement and prompts the **Programmer Agent** for corrections.

## Testing with Prompts
The system has been tested with various prompts to ensure robustness and compatibility across different environments. Here are some examples of prompts used:

- **Prompt 1**: "Generate PySpark code in Databricks to read a Parquet file, group by 'Region', and return total sales."
- **Prompt 2**: "Generate a SQL query for Snowflake to read from `sales_data`, group by `product_id`, and return total count."
- **Prompt 3**: "Generate Pandas code to read a CSV file, filter rows where `age > 30`, group by `city`, and calculate average income."

For full examples, refer to the `prompts.txt` file in the repository.

## How to Use
1. Clone the repository.
2. Run the AutoGen AI agents following the provided instructions.
3. Test the system with your own prompts or use the examples from `prompts.txt`.


- Developed by iSynergy TechSys Pvt. Ltd.