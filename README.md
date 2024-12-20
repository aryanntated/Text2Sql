# Overview
Text-to-SQL converter bridges the gap between non-technical users and databases, enabling anyone to query data without SQL expertise. This project transforms natural language questions into precise SQL queries using advanced machine learning techniques.

# Features
- Convert natural language prompts to SQL queries.
- Support for complex database interactions.
- Uses advanced language models for accurate query generation.
- Trained on extensive dataset of language-SQL query pairs.

# Dataset and Model
## Training Data

Datasets: WikiSQL and Spider
Total Examples: 78,577 natural language queries paired with SQL queries
Columns: Questions, Answers, Context

## Model Architecture
BART Model
-Combines bidirectional encoder (like BERT) with autoregressive decoder (like GPT)
-Employs advanced training techniques:
  - Token masking
  - Deletion
  - Text infilling
  - Sentence permutation
  - Document rotation



## Query Parsing

- SQLGlot used to parse queries
- Infers column types from:

   - Operators (>, <)
   - Functions (MIN, MAX, AVG, SUM)
   - Defaults to VARCHAR if uncertain



## Performance

Fine-tuned model deployed on Hugging Face
Evaluated using BELU score

Installation
```bash
   git clone https://github.com/HiyaJain22/Text2Sql.git
   ```

# Example usage
natural_language_query = "Show me the top 5 customers by total sales"

sql_query = convert_to_sql(natural_language_query) 

print(sql_query)

# Contact

Hiya Jain - hjain2209@gmail.com

Aryann Tated - aryann.k.tated@gmail.com

Yash Thakkar - yashthakar2710@gmail.com


# Acknowledgments

- WikiSQL Dataset
- Spider Dataset
- Hugging Face

# Model is uploaded on Hugging Face 
Feel free to check it out- 
https://huggingface.co/Hiyaj/bart-small-text2sql
