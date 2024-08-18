# Convert your natural language questions to SQL queries
Welcome to simple-text-to-query ! This project demonstrates how to leverage OpenAI's ChatGPT as well as a local LLM to convert natural language text into SQL queries using SQLite3.

## Overview

This repository contains a Jupyter notebook that showcases a practical approach to translating natural language into SQL queries. By integrating ChatGPT with SQLite3, users can input natural language text and receive corresponding SQL queries that can be executed against an SQLite database. We also demonstrate how injecting SQL schema information can prevent hallucination by LLM. Finally, if you want your database information to be private, you can just load the LLM weights locally and run queries againts them.

## Features

- **SQLite3 Integration:** Setup a local SQLite3 DB. Execute the generated SQL queries on an SQLite3 database.
- **Translate to SQL:** Utilizes ChatGPT or a local LLM to understand and convert user questions written in plain languageto proper SQL syntax.
- **Load a LLM locally:** Showcases how to download and use the LLM weights locally.
- **Prevent hallucination:** Learn how to modify your prompts to avoid hallucinations.

## Requirements

To run this notebook, you'll need:

- Python 3.7 or higher
- Jupyter Notebook or JupyterLab
- Required Python libraries, which can be installed using `pip`

### Install Dependencies

You can install the required dependencies using pip. Here’s a sample `requirements.txt`:

```
openai
sqlite3
huggingface_hub
torch
transformers
```

Install the dependencies with:

```bash
pip install -r requirements.txt
```

## Setup

1. **Clone the Repository:**

   ```bash
   https://github.com/saketd403/simple-text-to-query.git
   cd simple-text-to-query
   ```

2. **Obtain API Key:**

   Sign up for OpenAI and obtain an API key. Note that this might require you to pay for subscription.

3. **Open the Notebook:**

   Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

   Navigate to `simple-text-to-query.ipynb` and open it.

## Usage

1. **Load the Notebook:**

   Open the `simple-text-to-query.ipynb` notebook in Jupyter.

2. **Input Natural Language Queries:**

   In the notebook, you will find cells where you can enter natural language text. The notebook will use ChatGPT to convert this text into an SQL query.

3. **Execute the SQL Query:**

   The generated SQL query is then executed against an SQLite3 database. The results are displayed within the notebook.

## Example

Here's an example of how a natural language query might be converted:

- **Input:** "Show me all users who signed up in the last month."
- **Generated SQL Query:** `SELECT * FROM users WHERE signup_date >= DATE('now', '-1 month');`

## Contributing

Contributions are welcome! Please follow these steps if you want to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Create a new Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

