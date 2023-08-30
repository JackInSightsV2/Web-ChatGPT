# Web-ChatGPT README

## Overview
Web-ChatGPT is a Python-based tool that combines the capabilities of OpenAI's ChatGPT model with web search and scraping functionalities. The tool allows for detailed research on any given topic and returns results backed up by data fetched from the web. The tool is equipped to provide a web interface via Streamlit and can also be accessed as an API endpoint through FastAPI.

![image](https://github.com/JackInSightsV2/Web-ChatGPT/assets/99128415/1a3ed656-707f-4f2c-8473-9e0b5bb3626f)

## Features
1. **Search Functionality**: Uses a custom search API to fetch results related to the given query.
2. **Web Scraping**: Scrapes content from specified websites.
3. **Summary**: Summarizes lengthy content for better readability.
4. **Web App**: A user-friendly interface using Streamlit for quick research tasks.
5. **API Endpoint**: FastAPI-based endpoint for easy integration into other applications. (app_api.py)

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

Save the above in a file called .env

## Bugs

Model changing is not working at the moment. Need to get the global variable correct. 


## How to Run

### Running as a Streamlit Web App

Download the app.py and requirement.txt, create your .env file in the same folder and add your API keys

```bash
$ pip install -r requirements.txt
```

```bash
$ streamlit run app.py
```

After running the script, Streamlit will provide a local URL where you can access the web application.

Sometimes you may need to provide the entire string to get streamlit to run

```bash
$ C:\Users\user\AppData\Roaming\Python\Python311\Scripts\streamlit run "D:/Coding/Research Bot/app.py"
```

### Running as an API Endpoint with FastAPI (app_api.py)

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

Originally created by https://github.com/JayZeeDesign
https://www.youtube.com/watch?v=ogQUlS7CkYA
