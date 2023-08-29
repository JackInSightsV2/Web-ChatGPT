# Web ChatGPT README

## Overview
Web ChatGPT is a Python-based tool that combines the capabilities of OpenAI's ChatGPT model with web search and scraping functionalities. The tool allows for detailed research on any given topic and returns results backed up by data fetched from the web. The tool is equipped to provide a web interface via Streamlit and can also be accessed as an API endpoint through FastAPI.

## Features
1. **Search Functionality**: Uses a custom search API to fetch results related to the given query.
2. **Web Scraping**: Scrapes content from specified websites.
3. **Summary**: Summarizes lengthy content for better readability.
4. **Web App**: A user-friendly interface using Streamlit for quick research tasks.
5. **API Endpoint**: FastAPI-based endpoint for easy integration into other applications.

## Dependencies
1. `os`
2. `dotenv`
3. `langchain`
4. `requests`
5. `bs4`
6. `json`
7. `fastapi`
8. `streamlit`
9. `pydantic`

## Environment Variables
Make sure to set the following environment variables:

- `BROWSERLESS_API_KEY`: Your API key for browserless (used for web scraping).
- `SERP_API_KEY`: Your API key for the custom search engine.
- `OPENAI_API_KEY`: Your API key for OpenAI.

## How to Run

### Running as a Streamlit Web App

Execute the Python script:

```bash
$ python web_chatgpt.py
```

After running the script, Streamlit will provide a local URL where you can access the Web ChatGPT application.

### Running as an API Endpoint with FastAPI

Execute the following command:

```bash
$ uvicorn web_chatgpt:app --reload
```

Once the server is up, you can make a `POST` request to the root (`/`) with a payload containing the query:

```json
{
    "query": "YOUR_RESEARCH_TOPIC"
}
```

The response will contain the research output for the given topic.

## Caution

Do not provide made-up URLs for scraping. Always ensure that the provided URLs come from authentic search results.

## Contribution & Feedback

Feel free to fork this repository and submit pull requests for any improvements or features you'd like to add. We appreciate any feedback or issues you find and would be happy to address them.

---

Created by the Web ChatGPT team.
